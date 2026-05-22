# Changelog

All notable changes to the Splash Roofing Marketing Microsite will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).

---

## [0.9.0] - 2026-05-22 - "Production-Ready Prototype"

### Status
**87% Complete** - 13 of 15 pages built and QA'd

### Added
- 13 complete HTML pages with Splash design system
- Full accessibility implementation (WCAG 2.2 AA target)
- Mobile responsive layouts (320px - 1920px tested)
- Keyboard navigation throughout
- Form validation (client-side JavaScript)
- FAQ accordions with ARIA
- 219 honest `{NEEDS:}` placeholders
- Comprehensive production handoff documentation

### Pages Built
- ✅ Main Page (homepage / routing hub)
- ✅ Strategy (why strategy comes first)
- ✅ One-Day Marketing Strategy (tangible offer)
- ✅ Digital Marketing (hub for channels)
- ✅ Search Engine Optimization (SEO service)
- ✅ Google Local Service Ads (LSA service)
- ✅ Email Marketing (follow-up service)
- ✅ Social Media Marketing (content service)
- ✅ Websites (design service)
- ✅ Video (video marketing service)
- ✅ Resources (lead magnet hub)
- ✅ Schedule A Roofing Strategy Call (conversion page)
- ✅ Thank You (confirmation page)

### Missing Pages
- ❌ Google Ads (PPC) - `/roofing-marketing/digital-marketing/google-ads-ppc/`
- ❌ Results - `/roofing-marketing/results/`

### Fixed (QA Round)
- Fixed: Added `lang="en"` to all 13 pages
- Fixed: Standardized primary CTA to "Schedule A Roofing Strategy Call"
- Fixed: Added active nav state to main page
- Fixed: Standardized all scorecard download links
- Fixed: Added form source tracking comments with CRM parameters
- Fixed: Added newsletter form ESP integration comments
- Fixed: Suppressed sticky mobile CTA on thank-you page
- Fixed: Updated email marketing hero subheadline for differentiation
- Fixed: Updated social media marketing hero subheadline for differentiation
- Fixed: Added CSS extraction production comment with guidance

### Technical Details
- Design System: Splash Website System (colors_and_type.css)
- Typography: Krona One, Montserrat, Open Sans (Google Fonts)
- CSS: Inlined (~70KB per page, ~910KB total duplication)
- JavaScript: Inlined (~8KB per page, ~104KB total duplication)
- Total Size: ~1.7MB across 13 pages
- SEO: Unique titles, meta descriptions, H1s, canonicals
- Accessibility: Semantic HTML, skip links, ARIA, keyboard nav, focus states

### Known Issues
- Two pages missing (PPC, Results) - block client preview
- 219 production assets needed (`{NEEDS:}` placeholders)
- CSS/JS should be extracted for production (~85% size reduction)
- Forms not connected to backend (placeholder actions)
- No analytics tracking yet
- Google Fonts via CDN (should self-host for production)

### Documentation Added
- README.md - Project overview and quick reference
- DEPLOYMENT-GUIDE.md - Step-by-step GitHub Pages setup
- deploy.sh - Automated deployment script
- CHANGELOG.md - Version history (this file)
- .gitignore - Git ignore patterns
- ROOFING-MICROSITE-QA-REPORT.md - 34-page comprehensive QA audit
- QA-FIXES-IMPLEMENTATION-GUIDE.md - 20-fix implementation plan
- QA-FIXES-APPLICATION-REPORT.md - Applied fixes report
- ROOFING-MICROSITE-PRODUCTION-HANDOFF.md - Production handoff document

---

## [0.8.0] - 2026-05-21 - "Initial Build"

### Added
- Initial 13 pages built with Splash design system
- Honest placeholder system (`{NEEDS:}`)
- Strategy-first positioning throughout
- Mobile responsive layouts
- Accessibility foundations

### Technical
- Semantic HTML5
- CSS custom properties (design tokens)
- Vanilla JavaScript (no frameworks)
- SVG inline graphics
- Google Fonts integration

---

## Upcoming Releases

### [1.0.0] - TBD - "Client Preview Ready"

#### Must Complete
- [ ] Build Google Ads (PPC) page
- [ ] Build Results page
- [ ] Gather Tier 1 production assets
- [ ] Connect forms to CRM
- [ ] Set up Google Analytics 4
- [ ] Final QA testing

#### Should Complete
- [ ] Extract CSS to shared file
- [ ] Extract JavaScript to shared file
- [ ] Minify CSS and JavaScript
- [ ] Cross-browser testing
- [ ] Real device testing
- [ ] Accessibility audit

### [1.1.0] - TBD - "Production Ready"

#### Must Complete
- [ ] Replace all 219 `{NEEDS:}` placeholders with real assets
- [ ] Optimize all images (WebP, lazy loading)
- [ ] Self-host fonts or optimize Google Fonts
- [ ] Performance optimization (target Lighthouse 90+)
- [ ] Legal review (privacy policy, terms)
- [ ] Stakeholder approval

#### Nice to Have
- [ ] Video testimonials
- [ ] Case study content
- [ ] Additional resources
- [ ] Blog/article content

---

## Version Numbering

This project follows [Semantic Versioning](https://semver.org/):

- **Major (X.0.0):** Significant changes, new pages, major redesign
- **Minor (0.X.0):** New features, content additions, improvements
- **Patch (0.0.X):** Bug fixes, copy edits, small tweaks

**Status Markers:**
- 0.x.x = Development/prototype
- 1.x.x = Client preview
- 2.x.x = Production launch
- 3.x.x = Post-launch iterations

---

## How to Contribute

When making changes:

1. Update the appropriate version section above
2. Use these categories:
   - **Added** - New features or pages
   - **Changed** - Changes to existing functionality
   - **Deprecated** - Soon-to-be removed features
   - **Removed** - Removed features
   - **Fixed** - Bug fixes
   - **Security** - Security improvements

3. Include:
   - What changed
   - Why it changed (if not obvious)
   - Who requested it (if applicable)
   - Related issue/ticket number (if applicable)

Example:
```markdown
### Fixed
- Fixed broken scorecard download link on Resources page (#42)
- Corrected typo in Email Marketing FAQ answer
- Updated phone number format validation on strategy call form
```

---

**Maintained by:** Splash Omnimedia Development Team  
**Last Updated:** May 22, 2026
