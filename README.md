# Strattora IQ³ Landing Page

Beautiful, fully responsive landing page with frosted glassmorphism design featuring:
- Complete feature showcase (12 features)
- Lexxi AI section with capabilities
- Interactive demo (scheduling, inventory, CRM, analytics, Lexxi chat)
- Pricing tiers
- Testimonials
- Mobile responsive

## Deploy to Vercel

```bash
npm i -g vercel
vercel --prod
```

## DNS Setup for strattora.com

Add these records to your domain registrar:

**CNAME Record:**
- Name: www
- Value: cname.vercel.com

**A Records:**
- 76.76.19.56
- 76.76.19.57
- 76.76.19.58
- 76.76.19.59

**TXT Record (Vercel verification):**
- Name: _vercel
- Value: (from Vercel deployment dashboard)

## Features Demo

All interactive sections work in-browser:
- Schedule appointments with stylist and date picker
- View inventory with stock levels
- Manage client profiles
- See analytics dashboard
- Chat with Lexxi AI

## Customization

Update branding in CSS variables (lines 10-20):
- `--primary`: Gold (#D4AF37)
- `--accent`: Rose gold (#E8D7C3)
- `--secondary`: Dark (#1a1a1a)
