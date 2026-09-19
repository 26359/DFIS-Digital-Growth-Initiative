# DFIS Website — Deployment & Operations Guide

## Project Structure

```
website/
├── index.html              # Homepage
├── coverage-compass.html   # Coverage Compass™ interactive tool
├── resources.html          # Resources & Learning Center
├── about.html              # About DFIS
├── contact.html            # Contact page with forms
├── css/
│   └── styles.css          # Complete design system
├── js/
│   ├── main.js             # Navigation, utilities, form helpers
│   ├── coverage-compass.js # Multi-step assessment engine
│   ├── ai-qa.js            # Rule-based AI educational assistant
│   └── lead-capture.js     # Form validation & lead submission
├── assets/
│   ├── images/             # Image assets (add as needed)
│   └── fonts/              # Custom fonts (if needed)
├── sitemap.xml             # SEO sitemap
└── robots.txt              # Search engine directives
```

## Deployment Options

### Option 1: Static Hosting (Free)
- **Netlify**: Drag and drop the `website/` folder to netlify.com
- **Vercel**: Import the project at vercel.com
- **GitHub Pages**: Push to a GitHub repo and enable Pages
- **Cloudflare Pages**: Free global CDN with SSL

### Option 2: WordPress Integration
1. Copy HTML files into your WordPress theme
2. Use the CSS from `css/styles.css` in your theme's stylesheet
3. Include the JavaScript files in your theme's footer
4. Replace static navigation with WordPress `wp_nav_menu()`
5. Replace hardcoded content with WordPress dynamic content where needed

### Option 3: Custom Server
1. Upload all files to your web server via FTP/SFTP
2. Ensure HTTPS/SSL is configured
3. Verify all file paths are correct
4. Test all functionality

## Coverage Compass™ Data Flow

1. User completes assessment (Step 1)
2. JavaScript generates personalized checklist (Step 2)
3. User interacts with AI Q&A (Step 3) — questions are tracked
4. User submits lead form (Step 4)
5. All data is bundled and submitted to your CRM/email

### Integration Points
- **CRM**: Update `submitLead()` in `js/lead-capture.js` to POST to your CRM API
- **Email**: Update `submitLead()` to trigger an email notification
- **Chatbot**: The AI Q&A component is rule-based and uses DFIS-approved content blocks in `js/ai-qa.js`

## Content Updates

### Updating AI Q&A Content
Edit `js/ai-qa.js`. The `knowledgeBase` object contains all approved content organized by category (auto, home, life, business, general). Add or modify responses as needed.

### Updating Coverage Checklist Items
Edit `generateChecklist()` in `js/coverage-compass.js`. The function dynamically generates checklist sections based on assessment answers.

### Updating Educational Articles
Edit `resources.html` directly or integrate with a CMS.

## Security Notes
- All forms include client-side validation
- Honeypot spam protection is automatically added
- CSRF token generation is included
- Rate limiting is implemented client-side
- All data transmission should use HTTPS in production
- In production, replace localStorage submissions with server-side API calls

## Compliance Reminders
- No automated quotes or binding coverage
- All AI responses use DFIS-approved content only
- Required disclosures are displayed on the AI Q&A component
- Privacy policy and terms of service links must be updated with real URLs
- Insurance licensing disclosures must be added per state requirements

## Performance Targets
- Page load: Under 3 seconds on 4G
- First Contentful Paint: Under 1.5 seconds
- Largest Contentful Paint: Under 2.5 seconds
- All images should be optimized (WebP, lazy loaded)

## Browser Support
- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+
- Mobile Safari (iOS 14+)
- Chrome for Android (latest)

---
*DFIS Digital Growth Initiative — Coverage Compass™*
*Last updated: September 18, 2026*
