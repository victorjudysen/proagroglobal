# 🚀 Deployment Guide
**Pro Agro Global Website**  
**Date:** October 13, 2025

---

## 📋 Pre-Deployment Checklist

### ✅ Files Ready for Deployment

#### HTML Files (5)
- [x] `index.html` - Homepage
- [x] `pages/about.html` - About page
- [x] `pages/services.html` - Services page
- [x] `pages/gallery.html` - Gallery page
- [x] `pages/contact.html` - Contact page

#### Assets
- [x] `assets/images/` - 48 images (44 used)
- [x] `assets/images/logo.png` - Company logo
- [x] `assets/documents/companyprofile.pdf` - Company profile

#### Documentation
- [x] `RENOVATION_COMPLETE.md` - Project summary
- [x] `RENOVATION_PROGRESS.md` - Progress tracking
- [x] `TESTING_CHECKLIST.md` - Testing guide
- [x] `IMAGE_OPTIMIZATION_GUIDE.md` - Optimization instructions
- [x] `DEPLOYMENT_GUIDE.md` - This file

#### Backup Files (Keep for rollback)
- [x] `index_backup.html`
- [x] `pages/about_backup.html`
- [x] `pages/services_backup.html`
- [x] `pages/gallery_backup.html`
- [x] `pages/contact_backup.html`

---

## 🎯 Pre-Deployment Tasks

### 1. Image Optimization (Recommended)
**Before deploying, compress all images to improve performance:**

See `IMAGE_OPTIMIZATION_GUIDE.md` for detailed instructions.

**Quick method:**
1. Visit https://tinypng.com/
2. Upload 20 images at a time (3 batches)
3. Download compressed versions
4. Replace original files

**Expected result:** 70-80% file size reduction

### 2. Final Testing
**Open website locally and verify:**

- [ ] All pages load correctly
- [ ] All navigation links work
- [ ] All images display properly
- [ ] Mobile menu works
- [ ] Contact form validates correctly
- [ ] Gallery filtering works
- [ ] Lightbox modal opens/closes
- [ ] FAQ accordion expands/collapses

### 3. Update Placeholder Links
**Before deploying, update these placeholder links:**

#### Social Media (Footer - All Pages)
Current: `href="#"`

Update to actual URLs:
```html
<!-- Facebook -->
<a href="https://www.facebook.com/proagroglobal" ...>

<!-- Instagram -->
<a href="https://www.instagram.com/proagroglobal" ...>

<!-- LinkedIn -->
<a href="https://www.linkedin.com/company/proagroglobal" ...>

<!-- Twitter/X (or remove if not used) -->
<a href="https://twitter.com/proagroglobal" ...>
```

#### Legal Pages (Footer)
Current: `href="#"`

Options:
1. Create actual Privacy Policy and Terms pages
2. Link to existing documents
3. Remove links temporarily

---

## 📁 File Structure for Deployment

```
proagroglobal/
├── index.html
├── pages/
│   ├── about.html
│   ├── services.html
│   ├── gallery.html
│   └── contact.html
├── assets/
│   ├── images/
│   │   ├── logo.png
│   │   ├── extrusion.jpg
│   │   ├── field.png
│   │   ├── fishpond.png
│   │   ├── greenhouses.jpg
│   │   ├── IMG-20251008-WA0069.jpg
│   │   ├── IMG-20251008-WA0070.jpg
│   │   └── ... (through WA0112.jpg)
│   └── documents/
│       └── companyprofile.pdf
└── (Optional: Don't deploy backup files)
```

---

## 🌐 Deployment Methods

### Option 1: GitHub Pages (Free)

**Best for:** Static websites, free hosting, easy deployment

**Steps:**

1. **Create GitHub repository** (if not exists):
```bash
git init
git add .
git commit -m "Website renovation complete"
git branch -M main
git remote add origin https://github.com/victorjudysen/proagroglobal.git
git push -u origin main
```

2. **Enable GitHub Pages:**
   - Go to repository Settings
   - Navigate to "Pages" section
   - Source: Deploy from branch
   - Branch: main
   - Folder: / (root)
   - Click Save

3. **Wait 2-5 minutes**, then visit:
   - `https://victorjudysen.github.io/proagroglobal/`

4. **Custom domain (optional):**
   - Add CNAME file with your domain
   - Configure DNS settings
   - Enable HTTPS

