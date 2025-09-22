# DynamicsPro.ca - Business Dynamics Pro Website

A modern, responsive website for Business Dynamics Pro Inc., built with Astro framework and deployed on Netlify with integrated forms functionality.

[![Netlify Status](https://api.netlify.com/api/v1/badges/bdb808c6-f85a-4ae5-8b42-b0b02cd3b55b/deploy-status)](https://app.netlify.com/projects/dynamicspro/deploys)

## 🌐 Live Site
- **Production**: https://dynamicspro.ca
- **Repository**: https://github.com/Irajmehr/dynamicspro.ca
- **Admin Panel**: https://app.netlify.com/projects/dynamicspro

## 🚀 Quick Start

```bash
# Install dependencies
npm install

# Start development server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview
```

## 📁 Project Structure

```
src/
├── assets/          # Static assets (images, icons)
├── components/      # Reusable Astro components
│   ├── About.astro
│   ├── CaseStudies.astro
│   ├── Contact.astro      # Main contact form with Netlify integration
│   ├── Header.astro
│   ├── Hero.astro
│   ├── Industries.astro
│   ├── Services.astro
│   └── Welcome.astro
├── layouts/         # Page layouts
│   └── Layout.astro
├── pages/           # Route pages
│   ├── index.astro
│   ├── thank-you.astro    # Form submission thank you page
│   ├── industries/        # Industry-specific pages
│   └── services/          # Service-specific pages
public/              # Static public assets
├── BDP_Logo.svg
└── favicon.svg
netlify.toml         # Netlify configuration
```

## 📧 Contact Form System

### Form Configuration
The consultation form (`src/components/Contact.astro`) is configured with:

- **Form Name**: `consultation`
- **Method**: POST
- **Netlify Integration**: `data-netlify="true"`
- **Spam Protection**: reCAPTCHA enabled
- **Email Recipients**:
  - Primary: `iraj@dynamicspro.ca`
  - CC: `irajmehr@yahoo.com`

### Form Fields
- Company Name (required)
- Contact Person (required)
- Email Address (required)
- Phone Number
- Current ERP System
- Company Size
- Project Type
- Timeline
- Business Challenges & Requirements
- Preferred Consultation Format

### Email Notifications
Configured in `netlify.toml`:
```toml
[[notifications]]
  name = "consultation-form"
  type = "email"
  emails = ["iraj@dynamicspro.ca", "irajmehr@yahoo.com"]
  subject = "New Consultation Request from DynamicsPro.ca"
```

## 🛠️ Development Workflow

### Making Changes

1. **Local Development**
   ```bash
   git pull origin main
   npm run dev
   # Make your changes
   ```

2. **Testing Changes**
   ```bash
   npm run build
   npm run preview
   ```

3. **Committing Changes**
   ```bash
   git add .
   git commit -m "feat: description of changes"
   git push origin main
   ```

4. **Automatic Deployment**
   - Netlify automatically deploys on push to main branch
   - Build logs available at: https://app.netlify.com/projects/dynamicspro/deploys

### Using Netlify CLI

```bash
# Link to existing site (if needed)
netlify link --name dynamicspro

# Deploy to preview
netlify deploy

# Deploy to production
netlify deploy --prod

# Open site in browser
netlify open:site

# Open admin panel
netlify open:admin

# Check site status
netlify status
```

## 🔧 Common Modifications

### Adding New Pages

1. Create new `.astro` file in `src/pages/`
2. Follow existing page structure
3. Add navigation links in `Header.astro` if needed
4. Deploy changes

### Updating Contact Information

Update these files:
- `src/components/Contact.astro` - Contact section
- `src/components/Header.astro` - Header contact info
- `netlify.toml` - Email notification settings

### Modifying Form Fields

1. Edit form in `src/components/Contact.astro`
2. Update validation logic if needed
3. Test thoroughly before deploying

### Adding New Services/Industries

1. Create new page in respective folder
2. Add to navigation menu
3. Update relevant sections in main components

## 🎨 Styling System

- **Framework**: Tailwind CSS
- **Configuration**: `tailwind.config.mjs`
- **Color Scheme**:
  - Primary: Blue variants
  - Accent: Purple/indigo variants
  - Success: Green variants

### Custom Color Classes
```css
primary-50 to primary-900
accent-50 to accent-900
success-50 to success-900
```

## 🔍 Troubleshooting

### Form Submissions Not Working

1. **Check Netlify Forms Detection**
   - Forms must have `data-netlify="true"`
   - Forms need `name` attribute
   - Forms must be in deployed HTML (not JS-generated)

2. **Verify Email Settings**
   - Check `netlify.toml` configuration
   - Verify email addresses are correct
   - Check Netlify dashboard for form submissions

3. **Debug Form Issues**
   ```bash
   # Check form status in Netlify dashboard
   netlify open:admin
   # Navigate to Forms section
   ```

### Build Failures

1. **Check Dependencies**
   ```bash
   npm install
   npm audit fix
   ```

2. **Verify Astro Configuration**
   - Check `astro.config.mjs`
   - Ensure all imports are correct

3. **Check Build Logs**
   - View logs in Netlify dashboard
   - Look for specific error messages

### Deployment Issues

1. **Verify Git Status**
   ```bash
   git status
   git log --oneline -5
   ```

2. **Check Netlify Configuration**
   ```bash
   netlify status
   netlify sites:list
   ```

3. **Manual Deployment**
   ```bash
   npm run build
   netlify deploy --prod --dir=dist
   ```

## 📞 Support Contacts

- **Primary**: iraj@dynamicspro.ca
- **Secondary**: irajmehr@yahoo.com
- **Phone**: 416-843-6575

## 🔐 Security Features

- **Headers**: Configured in `netlify.toml`
  - X-Frame-Options: DENY
  - X-XSS-Protection: 1; mode=block
  - X-Content-Type-Options: nosniff
  - Referrer-Policy: strict-origin-when-cross-origin

- **Form Security**:
  - reCAPTCHA protection
  - Netlify spam filtering
  - Input validation

## 📈 Analytics & Monitoring

- Monitor form submissions in Netlify dashboard
- Check deployment status with badge
- Review build logs for issues

## 🚀 Future Enhancements

### Potential Additions
- Blog/News section
- Client testimonials
- Case study details
- Interactive project calculator
- Live chat integration
- Multi-language support

### Technical Improvements
- Add analytics (Google Analytics/Plausible)
- Implement SEO optimizations
- Add progressive web app features
- Set up automated testing
- Configure staging environment

---

## 📝 Change Log

### 2025-01-22 - Initial Release
- ✅ Complete website design and development
- ✅ GitHub repository setup
- ✅ Netlify deployment configuration
- ✅ Contact form integration with email notifications
- ✅ reCAPTCHA spam protection
- ✅ Mobile-responsive design
- ✅ Professional consultation form

### 2025-01-22 - Form System Enhancement
- ✅ Netlify Forms integration
- ✅ Email routing to multiple recipients
- ✅ Thank-you page creation
- ✅ Comprehensive form validation

---

*Last Updated: January 22, 2025*
