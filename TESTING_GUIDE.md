# Testing Guide - Photography Portfolio

The development server is now running at: **http://localhost:8080**

## 🧪 Manual Testing Checklist

### 1. Initial Page Load
- [ ] Page loads without errors (check browser console - F12)
- [ ] All fonts load correctly (Playfair Display, Inter, Cinzel, Roboto Slab)
- [ ] Favicon appears in browser tab
- [ ] Page title shows "Photography Portfolio — Abshir Rageh"

### 2. Navigation Testing
- [ ] **Desktop Navigation:**
  - [ ] Click "Projects" - should smooth scroll to projects section
  - [ ] Click "Consultations" - should smooth scroll to consultation form
  - [ ] Navigation stays sticky when scrolling
  
- [ ] **Mobile Navigation (resize browser to < 768px):**
  - [ ] Hamburger menu icon appears
  - [ ] Click hamburger - menu opens
  - [ ] Click "Projects" - menu closes and scrolls to section
  - [ ] Click "Consultations" - menu closes and scrolls to section

### 3. Project Cards Testing
Test all 6 project cards:
- [ ] **Stetson** - Click to open modal
- [ ] **Miller High Life x Tie Bar** - Click to open modal
- [ ] **Fender Guitars x Kyser Capos** - Click to open modal
- [ ] **Taylor Stitch** - Click to open modal
- [ ] **Kyser Capos** - Click to open modal
- [ ] **Project Shine** - Click to open modal

For each project modal:
- [ ] Modal opens correctly
- [ ] Project title and details display
- [ ] "How It Feels Being On This Project" section shows
- [ ] Videos embed correctly (if present)
- [ ] Image gallery displays
- [ ] Click on any image - image modal opens with CORRECT image (bug fix validation)
- [ ] Close image modal with X button
- [ ] Close image modal with ESC key
- [ ] Close image modal by clicking outside
- [ ] Close project modal with X button
- [ ] Close project modal with ESC key
- [ ] Close project modal by clicking outside
- [ ] Body scroll is disabled when modal is open
- [ ] Body scroll is restored when modal closes

### 4. Image Modal Bug Fix Validation
**CRITICAL TEST - This was the main bug we fixed:**

For any project (e.g., Stetson with 8 images):
- [ ] Click image 1 - modal shows stetson-1.svg ✓
- [ ] Close and click image 2 - modal shows stetson-2.svg (NOT stetson-1.svg) ✓
- [ ] Close and click image 3 - modal shows stetson-3.svg ✓
- [ ] Close and click image 5 - modal shows stetson-5.svg ✓
- [ ] Close and click image 8 - modal shows stetson-8.svg ✓

**Expected:** Each image should show the correct numbered file
**Bug (if present):** All images would show -1.svg file

### 5. Contact Form Testing
- [ ] Form displays correctly
- [ ] Try submitting empty form - validation errors appear
- [ ] Fill in Name field
- [ ] Fill in Email field (use valid email format)
- [ ] Fill in Project Type (optional)
- [ ] Fill in Message (optional)
- [ ] Click "BOOK A CONSULTATION"
- [ ] Note: Form will show error because Formspree ID is placeholder
- [ ] Expected error: "Form not found" or similar from Formspree

### 6. Social Media Links Testing
- [ ] **Instagram button (purple gradient)** in consultation section
  - [ ] Click - opens https://www.instagram.com/yourusername (placeholder)
  - [ ] Opens in new tab
  
- [ ] **Footer Instagram icon**
  - [ ] Hover - icon scales up, background changes to orange
  - [ ] Click - opens Instagram (placeholder)
  
- [ ] **Footer Email icon**
  - [ ] Hover - icon scales up, background changes to orange
  - [ ] Click - opens email client with mailto:your@email.com
  
- [ ] **Project card Instagram icons**
  - [ ] Each project card has floating Instagram icon
  - [ ] Hover - changes color to orange
  - [ ] Click - opens Instagram (placeholder)

### 7. Animations Testing
- [ ] **Scroll Animations:**
  - [ ] Scroll down page slowly
  - [ ] "Featured Projects" heading fades in when visible
  - [ ] Project cards fade in as they enter viewport
  - [ ] Consultation section elements animate in
  
- [ ] **Hover Effects:**
  - [ ] Project cards lift up on hover (translateY + scale)
  - [ ] Social media icons scale up on hover
  - [ ] Buttons show hover states
  - [ ] Instagram icons have floating animation
  
- [ ] **Button Animations:**
  - [ ] "View Project →" buttons show shimmer effect on hover
  - [ ] "BOOK A CONSULTATION" button changes style on hover

### 8. Responsive Design Testing

**Mobile (375px - iPhone SE):**
- [ ] Resize browser to 375px width
- [ ] Navigation shows hamburger menu
- [ ] Project grid shows 1 column
- [ ] All text is readable
- [ ] Images scale properly
- [ ] Modals fit on screen
- [ ] Form is usable

**Tablet (768px - iPad):**
- [ ] Resize browser to 768px width
- [ ] Navigation shows full menu
- [ ] Project grid shows 2 columns
- [ ] Layout looks balanced
- [ ] Modals display well

**Desktop (1280px+):**
- [ ] Resize browser to 1280px+ width
- [ ] Project grid shows 3 columns
- [ ] Maximum width container centers content
- [ ] Plenty of whitespace
- [ ] All elements properly aligned

### 9. Console Error Check
Open browser console (F12 → Console tab):
- [ ] No JavaScript errors
- [ ] No 404 errors for missing files
- [ ] No CSS errors
- [ ] Check for any warnings

### 10. Performance Check
- [ ] Page loads quickly (< 2 seconds)
- [ ] Animations are smooth (60fps)
- [ ] No layout shifts during load
- [ ] Images load progressively

## 🐛 Known Issues to Verify Are Fixed

### ✅ Fixed Issues:
1. **Image Modal Bug** - Now shows correct image when clicked (not always image-1)
2. **Manifest.json** - Updated to "Abshir Rageh Photography"
3. **Social Links** - Removed LinkedIn, Vimeo, YouTube (kept only Instagram & Email)
4. **TODO Comments** - Added clear markers for placeholders

### ⚠️ Expected Placeholder Warnings:
1. **Formspree Form** - Will not submit (needs real form ID)
2. **Instagram Links** - Go to /yourusername (needs real username)
3. **Email Link** - Opens your@email.com (needs real email)
4. **Images** - SVG placeholders (should be replaced with real photos)

## 📝 Testing Results

After completing the tests above, note any issues found:

**Issues Found:**
- [ ] Issue 1: _____________________
- [ ] Issue 2: _____________________
- [ ] Issue 3: _____________________

**All Tests Passed:**
- [ ] Yes, ready for configuration
- [ ] No, needs fixes (list above)

---

## 🚀 Next Steps After Testing

If all tests pass:
1. Update Instagram username in all locations
2. Update email address
3. Get Formspree form ID and update
4. Replace SVG images with real photography
5. Deploy to production

**Server is running at: http://localhost:8080**
**To stop server: Press Ctrl+C in the terminal**
