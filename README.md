# Nachtbril Fiets Landing Page - Maintenance Guide

This guide will help you maintain and customize the Nachtbril Fiets landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common maintenance tasks.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo. To update:

1. **Logo Text:**
```html
<a href="/" class="text-2xl font-bold text-blue-600">Nachtbril Fiets</a>
```
- Replace "Nachtbril Fiets" with your desired text
- The `text-2xl` class controls size
- `text-blue-600` controls the blue color

2. **Navigation Menu Items:**
```html
<a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Kenmerken</a>
```
- Replace "Kenmerken" with your desired text
- Keep the `hover:text-blue-600` class for the hover effect
- Maintain the `transition-colors duration-300` for smooth transitions

### Hero Section
Located at the top of the page:
```html
<h1 class="text-5xl md:text-6xl font-bold text-gray-900 mb-6">Nachtbril Fiets</h1>
<p class="text-2xl md:text-3xl text-gray-600 mb-8">Nu met 10% Korting - Veilig en Comfortabel Fietsen in het Donker</p>
```
- `text-5xl` and `md:text-6xl` control text size on mobile and desktop
- `mb-6` and `mb-8` control bottom margin spacing

### Tailwind CSS Class Guide
Common classes used throughout:
- Text sizes: `text-sm`, `text-lg`, `text-xl`, `text-2xl`
- Colors: `text-gray-600`, `text-blue-600`, `text-white`
- Spacing: `px-6` (horizontal padding), `py-4` (vertical padding)
- Margins: `mb-4` (margin bottom), `mt-2` (margin top)

## Managing Links

### Navigation Links
Current links in the navigation:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Kenmerken</a>
    <a href="#benefits">Voordelen</a>
    <a href="#faq">FAQ</a>
    <a href="https://nachtbril.com/shop">Koop Nu</a>
</div>
```

To update:
1. Internal links (starting with #):
   - Match the `href` with the `id` of the target section
   - Example: `href="#features"` links to `<section id="features">`

2. External links:
   - Replace `https://nachtbril.com/shop` with your shop URL
   - Always include `https://` for external links

### Call-to-Action Buttons
```html
<a href="https://nachtbril.com/shop" class="inline-block bg-blue-600 text-white px-8 py-4 rounded-full">
    Profiteer Nu van 10% Korting
</a>
```
- Update the `href` attribute with your shop URL
- Maintain the classes for consistent styling

## Adding Privacy and Terms Pages

### Footer Links
Current footer structure:
```html
<ul class="space-y-2">
    <li><a href="#" class="hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="hover:text-blue-400 transition-colors duration-300">Algemene Voorwaarden</a></li>
</ul>
```

To add privacy and terms pages:
1. Create new HTML files:
   - `privacy.html`
   - `terms.html`

2. Update the footer links:
```html
<li><a href="privacy.html" class="hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-blue-400 transition-colors duration-300">Algemene Voorwaarden</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links:**
   - Ensure section IDs match exactly with href attributes
   - Check for typos in IDs
   ```html
   <!-- Link -->
   <a href="#features">
   <!-- Must match exactly -->
   <section id="features">
   ```

2. **Responsive Design Issues:**
   - Check mobile-specific classes (start with `md:` or `sm:`)
   - Test on different screen sizes
   - Example of responsive text:
   ```html
   <h1 class="text-5xl md:text-6xl">
   <!-- text-5xl for mobile, md:text-6xl for desktop -->
   ```

3. **Styling Problems:**
   - Verify Tailwind CSS is properly loaded
   - Check for missing classes
   - Ensure proper nesting of elements

### Need Help?
If you encounter issues:
1. Check the browser console for errors
2. Verify all files are in the correct directory
3. Ensure all links use the correct relative or absolute paths
4. Test the page in multiple browsers

Remember to always backup your files before making changes, and test thoroughly after each modification.