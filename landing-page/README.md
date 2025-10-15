# Deep Study AI Landing Page

Simple, modern landing page for deepstudyai.com showcasing the Empathy Framework.

## Files

```
landing-page/
├── index.html          # Main landing page
├── styles.css          # All styling
└── README.md           # This file
```

## Features

- **Modern Design**: Dark theme with gradient accents
- **Fully Responsive**: Works on mobile, tablet, and desktop
- **No Dependencies**: Pure HTML and CSS (no JavaScript required)
- **Fast Loading**: No external frameworks, minimal CSS
- **SEO Optimized**: Proper meta tags and semantic HTML

## Local Testing

Open `index.html` in your browser:

```bash
# macOS
open index.html

# Linux
xdg-open index.html

# Windows
start index.html
```

Or use a simple HTTP server:

```bash
# Python 3
python3 -m http.server 8000

# Node.js (if you have http-server installed)
npx http-server

# Then open: http://localhost:8000
```

## Deployment Options

### Option 1: GitHub Pages (Free, Easiest)

1. Create a new repository called `deepstudyai.com`
2. Push these files to the repository
3. Go to Settings → Pages
4. Select "Deploy from branch" → main branch → root
5. Add custom domain: `deepstudyai.com`
6. Configure DNS:
   - Add A records pointing to GitHub Pages IPs
   - Add CNAME record: `www` → `Deep-Study-AI.github.io`

### Option 2: Vercel (Free, Fast)

```bash
# Install Vercel CLI
npm i -g vercel

# Deploy
cd landing-page
vercel

# Add custom domain in Vercel dashboard
```

### Option 3: Netlify (Free, Easy)

1. Drag and drop the `landing-page` folder to netlify.com/drop
2. Or connect GitHub repository
3. Add custom domain in Netlify settings
4. Configure DNS:
   - Add CNAME: `www` → your-site.netlify.app
   - Add ALIAS/ANAME: `@` → apex-loadbalancer.netlify.com

### Option 4: Cloudflare Pages (Free, CDN)

1. Connect GitHub repository to Cloudflare Pages
2. Build settings: None (static HTML)
3. Output directory: `/landing-page`
4. Add custom domain in Cloudflare dashboard

### Option 5: AWS S3 + CloudFront (Scalable)

```bash
# Upload to S3
aws s3 sync . s3://deepstudyai.com --exclude "*.md"

# Configure S3 bucket for static hosting
# Set up CloudFront distribution
# Point Route 53 to CloudFront
```

## DNS Configuration

Once you choose a hosting provider, configure your DNS:

### For deepstudyai.com domain:

**A Records (GitHub Pages):**
```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

**CNAME Record:**
```
www → [your-host].github.io (or netlify.app, vercel.app, etc.)
```

## Customization

### Colors

Edit CSS variables in `styles.css`:

```css
:root {
    --primary: #6366f1;      /* Main brand color */
    --primary-dark: #4f46e5; /* Hover states */
    --secondary: #8b5cf6;    /* Accent color */
    --accent: #ec4899;       /* Additional accent */
}
```

### Content

Edit `index.html` sections:
- **Hero**: Main headline and value proposition
- **Features**: 16 wizard cards
- **Pricing**: Tier details and prices
- **Footer**: Links and contact info

### Images/Logos

To add a logo, replace the emoji in:

```html
<div class="logo-icon">🧠</div>
```

With:

```html
<img src="logo.png" alt="Deep Study AI" width="32" height="32">
```

## Performance

Current performance:
- **Load Time**: < 1 second
- **Page Size**: ~50KB (HTML + CSS)
- **No JavaScript**: Pure HTML/CSS
- **Lighthouse Score**: 95+ expected

## Browser Support

- ✅ Chrome/Edge (latest)
- ✅ Firefox (latest)
- ✅ Safari (latest)
- ✅ Mobile browsers (iOS Safari, Chrome Mobile)

## SEO

The page includes:
- ✅ Meta description
- ✅ Keywords
- ✅ Semantic HTML (h1, h2, nav, section, footer)
- ✅ Alt text for icons
- ✅ Proper heading hierarchy
- ✅ Mobile responsive

To improve SEO further:
1. Add `robots.txt`
2. Add `sitemap.xml`
3. Set up Google Analytics
4. Add Open Graph tags for social sharing
5. Add structured data (JSON-LD)

## Next Steps

1. **Choose hosting provider** (recommend: GitHub Pages or Vercel)
2. **Deploy landing page**
3. **Configure custom domain** (deepstudyai.com)
4. **Test on mobile devices**
5. **Set up analytics** (Google Analytics, Plausible, or Fathom)
6. **Add email capture** (when ready for launch)
7. **Create blog** (optional, for SEO and content marketing)

## Email Capture (Future)

When ready to capture emails, add a form service:

**Option A: Mailchimp**
```html
<form action="https://yoursite.us1.list-manage.com/subscribe/post" method="POST">
    <input type="email" name="EMAIL" placeholder="Enter your email">
    <button type="submit">Get Early Access</button>
</form>
```

**Option B: ConvertKit**
**Option C: Custom (with backend)**

## License

This landing page is part of the Deep Study AI marketing materials.

## Contact

For questions about deployment:
- Email: patrick.roebuck@deepstudyai.com
- GitHub: https://github.com/Deep-Study-AI

---

Built with ❤️ by Deep Study AI, LLC
