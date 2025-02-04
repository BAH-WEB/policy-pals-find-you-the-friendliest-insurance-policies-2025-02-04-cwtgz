# PolicyPals Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the PolicyPals landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance for common maintenance tasks.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Main Sections Overview
The landing page is divided into these key sections:
- Header (Navigation)
- Hero Section
- Features Section
- Benefits Section
- FAQ Section
- Call-to-Action Section
- Footer

### Updating Text Content

#### Hero Section
```html
<!-- Located in the main section -->
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight tracking-tight mb-8 bg-gradient-to-r from-blue-500 to-teal-400 bg-clip-text text-transparent">
    Policy Pals Find You The Friendliest Insurance Policies
</h1>
```
To update the main heading:
1. Locate the `<h1>` tag in the hero section
2. Replace the text while keeping all HTML tags intact
3. Maintain the existing capitalization style

#### Features Section
Each feature card follows this structure:
```html
<div class="bg-gray-800 rounded-2xl p-8 hover:shadow-xl hover:scale-105 transition-all duration-300">
    <h3 class="text-xl font-semibold mb-4">Personalised Policy Matching</h3>
    <p class="text-gray-400">Find insurance policies perfectly tailored to your unique needs and preferences.</p>
</div>
```
To update feature cards:
1. Locate the features section (id="features")
2. Find the specific card you want to update
3. Modify the `<h3>` text for the title
4. Update the `<p>` text for the description

### Modifying Tailwind CSS Classes

#### Understanding Responsive Classes
The page uses these breakpoints:
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

#### Common Style Classes
- Background colors: `bg-gray-900`, `bg-gray-800`
- Text colors: `text-gray-100`, `text-gray-400`
- Padding: `p-8`, `py-24`, `px-4`
- Margins: `mb-8`, `mt-4`
- Hover effects: `hover:shadow-xl`, `hover:scale-105`

## Fixing Broken Links

### Current Link Structure
```html
<!-- Navigation Links -->
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="https://www.PolicyPals.Co.Uk">Get Started</a>
```

### Updating External Links
1. Locate the "Get Started" button links:
```html
<a href="https://www.PolicyPals.Co.Uk" class="inline-block px-8 py-4...">
```
2. Replace the URL with your actual website URL
3. Ensure the URL includes `https://` or `http://`
4. Test the link after updating

### Internal Section Links
Current internal links use anchor tags (#):
- `#features`
- `#benefits`
- `#faq`

To update:
1. Ensure section IDs match the href values
2. Example:
```html
<!-- Navigation link -->
<a href="#features">Features</a>

<!-- Matching section ID -->
<section id="features" class="py-24 bg-gray-800/50">
```

## Linking Privacy and Terms Pages

### Footer Link Updates
Locate the legal section in the footer:
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
1. Create `privacy.html` and `terms.html` in your project directory
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Check that section IDs exactly match href values
   - IDs are case-sensitive
   - Remove any spaces in IDs

2. **Responsive Design Issues**
   - Verify all responsive classes (md:, lg:) are properly spaced
   - Test on different screen sizes
   - Use browser developer tools to check breakpoints

3. **Styling Inconsistencies**
   - Keep gradient classes consistent:
     ```html
     bg-gradient-to-r from-blue-500 to-teal-400
     ```
   - Maintain consistent spacing classes (margin/padding)
   - Use the same hover effect classes for similar elements

Remember to always test your changes across different devices and browsers to ensure consistency.