# Landing Page Maintenance Guide

This guide will help you maintain and customize your landing page. Follow these detailed instructions to make common updates while preserving the design and functionality.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains your brand name and navigation menu. To update:

1. Change the brand name:
```html
<!-- Find this line in the header -->
<a href="/" class="text-2xl font-bold text-gray-900">Lorem ipsum</a>
```
Replace "Lorem ipsum" with your brand name.

### Hero Section
Located at the top of the page with the main heading and two buttons:

1. Update the main heading:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8">
    Lorem ipsum dolor
</h1>
```
Replace "Lorem ipsum dolor" with your headline.

2. Modify button text:
```html
<button class="bg-indigo-600 text-white px-8 py-4 rounded-full text-lg font-semibold">
    Get Started Now
</button>
```

### Tailwind CSS Class Guide
Common classes used in this template:
- `text-{size}`: Controls text size (xl, 2xl, 3xl, etc.)
- `font-{weight}`: Controls text weight (bold, semibold, normal)
- `bg-{color}`: Sets background color
- `text-{color}`: Sets text color
- `px-{size}` and `py-{size}`: Sets padding
- `mb-{size}`: Sets margin bottom

Example of modifying a button's appearance:
```html
<!-- Original -->
<button class="bg-indigo-600 text-white px-6 py-2">

<!-- Modified for larger size and different color -->
<button class="bg-blue-600 text-white px-8 py-4">
```

## Fixing Broken Links

### Navigation Menu Links
Current navigation links are:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#solutions">Solutions</a>
    <a href="#contact">Contact</a>
</div>
```

To update:
1. Identify the section ID you want to link to
2. Update the `href` attribute with `#section-id`
3. Example:
```html
<!-- Linking to a new section -->
<a href="#pricing" class="text-gray-600 hover:text-gray-900">Pricing</a>
```

### Footer Links
Located at the bottom of the page:
```html
<ul class="space-y-2">
    <li><a href="#" class="text-gray-400 hover:text-white">About</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white">Features</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white">Contact</a></li>
</ul>
```

To update:
1. Replace `#` with your actual URL
2. Example: `<a href="about.html">About</a>`

## Linking Privacy and Terms Pages

### Adding Privacy Policy Link
Find this section in the footer:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white">Terms of Service</a></li>
    </ul>
</div>
```

Update the links:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Navigation Links**
   - Ensure section IDs match exactly with href attributes
   - Check for typos in IDs and hrefs
   - Verify that sections have the correct ID attribute

2. **Responsive Design Issues**
   - Don't remove `md:` or `lg:` prefixes from classes
   - Keep the mobile menu button intact:
   ```html
   <button class="md:hidden text-gray-600">
   ```

3. **Social Media Icons**
   - Update social media links in the footer:
   ```html
   <a href="https://facebook.com/your-page" class="text-gray-400 hover:text-white">
   ```

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs) for class references
- Verify all HTML tags are properly closed
- Use browser developer tools (F12) to inspect elements
- Test the page on different screen sizes

Remember to:
- Keep backup copies of your original files
- Test all links after making changes
- Maintain consistent styling across all pages
- Preview changes in multiple browsers