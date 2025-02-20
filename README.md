# Landing Page Maintenance Guide
A comprehensive guide for maintaining and customizing the DiferenciasEntre landing page.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Legal Pages](#adding-legal-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Main Sections Overview
The landing page consists of these key sections:
1. Header/Navigation (fixed at top)
2. Hero Section (main banner)
3. Features Section
4. Benefits Section
5. FAQ Section
6. Call-to-Action Section
7. Footer

### Updating Text Content

#### Hero Section
Located near the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
    Diferencias Entre Conceptos y Términos Explicadas de Forma Clara
</h1>
```
To modify:
1. Locate this `<h1>` tag
2. Replace the text between the tags
3. Keep the existing classes to maintain styling

#### Features Cards
Each feature card follows this structure:
```html
<div class="bg-white rounded-xl p-8 shadow-lg hover:shadow-xl transition-shadow duration-300">
    <h3 class="text-xl font-semibold mb-4">Comparaciones Claras</h3>
    <p class="text-gray-600 leading-relaxed">Explicaciones detalladas...</p>
</div>
```
To modify:
1. Find the feature cards in the "características" section
2. Update the `<h3>` title text
3. Update the `<p>` description text
4. Maintain all existing classes

### Understanding Tailwind Classes

#### Common Class Patterns
- Text Sizes: `text-xl`, `text-2xl`, etc.
- Colors: `text-gray-600`, `bg-blue-600`
- Spacing: `p-8` (padding), `mb-4` (margin bottom)
- Responsive: `md:text-4xl` (applies at medium screens)

Example of modifying text size:
```html
<!-- Original -->
<h3 class="text-xl font-semibold mb-4">

<!-- Making text larger -->
<h3 class="text-2xl font-semibold mb-4">
```

## Managing Links

### Navigation Menu Links
Located in the header:
```html
<div class="hidden md:flex space-x-8">
    <a href="#caracteristicas">Características</a>
    <a href="#beneficios">Beneficios</a>
    <a href="#faq">FAQ</a>
    <a href="#contacto">Contacto</a>
</div>
```
To update:
1. Locate the `<a>` tag you want to modify
2. Change the `href` attribute to your desired destination
3. Update the link text between the tags

### External Links
The main call-to-action buttons link to:
```html
<a href="https://diferenciasentre.net/">
```
To modify:
1. Replace the URL with your desired destination
2. Test the link after updating
3. Consider adding `target="_blank"` for external links

## Adding Legal Pages

### Footer Legal Links
Located at the bottom of the page:
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacidad</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Términos</a></li>
    </ul>
</div>
```

To add privacy and terms pages:
1. Create `privacy.html` and `terms.html` in your project directory
2. Update the links in the footer:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacidad</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Términos</a></li>
```

## Troubleshooting

### Common Issues

#### Broken Links
If links aren't working:
1. Check for typos in the `href` attribute
2. Verify file names match exactly (case-sensitive)
3. Ensure files are in the correct directory
4. Test internal links (starting with #) match section IDs

#### Responsive Issues
If mobile layout looks wrong:
1. Check that Tailwind CSS is properly loaded
2. Verify responsive classes (md:, lg:) are present
3. Test different screen sizes using browser dev tools

#### Style Problems
If styles aren't applying:
1. Confirm Tailwind CSS link is working:
```html
<link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
```
2. Check for missing or misspelled classes
3. Ensure Font Awesome is loaded for icons

### Need Help?
- Check Tailwind CSS documentation for class references
- Verify HTML structure matches the original
- Test changes in multiple browsers
- Use browser developer tools to inspect elements

Remember to always backup your files before making changes and test thoroughly after modifications.