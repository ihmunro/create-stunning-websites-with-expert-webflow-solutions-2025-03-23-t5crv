# Landing Page Maintenance Guide

This guide will help you maintain and customize the Webflow Expert landing page. Whether you're new to web development or need a quick reference, follow these instructions to make updates while preserving the design integrity.

## 1. Updating Text and Tailwind CSS Classes

### Text Content Updates

#### Hero Section
```html
<!-- Located in the main hero section -->
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-6...">
    Create Stunning Websites with Expert Webflow Solutions
</h1>
```
To modify:
1. Locate the `<h1>` tag in the hero section
2. Replace the text between the opening and closing tags
3. Maintain the existing classes to preserve styling

#### Features Section
Each feature card follows this structure:
```html
<div class="p-8 rounded-2xl bg-gray-800/50...">
    <h3 class="text-xl font-semibold mb-4">Custom Webflow Designs</h3>
    <p class="text-gray-400">Tailored solutions that perfectly match...</p>
</div>
```
To update:
1. Find the feature cards within the `features` section
2. Modify the `<h3>` title text
3. Update the description in the `<p>` tag

### Tailwind CSS Classes Explained

#### Responsive Design Classes
- `md:` prefix: Applies styles on medium screens (768px+)
- `lg:` prefix: Applies styles on large screens (1024px+)
Example:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl">
<!-- text-4xl (mobile) → text-5xl (tablet) → text-6xl (desktop) -->
```

#### Common Styling Classes
- `bg-gray-900`: Dark background
- `text-gray-100`: Light text
- `rounded-2xl`: Rounded corners
- `hover:scale-105`: Slight zoom on hover
- `transition-all`: Smooth transitions

## 2. Fixing Broken Links

### Navigation Menu Links
Current structure:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update internal links:
1. Locate the link in the navigation menu
2. Update the `href` attribute:
   - Internal sections: Use `#section-name`
   - External pages: Use full URL (e.g., `https://example.com`)

### Call-to-Action Buttons
```html
<a href="https://example.com" class="inline-block px-8 py-4...">
    Get Started Today
</a>
```
Replace `https://example.com` with your actual booking or contact page URL.

## 3. Linking Privacy and Terms Pages

### Footer Link Updates
Current structure:
```html
<div>
    <h3 class="text-xl font-bold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white...">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white...">Terms of Service</a></li>
    </ul>
</div>
```

To add privacy and terms pages:
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white...">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white...">Terms of Service</a></li>
```

## Troubleshooting Tips

### Common Issues and Solutions

1. **Broken Layout**
   - Check for missing closing tags
   - Verify Tailwind classes are spelled correctly
   - Ensure responsive prefixes (`md:`, `lg:`) are properly used

2. **Links Not Working**
   - Verify file paths are correct
   - Check for proper URL formatting
   - Ensure IDs match section names for internal links

3. **Styling Issues**
   - Confirm Tailwind CDN is properly loaded
   - Check for conflicting classes
   - Verify proper nesting of elements

### Best Practices

1. Always test changes across different screen sizes
2. Maintain consistent spacing using provided Tailwind classes
3. Keep the gradient styling consistent across sections
4. Preserve the responsive design structure
5. Test all links after making changes

## Need Help?

If you encounter issues or need assistance:
1. Check the HTML structure carefully
2. Verify all changes against the original code
3. Test on multiple browsers
4. Consult the [Tailwind CSS documentation](https://tailwindcss.com/docs)

Remember to back up your files before making significant changes.