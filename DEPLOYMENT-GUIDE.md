# GitHub Deployment Guide

Step-by-step instructions for deploying the Splash Roofing Marketing Microsite to GitHub Pages.

---

## Prerequisites

- GitHub account
- Git installed locally
- Repository access/ownership

---

## Step 1: Create GitHub Repository

### Option A: Create New Repository on GitHub.com

1. Go to https://github.com
2. Click **"New repository"** (green button)
3. Repository name: `splash-roofing-microsite` (or your choice)
4. Description: "Strategy-first marketing microsite for roofing companies"
5. Visibility: **Public** (for GitHub Pages) or **Private** (if organization allows)
6. ✅ Check "Add a README file" (optional - we have one)
7. ✅ Add .gitignore: None (we have one)
8. License: None (internal project)
9. Click **"Create repository"**

### Option B: Use GitHub CLI

```bash
gh repo create splash-roofing-microsite --public --description "Strategy-first marketing microsite for roofing companies"
```

---

## Step 2: Initialize Local Repository

Navigate to the deployment folder:

```bash
cd /mnt/user-data/outputs/github-deploy
```

Initialize Git (if not already):

```bash
git init
```

Add all files:

```bash
git add .
```

Commit:

```bash
git commit -m "Initial commit: Splash Roofing Marketing Microsite - 13 pages complete"
```

---

## Step 3: Connect to GitHub Remote

Add remote (replace USERNAME and REPO with yours):

```bash
git remote add origin https://github.com/USERNAME/REPO.git
```

Or with SSH:

```bash
git remote add origin git@github.com:USERNAME/REPO.git
```

Verify remote:

```bash
git remote -v
```

---

## Step 4: Push to GitHub

Push to main branch:

```bash
git branch -M main
git push -u origin main
```

Enter your GitHub credentials when prompted (or use SSH key).

---

## Step 5: Enable GitHub Pages

### Via GitHub.com:

1. Go to your repository on GitHub
2. Click **Settings** tab
3. Scroll to **Pages** in left sidebar
4. Under **Source**:
   - Branch: `main`
   - Folder: `/ (root)`
5. Click **Save**
6. Wait 1-2 minutes for deployment

### Via GitHub CLI:

```bash
gh repo edit --enable-pages --pages-branch main
```

---

## Step 6: Access Your Site

Your site will be live at:

```
https://USERNAME.github.io/REPO/roofing-marketing/
```

Example:
```
https://splashonnimedia.github.io/splash-roofing-microsite/roofing-marketing/
```

**Note:** The URL includes `/roofing-marketing/` because all pages are in that subfolder.

---

## Step 7: Configure Custom Domain (Optional)

### If you want: `roofing.splashonnimedia.com`

1. In GitHub repository Settings → Pages
2. Enter custom domain: `roofing.splashonnimedia.com`
3. Click **Save**
4. GitHub creates CNAME file automatically

### DNS Configuration:

Add these DNS records at your domain provider:

**Option A: Subdomain (recommended for microsite)**
```
Type: CNAME
Name: roofing
Value: USERNAME.github.io
TTL: 3600
```

**Option B: Apex domain (roofing-marketing.com)**
```
Type: A
Name: @
Value: 185.199.108.153
Value: 185.199.109.153
Value: 185.199.110.153
Value: 185.199.111.153
TTL: 3600
```

**Also add CNAME for www:**
```
Type: CNAME
Name: www
Value: USERNAME.github.io
TTL: 3600
```

### Enable HTTPS:

1. Wait for DNS propagation (5 minutes - 48 hours)
2. In GitHub Pages settings
3. Check **"Enforce HTTPS"**

---

## Step 8: Verify Deployment

### Check these pages load:

```
https://YOUR-DOMAIN/roofing-marketing/
https://YOUR-DOMAIN/roofing-marketing/strategy.html
https://YOUR-DOMAIN/roofing-marketing/digital-marketing.html
https://YOUR-DOMAIN/roofing-marketing/schedule-strategy-call.html
```

### Test functionality:

