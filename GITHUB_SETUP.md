# GitHub Setup & Deployment Guide

## 1. Create GitHub Repository

```bash
cd /Users/timpoisal/Downloads/strattora-landing

# Create new repo at github.com/tjpoisal/strattora-landing

git remote add origin https://github.com/tjpoisal/strattora-landing.git
git branch -M main
git push -u origin main
```

## 2. Vercel Deployment

### Option A: Manual (Recommended for First Deploy)
```bash
# Install Vercel CLI
npm i -g vercel

# Login to Vercel
vercel login

# Deploy to production
vercel --prod

# You'll get a production URL
```

### Option B: GitHub Auto-Deploy
1. Connect GitHub repo to Vercel dashboard
2. Vercel will auto-deploy on every push to `main`

## 3. Setup Custom Domain

### In Vercel Dashboard:
1. Go to Project Settings → Domains
2. Add domain: `strattora.com`
3. Vercel will show you DNS records to add

### In Your Domain Registrar (Namecheap, GoDaddy, etc.):

**Method 1: CNAME (Recommended)**
```
Name: www
Type: CNAME
Value: cname.vercel.com
```

**Method 2: A Records**
```
Type: A
Value: 76.76.19.56
Type: A
Value: 76.76.19.57
Type: A
Value: 76.76.19.58
Type: A
Value: 76.76.19.59
```

**Also add TXT record for verification:**
```
Name: _vercel
Value: [from Vercel dashboard]
```

## 4. Verify DNS (5-10 minutes)

```bash
nslookup strattora.com
dig strattora.com
```

## 5. Enable HTTPS

Vercel auto-enables HTTPS once DNS propagates.

## What's Deployed

- ✓ Full landing page with 12 features
- ✓ Frosted glassmorphism design
- ✓ Interactive demo (5 tabs)
- ✓ Pricing section
- ✓ Testimonials
- ✓ Mobile responsive
- ✓ Auto-deploys on git push

## Files Structure

```
strattora-landing/
├── index.html           # Complete landing page (40KB)
├── vercel.json          # Vercel config
├── .github/
│   └── workflows/
│       └── deploy.yml   # Auto-deploy on push
├── README.md
├── GITHUB_SETUP.md      # This file
└── DEPLOY.sh            # Manual deploy script
```

## Production Checklist

- [ ] Create GitHub repo
- [ ] Run: `git push -u origin main`
- [ ] Connect to Vercel
- [ ] Add custom domain strattora.com
- [ ] Add DNS records
- [ ] Wait 10 minutes for DNS propagation
- [ ] Visit https://strattora.com
- [ ] Test all interactive features
- [ ] Set up email domain (strattora.com email)

## Next Steps After Deployment

1. Add email setup (Vercel has guides for this)
2. Set up contact form backend (Firebase, Netlify Forms, etc.)
3. Add blog section (optional)
4. Add analytics (Google Analytics, Vercel Analytics)
5. Add newsletter signup
