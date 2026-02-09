# Deployment Guide - Photography Portfolio

This guide will help you deploy your photography portfolio to the web using GitHub Pages, Vercel, or Netlify.

---

## Option 1: GitHub Pages (Free & Easy)

### Prerequisites:
- GitHub account (create at https://github.com)
- Git installed on your computer

### Step 1: Initialize Git Repository

```bash
cd "/Users/sports/Documents/Web Abshir"
git init
git add .
git commit -m "Initial commit - Photography portfolio"
```

### Step 2: Create GitHub Repository

1. Go to https://github.com/new
2. Repository name: `photography-portfolio` (or your preferred name)
3. Description: "Abshir Rageh Photography Portfolio"
4. Keep it Public (required for free GitHub Pages)
5. **DO NOT** initialize with README, .gitignore, or license
6. Click "Create repository"

### Step 3: Push to GitHub

```bash
# Replace 'yourusername' with your actual GitHub username
git remote add origin https://github.com/yourusername/photography-portfolio.git
git branch -M main
git push -u origin main
```

### Step 4: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click "Settings" tab
3. Click "Pages" in the left sidebar
4. Under "Source", select "main" branch
5. Click "Save"
6. Wait 1-2 minutes for deployment

Your site will be live at: `https://yourusername.github.io/photography-portfolio/`

### Step 5: Custom Domain (Optional)

If you have a custom domain:
1. In GitHub Pages settings, add your custom domain
2. Update your domain's DNS settings:
   - Add CNAME record pointing to `yourusername.github.io`
3. Enable "Enforce HTTPS"

---

## Option 2: Vercel (Recommended - Fastest)

### Why Vercel?
- ✅ Instant deployments
- ✅ Automatic HTTPS
- ✅ Free custom domain
- ✅ Automatic rebuilds on git push
- ✅ Best performance

### Step 1: Push to GitHub First
Follow Option 1, Steps 1-3 above to push your code to GitHub.

### Step 2: Deploy to Vercel

1. Go to https://vercel.com/signup
2. Sign up with GitHub
3. Click "Add New Project"
4. Import your `photography-portfolio` repository
5. Configure:
   - **Framework Preset:** Other
   - **Root Directory:** ./
   - **Build Command:** (leave empty)
   - **Output Directory:** (leave empty)
6. Click "Deploy"

Your site will be live at: `https://your-project-name.vercel.app`

### Step 3: Custom Domain on Vercel

1. Go to Project Settings → Domains
2. Add your custom domain
3. Follow DNS configuration instructions
4. Vercel automatically handles HTTPS

---

## Option 3: Netlify (Also Great)

### Why Netlify?
- ✅ Drag & drop deployment
- ✅ Form handling (perfect for your contact form!)
- ✅ Automatic HTTPS
- ✅ Free custom domain

### Method A: Drag & Drop (Easiest)

1. Go to https://app.netlify.com/drop
2. Drag your entire project folder onto the page
3. Done! Your site is live

### Method B: Git Integration (Recommended)

1. Push to GitHub (see Option 1, Steps 1-3)
2. Go to https://app.netlify.com
3. Click "Add new site" → "Import an existing project"
4. Choose GitHub and authorize
5. Select your repository
6. Configure:
   - **Build command:** (leave empty)
   - **Publish directory:** ./
7. Click "Deploy site"

Your site will be live at: `https://random-name-12345.netlify.app`

### Step 3: Setup Contact Form on Netlify

Netlify has built-in form handling! Update your form in `index.html`:

```html
<!-- Replace the Formspree form with Netlify form -->
<form name="consultation" method="POST" data-netlify="true" netlify-honeypot="bot-field">
  <input type="hidden" name="form-name" value="consultation">
  <input type="hidden" name="bot-field">
  <!-- rest of your form fields -->
</form>
```

Forms will be sent to your Netlify dashboard and email!

### Step 4: Custom Domain on Netlify

1. Go to Site Settings → Domain Management
2. Click "Add custom domain"
3. Follow DNS configuration instructions

---

## Quick Comparison

| Feature | GitHub Pages | Vercel | Netlify |
|---------|-------------|--------|---------|
| **Ease of Setup** | Medium | Easy | Easiest |
| **Speed** | Good | Excellent | Excellent |
| **Custom Domain** | Yes | Yes (easier) | Yes (easier) |
| **Form Handling** | No | No | Yes (built-in) |
| **HTTPS** | Yes | Yes (auto) | Yes (auto) |
| **Build Time** | 1-2 min | Instant | Instant |
| **Best For** | Simple sites | Performance | Forms & features |

---

## Recommended Workflow

### For Your Portfolio, I Recommend:

**Option: Netlify** (Best overall for your needs)
- Built-in form handling (no Formspree needed!)
- Easiest deployment
- Great performance
- Free tier is generous

### Steps:
1. Push code to GitHub (for version control)
2. Deploy to Netlify (for hosting)
3. Use Netlify Forms (replace Formspree)
4. Add custom domain if you have one

---

## Before Deploying - Final Checklist

- [ ] Update Instagram username in all locations
- [ ] Update email address
- [ ] Replace placeholder images with real photography
- [ ] Test locally one more time: `python3 -m http.server 8080`
- [ ] Commit all changes: `git add . && git commit -m "Ready for deployment"`

---

## After Deployment

### Test Your Live Site:
- [ ] All pages load correctly
- [ ] Images display properly
- [ ] Contact form works
- [ ] Social media links work
- [ ] Mobile responsive
- [ ] HTTPS is enabled

### Share Your Portfolio:
- [ ] Add to Instagram bio
- [ ] Share on social media
- [ ] Add to email signature
- [ ] Update LinkedIn profile

---

## Need Help?

### Common Issues:

**Images not loading:**
- Check file paths are correct (case-sensitive!)
- Ensure images are in `/assets/images/` folder
- Verify images are committed to git

**Form not working:**
- For Netlify: Use Netlify Forms (see above)
- For others: Get Formspree form ID from https://formspree.io

**Custom domain not working:**
- Wait 24-48 hours for DNS propagation
- Check DNS settings are correct
- Verify CNAME/A records point to correct host

---

## Quick Deploy Commands

### Update and Redeploy:
```bash
cd "/Users/sports/Documents/Web Abshir"
git add .
git commit -m "Update portfolio"
git push
```

Vercel and Netlify will automatically redeploy!

---

**Ready to deploy? Choose your platform and follow the steps above!**
