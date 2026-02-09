# Configuration Checklist - Before Going Live

This checklist tracks all the placeholders and configurations that need your personal details before the site goes live.

## ✅ Completed
- [x] Fixed image modal bug (now shows correct clicked image)
- [x] Updated manifest.json with "Abshir Rageh Photography"
- [x] Removed LinkedIn, Vimeo, and YouTube social links
- [x] Added clear TODO comments for remaining placeholders

## 🔴 Required - Needs Your Information

### 1. Instagram Username
**Location:** Multiple places in `index.html`
- Line ~296: Instagram connect button
- Line ~337: Footer social links  
- Line ~440: Project card Instagram links

**Current:** `https://www.instagram.com/yourusername`
**Action:** Replace `yourusername` with your actual Instagram username

### 2. Email Address
**Location:** `index.html` line ~351
**Current:** `mailto:your@email.com`
**Action:** Replace `your@email.com` with your actual email address

### 3. Formspree Form ID
**Location:** `index.html` line ~308
**Current:** `action="https://formspree.io/f/your-form-id"`
**Action:** 
1. Go to https://formspree.io and create a free account
2. Create a new form
3. Copy your form ID (looks like: `xyzabc123`)
4. Replace `your-form-id` with your actual form ID

## 📋 Optional Improvements

### Images
- Current: Using `.svg` placeholder images
- Recommendation: Replace with actual photography in `.jpg` or `.webp` format
- Location: `/assets/images/` directory

### Project Content
- Review project descriptions in the JavaScript `projectData` object (line ~420)
- Update with your actual project details, dates, and stories

### SEO & Analytics
- Add Open Graph meta tags for social media sharing
- Add Google Analytics or privacy-friendly alternative (Plausible, Fathom)
- Add structured data (JSON-LD) for better search results

## 🧪 Testing Checklist

Before going live, test:
- [ ] Contact form submits successfully to your email
- [ ] All Instagram links go to your profile
- [ ] Email link opens your email client
- [ ] All project modals open correctly
- [ ] Image modals show the correct images when clicked
- [ ] Mobile responsive design works on phone/tablet
- [ ] All animations work smoothly
- [ ] Page loads quickly

## 🚀 Deployment

Once all items above are completed:
1. Test locally: `npm start` or `python3 -m http.server 8000`
2. Deploy to your chosen platform (Vercel, Netlify, GitHub Pages)
3. Test the live site thoroughly
4. Share your portfolio!

---

**Quick Find & Replace Guide:**
- Find: `yourusername` → Replace with your Instagram username
- Find: `your@email.com` → Replace with your email
- Find: `your-form-id` → Replace with your Formspree form ID
