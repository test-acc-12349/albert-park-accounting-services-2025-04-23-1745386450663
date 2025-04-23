# Albert Park Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Albert Park Accounting Services landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the company name and navigation menu.

```html
<!-- Company Name -->
<div class="text-2xl font-bold bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">
    Albert Park  <!-- Edit this text to change company name -->
</div>
```

To modify the company name:
1. Locate this section at the top of the page
2. Replace "Albert Park" with your desired text
3. Keep the surrounding div and classes intact to maintain the gradient effect

### Hero Section
The main headline and subheading are in the hero section:

```html
<h1 class="text-4xl md:text-5xl lg:text-7xl font-bold leading-tight mb-8 bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent">
    Albert Park accounting services  <!-- Main headline -->
</h1>
<p class="text-xl md:text-2xl lg:text-3xl text-gray-300 mb-12 max-w-3xl mx-auto">
    Your financial success is our bottom line  <!-- Subheading -->
</p>
```

Important Tailwind Classes Explained:
- `text-4xl md:text-5xl lg:text-7xl`: Responsive text sizing
  - `text-4xl`: Base size for mobile
  - `md:text-5xl`: Medium screens
  - `lg:text-7xl`: Large screens
- `bg-gradient-to-r`: Creates right-flowing gradient
- `from-purple-400 to-pink-400`: Gradient colors

### Features Section
Each feature card follows this structure:

```html
<div class="bg-gray-800/50 rounded-2xl p-8 hover:bg-gray-800 transition-all duration-300 transform hover:scale-105 hover:shadow-2xl">
    <!-- Icon container -->
    <div class="w-16 h-16 bg-gradient-to-br from-purple-500 to-pink-500 rounded-xl mb-6 flex items-center justify-center">
        <!-- SVG icon here -->
    </div>
    <h3 class="text-xl font-semibold mb-4">Tax Optimization</h3>
    <p class="text-gray-400">Strategic tax planning and optimization...</p>
</div>
```

To update feature cards:
1. Locate the features section (id="features")
2. Find the specific card you want to modify
3. Update the h3 text for the title
4. Modify the p text for the description
5. Keep all classes intact to maintain styling

## Fixing Broken Links

### Navigation Menu Links
Current navigation links are:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-300 hover:text-white transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-300 hover:text-white transition-colors duration-300">Benefits</a>
    <a href="#contact" class="text-gray-300 hover:text-white transition-colors duration-300">Contact</a>
</div>
```

To update navigation links:
1. Identify the section you want to link to
2. Update the href attribute with either:
   - Internal link: Use "#section-id" format
   - External link: Use full URL (https://example.com)

### Call-to-Action Links
Current placeholder links that need updating:

```html
<a href="https://theaccountants.com" class="inline-block px-8 py-4 text-lg font-semibold rounded-full bg-gradient-to-r from-purple-500 to-pink-500">
    Get Started Today
</a>
```

Replace "https://theaccountants.com" with your actual booking or contact page URL.

## Linking Privacy and Terms Pages

### Footer Links Section
Locate the Legal section in the footer:

```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-gray-400">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add privacy and terms pages:
1. Create privacy.html and terms.html in your root directory
2. Update the href attributes:

```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

Common Issues and Solutions:

1. **Broken Gradients**
   - Ensure all gradient classes remain intact
   - Check for typos in color classes (e.g., from-purple-500)

2. **Responsive Issues**
   - Verify responsive classes are present (md:, lg: prefixes)
   - Test on different screen sizes using browser dev tools

3. **Link Problems**
   - Check for proper href formatting
   - Verify file paths for internal links
   - Test all links after updating

Remember to:
- Always backup your code before making changes
- Test all modifications in a development environment first
- Validate your HTML using W3C Validator
- Check mobile responsiveness after any changes

For additional help, consult the [Tailwind CSS documentation](https://tailwindcss.com/docs) or reach out to your development team.