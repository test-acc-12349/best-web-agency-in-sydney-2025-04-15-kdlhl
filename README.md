# Landing Page Maintenance Guide

This guide will help you maintain and customize the WebAgency landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your company name and navigation menu. To update:

1. **Company Name:**
```html
<a href="/" class="text-2xl font-bold text-white hover:text-blue-400 transition-colors duration-300">
    WebAgency <!-- Change this text -->
</a>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-300 hover:text-white transition-colors duration-300">Features</a>
    <!-- Repeat for each menu item -->
</div>
```

### Hero Section
Update your main headline and subheading:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-blue-400 to-purple-400 bg-clip-text text-transparent">
    Best Web Agency In Sydney <!-- Change headline here -->
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">
    Grow your business with clicks <!-- Change subheading here -->
</p>
```

### Tailwind CSS Class Guide
Common classes used throughout:
- Text sizes: `text-sm`, `text-base`, `text-lg`, `text-xl`, `text-2xl`, etc.
- Colors: `text-gray-300`, `bg-blue-600`, `from-blue-400`
- Spacing: `px-6` (padding left/right), `py-4` (padding top/bottom), `mb-8` (margin bottom)
- Responsive: `md:text-2xl` (applies at medium screens and up)

Example of modifying a button:
```html
<!-- Original -->
<a href="#" class="inline-flex items-center px-8 py-4 bg-blue-600">

<!-- Modified for green color -->
<a href="#" class="inline-flex items-center px-8 py-4 bg-green-600">
```

## Managing Links

### Navigation Links
All internal section links start with #:
```html
<!-- Current internal links -->
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>

<!-- External link example -->
<a href="https://fixrr.online">Get Started</a>
```

To update:
1. Find the link in the HTML
2. Change the `href` attribute
3. Update the displayed text between the `<a>` tags

### Call-to-Action Buttons
Located in hero and CTA sections:
```html
<!-- Update this URL for all CTA buttons -->
<a href="https://fixrr.online" class="inline-flex items-center...">
```

## Adding Privacy and Terms Pages

### Footer Link Updates
Locate the Legal section in the footer:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To link to new pages:
1. Create `privacy.html` and `terms.html` in your project folder
2. Update the links:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Ensure section IDs match the href attributes
   - Check for typos in the href values
   - Verify that section IDs are unique

2. **Responsive Design Problems**
   - Check mobile view using browser dev tools
   - Verify media query classes (md:, lg:) are correct
   - Test different screen sizes

3. **Style Changes Not Working**
   - Confirm Tailwind CDN is loading
   - Check for typos in class names
   - Verify class order (Tailwind uses last-applied rule)

### Need Help?
- Validate HTML at [W3C Validator](https://validator.w3.org/)
- Test responsiveness using Chrome DevTools
- Check Tailwind documentation for class references

Remember to always test changes in multiple browsers and screen sizes before deploying to production.