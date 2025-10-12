# Website Testing Checklist
**Date:** October 13, 2025  
**Website:** Pro Agro Global Ltd  
**Pages:** 5 (Homepage, About, Services, Gallery, Contact)

---

## ✅ Navigation Testing

### Desktop Navigation
- [ ] Click "Home" in navbar → Should stay on/return to `index.html`
- [ ] Click "About" in navbar → Should navigate to `pages/about.html`
- [ ] Click "Services" in navbar → Should navigate to `pages/services.html`
- [ ] Click "Gallery" in navbar → Should navigate to `pages/gallery.html`
- [ ] Click "Get Quote" button in navbar → Should navigate to `pages/contact.html`
- [ ] Click logo → Should return to `index.html`
- [ ] Verify active states (green text + border) show on current page

### Mobile Navigation (< 768px)
- [ ] Click hamburger menu icon → Menu should open
- [ ] Click each menu item → Should navigate correctly
- [ ] Click hamburger again → Menu should close
- [ ] Verify mobile menu styling and animations work
- [ ] Test on actual mobile device (not just browser resize)

### Page-to-Page Navigation
- [ ] Navigate: Home → About → Services → Gallery → Contact
- [ ] Use browser back button on each page
- [ ] Verify all "back-to-top" buttons appear after scrolling
- [ ] Test all footer links on every page

---

## ✅ Homepage (index.html) Links

### Hero Section
- [ ] "Our Services" button → Should go to `pages/services.html`
- [ ] "Contact Us" button → Should go to `pages/contact.html`
- [ ] Scroll down indicator → Should smoothly scroll to Welcome section

### Welcome Section
- [ ] "Learn More About Us" button → Should go to `pages/about.html`

### Services Section (4 cards)
- [ ] "Learn More" under Irrigation → Should go to `pages/services.html#irrigation`
- [ ] "Learn More" under Greenhouses → Should go to `pages/services.html#greenhouses`
- [ ] "Learn More" under Geomembranes → Should go to `pages/services.html#geomembranes`
- [ ] "Learn More" under Civil Engineering → Should go to `pages/services.html#civil`
- [ ] Verify section anchors scroll to correct sections on services page

### Projects Section
- [ ] "View Complete Portfolio" button → Should go to `pages/gallery.html`

### Footer - Quick Links
- [ ] Home → `index.html`
- [ ] About Us → `pages/about.html`
- [ ] Services → `pages/services.html`
- [ ] Gallery → `pages/gallery.html`
- [ ] Contact → `pages/contact.html`

### Footer - Our Services
- [ ] Irrigation Systems → `pages/services.html#irrigation`
- [ ] Greenhouses → `pages/services.html#greenhouses`
- [ ] Geomembranes → `pages/services.html#geomembranes`
- [ ] Civil Engineering → `pages/services.html#civil`

---

## ✅ About Page Testing

### Navigation
- [ ] Verify "About" link has active state in navbar
- [ ] All navbar links work correctly
- [ ] Footer links work correctly

### Content
- [ ] Hero image loads (`IMG-20251008-WA0081.jpg`)
- [ ] Story grid shows 4 images correctly
- [ ] Mission & Vision cards display properly
- [ ] Core Values section readable
- [ ] Achievements stats visible
- [ ] Why Choose Us section displays all 6 reasons
- [ ] CTA buttons at bottom work

---

## ✅ Services Page Testing

