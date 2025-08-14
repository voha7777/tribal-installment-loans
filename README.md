# Tribal Loans Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Tribal Loans landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo. To update:

1. **Logo Text:**
```html
<a href="/" class="text-2xl font-bold text-blue-600">TribalLoans</a>
```
- Replace "TribalLoans" with your desired text
- Adjust size using `text-2xl` (options: text-lg, text-xl, text-3xl)
- Change color using `text-blue-600` (options: text-red-600, text-green-600)

### Hero Section
Located at the top of the page with the main headline:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
    Tribal Installment Loans with Fast Approval and Easy Terms
</h1>
```
- Update the headline text between the h1 tags
- Responsive text sizes are already set up:
  - Mobile: `text-4xl`
  - Tablet: `md:text-5xl`
  - Desktop: `lg:text-6xl`

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white rounded-2xl p-8 shadow-lg hover:shadow-xl transition-shadow duration-300">
    <h3 class="text-xl font-semibold mb-4">Fast Approval</h3>
    <p class="text-gray-600">Quick decision process...</p>
</div>
```
To modify:
1. Change the heading text within `<h3>` tags
2. Update description text within `<p>` tags
3. Adjust padding using `p-8` (options: p-4, p-6, p-10)

## Managing Links

### Navigation Menu Links
Current navigation links are:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update:
1. Internal links (same page):
   - Use `#section-name` format
   - Ensure section IDs match exactly
   - Example: `<a href="#features">Features</a>`

2. External links:
   - Replace `#` with full URL
   - Example: `<a href="https://www.example.com/page">Link Text</a>`

### Apply Now Button
Located in multiple places:
```html
<a href="https://www.tribal-installment-loans.com/apply" class="inline-flex items-center...">
```
- Replace the URL with your actual application page
- Maintain the `inline-flex` and other classes for consistent styling

## Adding Privacy and Terms Pages

### Footer Legal Links
Current placeholder links:
```html
<ul class="space-y-2 text-sm">
    <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

To link to new pages:
1. Create privacy.html and terms.html in your root directory
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Check that section IDs match href attributes exactly
   - Example: `href="#features"` must match `id="features"`
   - IDs are case-sensitive

2. **Responsive Design Issues**
   - Classes starting with `md:` apply to tablet and up
   - Classes starting with `lg:` apply to desktop
   - Never remove responsive classes unless you understand the impact

3. **Styling Problems**
   - Keep the `class="..."` attribute intact
   - Add new classes at the end of existing ones
   - Maintain spacing between class names

### Best Practices

1. Always test changes on multiple screen sizes
2. Keep a backup of the original file before making changes
3. Validate external URLs before adding them
4. Maintain consistent spacing and indentation
5. Test all links after making changes

Need more help? Contact technical support or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).