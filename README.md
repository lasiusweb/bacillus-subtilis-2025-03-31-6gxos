# ProbioticFy Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the ProbioticFy landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains your brand name and navigation menu. To update:

1. **Brand Name:**
```html
<!-- Find this line in the header section -->
<a href="/" class="text-2xl font-bold">ProbioticFy</a>
```
Simply replace "ProbioticFy" with your desired brand name.

2. **Navigation Items:**
```html
<a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors duration-200">Features</a>
```
- To change text: Replace "Features" with new text
- To modify colors: 
  - `text-gray-600` controls normal state color
  - `hover:text-gray-900` controls hover state color

### Hero Section
Located at the top of the page with a large background image:

```html
<h1 class="text-4xl md:text-6xl font-bold mb-6">Bacillus subtilis</h1>
<p class="text-xl md:text-2xl mb-8">Supercharge soil & protect crops with Bacillus subtilis!</p>
```

- To update heading size:
  - `text-4xl` controls mobile size
  - `md:text-6xl` controls desktop size
- To adjust spacing:
  - `mb-6` adds margin bottom (can be 1-16)

### Features Section
Each feature card follows this structure:

```html
<div class="bg-white p-8 rounded-xl shadow-lg hover:shadow-xl transition-shadow duration-300">
```

Common Tailwind classes explained:
- `p-8`: Padding on all sides
- `rounded-xl`: Rounded corners
- `shadow-lg`: Box shadow
- `hover:shadow-xl`: Larger shadow on hover

## Fixing Broken Links

### Navigation Menu Links
Current internal links in the navigation:

```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
```

To update:
1. For internal sections: Use `#section-name`
2. For external pages: Use full URL
   ```html
   <a href="https://example.com/page">Page Name</a>
   ```

### Mobile Menu Links
Ensure mobile menu links match desktop navigation:

```html
<div x-show="isOpen" class="md:hidden">
    <div class="px-2 pt-2 pb-3 space-y-1">
        <!-- Update these links to match desktop navigation -->
        <a href="#features" class="block px-3 py-2 text-gray-600 hover:text-gray-900">Features</a>
    </div>
</div>
```

## Linking Privacy and Terms Pages

### Footer Policy Links
Located in the footer section:

```html
<div>
    <h4 class="text-lg font-semibold mb-4">Policies</h4>
    <ul class="space-y-2">
        <!-- Update these href attributes -->
        <li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-200">Privacy Policy</a></li>
        <li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-200">Terms of Service</a></li>
    </ul>
</div>
```

To add new policy pages:
1. Create new HTML files (e.g., `privacy.html`, `terms.html`)
2. Update the `href` attributes to point to these files
3. Maintain consistent styling using the same classes

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Ensure section IDs match href attributes
   - Example: `href="#features"` needs matching `id="features"` in section

2. **Responsive Design Issues**
   - Check mobile classes (default) vs desktop classes (prefixed with `md:`)
   - Example: `text-4xl md:text-6xl`

3. **Image Loading Problems**
   - Verify image URLs are correct
   - Use relative paths for local images
   - Example:
   ```html
   <img src="./images/your-image.jpg" alt="Description">
   ```

### CSS Class Reference

Common Tailwind classes used in this page:

- Text sizes: `text-sm`, `text-xl`, `text-2xl`, `text-4xl`
- Colors: `text-gray-600`, `text-white`, `bg-green-600`
- Spacing: `p-8` (padding), `mb-6` (margin bottom)
- Flex: `flex`, `items-center`, `justify-between`
- Grid: `grid`, `grid-cols-1`, `md:grid-cols-2`

Remember to maintain the responsive design by keeping both mobile and desktop classes when updating styles.

Need more help? Contact technical support or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).