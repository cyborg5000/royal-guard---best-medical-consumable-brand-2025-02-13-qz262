# Royal Guard Landing Page - Maintenance Guide

This guide will help you maintain and customize the Royal Guard landing page. It's written for beginners and provides step-by-step instructions for common updates.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. Company Name:
```html
<div class="text-2xl font-bold text-blue-600">Royal Guard</div>
```
- Replace "Royal Guard" with your company name
- Adjust text size by changing `text-2xl` to `text-xl` (smaller) or `text-3xl` (larger)

### Hero Section
Located at the top of the page with the main headline:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">
    Royal Guard - Best Medical Consumable Brand
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-8">
    Unique PU Gloves for Ultimate Protection
</p>
```
- Update the heading and subheading text as needed
- The `md:` and `lg:` prefixes control text size on different screen sizes

### Features Section
Each feature card follows this structure:
```html
<div class="p-8 bg-white rounded-2xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <h3 class="text-xl font-semibold mb-4">Best Quality</h3>
    <p class="text-gray-600">Premium materials and rigorous quality control...</p>
</div>
```
- Update the heading and description text
- Keep the existing classes to maintain styling
- Don't remove the `hover:` classes as they create interactive effects

## Managing Links

### Navigation Menu Links
The navigation menu contains internal page links:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Benefits</a>
    <!-- ... -->
</div>
```
To update:
1. The `href="#features"` links to page sections
2. Ensure section IDs match these links (e.g., `id="features"`)
3. To link to external pages, replace with full URLs: `href="https://example.com"`

### Call-to-Action Links
Several buttons link to "pm.sg":
```html
<a href="https://pm.sg" class="inline-block px-8 py-4 bg-blue-600 text-white text-lg rounded-full hover:bg-blue-700">
    Explore Our Products
</a>
```
To update:
1. Replace `https://pm.sg` with your desired URL
2. Keep all styling classes to maintain button appearance
3. Update button text between the `<a>` tags

## Adding Privacy and Terms Pages

### Footer Links
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

To add privacy and terms pages:
1. Create two new files: `privacy.html` and `terms.html`
2. Update the links in the footer:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

Common Issues:

1. **Broken Internal Links**
   - Check that section IDs match navigation links exactly
   - Example: `href="#features"` must link to `id="features"`

2. **Responsive Design Issues**
   - Don't remove `md:` or `lg:` prefixes from classes
   - These control how elements appear on different screen sizes

3. **Style Changes Not Working**
   - Ensure Tailwind CSS is properly loaded:
   ```html
   <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
   ```
   - Check that you haven't removed important utility classes

4. **Button Styling Lost**
   - Always keep these classes together for buttons:
   ```html
   inline-block px-8 py-4 bg-blue-600 text-white rounded-full hover:bg-blue-700
   ```

Remember:
- Always test changes across different screen sizes
- Keep a backup of the original code
- Maintain consistent spacing and indentation
- Test all links after making changes

Need more help? Contact your web development team or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).