**Pros:** Free, automatic deployment, HTTPS included  
**Cons:** Public repository (unless Pro account)

---

### Option 2: Netlify (Recommended)

**Best for:** Easy deployment, instant previews, forms backend

**Steps:**

1. **Sign up:** https://netlify.com (free account)

2. **Deploy via drag & drop:**
   - Click "Add new site" → "Deploy manually"
   - Drag project folder to upload area
   - Wait 30 seconds
   - Site live at `random-name.netlify.app`

3. **Or deploy via Git:**
   - Connect GitHub repository
   - Auto-deploy on push
   - Build settings: None needed (static site)

4. **Configure:**
   - Change site name
   - Add custom domain
   - Enable forms (contact form will work!)

**Pros:** Free, drag-drop deployment, forms backend, custom domains  
**Cons:** Bandwidth limits on free tier

**Contact form integration:**
Add to `pages/contact.html` form tag:
```html
<form name="contact" method="POST" data-netlify="true">
```

---

### Option 3: Vercel

**Best for:** Fast deployment, great performance, preview URLs

**Steps:**

1. **Sign up:** https://vercel.com (free account)

2. **Import project:**
   - Click "Add New" → "Project"
   - Import from GitHub
   - Or drag & drop folder

3. **Deploy:**
   - Framework: Other
   - Build command: None
   - Output directory: ./ (root)
   - Click Deploy

4. **Live in 30 seconds:**
   - `your-project.vercel.app`

**Pros:** Free, excellent performance, custom domains  
**Cons:** Need account

---

### Option 4: Traditional Web Hosting

**Best for:** Existing hosting plan, full control

**Via FTP/SFTP:**

1. **Connect to server:**
   - Use FileZilla, Cyberduck, or WinSCP
   - Enter host, username, password

2. **Upload files:**
   - Upload `index.html` to root (or public_html/)
   - Upload `pages/` folder
   - Upload `assets/` folder

3. **Set permissions:**
   - Files: 644
   - Folders: 755

4. **Visit your domain:**
   - `https://yourdomain.com`

**Via cPanel:**
1. Login to cPanel
2. Open File Manager
3. Navigate to public_html
4. Upload all files/folders
5. Extract if uploaded as ZIP

---

### Option 5: AWS S3 + CloudFront

**Best for:** Scalability, CDN, professional setup

**Steps:**

1. **Create S3 bucket:**
   - Name: your-website-name
   - Region: Closest to users
   - Disable "Block all public access"

2. **Upload files:**
   - Upload all HTML, CSS, images
   - Set public read permissions

3. **Enable static website hosting:**
   - Properties → Static website hosting
   - Index document: `index.html`
   - Error document: `index.html`

4. **Configure CloudFront** (optional):
   - Create distribution
   - Origin: S3 bucket
   - Enable HTTPS

5. **Custom domain:**
   - Route 53 or your DNS provider
   - Point to S3 or CloudFront

**Pros:** Enterprise-grade, scalable, CDN included  
**Cons:** More complex, costs apply

---

## 🔧 Post-Deployment Tasks

### 1. Verify Deployment
- [ ] Visit live URL
- [ ] Test all 5 pages
- [ ] Check all navigation links
- [ ] Test on mobile device
- [ ] Verify images load
- [ ] Test contact form (if backend enabled)

### 2. Performance Check
- [ ] Run PageSpeed Insights: https://pagespeed.web.dev/
- [ ] Target: 90+ desktop, 85+ mobile
- [ ] Fix any issues found

### 3. SEO Setup

#### Google Search Console
1. Visit https://search.google.com/search-console
2. Add property (your domain)
3. Verify ownership
4. Submit sitemap (create if needed)

#### Create Sitemap (Optional)
Create `sitemap.xml`:
```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
  <url>
    <loc>https://yourdomain.com/</loc>
    <priority>1.0</priority>
  </url>
  <url>
    <loc>https://yourdomain.com/pages/about.html</loc>
    <priority>0.8</priority>
  </url>
  <url>
    <loc>https://yourdomain.com/pages/services.html</loc>
    <priority>0.8</priority>
  </url>
  <url>
    <loc>https://yourdomain.com/pages/gallery.html</loc>
    <priority>0.8</priority>
  </url>
  <url>
    <loc>https://yourdomain.com/pages/contact.html</loc>
    <priority>0.8</priority>
  </url>
</urlset>
```

