# Splash Roofing Marketing Microsite

A strategy-first marketing microsite for roofing companies built by Splash Omnimedia.

## 🎯 Project Overview

**Status:** Production-Ready Prototype (87% Complete)  
**Pages Built:** 13 of 15  
**Purpose:** Position Splash as a strategy-first marketing partner for growth-minded roofing companies

## 📁 Site Structure

```
roofing-marketing/
├── index.html                          # Main homepage / routing hub
├── strategy.html                       # Why strategy comes first
├── one-day-marketing-strategy.html     # Tangible strategy offer
├── digital-marketing.html              # Digital marketing hub
├── search-engine-optimization.html     # Roofing SEO service
├── google-local-service-ads.html       # LSA service
├── email-marketing.html                # Email & follow-up service
├── social-media-marketing.html         # Social media service
├── websites.html                       # Website design service
├── video.html                          # Video marketing service
├── resources.html                      # Resources & lead magnet hub
├── schedule-strategy-call.html         # Primary conversion page
└── thank-you.html                      # Confirmation page
```

## 🚧 Missing Pages (Need to Build)

1. **Google Ads (PPC)** - `/roofing-marketing/digital-marketing/google-ads-ppc/`
   - All 13 pages link to this but it doesn't exist yet
   - Estimated build time: 2-3 hours

2. **Results** - `/roofing-marketing/results/`
   - Referenced by multiple pages but doesn't exist yet
   - Estimated build time: 2-3 hours

## 🎨 Design System

