# Texas Web Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Texas Web Design landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your main navigation and logo. To update:

1. **Company Name/Logo**
```html
<!-- Find this line in the header section -->
<a href="/" class="text-2xl font-bold text-blue-600">Texas Web Design</a>
```
- Replace "Texas Web Design" with your company name
- Adjust text size by changing `text-2xl` to `text-xl` (smaller) or `text-3xl` (larger)

2. **Navigation Menu Items**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600">Features</a>
    <!-- Additional menu items -->
</div>
```
- Change menu text by editing the text between `<a>` tags
- Maintain the `hidden md:flex` class to ensure proper mobile responsiveness

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold">Best Websites In Texas</h1>
<p class="text-xl md:text-2xl text-gray-600">Professional web design solutions...</p>
```
- Update headline text between the `<h1>` tags
- Modify subheading in the `<p>` tag
- Keep the responsive text classes (`text-4xl md:text-5xl lg:text-6xl`) to maintain proper sizing across devices

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white rounded-xl p-8 shadow-lg hover:shadow-xl">
    <h3 class="text-xl font-bold mb-4">Free Hosting</h3>
    <p class="text-gray-600">Premium hosting included...</p>
</div>
```
To modify:
1. Change feature title between `<h3>` tags
2. Update description in the `<p>` tag
3. Maintain spacing classes (`mb-4`, `p-8`) for consistent layout

## Managing Links

### Navigation Links
Current navigation links are:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update:
1. Internal links (same page):
   - Keep the `#` symbol
   - Match the ID of the section you're linking to
   Example: `<a href="#new-section">New Section</a>`

2. External links:
   - Replace `#` with full URL
   Example: `<a href="https://yoursite.com/page">Page</a>`

### Call-to-Action Buttons
Located in hero and CTA sections:
```html
<a href="https://twd.com" class="inline-block px-8 py-4 bg-blue-600">Start Your Project</a>
```
- Replace `https://twd.com` with your actual URL
- Maintain the styling classes to keep consistent button appearance

## Adding Privacy and Terms Pages

### Footer Legal Links
Current placeholder links:
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Create new files:
   - `privacy.html`
   - `terms.html`

2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Layout**
- Check that you haven't removed important Tailwind classes
- Verify all `div` tags are properly closed
- Maintain the responsive classes (e.g., `md:`, `lg:` prefixes)

2. **Links Not Working**
- Ensure file names match exactly (case-sensitive)
- Verify all URLs start with `http://` or `https://`
- Check that internal link IDs match section IDs

3. **Inconsistent Styling**
- Copy existing class strings when creating new elements
- Keep the same class order for similar elements
- Maintain spacing classes (`mb-4`, `py-24`, etc.)

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs) for styling references
- Validate your HTML using [W3C Validator](https://validator.w3.org/)
- Test all links before deploying changes

Remember to always make a backup of your files before making significant changes, and test your updates across different devices and browsers.