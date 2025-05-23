# BusinessPlan.AI Landing Page Maintenance Guide

This guide will help you maintain and customize the BusinessPlan.AI landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the logo and navigation menu. To update:

```html
<!-- Logo Text (Line 19) -->
<a href="/" class="text-xl font-bold text-blue-600">BusinessPlan.AI</a>
```
- Change "BusinessPlan.AI" to your desired brand name
- The `text-blue-600` class controls the blue color (adjust number for different shades: 500-900)

### Hero Section
Located at the top of the page:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">
    How To Start An Online Business
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-8">
    3 Step Business Plan Generator
</p>
```
- Update text between the tags
- Text sizes use responsive classes:
  - `text-4xl`: mobile devices
  - `md:text-5xl`: medium screens
  - `lg:text-6xl`: large screens

### Tailwind CSS Tips for Beginners
- Spacing classes use this format: `m-[number]` for margin, `p-[number]` for padding
  - Example: `mb-6` means "margin-bottom: 1.5rem"
- Colors use format: `[type]-[color]-[shade]`
  - Example: `text-blue-600`, `bg-gray-50`
- Responsive prefixes: `sm:`, `md:`, `lg:`
  - Example: `md:grid-cols-3` applies on medium screens and up

## Managing Links

### Navigation Menu Links
Current navigation links are:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-blue-600">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-blue-600">FAQ</a>
</div>
```

To update:
1. Locate the `href` attribute
2. Replace `#features` with your new link
3. Update the text between `<a>` tags

### Call-to-Action Buttons
The main CTA buttons currently point to "https://ninja200.online":

```html
<!-- Update this URL in all CTA buttons -->
<a href="https://ninja200.online" class="bg-blue-600 text-white px-6 py-2 rounded-full">
    Get Started
</a>
```

To update:
1. Find all instances of `https://ninja200.online`
2. Replace with your target URL
3. Test all buttons after updating

## Adding Privacy and Terms Pages

### Footer Link Setup
Current footer links structure:

```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white">Terms of Service</a></li>
    </ul>
</div>
```

To add privacy and terms pages:

1. Create new files:
   ```bash
   touch privacy.html
   touch terms.html
   ```

2. Update the footer links:
   ```html
   <li><a href="privacy.html" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
   <li><a href="terms.html" class="text-gray-400 hover:text-white">Terms of Service</a></li>
   ```

3. Ensure consistent styling by copying the header and footer from index.html to your new pages

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Check that section IDs match href attributes
   - Example: `href="#features"` needs matching `id="features"` in content

2. **Responsive Design Issues**
   - Verify responsive classes are properly ordered:
   ```html
   <!-- Correct -->
   <div class="text-sm md:text-base lg:text-lg">
   
   <!-- Incorrect -->
   <div class="lg:text-lg text-sm md:text-base">
   ```

3. **Missing Styles**
   - Confirm Tailwind CDN is loaded:
   ```html
   <script src="https://cdn.tailwindcss.com"></script>
   ```
   - Check for typos in class names

### Need Help?
- Reference the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Use browser developer tools (F12) to inspect elements
- Test all changes across different screen sizes

Remember to:
- Back up files before making changes
- Test all links after updates
- View changes on multiple devices
- Keep consistent styling throughout