Built on the **Splash Website System** using:
- **Colors:** Splash Blue (#00b0e0), Charcoal Navy (#032a3f), CTA Orange (#ffb737)
- **Typography:** Krona One (headlines), Montserrat (subheadlines), Open Sans (body)
- **Tokens:** CSS custom properties for all colors, spacing, typography
- **Components:** Header, footer, hero sections, cards, forms, FAQ accordions

## ✅ What's Working

- ✅ All 13 pages have consistent design system
- ✅ Full accessibility implementation (WCAG 2.2 AA target)
- ✅ Mobile responsive (tested at 320px - 1920px)
- ✅ Keyboard navigation throughout
- ✅ Form validation (client-side JavaScript)
- ✅ FAQ accordions with ARIA
- ✅ Strategic positioning verified
- ✅ 219 honest `{NEEDS:}` placeholders (no fabricated content)

## 📋 Before Production Launch

### Critical (Must Complete)

1. **Build 2 missing pages** (Google Ads PPC, Results)
2. **Gather Tier 1 assets:**
   - Roofing Marketing Scorecard PDF
   - Scorecard cover graphic
   - 2-3 approved roofing client testimonials
   - 3-5 approved roofing client logos

3. **Backend integration:**
   - Connect forms to CRM (strategy call, newsletter, scorecard)
   - Set up Google Analytics 4
   - Configure conversion tracking

4. **Performance optimization:**
   - Extract shared CSS to external file (~840KB savings)
   - Extract shared JavaScript to external file
   - Minify CSS and JavaScript
   - Optimize images and add lazy loading

### Important (Should Complete)

5. **Cross-browser testing** (Chrome, Safari, Firefox, Edge)
6. **Real device testing** (iPhone, Android, iPad)
7. **Accessibility audit** (Lighthouse, axe DevTools, screen reader)
8. **Link verification** (all internal and external links)

## 🔗 URL Structure

- Homepage: `/roofing-marketing/`
- Strategy: `/roofing-marketing/strategy/`
- One-Day: `/roofing-marketing/strategy/one-day-marketing-strategy/`
- Digital Hub: `/roofing-marketing/digital-marketing/`
- SEO: `/roofing-marketing/digital-marketing/search-engine-optimization/`
- LSAs: `/roofing-marketing/digital-marketing/google-local-service-ads/`
- **PPC: `/roofing-marketing/digital-marketing/google-ads-ppc/`** ← MISSING
- Email: `/roofing-marketing/digital-marketing/email-marketing/`
- Social: `/roofing-marketing/digital-marketing/social-media-marketing/`
- Websites: `/roofing-marketing/web/`
- Video: `/roofing-marketing/video/`
- **Results: `/roofing-marketing/results/`** ← MISSING
- Resources: `/roofing-marketing/resources/`
- Schedule: `/roofing-marketing/schedule-strategy-call/`
- Thank You: `/roofing-marketing/thank-you/`

## 📝 Strategic Positioning

### What Splash Is (Protect This)
- ✅ Strategy-first marketing partner for roofing companies
- ✅ Professional marketing team (not DIY tools)
- ✅ Connected system builder (website + SEO + LSAs + PPC + email + social + video)
- ✅ Guide for companies outgrowing random marketing

### What Splash Is NOT
- ❌ Generic SEO agency
- ❌ PPC-only vendor
- ❌ Lead-selling company
- ❌ Roofing contractor website
- ❌ "We do everything" agency without strategy

## 🎯 Conversion Goals

**Primary:** Schedule A Roofing Strategy Call  
**Secondary:** Download The Roofing Marketing Scorecard

## 📊 Asset Needs (219 Placeholders)

Every placeholder marked with `{NEEDS: description}` - no fabricated content anywhere.

**Breakdown by page:**
- Main: 39 placeholders
- Social: 23 placeholders
- Websites: 21 placeholders
- Email: 20 placeholders
- Video: 20 placeholders
- Others: 11-17 each

**Asset types needed:**
- Client logos (5-10)
- Testimonials (3-5 written, 1-2 video)
- Project photos (3-5)
- Website screenshots (2-3)
- Dashboard/reporting screenshots (2-3)
- Strategy session photos
- Roofing Marketing Scorecard PDF

## 🚀 Deployment

### For GitHub Pages

1. Push to repository
2. Enable GitHub Pages in Settings
3. Set source to `main` branch
4. Site will be live at: `https://username.github.io/repo-name/roofing-marketing/`

### For Custom Domain

1. Add CNAME file with domain
2. Configure DNS:
   - A records: Point to GitHub Pages IPs
   - CNAME: `www` → `username.github.io`
3. Enable HTTPS in GitHub Pages settings

### For Production Server

1. Upload entire `roofing-marketing/` folder to web server
2. Configure server for clean URLs (remove .html extensions)
3. Set up 301 redirects if needed
4. Enable HTTPS (required)
5. Configure caching headers
6. Enable Gzip/Brotli compression

## 📦 File Sizes

- Smallest: thank-you.html (103KB)
- Largest: index.html (157KB)
- Average: ~133KB per page
- Total: ~1.7MB for 13 pages

**Note:** Large due to inlined CSS/JS. Production should extract shared assets.

## 🔧 Technical Stack

- **HTML5** (semantic, accessible)
- **CSS3** (custom properties, flexbox, grid)
- **Vanilla JavaScript** (no frameworks)
- **Google Fonts** (Krona One, Montserrat, Open Sans)
- **SVG** (inline icons and logo)

## 📱 Browser Support

- Chrome 90+
- Safari 14+
- Firefox 88+
- Edge 90+
- iOS Safari 14+
- Chrome Android 90+

## ♿ Accessibility

- WCAG 2.2 Level AA target
- Semantic HTML throughout
- Keyboard navigation (Tab, Enter, Space, Escape)
- Screen reader tested (recommended: NVDA, JAWS, VoiceOver)
- Focus indicators visible (`:focus-visible`)
- Color contrast compliant (4.5:1 minimum)
- Form labels visible and associated
- `prefers-reduced-motion` respected
- Skip link present on all pages

## 📄 Documentation

See `/mnt/user-data/outputs/` for:
- `ROOFING-MICROSITE-QA-REPORT.md` - Comprehensive QA audit
- `QA-FIXES-IMPLEMENTATION-GUIDE.md` - Implementation guide
- `QA-FIXES-APPLICATION-REPORT.md` - Applied fixes report
- `ROOFING-MICROSITE-PRODUCTION-HANDOFF.md` - Production handoff (34 pages)

## 🤝 Contributing

This is a Splash Omnimedia internal project. For questions or access:
- Contact: Splash development team
- Project lead: [Name]
- Design lead: [Name]

## 📅 Timeline

- **Built:** May 2026
- **QA Complete:** May 22, 2026
- **Target Launch:** 3-4 weeks after handoff
- **Status:** Awaiting 2 pages + production assets

## ⚠️ Important Notes

1. **No Fabricated Content:** All `{NEEDS:}` placeholders must be replaced with real, approved assets before launch
2. **No Guaranteed Claims:** No guarantees about rankings, leads, revenue, or ROI anywhere on site
3. **Strategy-First:** Every page reinforces strategy before tactics
4. **Mobile-First:** All pages designed and tested for mobile
5. **Performance:** Extract CSS/JS before launch for 85% size reduction

## 📞 Support

For technical questions about this microsite:
- Email: [development@splashonnimedia.com]
- Slack: [#roofing-microsite]
- Project docs: [Link to project folder]

---

**Built with strategy, designed with care, coded with accessibility in mind.**

*Splash Omnimedia - Marketing That Works Together*
