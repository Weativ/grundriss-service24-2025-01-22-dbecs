# Grundriss-Service24 Landing Page - Maintenance Guide

This guide will help you maintain and customize the Grundriss-Service24 landing page. Whether you're new to HTML and CSS or just getting started, follow these instructions to make updates safely and effectively.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your logo and navigation menu. To update:

1. **Logo Text:**
```html
<a href="#" class="text-2xl font-bold text-blue-600">Grundriss-Service24</a>
```
- Replace "Grundriss-Service24" with your desired text
- The `text-2xl` class controls size
- `text-blue-600` controls the blue color

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">
    Ihr Grundriss, schnell und professionell
</h1>
```
- Update the text between the `<h1>` tags
- The classes control responsive sizing:
  - `text-4xl`: mobile size
  - `md:text-5xl`: tablet size
  - `lg:text-6xl`: desktop size

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white p-8 rounded-xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mb-6">
        <i class="fas fa-star text-blue-600 text-2xl"></i>
    </div>
    <h3 class="text-xl font-semibold mb-4">Professionell</h3>
    <p class="text-gray-600">Hochwertige Grundrisse nach Ihren Anforderungen</p>
</div>
```
To modify:
1. Change the icon by updating the `fa-star` class to any [Font Awesome](https://fontawesome.com/icons) icon
2. Update the heading text in the `<h3>` tag
3. Modify the description in the `<p>` tag

## Managing Links

### Navigation Menu Links
Current navigation structure:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="hover:text-blue-600 transition-colors duration-300">Features</a>
    <a href="#benefits" class="hover:text-blue-600 transition-colors duration-300">Vorteile</a>
    <a href="#faq" class="hover:text-blue-600 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="hover:text-blue-600 transition-colors duration-300">Kontakt</a>
</div>
```
To update:
1. The `href="#features"` links to sections on the same page
2. To link to external pages, replace with full URLs:
```html
<a href="https://yourwebsite.com/page" class="hover:text-blue-600 transition-colors duration-300">
```

### Email Links
Find and update all email links:
```html
<a href="mailto:info@weativ.de">info@weativ.de</a>
```
Replace `info@weativ.de` with your email address in both the `href` and display text.

## Adding Privacy and Terms Pages

### Footer Link Updates
Current footer links:
```html
<ul class="space-y-2">
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Impressum</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Datenschutz</a></li>
</ul>
```

To add privacy and terms pages:
1. Create new HTML files:
   - `privacy.html`
   - `terms.html`
2. Update the links:
```html
<ul class="space-y-2">
    <li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Impressum</a></li>
    <li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Datenschutz</a></li>
</ul>
```

## Troubleshooting

### Common Issues

1. **Broken Links**
   - Check that all `href` attributes point to valid files or URLs
   - Verify file names match exactly (case-sensitive)
   - Test all links after updating

2. **Styling Problems**
   - If styles aren't applying, check the Tailwind CDN link is working:
```html
<script src="https://cdn.tailwindcss.com"></script>
```
   - Ensure classes are spelled correctly
   - Check for missing spaces between multiple classes

3. **Missing Icons**
   - Verify the Font Awesome CDN is loaded:
```html
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
```
   - Confirm icon class names are correct

### Need Help?
If you encounter issues:
1. Check the browser's developer tools (F12) for errors
2. Verify all files are in the correct directory
3. Ensure all HTML tags are properly closed
4. Compare your changes against the original code

Remember to always backup your files before making changes!