#### Create robots.txt
Create `robots.txt` in root:
```
User-agent: *
Allow: /
Sitemap: https://yourdomain.com/sitemap.xml
```

### 4. Analytics Setup (Optional)

#### Google Analytics 4
1. Create GA4 property
2. Get tracking ID (G-XXXXXXXXXX)
3. Add to all pages before `</head>`:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>
```

### 5. Monitor & Maintain
- [ ] Check website weekly
- [ ] Monitor contact form submissions
- [ ] Review analytics monthly
- [ ] Update content as needed
- [ ] Check for broken links quarterly

---

## 🔄 Update Process

### When you need to make changes:

1. **Edit local files**
2. **Test locally** (open in browser)
3. **Re-upload changed files** via:
   - Git push (if using GitHub/Netlify/Vercel)
   - FTP upload (if using traditional hosting)
   - S3 sync (if using AWS)

### Version Control (Recommended)
```bash
# Make changes to files
git add .
git commit -m "Update: describe changes"
git push origin main
```

If using Netlify/Vercel with Git, site auto-deploys!

---

## ⚡ Performance Optimization Checklist

### Before Going Live:
- [ ] Compress all images (see IMAGE_OPTIMIZATION_GUIDE.md)
- [ ] Minify CSS (already done)
- [ ] Enable gzip compression (server config)
- [ ] Enable browser caching (server config)
- [ ] Use CDN for assets (optional)

### Server Configuration (if applicable)

#### Enable Gzip (.htaccess for Apache)
```apache
<IfModule mod_deflate.c>
  AddOutputFilterByType DEFLATE text/html text/plain text/xml text/css text/javascript application/javascript
</IfModule>
```

#### Browser Caching (.htaccess)
```apache
<IfModule mod_expires.c>
  ExpiresActive On
  ExpiresByType image/jpg "access 1 year"
  ExpiresByType image/jpeg "access 1 year"
  ExpiresByType image/gif "access 1 year"
  ExpiresByType image/png "access 1 year"
  ExpiresByType text/css "access 1 month"
  ExpiresByType application/javascript "access 1 month"
</IfModule>
```

---

## 🐛 Troubleshooting

### Images not loading
- Check file paths are correct (case-sensitive on Linux)
- Verify images uploaded to correct folder
- Check file permissions (644)

### Navigation not working
- Verify all HTML files in correct folders
- Check relative paths in links
- Test on actual server, not just locally

### Form not submitting
- If using Netlify, add `data-netlify="true"` to form
- Otherwise, implement backend (PHP, Node.js, etc.)
- Or use FormSpree, Formsubmit.co

### Performance issues
- Compress images (most common issue)
- Enable CDN
- Use browser caching
- Minimize redirects

---

## 📊 Success Metrics

### After 1 Week:
- [ ] Website indexed by Google
- [ ] PageSpeed score 85+
- [ ] No broken links
- [ ] Contact form working
- [ ] Mobile responsive on all devices

### After 1 Month:
- [ ] Organic search traffic
- [ ] Form submissions received
- [ ] Analytics data collected
- [ ] User feedback gathered

---

## 📞 Support Resources

### Documentation:
- RENOVATION_COMPLETE.md - Project overview
- TESTING_CHECKLIST.md - Testing guide
- IMAGE_OPTIMIZATION_GUIDE.md - Image compression

### Online Resources:
- PageSpeed Insights: https://pagespeed.web.dev/
- TinyPNG: https://tinypng.com/
- Google Search Console: https://search.google.com/search-console
- Netlify Docs: https://docs.netlify.com/
- GitHub Pages: https://pages.github.com/

---

## ✅ Final Deployment Checklist

**Before going live:**
- [ ] Images optimized (compressed)
- [ ] All links tested
- [ ] Social media URLs updated
- [ ] Contact form tested
- [ ] Mobile responsive verified
- [ ] Cross-browser tested
- [ ] SEO meta tags verified
- [ ] Analytics installed (optional)
- [ ] Backup files created
- [ ] DNS configured (if custom domain)

**After deployment:**
- [ ] Verify live site loads
- [ ] Test all pages live
- [ ] Run PageSpeed test
- [ ] Submit to Google Search Console
- [ ] Monitor for 24 hours
- [ ] Celebrate! 🎉

---

**Deployment Date:** _____________  
**Deployed By:** _____________  
**Live URL:** _____________  
**Status:** ⏳ Pending / ✅ Live  

**Notes:**
