# MoonDesk Landing Page

Single-page marketing site for MoonDesk — AI-Powered Programme Management by Tek4All.

**Live URL:** [moondesk.tekforall.org](https://moondesk.tekforall.org)

## Stack

- **Pure HTML/CSS/JS** — zero build step, maximum performance
- **Fonts:** DM Sans (body), Instrument Sans (display), JetBrains Mono (mono)
- **Icons:** Lucide via CDN
- **Deployed on:** Vercel (static)

## Design System

Matches the MoonDesk application retro monochrome UI:

| Token | Value | Usage |
|-------|-------|-------|
| Background | `#FAF9F6` | Page background (cream) |
| Text | `#1A1A1A` | Primary text, buttons |
| White | `#FFFFFF` | Cards, inputs |
| Border | `#C4C3BF` | All borders (2px solid) |
| Muted | `#5C5B58` | Body text |
| Muted Light | `#8A8986` | Labels, captions |
| Shadow | `4px 4px 0` | Retro hard shadow (no blur) |
| Radius | `18px` | Cards |
| Radius SM | `12px` | Buttons, inputs, small cards |

## Sections

1. Sticky top nav with anchors + "Book a Demo" CTA
2. Hero with product screenshot mock
3. Problem cards (6 pain points)
4. Who it's for (segment chips + buyer/user split)
5. What MoonDesk is (3 value cards)
6. Core features (5 numbered feature cards)
7. Product tour (2×2 screenshot grid)
8. Platform modules (7 modules, 2-column layout)
9. Luna AI (3 capability cards + governance box)
10. Security (RBAC, groups, hierarchy + org tree)
11. Onboarding timeline (7-step horizontal timeline)
12. Subscription (single package pricing card)
13. FAQ accordion (6 questions)
14. Book a Demo form + footer

## Local Development

```bash
# Just open in browser — no build required
open index.html

# Or use any static server
npx serve .
python3 -m http.server 3000
```

## Deploy to Vercel

```bash
# 1. Create GitHub repo
gh repo create moondesk-landing --public
git init
git add -A
git commit -m "feat: MoonDesk landing page"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/moondesk-landing.git
git push -u origin main

# 2. Connect to Vercel
#    - Go to vercel.com/new
#    - Import the moondesk-landing repo
#    - Framework: Other
#    - Build command: (leave empty)
#    - Output directory: .
#    - Deploy

# 3. Custom domain
#    - In Vercel project → Settings → Domains
#    - Add: moondesk.tekforall.org
#    - Set DNS CNAME: moondesk → cname.vercel-dns.com
```

## Form Integration

The demo form currently simulates submission. To connect a real backend:

1. **Formspree:** Change the form action to `https://formspree.io/f/YOUR_ID`
2. **Google Forms:** Redirect to a Google Form
3. **Supabase:** POST to a Supabase edge function
4. **Email API:** Connect to SendGrid/Resend

## Customisation

- Replace `hello@tekforall.org` in footer with real contact email
- Add real screenshots by replacing the mock UI components with `<img>` tags
- Add Calendly embed by replacing the form with `<div class="calendly-inline-widget" ...>`
- Update the `© 2025` year in footer

## License

Proprietary — Tek4All Foundation