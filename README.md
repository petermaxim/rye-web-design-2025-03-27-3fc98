# Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Rye Web Design landing page. Follow these steps to make common updates while preserving the page's functionality and design integrity.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name:**
```html
<a href="#" class="text-2xl font-bold text-white hover:text-blue-400">
    Rye Web Design  <!-- Change this text -->
</a>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>  <!-- Change menu text here -->
    <a href="#benefits">Benefits</a>
    <a href="#contact">Get Started</a>
</div>
```

### Hero Section
Located at the top of the page with the main headline:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-6">
    Affordable Websites for Service Businesses  <!-- Update main headline -->
</h1>
<p class="text-xl text-gray-400 mb-12">
    Professional web design solutions  <!-- Update subheading -->
</p>
```

### Tailwind CSS Classes Explained
Common classes used throughout the page:

- Text sizes: `text-sm`, `text-base`, `text-lg`, `text-xl`, etc.
- Colors: `text-gray-400`, `bg-blue-600`, `text-white`
- Spacing: `px-6` (padding left/right), `py-4` (padding top/bottom), `mb-12` (margin bottom)
- Responsive design: `md:text-5xl` (applies at medium screens and up)

To modify styling:
1. Find the element you want to change
2. Locate its class attribute
3. Add or modify Tailwind classes
4. Test on different screen sizes

## Managing Links

### Internal Navigation Links
Current internal links and how to update them:

```html
<!-- Navigation Menu -->
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#contact">Get Started</a>

<!-- To update, match the href with the section ID -->
<section id="features">  <!-- This ID must match the href above -->
```

### External Links
Current external links that need attention:

```html
<!-- Form Link -->
<a href="https://form.zippsites.com">Start Your Project</a>

<!-- Email Link -->
<a href="mailto:hello@zippsites.com">hello@zippsites.com</a>
```

To update external links:
1. Locate the `<a>` tag
2. Change the `href` attribute to your new URL
3. Update the displayed text between the tags
4. Test the link to ensure it works

## Adding Privacy and Terms Pages

### Current Footer Links
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white">Terms of Service</a></li>
    </ul>
</div>
```

### Steps to Add Policy Pages

1. Create new HTML files:
   - Create `privacy.html`
   - Create `terms.html`

2. Update the footer links:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white">Terms of Service</a></li>
```

3. Ensure consistent styling by copying these classes to new page links:
   - `text-gray-400` for normal state
   - `hover:text-white` for hover state
   - `transition-colors duration-300` for smooth transitions

## Troubleshooting

Common issues and solutions:

1. **Broken Internal Links**
   - Verify that section IDs match the href attributes exactly
   - Check for typos in both the link and section ID
   - Ensure IDs are unique across the page

2. **Responsive Design Issues**
   - Check mobile view using browser developer tools
   - Verify media query classes (e.g., `md:`, `lg:`) are correct
   - Test on different screen sizes

3. **Styling Problems**
   - Confirm Tailwind CSS is properly loaded
   - Check for conflicting classes
   - Verify class names are spelled correctly

Remember to:
- Always test changes in multiple browsers
- Validate links before deploying
- Keep backups of working versions
- Test responsive design at various screen sizes

For additional help, consult the [Tailwind CSS documentation](https://tailwindcss.com/docs) or contact your web development team.