### Navigation
- [ ] Verify "Services" link has active state in navbar
- [ ] All navbar links work correctly
- [ ] Section anchors work when linked from homepage (#irrigation, #greenhouses, #geomembranes, #civil)

### Content
- [ ] Hero image loads (`IMG-20251008-WA0086.jpg`)
- [ ] Overview cards display all 4 services
- [ ] **Irrigation section:** 4 images load (WA0087-090), content displays
- [ ] **Greenhouses section:** 4 images load (WA0091-094), content displays
- [ ] **Geomembranes section:** 3 images load (WA0095-097), stats visible
- [ ] **Civil Engineering section:** 3 images load, content displays
- [ ] Process timeline shows all 5 steps
- [ ] CTA section at bottom works

---

## ✅ Gallery Page Testing

### Navigation
- [ ] Verify "Gallery" link has active state in navbar
- [ ] All navbar links work correctly

### Gallery Functionality
- [ ] Click "All" filter → Shows all 18 images
- [ ] Click "Irrigation" filter → Shows 5 irrigation images
- [ ] Click "Greenhouses" filter → Shows 4 greenhouse images
- [ ] Click "Geomembranes" filter → Shows 4 geomembrane images
- [ ] Click "Civil" filter → Shows 4 civil engineering images
- [ ] Active filter button has green background
- [ ] Hover effects work on gallery images

### Lightbox Modal
- [ ] Click any image → Lightbox opens with correct image
- [ ] Click "Previous" button → Shows previous image (circular navigation)
- [ ] Click "Next" button → Shows next image (circular navigation)
- [ ] Press "←" (left arrow) key → Previous image
- [ ] Press "→" (right arrow) key → Next image
- [ ] Press "ESC" key → Lightbox closes
- [ ] Click outside modal (on overlay) → Lightbox closes
- [ ] Click "×" close button → Lightbox closes
- [ ] Project title and description display correctly
- [ ] Lightbox respects filtered images (only navigates within visible category)
- [ ] Zoom-in animation works on open

---

## ✅ Contact Page Testing

### Navigation
- [ ] Verify "Contact" link has active state in navbar
- [ ] All navbar links work correctly

### Contact Cards
- [ ] Phone number link is clickable (tel: link)
- [ ] Email link opens email client (mailto: link)
- [ ] Office address displays correctly

### Contact Form
- [ ] Try submitting empty form → Should show validation errors
- [ ] Fill in name only → Should require other fields
- [ ] Enter invalid email format → Should show error
- [ ] Select a service from dropdown → Should work
- [ ] Try submitting without checking terms → Should show error
- [ ] Fill all fields correctly + check terms → Form submits
- [ ] Success message appears after submission
- [ ] Form resets after successful submission

### FAQ Accordion
- [ ] Click question 1 → Should expand with smooth animation
- [ ] Click question 2 → Question 1 closes, question 2 opens (one-at-a-time)
- [ ] Click same question again → Should close
- [ ] Test all 6 FAQ items
- [ ] Chevron icons rotate correctly

### Other Elements
- [ ] Google Maps iframe loads correctly
- [ ] Business hours display properly
- [ ] Contact details (address, phone, email) visible
- [ ] Social media icons present (even if placeholder links)
- [ ] Quick links card works (Services, Gallery, About, Company Profile)

---

## ✅ Responsive Design Testing

### Mobile (320px - 767px)
Test on: iPhone SE (320px), iPhone 12 (375px), iPhone 14 Pro Max (414px)
- [ ] Homepage displays correctly, no horizontal scroll
- [ ] About page layout stacks properly
- [ ] Services page readable, images scale correctly
- [ ] Gallery grid adjusts (1-2 columns)
- [ ] Contact form fields stack vertically
- [ ] Mobile menu works smoothly
- [ ] All buttons are tap-friendly (min 44px touch target)
- [ ] Text is readable (minimum 16px body text)
- [ ] Images don't overflow containers

### Tablet (768px - 1365px)
Test on: iPad (768px), iPad Pro (1024px)
- [ ] Homepage layout looks balanced
- [ ] About page uses 2-column grids where appropriate
- [ ] Services page displays well
- [ ] Gallery uses 2-3 column grid
- [ ] Contact form has good spacing
- [ ] Desktop navbar shows (not hamburger menu)
- [ ] Images scale proportionally

### Desktop (1366px+)
Test on: Laptop (1366px), Full HD (1920px), QHD (2560px)
- [ ] All pages use max-width container (7xl = 1280px)
- [ ] Content is centered, not stretched edge-to-edge
- [ ] Multi-column layouts display correctly
- [ ] Hero sections have full-width backgrounds
- [ ] Gallery uses 3-4 column grid
- [ ] No excessive white space
- [ ] Images are sharp (not pixelated)

---

## ✅ Cross-Browser Testing

### Chrome (Latest)
- [ ] All pages load correctly
- [ ] JavaScript features work (lightbox, accordion, filtering)
- [ ] CSS animations smooth
- [ ] Font rendering good

### Firefox (Latest)
- [ ] All pages load correctly
- [ ] JavaScript features work
- [ ] CSS grid/flexbox layouts correct
- [ ] No console errors

### Safari (macOS/iOS)
- [ ] All pages load correctly
- [ ] JavaScript features work
- [ ] webkit-specific CSS works
- [ ] Forms work on iOS

### Edge (Latest)
- [ ] All pages load correctly
- [ ] JavaScript features work
- [ ] Performance good

---

## ✅ Image Testing

### Image Loading
- [ ] All homepage images load (12 images: WA0069-080)
- [ ] All about page images load (5 images: WA0081-085)
- [ ] All services page images load (14 images: WA0086-099)
- [ ] All gallery images load (18 total, 13 new + 5 reused)
- [ ] Contact page hero image loads
- [ ] Logo displays correctly on all pages

### Image Quality
- [ ] Images are not pixelated or blurry
- [ ] Images scale proportionally (no distortion)
- [ ] Hover zoom effects work without quality loss
- [ ] Lightbox images display at good quality

### Alt Text
- [ ] All images have descriptive alt text
- [ ] Alt text is meaningful (not just filename)

---

## ✅ Performance Testing

### PageSpeed Insights
Run test on all 5 pages: https://pagespeed.web.dev/

**Homepage:**
- [ ] Desktop score: Target 90+
- [ ] Mobile score: Target 85+
- [ ] First Contentful Paint (FCP): < 1.8s
- [ ] Largest Contentful Paint (LCP): < 2.5s
- [ ] Cumulative Layout Shift (CLS): < 0.1
- [ ] Time to Interactive (TTI): < 3.8s

**About Page:**
- [ ] Desktop score: ___
- [ ] Mobile score: ___

**Services Page:**
- [ ] Desktop score: ___
- [ ] Mobile score: ___

**Gallery Page:**
- [ ] Desktop score: ___
- [ ] Mobile score: ___

**Contact Page:**
- [ ] Desktop score: ___
- [ ] Mobile score: ___

### Manual Performance Check
- [ ] Pages load within 3 seconds on good connection
- [ ] No render-blocking resources
- [ ] Images load progressively
- [ ] No cumulative layout shift (content jumping)
- [ ] Smooth scrolling throughout

---

## ✅ Accessibility Testing

### Keyboard Navigation
- [ ] Tab through all interactive elements
- [ ] Skip to main content link works
- [ ] Focus indicators visible
- [ ] Lightbox can be controlled via keyboard
- [ ] Forms are fully keyboard accessible
- [ ] Mobile menu keyboard accessible

### Screen Reader Testing
- [ ] Page structure makes sense
- [ ] ARIA labels present on icon buttons
- [ ] Form labels properly associated
- [ ] Image alt text reads correctly
- [ ] Heading hierarchy logical (H1 → H2 → H3)

### Color Contrast
- [ ] Text meets WCAG AA standards (4.5:1 ratio)
- [ ] Button text readable
- [ ] Links distinguishable
- [ ] Focus indicators visible

---

## ✅ SEO Validation

### Meta Tags (Check all 5 pages)
- [ ] Title tags present and unique
- [ ] Meta descriptions present and compelling
- [ ] Open Graph tags present
- [ ] Canonical URLs set
- [ ] Language attribute set

### Content
- [ ] Each page has one H1 heading
- [ ] Heading hierarchy makes sense
- [ ] Internal linking implemented
- [ ] All links have descriptive text (no "click here")

---

## ✅ Form Functionality

### Contact Form Validation
- [ ] Name field: Required, min 2 characters
- [ ] Email field: Required, valid format
- [ ] Phone field: Required
- [ ] Service dropdown: Required
- [ ] Subject field: Required
- [ ] Message field: Required, min characters
- [ ] Terms checkbox: Required

### Form Submission
- [ ] Success message displays
- [ ] Form clears after submission
- [ ] Error messages are clear
- [ ] Form doesn't submit with invalid data

---

## ✅ Console Errors

Check browser console on all pages:
- [ ] Homepage: No JavaScript errors
- [ ] About: No JavaScript errors
- [ ] Services: No JavaScript errors
- [ ] Gallery: No JavaScript errors
- [ ] Contact: No JavaScript errors
- [ ] No 404 errors for missing resources
- [ ] No CSS errors

---

## 🚀 Image Optimization Tasks

### Compression Needed
Total images: 48 (IMG-20251008-WA0069.jpg through WA0112.jpg)

**Tools to use:**
- TinyPNG (https://tinypng.com/) - Online, batch upload
- Squoosh (https://squoosh.app/) - Online, more control
- ImageOptim (macOS) - Drag and drop
- RIOT (Windows) - Local tool

**Target:**
- 70-80% file size reduction
- No visible quality loss
- Maintain aspect ratios

**Process:**
1. [ ] Backup original images folder
2. [ ] Compress all 48 images
3. [ ] Replace original images with compressed versions
4. [ ] Test website to ensure images still look good
5. [ ] Run PageSpeed Insights again to measure improvement

---

## 📋 Known Issues / Notes

**Placeholder Links:**
- Social media icons currently link to "#" (need real URLs)
- Privacy Policy and Terms of Service link to "#" (need pages created)

**Future Enhancements:**
- Consider adding lazy loading for images
- Consider adding image srcset for responsive images
- Consider adding a loading skeleton for gallery
- Consider adding form backend (currently frontend only)

---

## ✅ Final Verification

- [ ] All 5 pages accessible via navigation
- [ ] All 44 unique images displayed correctly
- [ ] All interactive features working
- [ ] Responsive on all devices
- [ ] No broken links
- [ ] No console errors
- [ ] Good performance scores
- [ ] Backup files safely stored
- [ ] Documentation complete

---

**Completion Date:** _____________  
**Tested By:** _____________  
**Status:** ⏳ In Progress / ✅ Complete  
**Notes:**

