# Repository Structure

```
splash-roofing-microsite/
├── README.md                    # Project overview and quick reference
├── DEPLOYMENT-GUIDE.md          # Step-by-step GitHub Pages setup
├── CHANGELOG.md                 # Version history and changes
├── STRUCTURE.md                 # This file - directory structure
├── .gitignore                   # Git ignore patterns
├── deploy.sh                    # Automated deployment script (executable)
│
└── roofing-marketing/           # Main microsite folder
    ├── index.html               # Homepage / routing hub
    ├── strategy.html            # Strategy parent page
    ├── one-day-marketing-strategy.html  # Strategy offer page
    ├── digital-marketing.html   # Digital hub page
    ├── search-engine-optimization.html  # SEO service page
    ├── google-local-service-ads.html    # LSA service page
    ├── email-marketing.html     # Email service page
    ├── social-media-marketing.html      # Social service page
    ├── websites.html            # Website service page
    ├── video.html               # Video service page
    ├── resources.html           # Resources hub page
    ├── schedule-strategy-call.html      # Conversion form page
    └── thank-you.html           # Confirmation page
```

## File Sizes

| File | Size | Notes |
|------|------|-------|
| index.html | 157KB | Largest (hub page with most content) |
| social-media-marketing.html | 142KB | Second largest (many content types) |
| video.html | 146KB | Large (comprehensive video coverage) |
| websites.html | 144KB | Large (visual examples) |
| resources.html | 139KB | Large (resource library) |
| email-marketing.html | 135KB | Medium-large |
| schedule-strategy-call.html | 135KB | Medium-large (comprehensive form) |
| google-local-service-ads.html | 133KB | Medium |
| search-engine-optimization.html | 131KB | Medium |
| digital-marketing.html | 129KB | Medium (hub page) |
| one-day-marketing-strategy.html | 125KB | Medium |
| strategy.html | 110KB | Smallest service page |
| thank-you.html | 103KB | Smallest overall (confirmation) |
| **Total** | **~1.7MB** | Across 13 pages |

## Missing Files

These pages are referenced but don't exist yet:

1. **google-ads-ppc.html** (PPC service page)
   - Referenced by all 13 pages
   - Should be in: `roofing-marketing/`
   - Will be child of digital-marketing.html

2. **results.html** (Proof/portfolio page)
   - Referenced by multiple pages
   - Should be in: `roofing-marketing/`
   - Top-level service page

## Documentation Files

| File | Purpose |
|------|---------|
| README.md | Quick start, overview, status |
| DEPLOYMENT-GUIDE.md | Step-by-step GitHub setup |
| CHANGELOG.md | Version history |
| STRUCTURE.md | This file - repository layout |
| .gitignore | Git exclusions |
| deploy.sh | Automated Git setup and push |

## Future Assets Folder (Recommended)

For production, create:

```
roofing-marketing/
├── assets/
│   ├── css/
│   │   └── roofing-microsite.css       # Extracted shared CSS
│   ├── js/
│   │   └── roofing-microsite.js        # Extracted shared JavaScript
│   ├── images/
│   │   ├── hero/                       # Hero section images
│   │   ├── proof/                      # Client logos, testimonials
│   │   ├── projects/                   # Project photos
│   │   └── resources/                  # Scorecard, guides
│   ├── video/
│   │   └── testimonials/               # Video testimonials
│   └── fonts/                          # Self-hosted fonts (optional)
│       ├── KronaOne-Regular.woff2
│       ├── Montserrat-*.woff2
│       └── OpenSans-*.woff2
```

## URL Structure

When deployed to GitHub Pages, URLs will be:

```
Base: https://USERNAME.github.io/REPO/roofing-marketing/

Pages:
├── /roofing-marketing/                                    (index.html)
├── /roofing-marketing/strategy.html
├── /roofing-marketing/one-day-marketing-strategy.html
├── /roofing-marketing/digital-marketing.html
├── /roofing-marketing/search-engine-optimization.html
├── /roofing-marketing/google-local-service-ads.html
├── /roofing-marketing/email-marketing.html
├── /roofing-marketing/social-media-marketing.html
├── /roofing-marketing/websites.html
├── /roofing-marketing/video.html
├── /roofing-marketing/resources.html
├── /roofing-marketing/schedule-strategy-call.html
└── /roofing-marketing/thank-you.html
```

## Clean URLs (Production)

For production with clean URLs (no .html), you can:

1. **Use Jekyll** (GitHub Pages native):
   - Add `_config.yml` with `permalink: pretty`
   - Automatically removes .html

2. **Server configuration**:
   - Apache: .htaccess with mod_rewrite
   - Nginx: rewrite rules in config
   - Cloudflare: Page rules

3. **Update all internal links** to not include .html

## Repository Branches

Recommended branch structure:

```
main              # Production-ready code (deploy from here)
├── development   # Active development
├── feature/*     # Feature branches
└── hotfix/*      # Emergency fixes
```

## File Naming Conventions

- All lowercase
- Hyphen-separated (kebab-case)
- Descriptive names
- Match URL structure
- No spaces or special characters

## Git Workflow

1. Clone repository
2. Create feature branch
3. Make changes
4. Test locally
5. Commit with clear message
6. Push to GitHub
7. Create pull request (if team workflow)
8. Merge to main
9. GitHub Pages auto-deploys

## Deployment Checklist

Before deploying:

- [ ] All files in correct folders
- [ ] No broken internal links
- [ ] README.md is up to date
- [ ] CHANGELOG.md reflects changes
- [ ] .gitignore excludes sensitive files
- [ ] No credentials in files
- [ ] Test pages load locally
- [ ] Verify mobile responsive
- [ ] Check accessibility (basic)

After deploying:

- [ ] Verify all pages load on GitHub Pages
- [ ] Test navigation works
- [ ] Check mobile layout
- [ ] Verify forms validate (won't submit without backend)
- [ ] Test internal links
- [ ] Check FAQ accordions work
- [ ] Verify mobile menu works

## Maintenance

### Weekly
- Check for broken links
- Review analytics (when set up)
- Monitor form submissions (when connected)

### Monthly
- Update CHANGELOG with significant changes
- Review and update content
- Performance audit (Lighthouse)

### Quarterly
- Accessibility audit
- Security review
- Content refresh
- Asset optimization

## Need Help?

- **GitHub Docs:** https://docs.github.com
- **GitHub Pages:** https://docs.github.com/pages
- **Git Docs:** https://git-scm.com/doc
- **Markdown Guide:** https://www.markdownguide.org

## Quick Commands

```bash
# View structure
tree -L 2

# Count files
find . -name "*.html" | wc -l

# Check file sizes
du -sh roofing-marketing/*.html

# Find large files
find . -type f -size +100k

# Count placeholder needs
grep -r "{NEEDS" roofing-marketing/*.html | wc -l

# Validate HTML (if w3c validator installed)
html5validator --root roofing-marketing/
```
