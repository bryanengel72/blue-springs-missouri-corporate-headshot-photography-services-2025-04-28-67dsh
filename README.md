# Landing Page Maintenance Guide
## For 101Headshots Corporate Photography Website

This guide provides detailed instructions for maintaining and customizing the 101Headshots landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Main Sections Overview
The landing page consists of these key sections:
- Header (Navigation)
- Hero Section
- Services Section
- Benefits Section
- Contact Section
- Footer

### Updating Text Content

#### Header/Navigation
```html
<!-- Located at the top of the page -->
<a href="/" class="text-2xl font-bold">101Headshots</a>
```
To update the company name, modify the text between the `<a>` tags.

#### Hero Section
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8">
    Blue Springs, Missouri Corporate Headshot Photography Services
</h1>
```
To update the main headline, replace the text while keeping the classes intact.

### Modifying Tailwind CSS Classes

#### Understanding Responsive Classes
The site uses these breakpoints:
- `md:` - Medium screens (768px and up)
- `lg:` - Large screens (1024px and up)

Example:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl">
```
This means:
- Mobile: text-4xl (2.25rem)
- Tablet: text-5xl (3rem)
- Desktop: text-6xl (3.75rem)

#### Common Class Modifications

1. **Changing Colors**
```html
<!-- Current gradient background -->
<div class="bg-gradient-to-r from-blue-500 to-indigo-600">
```
To change colors, replace `blue-500` and `indigo-600` with other color values (e.g., `purple-500`).

2. **Adjusting Spacing**
```html
<!-- Current padding -->
<div class="p-8">
```
Padding scale:
- p-2 (0.5rem)
- p-4 (1rem)
- p-8 (2rem)

## Fixing Broken Links

### Current Link Inventory
```html
<!-- Navigation Links -->
<a href="#services">Services</a>
<a href="#benefits">Benefits</a>
<a href="#contact">Contact</a>

<!-- Main CTA Link -->
<a href="https://www.101headshots.com">Book Your Session</a>

<!-- Email Link -->
<a href="mailto:bryan@101headshots.com">bryan@101headshots.com</a>
```

### Updating Links

1. **Internal Links**
To update section links:
```html
<!-- Original -->
<a href="#services">Services</a>

<!-- Update to new section -->
<a href="#new-section-id">New Section Name</a>
```

2. **External Links**
To update the booking link:
```html
<!-- Original -->
<a href="https://www.101headshots.com">Book Your Session</a>

<!-- Update to new URL -->
<a href="https://your-new-url.com">Book Your Session</a>
```

## Linking Privacy and Terms Pages

### Current Footer Links
```html
<!-- Located in footer section -->
<div>
    <h3 class="text-xl font-bold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white">Terms of Service</a></li>
    </ul>
</div>
```

### Adding Policy Pages

1. Create new HTML files:
   - `privacy.html`
   - `terms.html`

2. Update the footer links:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Responsive Layout**
If the responsive layout breaks:
- Check for missing `md:` or `lg:` prefixes
- Verify container classes are present: `container mx-auto px-6`

2. **Gradient Text Not Showing**
If gradient text disappears:
```html
<!-- Required classes for gradient text -->
class="bg-gradient-to-r from-blue-400 to-indigo-500 bg-clip-text text-transparent"
```

3. **Navigation Links Not Working**
For section links (#services, #benefits, etc.):
- Verify section IDs match exactly
- Ensure scroll-smooth class is on html tag
```html
<html lang="en" class="scroll-smooth">
```

### Need Help?
If you encounter issues:
1. Check the Tailwind CSS documentation
2. Verify all classes are spelled correctly
3. Ensure proper nesting of HTML elements
4. Test responsive layouts using browser dev tools

Remember to always test changes across different screen sizes before deploying to production.