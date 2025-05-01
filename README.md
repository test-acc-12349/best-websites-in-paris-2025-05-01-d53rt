# Landing Page Maintenance Guide

This guide will help you maintain and customize your landing page. Follow these detailed instructions to make updates while preserving the design and functionality.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains your main navigation and logo. To update:

1. Change the logo text:
```html
<!-- Find this line in the header section -->
<a href="/" class="text-2xl font-bold text-gray-900">Paris Web</a>
```
Simply replace "Paris Web" with your desired text.

### Hero Section
The hero section is your main banner area. To modify:

1. Update the main heading:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
    Best Websites In Paris
</h1>
```
Replace "Best Websites In Paris" with your heading.

2. Update the subheading:
```html
<p class="text-xl md:text-2xl text-gray-600 mb-10">
    Custom Websites For Your Business
</p>
```

### Understanding Tailwind Classes
Common classes used in this template:

- Text sizes: `text-xl`, `text-2xl`, `text-3xl`, etc.
- Colors: `text-gray-900`, `bg-blue-600`, etc.
- Spacing: `px-4`, `py-24`, `mb-6`, etc.
- Responsive prefixes: `md:`, `lg:` (for different screen sizes)

Example of modifying a button's appearance:
```html
<!-- Original button -->
<a href="https://sigmaseo.io" class="inline-flex items-center px-8 py-4 border border-transparent text-lg font-semibold rounded-md text-white bg-blue-600 hover:bg-blue-700">

<!-- To change color to green -->
<a href="https://sigmaseo.io" class="inline-flex items-center px-8 py-4 border border-transparent text-lg font-semibold rounded-md text-white bg-green-600 hover:bg-green-700">
```

## Fixing Broken Links

### Navigation Menu Links
Current internal links in the navigation:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update:
1. For internal sections, keep the `#` prefix
2. For external links, use the full URL
3. Ensure the href matches the section's ID

Example updating the Features link:
```html
<!-- Original -->
<a href="#features">Features</a>

<!-- Updated to external link -->
<a href="https://yoursite.com/features">Features</a>
```

### Call-to-Action Links
Update all instances of the placeholder URL:
```html
<!-- Find all instances of -->
<a href="https://sigmaseo.io">

<!-- Replace with your actual URL -->
<a href="https://your-actual-website.com">
```

## Linking Privacy and Terms Pages

### Footer Link Updates
Located in the footer section:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To update:
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Ensure section IDs match the href attributes
   - Check for typos in the href values
   - Verify that all referenced sections exist

2. **Responsive Design Issues**
   - Keep the responsive prefixes (`md:`, `lg:`) when updating classes
   - Test on multiple screen sizes after making changes
   - Don't remove container classes that maintain layout

3. **Style Inconsistencies**
   - Maintain color schemes using Tailwind's color classes
   - Keep consistent spacing using Tailwind's spacing utilities
   - Match font sizes with existing patterns

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Verify all links work using your browser's developer tools
- Test your page on multiple devices and browsers
- Keep a backup of the original code before making changes

Remember to always test your changes thoroughly before deploying to a live site.