- ✅ Navigation menu works
- ✅ Mobile menu opens/closes
- ✅ FAQ accordions expand/collapse
- ✅ Forms validate (but won't submit - no backend yet)
- ✅ All internal links work
- ✅ Responsive layout on mobile

---

## Step 9: Set Up Clean URLs (Optional)

By default, GitHub Pages requires `.html` extensions in URLs. To remove them:

### Option 1: Use Jekyll (GitHub Pages native)

Create `_config.yml`:

```yaml
permalink: pretty
```

This removes `.html` from URLs automatically.

### Option 2: Use Custom Domain + Cloudflare

1. Point domain to Cloudflare
2. Use Cloudflare Page Rules to rewrite URLs
3. Rule: `roofing-marketing/*` → Remove .html extension

### Option 3: Accept .html in URLs (simplest)

Just update all internal links to include `.html`:
- `/roofing-marketing/strategy/` → `/roofing-marketing/strategy.html`

---

## Troubleshooting

### Site not loading?

**Check:**
- Repository is public (or organization allows private Pages)
- GitHub Pages is enabled in Settings
- Branch is set to `main`
- Files are in root or specified folder
- Wait 1-2 minutes for initial deployment

### 404 errors?

**Check:**
- URL path is correct: `/roofing-marketing/` not `/`
- File names match exactly (case-sensitive on Linux servers)
- Internal links use correct paths

### Styles not loading?

**Check:**
- CSS is inlined (currently is, so should work)
- No external stylesheet references broken
- Google Fonts CDN is accessible

### Custom domain not working?

**Check:**
- DNS records are correct
- Wait for DNS propagation (up to 48 hours)
- CNAME file exists in repository root
- HTTPS enforcement disabled during DNS setup

---

## Updating the Site

After making changes locally:

```bash
# Check what changed
git status

# Add changes
git add .

# Commit with descriptive message
git commit -m "Fix: Updated hero copy on strategy page"

# Push to GitHub
git push origin main
```

GitHub Pages will automatically rebuild (takes 1-2 minutes).

---

## Managing Branches

### Create development branch:

```bash
git checkout -b development
git push -u origin development
```

### Switch between branches:

```bash
git checkout main
git checkout development
```

### Merge development to main:

```bash
git checkout main
git merge development
git push origin main
```

---

## Best Practices

### Commit Messages:

Use clear, descriptive messages:
- ✅ "Add: Google Ads PPC page"
- ✅ "Fix: Correct scorecard download link"
- ✅ "Update: SEO page hero subheadline"
- ❌ "updates"
- ❌ "fixed stuff"

### Before Pushing:

- ✅ Test all pages locally
- ✅ Verify no broken links
- ✅ Check mobile responsive
- ✅ Validate HTML (if possible)
- ✅ Remove sensitive data

### File Organization:

- ✅ Keep all pages in `roofing-marketing/` folder
- ✅ Create `assets/` folder for CSS/JS when extracted
- ✅ Create `images/` folder for production images
- ✅ Keep documentation in repository root

---

## Production Checklist

Before marking site as "production ready":

- [ ] Build 2 missing pages (PPC, Results)
- [ ] Replace all 219 `{NEEDS:}` placeholders with real assets
- [ ] Extract CSS to external file
- [ ] Extract JavaScript to external file
- [ ] Minify CSS and JavaScript
- [ ] Optimize all images
- [ ] Add alt text to all images
- [ ] Connect forms to CRM
- [ ] Set up Google Analytics
- [ ] Test on real mobile devices
- [ ] Run Lighthouse audit (target 90+)
- [ ] Run accessibility audit (axe DevTools)
- [ ] Verify all links work
- [ ] Get stakeholder approval

---

## Security Notes

### Never commit:

- ❌ API keys
- ❌ Database credentials
- ❌ CRM passwords
- ❌ Personal information
- ❌ Client proprietary data

### Use .gitignore:

Already set up to exclude:
- Environment files (.env)
- Credentials (*.key, *.pem)
- Temporary files
- Operating system files

---

## Support Resources

- **GitHub Pages Docs:** https://docs.github.com/pages
- **GitHub Docs:** https://docs.github.com
- **Git Documentation:** https://git-scm.com/doc
- **GitHub Community:** https://github.com/community

---

## Quick Reference Commands

```bash
# Check status
git status

# Add all changes
git add .

# Commit changes
git commit -m "Your message here"

# Push to GitHub
git push origin main

# Pull latest changes
git pull origin main

# View commit history
git log --oneline

# Create new branch
git checkout -b branch-name

# Switch branches
git checkout branch-name

# View remotes
git remote -v
```

---

**That's it! Your site should now be live on GitHub Pages. 🚀**

For questions, contact the Splash development team or refer to the main README.md.
