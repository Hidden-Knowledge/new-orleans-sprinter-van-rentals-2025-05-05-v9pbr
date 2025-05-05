# New Orleans Sprinter Van Rentals Directory Website

A modern directory website showcasing 50+ luxury sprinter vans available for rent in New Orleans with instant booking capabilities.

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Getting Started](#getting-started)
- [Directory Structure](#directory-structure)
- [Customization Guide](#customization-guide)
- [Deployment](#deployment)
- [Custom Domain Setup](#custom-domain-setup)
- [Troubleshooting](#troubleshooting)
- [Support & Resources](#support--resources)

## Overview

New Orleans Sprinter Van Rentals is a responsive directory website featuring a clean, 3-column grid layout showcasing luxury van rentals. The site enables users to browse, compare, and instantly book vehicles.

## Features

- Responsive 3-column grid layout
- Advanced filtering system
- Instant booking integration
- High-resolution image gallery
- Search functionality
- Category-based navigation
- Mobile-optimized interface
- Contact form integration
- SEO-optimized structure

## Getting Started

### Prerequisites
- Node.js (v14 or higher)
- npm or yarn
- Git

### Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/nola-van-rentals.git

# Navigate to project directory
cd nola-van-rentals

# Install dependencies
npm install

# Start development server
npm run dev
```

## Directory Structure

```
nola-van-rentals/
├── src/
│   ├── components/
│   │   ├── Directory/
│   │   ├── Hero/
│   │   └── Navigation/
│   ├── data/
│   │   └── listings.json
│   └── styles/
├── public/
│   └── images/
├── config/
└── package.json
```

## Customization Guide

### Adding/Editing Directory Items

1. Navigate to `src/data/listings.json`
2. Add new listing using the following format:

```json
{
  "id": "van-001",
  "title": "2023 Mercedes Sprinter Luxury",
  "category": "luxury",
  "capacity": "12",
  "price": "299",
  "image": "sprinter-001.jpg",
  "features": ["WiFi", "TV", "Kitchen"]
}
```

### Modifying Category Labels

Edit the categories in `src/config/categories.js`:

```javascript
export const categories = [
  {
    id: "luxury",
    label: "Luxury Vans",
    icon: "luxury-icon.svg"
  },
  // Add more categories
];
```

### Updating Hero Section

1. Open `src/components/Hero/Hero.js`
2. Modify content within the component:

```javascript
<HeroSection>
  <HeroTitle>Find Your Perfect Sprinter Van</HeroTitle>
  <HeroSubtitle>50+ Luxury Vans Available</HeroSubtitle>
</HeroSection>
```

### Customizing Colors

1. Navigate to `src/styles/variables.css`
2. Update color variables:

```css
:root {
  --primary-color: #2A4365;
  --secondary-color: #4A5568;
  --accent-color: #F6AD55;
}
```

## Deployment

### Build for Production

```bash
# Create production build
npm run build

# Test production build locally
npm run serve
```

### Deploy to Hosting Platform

```bash
# Deploy to Vercel
vercel deploy

# Deploy to Netlify
netlify deploy --prod
```

## Custom Domain Setup

1. Purchase domain from preferred registrar
2. Add DNS records:
   ```
   Type  Name    Value
   A     @       76.76.21.21
   CNAME www     your-site.vercel.app
   ```
3. Configure domain in hosting platform dashboard
4. Wait for DNS propagation (24-48 hours)

## Troubleshooting

### Common Issues

**Images Not Loading**
- Verify image paths in `listings.json`
- Check image formats (supported: .jpg, .png, .webp)
- Ensure images are in `public/images/`

**Filtering Not Working**
- Clear browser cache
- Check category IDs match in listings and categories files
- Verify filter function in `src/utils/filters.js`

## Support & Resources

- [Documentation Wiki](https://github.com/yourusername/nola-van-rentals/wiki)
- [Issue Tracker](https://github.com/yourusername/nola-van-rentals/issues)
- [Contributing Guidelines](CONTRIBUTING.md)

### Community Support
- [Discord Community](https://discord.gg/nolarentals)
- [Stack Overflow Tag](https://stackoverflow.com/questions/tagged/nola-van-rentals)

### Updates & Maintenance

Regular updates are released monthly. To update:

```bash
git pull origin main
npm install
npm run build
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

Made with ❤️ in New Orleans