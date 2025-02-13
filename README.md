# Texas Web Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Texas Web Design landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Modifying Text Content

The page is divided into several key sections. Here's how to update text in each:

#### Header Section
```html
<!-- Location: Line 20 -->
<a href="/" class="text-2xl font-bold">
    Texas Web Design  <!-- Change company name here -->
</a>
```

#### Hero Section
```html
<!-- Location: Around Line 39 -->
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold mb-6">
    Best Websites In Texas  <!-- Change main headline here -->
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Creating stunning, high-performance websites  <!-- Change subheading here -->
</p>
```

#### Features Section
Each feature card follows this structure:
```html
<div class="p-8 rounded-2xl bg-white shadow-lg">
    <h3 class="text-2xl font-bold mb-4">
        Free Hosting  <!-- Change feature title here -->
    </h3>
    <p class="text-gray-600">
        Premium hosting included...  <!-- Change feature description here -->
    </p>
</div>
```

### Understanding Tailwind CSS Classes

Key classes used in this landing page:

1. **Text Sizes**
   - `text-xl`: Medium text
   - `text-2xl`: Larger text
   - `text-4xl`: Very large text
   - Example: Change `text-xl` to `text-2xl` to make text bigger

2. **Spacing**
   - `px-6`: Horizontal padding
   - `py-4`: Vertical padding
   - `mb-6`: Bottom margin
   - Example: Change `mb-6` to `mb-8` for more space below

3. **Colors**
   - `text-gray-600`: Gray text
   - `bg-white`: White background
   - `from-blue-600`: Gradient start color
   - Example: Change `text-gray-600` to `text-blue-600` for blue text

## Fixing Broken Links

### Navigation Menu Links
Current navigation links are:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#video">Video</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update a link:
1. Locate the `href` attribute
2. Replace the value with your new link
3. Example: Change `href="#features"` to `href="/features.html"`

### External Links
The main call-to-action button needs updating:
```html
<a href="https://twd.com" class="inline-block px-8 py-4">
    Get Started
</a>
```

Replace `https://twd.com` with your actual website URL.

## Linking Privacy and Terms Pages

### Footer Legal Links
Current placeholder links:
```html
<div>
    <h4 class="text-xl font-bold mb-6">Legal</h4>
    <ul class="space-y-3">
        <li><a href="#" class="hover:text-white transition duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="/privacy.html" class="hover:text-white transition duration-300">Privacy Policy</a></li>
<li><a href="/terms.html" class="hover:text-white transition duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Layout**
   - Check that you haven't removed any essential Tailwind classes
   - Verify all `div` tags are properly closed
   - Maintain the responsive classes (e.g., `md:text-2xl`)

2. **Links Not Working**
   - Ensure href values start with `/` for root-relative paths
   - Check for typos in file names
   - Verify files exist in the correct directory

3. **Icons Not Showing**
   - Verify the Font Awesome CDN link is present in the header
   - Check icon class names match Font Awesome 6.0.0 syntax

### Need Help?
- Double-check your changes against the original code
- Use browser developer tools (F12) to inspect elements
- Keep a backup of the original file before making changes

Remember: Always test your changes in multiple browsers and screen sizes to ensure everything works as expected.