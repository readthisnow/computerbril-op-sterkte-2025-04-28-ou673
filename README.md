# Landing Page Maintenance Guide

This guide will help you maintain and customize the Computerbril landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your main navigation and logo. To update:

1. **Logo Text**: Find this line and change the text "Computerbril":
```html
<a href="/" class="text-2xl font-bold text-indigo-600">Computerbril</a>
```

2. **Navigation Items**: Locate the navigation menu:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-indigo-600">Voordelen</a>
    <!-- Other menu items -->
</div>
```
To modify menu items, update the text between `<a>` tags.

### Hero Section
The main banner section contains:

1. **Main Heading**: Update the title and promotional text:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-extrabold text-white mb-8">
    Computerbril Op Sterkte
    <span class="block text-yellow-300 mt-2">Nu 20% Korting!</span>
</h1>
```

2. **Promotional Timer**: Modify the countdown text:
```html
<p class="text-xl md:text-2xl text-white/90 mb-12">
    Nog maar <span class="font-bold text-yellow-300">7 dagen</span> beschikbaar
</p>
```

### Tailwind CSS Tips for Beginners
- `text-{size}`: Controls text size (xl, 2xl, etc.)
- `font-{weight}`: Controls text boldness (bold, semibold, etc.)
- `mb-{number}`: Adds margin bottom (4, 8, 12, etc.)
- `bg-{color}`: Changes background color
- `hover:`: Adds hover effects

## Managing Links

### Navigation Links
Current links in the navigation:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Voordelen</a>
    <a href="#benefits">Features</a>
    <a href="#faq">FAQ</a>
    <a href="https://computerbril.org/winkel">Bestel Nu</a>
</div>
```

To update links:
1. Internal links (starting with #) connect to page sections
2. External links (starting with http) go to other websites
3. Replace `href` values with your desired URLs

### Call-to-Action Buttons
Update the main CTA button links:

```html
<a href="https://computerbril.org/winkel" class="inline-block bg-white text-indigo-600 px-8 py-4 rounded-full">
    Bekijk de Collectie
</a>
```

Replace `https://computerbril.org/winkel` with your shop URL.

## Adding Privacy and Terms Pages

### Footer Link Setup
Locate the footer links section:

```html
<div>
    <h3 class="text-xl font-semibold mb-4">Links</h3>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white">Terms of Service</a></li>
    </ul>
</div>
```

To add privacy and terms pages:

1. Create new files:
   - Create `privacy.html` in your root directory
   - Create `terms.html` in your root directory

2. Update the links:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Ensure section IDs match href values
   - Check for typos in IDs
   - Verify that sections have the correct id attribute
   ```html
   <!-- Example of correct section ID -->
   <section id="features" class="py-24 bg-white">
   ```

2. **Responsive Design Issues**
   - Check that you maintain the responsive classes:
     - `md:` for medium screens
     - `lg:` for large screens
   - Don't remove the `container` class from main sections
   ```html
   <div class="container mx-auto px-4 sm:px-6 lg:px-8">
   ```

3. **Style Conflicts**
   - Keep Tailwind classes in the original order
   - Don't remove utility classes without understanding their purpose
   - Test on multiple screen sizes after making changes

### Need Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Use browser developer tools to inspect elements
- Make one change at a time and test thoroughly
- Keep a backup of the original code

Remember to test all changes across different devices and browsers before publishing to your live site.