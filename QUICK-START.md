# Quick Start Guide

Get the Splash Roofing Marketing Microsite deployed to GitHub Pages in 5 minutes.

---

## 🚀 Fastest Path to Deployment

### Option 1: Automated Script (Recommended)

```bash
# Navigate to this folder
cd /path/to/github-deploy

# Run the deployment script
./deploy.sh
```

The script will:
1. Initialize Git repository
2. Add and commit files
3. Ask for your GitHub username and repo name
4. Add remote and push to GitHub
5. Give you instructions to enable GitHub Pages

---

### Option 2: Manual Commands

```bash
# 1. Initialize Git
git init

# 2. Add all files
git add .

# 3. Commit
git commit -m "Initial commit: Roofing microsite - 13 pages"

# 4. Set main branch
git branch -M main

# 5. Add remote (replace USERNAME and REPO)
git remote add origin https://github.com/USERNAME/REPO.git

# 6. Push to GitHub
git push -u origin main
```

Then:
1. Go to GitHub repository Settings → Pages
2. Set Source to `main` branch, `/` (root) folder
3. Save and wait 1-2 minutes

Your site will be live at:
```
https://USERNAME.github.io/REPO/roofing-marketing/
```

---

## 📋 Pre-Flight Checklist

Before deploying, verify:

- [ ] You have a GitHub account
- [ ] Git is installed (`git --version`)
- [ ] All 13 HTML files are in `roofing-marketing/` folder
- [ ] README.md and documentation files are present
- [ ] .gitignore is present

---

## 🎯 What You're Deploying

**13 Complete Pages:**
- Homepage (index.html)
- Strategy page
- One-Day Marketing Strategy page
- Digital Marketing hub
- SEO service page
- LSA service page
- Email service page
- Social service page
- Websites service page
- Video service page
- Resources hub
- Schedule call form page
- Thank you confirmation page

**Status:** 87% complete (2 pages missing: PPC, Results)

**Features:**
- ✅ Mobile responsive
- ✅ Accessibility (WCAG 2.2 AA)
- ✅ Forms with validation
- ✅ FAQ accordions
- ✅ Strategy-first positioning
- ✅ 219 honest placeholders

---

## 🔗 After Deployment

### Test These URLs:

```
https://YOUR-SITE/roofing-marketing/
https://YOUR-SITE/roofing-marketing/strategy.html
https://YOUR-SITE/roofing-marketing/digital-marketing.html
https://YOUR-SITE/roofing-marketing/schedule-strategy-call.html
```

### Verify These Work:

- [ ] Navigation menu
- [ ] Mobile menu (hamburger icon)
- [ ] FAQ accordions expand/collapse
- [ ] Forms validate (won't submit without backend)
- [ ] All internal links work
- [ ] Mobile layout looks good

---

## ⚠️ Known Limitations

**Before Launch:**
1. 2 pages missing (Google Ads PPC, Results)
2. Forms not connected to backend
3. 219 production assets needed
4. No analytics tracking yet
5. CSS/JS should be extracted

**After These Fixed:** Ready for client preview

---

## 📖 More Documentation

- **README.md** - Full project overview
- **DEPLOYMENT-GUIDE.md** - Detailed step-by-step GitHub setup
- **STRUCTURE.md** - Repository structure and file organization
- **CHANGELOG.md** - Version history and changes

---

## 🆘 Need Help?

### Common Issues

**Push failed?**
- Check you created the repository on GitHub first
- Verify your GitHub credentials
- Try: `git push -u origin main --force` (only if new repo)

**Site not loading?**
- Wait 2-3 minutes for first deployment
- Check GitHub Pages is enabled in Settings
- Verify URL includes `/roofing-marketing/` path

**Navigation broken?**
- Check all internal links include `.html` extension
- Verify file names match exactly (case-sensitive)

### Getting Support

- GitHub Docs: https://docs.github.com/pages
- Git Documentation: https://git-scm.com/doc
- Repository Issues: (create issue on GitHub repo)

---

## 🎉 Success!

Once deployed, share the link:

```
https://YOUR-USERNAME.github.io/YOUR-REPO/roofing-marketing/
```

**Next Steps:**
1. Test the live site thoroughly
2. Share with team for review
3. Document any bugs or issues
4. Plan for missing pages (PPC, Results)
5. Gather production assets

---

**Happy deploying! 🚀**
