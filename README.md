# Pogiso Tours Landing Page - Maintenance & Customization Guide

A comprehensive guide for maintaining, updating, and customizing the Pogiso Tours corporate shuttle landing page. This document is designed for developers of all skill levels.

---

## Table of Contents

1. [Overview](#overview)
2. [File Structure](#file-structure)
3. [Updating Text Content](#updating-text-content)
4. [Modifying Tailwind CSS Classes](#modifying-tailwind-css-classes)
5. [Fixing and Managing Links](#fixing-and-managing-links)
6. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
7. [Common Customizations](#common-customizations)
8. [Troubleshooting](#troubleshooting)
9. [Best Practices](#best-practices)

---

## Overview

The Pogiso Tours landing page is built with:
- **HTML5** for semantic structure
- **Tailwind CSS** for responsive styling (via CDN)
- **Font Awesome 6.4.0** for icons
- **Vanilla JavaScript** for interactive features (mobile menu, FAQ accordion)

The page is fully responsive and works on mobile, tablet, and desktop devices.

### Key Features
- Sticky header navigation
- Mobile-responsive hamburger menu
- Hero section with background image
- Feature cards with hover effects
- Benefits section with alternating image layouts
- Testimonials carousel
- Expandable FAQ section
- Contact form
- Comprehensive footer with links

---

## File Structure

```
project-root/
├── index.html          (Main landing page - you are here)
├── blog.html           (Referenced in footer - needs to be created)
├── privacy.html        (Privacy Policy page - needs to be created)
├── terms.html          (Terms of Service page - needs to be created)
└── css/
    └── custom.css      (Optional: for custom styles beyond Tailwind)
```

### Current File References
The `index.html` file references several other pages that may need to be created:
- `blog.html` - Blog page link in footer
- `privacy.html` - Privacy policy link in footer
- `terms.html` - Terms of service link in footer

---

## Updating Text Content

### Understanding the HTML Structure

Before making changes, understand that text in HTML is contained within tags. The most common ones on this page are:

- `<h1>`, `<h2>`, `<h3>` - Headings (h1 is largest, h3 is smaller)
- `<p>` - Paragraphs (body text)
- `<a>` - Links
- `<span>` - Inline text

### Section-by-Section Text Updates

#### 1. Announcement Bar (Top Banner)

**Location:** Lines 57-60

**Current Code:**
```html
<div class="bg-gradient-to-r from-blue-900 to-blue-800 text-white py-3 px-4 text-center text-sm md:text-base">
    <i class="fas fa-truck mr-2"></i>
    Fast Nationwide Service - 24/7 Call Centre Available
</div>
```

**How to Update:**
1. Find the text "Fast Nationwide Service - 24/7 Call Centre Available"
2. Replace it with your new announcement
3. Keep the `<i class="fas fa-truck mr-2"></i>` tag if you want the truck icon, or change it to another [Font Awesome icon](https://fontawesome.com/icons)

**Example - Change to Holiday Special:**
```html
<div class="bg-gradient-to-r from-blue-900 to-blue-800 text-white py-3 px-4 text-center text-sm md:text-base">
    <i class="fas fa-star mr-2"></i>
    Holiday Special: 20% Off All Bookings - Limited Time Offer
</div>
```

#### 2. Logo/Brand Name

**Location:** Lines 63-67

**Current Code:**
```html
<div class="flex items-center space-x-2">
    <i class="fas fa-shuttle-van text-blue-900 text-3xl"></i>
    <span class="text-xl md:text-2xl font-bold text-blue-900">Pogiso Tours</span>
</div>
```

**How to Update:**
Simply replace "Pogiso Tours" with your company name. The icon will remain the same.

```html
<span class="text-xl md:text-2xl font-bold text-blue-900">Your Company Name</span>
```

#### 3. Hero Section Main Heading

**Location:** Lines 116-119

**Current Code:**
```html
<h1 class="text-4xl md:text-6xl font-bold text-white mb-6 leading-tight tracking-tight">
    Corporate Shuttle & Tour Experts Nationwide
</h1>
```

**How to Update:**
Replace the text between `<h1>` and `</h1>` tags:

```html
<h1 class="text-4xl md:text-6xl font-bold text-white mb-6 leading-tight tracking-tight">
    Your New Main Headline Here
</h1>
```

**Important:** Keep the `class` attribute exactly as it is. This controls the styling (text size, color, spacing).

#### 4. Hero Section Subtitle

**Location:** Lines 120-122

**Current Code:**
```html
<p class="text-xl md:text-2xl text-gray-100 mb-8 leading-relaxed font-light">
    Safe. Punctual. Professional. Corporate Shuttle Excellence
</p>
```

**How to Update:**
```html
<p class="text-xl md:text-2xl text-gray-100 mb-8 leading-relaxed font-light">
    Your New Subtitle or Tagline Here
</p>
```

#### 5. Feature Cards Section

**Location:** Lines 136-186

There are three feature cards. Each follows this structure:

**Current Code Example (Luxury Fleet Card):**
```html
<div class="bg-white border-2 border-gray-200 rounded-xl p-8 transition-all duration-300 hover:shadow-xl hover:scale-105 hover:border-blue-900 cursor-pointer">
    <div class="bg-blue-100 w-16 h-16 rounded-full flex items-center justify-center mb-6 mx-auto">
        <i class="fas fa-car text-3xl text-blue-900"></i>
    </div>
    <h3 class="text-2xl font-bold text-gray-900 mb-3 text-center">Luxury Fleet</h3>
    <p class="text-gray-600 leading-relaxed text-center">
        Our modern, well-maintained vehicles are equipped with premium amenities for your comfort and convenience during every journey.
    </p>
</div>
```

**How to Update a Feature Card:**

1. **Change the Icon:** Replace `fas fa-car` with another icon from [Font Awesome](https://fontawesome.com/icons)
   - `fas fa-phone` for phone/support
   - `fas fa-map` for location
   - `fas fa-star` for quality
   - `fas fa-shield` for security

2. **Change the Title:** Replace "Luxury Fleet" with your feature name

3. **Change the Description:** Replace the paragraph text with your feature description

**Complete Example - Changing First Card:**
```html
<div class="bg-white border-2 border-gray-200 rounded-xl p-8 transition-all duration-300 hover:shadow-xl hover:scale-105 hover:border-blue-900 cursor-pointer">
    <div class="bg-blue-100 w-16 h-16 rounded-full flex items-center justify-center mb-6 mx-auto">
        <i class="fas fa-shield text-3xl text-blue-900"></i>  <!-- Changed icon -->
    </div>
    <h3 class="text-2xl font-bold text-gray-900 mb-3 text-center">Safety First</h3>  <!-- Changed title -->
    <p class="text-gray-600 leading-relaxed text-center">
        Every vehicle undergoes rigorous safety inspections and our drivers are certified professionals.
    </p>  <!-- Changed description -->
</div>
```

#### 6. Benefits Section Headings

**Location:** Lines 195-202 (Cost-Effective), Lines 221-228 (Professional Chauffeurs), Lines 249-256 (Reliable Nationwide)

**Current Code Example:**
```html
<h3 class="text-3xl md:text-4xl font-bold text-gray-900 mb-4">Cost-Effective Solutions</h3>
<p class="text-lg text-gray-600 leading-relaxed mb-6">
    We provide transparent, competitive pricing without compromising on quality...
</p>
```

**How to Update:**
Simply replace the heading and paragraph text. The styling remains the same.

#### 7. Benefits Bullet Points

**Location:** Lines 207-217 (Cost-Effective example)

**Current Code:**
```html
<ul class="space-y-3">
    <li class="flex items-start">
        <i class="fas fa-check text-blue-900 mr-3 mt-1 flex-shrink-0"></i>
        <span class="text-gray-700">Competitive rates for corporate contracts</span>
    </li>
    <li class="flex items-start">
        <i class="fas fa-check text-blue-900 mr-3 mt-1 flex-shrink-0"></i>
        <span class="text-gray-700">Flexible payment terms available</span>
    </li>
    <li class="flex items-start">
        <i class="fas fa-check text-blue-900 mr-3 mt-1 flex-shrink-0"></i>
        <span class="text-gray-700">Volume discounts for regular bookings</span>
    </li>
</ul>
```

**How to Update:**
Replace the text within each `<span class="text-gray-700">` tag:

```html
<ul class="space-y-3">
    <li class="flex items-start">
        <i class="fas fa-check text-blue-900 mr-3 mt-1 flex-shrink-0"></i>
        <span class="text-gray-700">Your first benefit here</span>
    </li>
    <li class="flex items-start">
        <i class="fas fa-check text-blue-900 mr-3 mt-1 flex-shrink-0"></i>
        <span class="text-gray-700">Your second benefit here</span>
    </li>
    <li class="flex items-start">
        <i class="fas fa-check text-blue-900 mr-3 mt-1 flex-shrink-0"></i>
        <span class="text-gray-700">Your third benefit here</span>
    </li>
</ul>
```

#### 8. About Us Section

**Location:** Lines 266-300

**Current Code:**
```html
<h2 class="text-4xl md:text-5xl font-bold text-gray-900 mb-4 tracking-tight">About Pogiso Tours</h2>
<p class="text-xl text-gray-600">Learn more about our company and mission</p>
```

And the content boxes:
```html
<div class="bg-gradient-to-br from-blue-50 to-blue-100 rounded-xl p-8 md:p-12 border border-blue-200">
    <h3 class="text-2xl font-bold text-gray-900 mb-4">Our History</h3>
    <p class="text-lg text-gray-700 leading-relaxed">
        Pogiso Tours was founded over a decade ago with a simple vision...
    </p>
</div>
```

**How to Update:**
Replace the heading and paragraph text while keeping all the `class` attributes intact.

#### 9. Testimonials Section

**Location:** Lines 318-400

**Current Code Example (First Testimonial):**
```html
<div class="bg-white rounded-xl p-8 shadow-lg transition-all duration-300 hover:shadow-xl hover:scale-105">
    <div class="flex items-center mb-4">
        <div class="flex text-yellow-400">
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
        </div>
        <span class="ml-2 text-gray-600 font-semibold">(5.0)</span>
    </div>
    <p class="text-gray-700 leading-relaxed mb-6">
        "Pogiso Tours has been instrumental in streamlining our executive transportation needs..."
    </p>
    <div class="border-t border-gray-200 pt-4">
        <p class="font-bold text-gray-900">Sarah Mitchell</p>
        <p class="text-gray-600 text-sm">Director of Operations, Tech Innovations Inc.</p>
    </div>
</div>
```

**How to Update:**
1. Replace the testimonial text (between the quotation marks)
2. Replace "Sarah Mitchell" with the actual person's name
3. Replace "Director of Operations, Tech Innovations Inc." with their title and company

**To Change Star Rating:**
To show fewer stars (e.g., 4 stars instead of 5), remove one `<i class="fas fa-star"></i>` line:

```html
<!-- 4 stars instead of 5 -->
<div class="flex text-yellow-400">
    <i class="fas fa-star"></i>
    <i class="fas fa-star"></i>
    <i class="fas fa-star"></i>
    <i class="fas fa-star"></i>
</div>
<span class="ml-2 text-gray-600 font-semibold">(4.0)</span>
```

#### 10. FAQ Section

**Location:** Lines 412-476

**Current Code Example (First FAQ Item):**
```html
<div class="faq-item bg-white border-2 border-gray-200 rounded-xl overflow-hidden transition-all duration-300">
    <button class="faq-header w-full px-8 py-6 flex items-center justify-between hover:bg-blue-50 transition-colors duration-300 text-left" onclick="toggleFaq(this)">
        <h3 class="text-xl font-bold text-gray-900 flex items-center">
            <i class="fas fa-question-circle text-blue-900 mr-3"></i>
            How do I book a shuttle service?
        </h3>
        <i class="fas fa-chevron-down text-blue-900 transition-transform duration-300"></i>
    </button>
    <div class="faq-answer px-8 pb-6 bg-gray-50">
        <p class="text-gray-700 leading-relaxed">
            Booking with Pogiso Tours is simple and convenient. You can book through our online portal...
        </p>
    </div>
</div>
```

**How to Update:**

1. **Change the Question:** Replace "How do I book a shuttle service?" with your question
2. **Change the Answer:** Replace the paragraph text with your answer

**Example - Adding a New FAQ Item:**

Copy the entire `<div class="faq-item">` block and paste it after the last FAQ item, then modify:

```html
<div class="faq-item bg-white border-2 border-gray-200 rounded-xl overflow-hidden transition-all duration-300">
    <button class="faq-header w-full px-8 py-6 flex items-center justify-between hover:bg-blue-50 transition-colors duration-300 text-left" onclick="toggleFaq(this)">
        <h3 class="text-xl font-bold text-gray-900 flex items-center">
            <i class="fas fa-question-circle text-blue-900 mr-3"></i>
            Your New Question Here?
        </h3>
        <i class="fas fa-chevron-down text-blue-900 transition-transform duration-300"></i>
    </button>
    <div class="faq-answer px-8 pb-6 bg-gray-50">
        <p class="text-gray-700 leading-relaxed">
            Your answer to the question goes here. You can include multiple paragraphs if needed.
        </p>
    </div>
</div>
```

#### 11. Contact Section

**Location:** Lines 483-533

**Current Code:**
```html
<h2 class="text-4xl md:text-5xl font-bold text-gray-900 mb-4 tracking-tight">Get In Touch</h2>
<p class="text-xl text-gray-600 leading-relaxed">We're here to help with any questions or special requests</p>
```

**Email Contact:**
```html
<a href="mailto:info@pogisostours.co.za" class="text-blue-900 hover:underline text-lg font-semibold">
    info@pogisostours.co.za
</a>
```

**How to Update:**
Replace `info@pogisostours.co.za` with your actual email address:

```html
<a href="mailto:your-email@yourcompany.com" class="text-blue-900 hover:underline text-lg font-semibold">
    your-email@yourcompany.com
</a>
```

#### 12. Footer Section

**Location:** Lines 538-650

**Company Description:**
```html
<p class="text-gray-400 leading-relaxed mb-6">
    Your trusted partner for premium corporate shuttle and tour services nationwide. Safe, punctual, and professional transportation excellence.
</p>
```

**How to Update:**
Replace with your company description:

```html
<p class="text-gray-400 leading-relaxed mb-6">
    Your new company description goes here. Keep it concise and focus on your unique value proposition.
</p>
```

**Footer Copyright Year:**
The year is automatically updated by JavaScript at line 657:
```javascript
document.getElementById('year').textContent = new Date().getFullYear();
```

This automatically displays the current year, so you don't need to update it manually.

---

## Modifying Tailwind CSS Classes

### What is Tailwind CSS?

Tailwind CSS is a utility-first CSS framework. Instead of writing CSS in separate files, you apply styling directly in HTML using class names. Each class does one specific thing.

### Understanding Common Tailwind Classes Used in This Page

#### Text and Font Classes

| Class | What It Does | Example |
|-------|-------------|---------|
| `text-white` | Makes text white | |
| `text-gray-900` | Makes text dark gray | |
| `text-gray-600` | Makes text medium gray | |
| `text-blue-900` | Makes text dark blue | |
| `text-xl` | Makes text extra large | |
| `text-2xl` | Makes text 2x large | |
| `text-4xl` | Makes text 4x large | |
| `font-bold` | Makes text bold | |
| `font-semibold` | Makes text semi-bold | |
| `font-light` | Makes text lighter weight | |

#### Color Classes

Tailwind uses a consistent color system. The pattern is `[color]-[shade]`:

```
text-blue-900      (dark blue text)
text-blue-800      (slightly lighter blue text)
text-blue-100      (light blue text)
bg-blue-900        (dark blue background)
bg-white           (white background)
bg-gray-50         (very light gray background)
border-gray-200    (light gray border)
```

**To Change Colors:**

1. Find the class you want to change
2. Replace it with a different color from the Tailwind palette

**Current Example - Hero Section Background:**
```html
<div class="bg-gradient-to-r from-blue-900 to-blue-800 text-white py-3 px-4">
```

This creates a gradient from dark blue to slightly lighter blue. To change it to purple:
```html
<div class="bg-gradient-to-r from-purple-900 to-purple-800 text-white py-3 px-4">
```

#### Spacing Classes

Tailwind uses `p` for padding (space inside) and `m` for margin (space outside):

| Class | Space Amount |
|-------|--------------|
| `p-4` | Small padding |
| `p-8` | Medium padding |
| `p-12` | Large padding |
| `px-4` | Padding left and right only |
| `py-3` | Padding top and bottom only |
| `mb-6` | Bottom margin |
| `mt-1` | Top margin |
| `space-y-3` | Space between vertical items |

**Example - Increase Padding in Feature Cards:**

Current:
```html
<div class="bg-white border-2 border-gray-200 rounded-xl p-8 transition-all duration-300">
```

To increase padding:
```html
<div class="bg-white border-2 border-gray-200 rounded-xl p-12 transition-all duration-300">
```

#### Responsive Design Classes

Tailwind uses prefixes to make designs responsive:

| Prefix | Applies to | Example |
|--------|-----------|---------|
| (none) | Mobile (small screens) | `text-lg` |
| `md:` | Medium screens (tablets) | `md:text-2xl` |
| `lg:` | Large screens (desktops) | `lg:px-8` |

**Current Example - Hero Heading:**
```html
<h1 class="text-4xl md:text-6xl font-bold text-white">
```

This means:
- On mobile: `text-4xl` (large)
- On tablets and up: `md:text-6xl` (extra large)

**To Change Responsive Sizes:**
```html
<!-- Make mobile text larger -->
<h1 class="text-5xl md:text-6xl font-bold text-white">

<!-- Make desktop text smaller -->
<h1 class="text-4xl md:text-5xl font-bold text-white">
```

#### Hover Effects

Classes that start with `hover:` apply styling when you hover over an element:

```html
<a href="#" class="text-gray-700 hover:text-blue-900 transition-colors duration-300">
    Link Text
</a>
```

This means:
- Normal state: Gray text
- When you hover: Text turns blue
- `transition-colors duration-300`: Smooth animation over 300 milliseconds

**To Change Hover Color:**
```html
<!-- Change from blue to green on hover -->
<a href="#" class="text-gray-700 hover:text-green-900 transition-colors duration-300">
    Link Text
</a>
```

#### Border and Shadow Classes

| Class | Effect |
|-------|--------|
| `border-2` | 2px border |
| `border-gray-200` | Light gray border |
| `rounded-xl` | Rounded corners (extra large) |
| `shadow-lg` | Large drop shadow |
| `hover:shadow-xl` | Extra large shadow on hover |

**Example - Make Cards Have Thicker Borders:**

Current:
```html
<div class="bg-white border-2 border-gray-200 rounded-xl p-8">
```

With thicker border:
```html
<div class="bg-white border-4 border-gray-300 rounded-xl p-8">
```

#### Display and Layout Classes

| Class | Effect |
|-------|--------|
| `flex` | Display as flexbox |
| `grid` | Display as grid |
| `grid-cols-1` | 1 column on mobile |
| `md:grid-cols-2` | 2 columns on tablet |
| `lg:grid-cols-3` | 3 columns on desktop |
| `hidden` | Hide element |
| `md:hidden` | Hide on tablet and up |
| `md:flex` | Show as flex on tablet and up |

**Example - Feature Cards Grid:**

Current:
```html
<div class="grid grid-cols-1 md:grid-cols-3 gap-8">
```

This means:
- Mobile: 1 column
- Tablet and up: 3 columns
- `gap-8`: 8 units of space between items

To change to 2 columns on tablet:
```html
<div class="grid grid-cols-1 md:grid-cols-2 gap-8">
```

### Common Customizations with Tailwind

#### Change Primary Color Throughout Page

The page uses `blue-900` as the primary color. To change it to another color:

1. Find all instances of `text-blue-900`, `bg-blue-900`, `border-blue-900`, `hover:text-blue-900`
2. Replace with your chosen color (e.g., `text-green-900`, `bg-green-900`)

**Using Find and Replace:**
- Open your code editor
- Press `Ctrl+H` (Windows) or `Cmd+H` (Mac) to open Find and Replace
- Find: `blue-900`
- Replace: `green-900`
- Click "Replace All"

#### Increase Font Sizes

To make all text larger:
- Change `text-xl` to `text-2xl`
- Change `text-2xl` to `text-3xl`
- Change `text-4xl` to `text-5xl`

#### Add More Spacing

To increase padding/margins throughout:
- Change `p-8` to `p-12`
- Change `mb-6` to `mb-8`
- Change `py-3` to `py-4`

#### Make Borders More Prominent

Change `border-2` to `border-4` for thicker borders:
```html
<!-- Before -->
<div class="border-2 border-gray-200">

<!-- After -->
<div class="border-4 border-gray-300">
```

---

## Fixing and Managing Links

### Understanding Links in HTML

A link is created with the `<a>` tag. The `href` attribute tells the browser where to go:

```html
<a href="https://example.com">Click Here</a>
```

**Types of Links:**
- **External links**: Go to other websites (`href="https://..."`)
- **Internal links**: Go to other pages on your site (`href="page.html"`)
- **Anchor links**: Jump to a section on the same page (`href="#section-id"`)
- **Email links**: Open email client (`href="mailto:email@example.com"`)

### All Links in This Page

#### Navigation Links (Desktop Menu)

**Location:** Lines 70-77

```html
<a href="#home" class="text-gray-700 hover:text-blue-900 transition-colors duration-300 font-medium">Home</a>
<a href="#features" class="text-gray-700 hover:text-blue-900 transition-colors duration-300 font-medium">Features</a>
<a href="#benefits" class="text-gray-700 hover:text-blue-900 transition-colors duration-300 font-medium">Benefits</a>
<a href="#about" class="text-gray-700 hover:text-blue-900 transition-colors duration-300 font-medium">About</a>
<a href="#testimonials" class="text-gray-700 hover:text-blue-900 transition-colors duration-300 font-medium">Testimonials</a>
<a href="#faq" class="text-gray-700 hover:text-blue-900 transition-colors duration-300 font-medium">FAQ</a>
<a href="#contact" class="text-gray-700 hover:text-blue-900 transition-colors duration-300 font-medium">Contact</a>
```

**Status:** ✅ These links are correct and working. They use anchor links (`#section-id`) that jump to sections on the same page.

#### Navigation Links (Mobile Menu)

**Location:** Lines 88-97

Same as desktop menu. ✅ Working correctly.

#### Book Now Buttons

**Location:** Lines 79-82 (Desktop), Lines 99-101 (Mobile), Lines 127-129 (Hero Section), Lines 489-492 (CTA Section)

```html
<a href="https://www.pogisostours.co.za/booking/" class="bg-blue-900 text-white px-6 py-2 rounded-lg font-semibold hover:bg-blue-800 transition-colors duration-300 transform hover:scale-105 transition-transform">
    Book Now
</a>
```

**Status:** ⚠️ This links to an external booking website. **This URL needs to be verified and updated if necessary.**

**How to Update:**
Replace the entire URL:
```html
<!-- Current -->
<a href="https://www.pogisostours.co.za/booking/">

<!-- Updated to your booking system -->
<a href="https://yourbookingsystem.com/pogiso-tours">
```

#### Footer Quick Links

**Location:** Lines 570-583

```html
<a href="#home" class="text-gray-400 hover:text-white transition-colors duration-300">Home</a>
<a href="#features" class="text-gray-400 hover:text-white transition-colors duration-300">Features</a>
<a href="#benefits" class="text-gray-400 hover:text-white transition-colors duration-300">Benefits</a>
<a href="#about" class="text-gray-400 hover:text-white transition-colors duration-300">About Us</a>
<a href="#testimonials" class="text-gray-400 hover:text-white transition-colors duration-300">Testimonials</a>
<a href="#faq" class="text-gray-400 hover:text-white transition-colors duration-300">FAQ</a>
```

**Status:** ✅ These are anchor links and working correctly.

#### Footer Services Links

**Location:** Lines 594-605

```html
<a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Corporate Shuttles</a>
<a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Tour Services</a>
<a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Airport Transfers</a>
<a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Event Transportation</a>
<a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Executive Chauffeur</a>
<a href="blog.html" class="text-gray-400 hover:text-white transition-colors duration-300">Blog</a>
```

**Status:** ⚠️ **PROBLEM DETECTED**: Most of these links use `href="#"` which means they don't go anywhere.

**How to Fix:**

Option 1: Link to service pages (if you have them):
```html
<a href="corporate-shuttles.html" class="text-gray-400 hover:text-white transition-colors duration-300">Corporate Shuttles</a>
<a href="tour-services.html" class="text-gray-400 hover:text-white transition-colors duration-300">Tour Services</a>
<a href="airport-transfers.html" class="text-gray-400 hover:text-white transition-colors duration-300">Airport Transfers</a>
```

Option 2: Link to external URLs:
```html
<a href="https://yourwebsite.com/corporate-shuttles" class="text-gray-400 hover:text-white transition-colors duration-300">Corporate Shuttles</a>
```

Option 3: Remove links that don't go anywhere:
```html
<span class="text-gray-400">Corporate Shuttles</span>
```

#### Email Contact Link

**Location:** Lines 615-617

```html
<a href="mailto:info@pogisostours.co.za" class="text-blue-900 hover:underline text-lg font-semibold">
    info@pogisostours.co.za
</a>
```

**How to Update:**
Replace the email address in both the `href` and the displayed text:

```html
<a href="mailto:your-email@yourcompany.com" class="text-blue-900 hover:underline text-lg font-semibold">
    your-email@yourcompany.com
</a>
```

#### Footer Contact Email (Repeated)

**Location:** Lines 627-630

```html
<li class="flex items-start">
    <i class="fas fa-envelope text-blue-400 mr-3 mt-1 flex-shrink-0"></i>
    <a href="mailto:info@pogisostours.co.za" class="text-gray-400 hover:text-white transition-colors duration-300">
        info@pogisostours.co.za
    </a>
</li>
```

**How to Update:**
Same as above - replace the email address:

```html
<a href="mailto:your-email@yourcompany.com" class="text-gray-400 hover:text-white transition-colors duration-300">
    your-email@yourcompany.com
</a>
```

#### Policy Links in Footer

**Location:** Lines 649-653

```html
<a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a>
<a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a>
<a href="blog.html" class="text-gray-400 hover:text-white transition-colors duration-300">Blog</a>
```

**Status:** ⚠️ These files don't exist yet and need to be created.

### Complete Link Audit Checklist

Use this checklist to verify all links:

- [ ] All `#home`, `#features`, `#benefits`, etc. anchor links work (they should jump to sections)
- [ ] "Book Now" buttons link to your actual booking system
- [ ] Email links use your actual email address
- [ ] Service links either go to service pages or are removed
- [ ] Footer policy links (`privacy.html`, `terms.html`, `blog.html`) either exist or are updated
- [ ] No links have `href="#"` unless they're intentionally disabled

---

## Linking Privacy and Terms Pages

### Step-by-Step Guide to Create and Link Policy Pages

#### Step 1: Create the Privacy Policy Page

1. In your project folder, create a new file called `privacy.html`
2. Copy and paste this basic template:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy - Pogiso Tours">
    <title>Privacy Policy | Pogiso Tours</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
</head>
<body class="bg-white text-gray-900 font-sans">
    <!-- Header Navigation (Copy from index.html) -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
            <div class="flex items-center space-x-2">
                <i class="fas fa-shuttle-van text-blue-900 text-3xl"></i>
                <span class="text-xl md:text-2xl font-bold text-blue-900">Pogiso Tours</span>
            </div>
            <div class="hidden md:flex items-center space-x-8">
                <a href="index.html#home" class="text-gray-700 hover:text-blue-900 transition-colors duration-300 font-medium">Home</a>
                <a href="index.html#features" class="text-gray-700 hover:text-blue-900 transition-colors duration-300 font-medium">Features</a>
                <a href="index.html#contact" class="text-gray-700 hover:text-blue-900 transition-colors duration-300 font-medium">Contact</a>
            </div>
            <div class="hidden md:block">
                <a href="https://www.pogisostours.co.za/booking/" class="bg-blue-900 text-white px-6 py-2 rounded-lg font-semibold hover:bg-blue-800 transition-colors duration-300">
                    Book Now
                </a>
            </div>
        </nav>
    </header>

    <!-- Main Content -->
    <section class="py-24 bg-white">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8">Privacy Policy</h1>
            
            <div class="prose prose-lg max-w-none">
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">1. Introduction</h2>
                <p class="text-gray-700 leading-relaxed mb-6">
                    Pogiso Tours ("we," "us," or "our") operates the website. This page informs you of our policies regarding the collection, use, and disclosure of personal data when you use our service and the choices you have associated with that data.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">2. Information Collection and Use</h2>
                <p class="text-gray-700 leading-relaxed mb-6">
                    We collect several different types of information for various purposes to provide and improve our service to you.
                </p>
                <ul class="list-disc list-inside space-y-3 mb-6 text-gray-700">
                    <li>Personal Data: Name, email address, phone number, booking information</li>
                    <li>Usage Data: Browser type, IP address, pages visited, time and date of visit</li>
                    <li>Cookies and Tracking: We use cookies to track activity on our service</li>
                </ul>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">3. Use of Data</h2>
                <p class="text-gray-700 leading-relaxed mb-6">
                    Pogiso Tours uses the collected data for various purposes:
                </p>
                <ul class="list-disc list-inside space-y-3 mb-6 text-gray-700">
                    <li>To provide and maintain our service</li>
                    <li>To notify you about changes to our service</li>
                    <li>To allow you to participate in interactive features of our service</li>
                    <li>To provide customer support</li>
                    <li>To gather analysis or valuable information so we can improve our service</li>
                    <li>To monitor the usage of our service</li>
                    <li>To detect, prevent and address technical issues</li>
                </ul>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">4. Security of Data</h2>
                <p class="text-gray-700 leading-relaxed mb-6">
                    The security of your data is important to us, but remember that no method of transmission over the Internet or method of electronic storage is 100% secure. While we strive to use commercially acceptable means to protect your Personal Data, we cannot guarantee its absolute security.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">5. Contact Us</h2>
                <p class="text-gray-700 leading-relaxed">
                    If you have any questions about this Privacy Policy, please contact us at:
                </p>
                <p class="text-gray-700 leading-relaxed mt-4">
                    Email: <a href="mailto:info@pogisostours.co.za" class="text-blue-900 hover:underline">info@pogisostours.co.za</a>
                </p>
            </div>
        </div>
    </section>

    <!-- Footer (Copy from index.html) -->
    <footer class="bg-gray-900 text-gray-300 py-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center">
                <p class="text-gray-400 mb-4">
                    &copy; <span id="year"></span> Pogiso Tours. All rights reserved.
                </p>
                <div class="flex space-x-6 justify-center">
                    <a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a>
                    <a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a>
                </div>
            </div>
        </div>
    </footer>

    <script>
        document.getElementById('year').textContent = new Date().getFullYear();
    </script>
</body>
</html>
```

#### Step 2: Create the Terms of Service Page

1. In your project folder, create a new file called `terms.html`
2. Copy and paste this basic template:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service - Pogiso Tours">
    <title>Terms of Service | Pogiso Tours</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
</head>
<body class="bg-white text-gray-900 font-sans">
    <!-- Header Navigation -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
            <div class="flex items-center space-x-2">
                <i class="fas fa-shuttle-van text-blue-900 text-3xl"></i>
                <span class="text-xl md:text-2xl font-bold text-blue-900">Pogiso Tours</span>
            </div>
            <div class="hidden md:flex items-center space-x-8">
                <a href="index.html#home" class="text-gray-700 hover:text-blue-900 transition-colors duration-300 font-medium">Home</a>
                <a href="index.html#features" class="text-gray-700 hover:text-blue-900 transition-colors duration-300 font-medium">Features</a>
                <a href="index.html#contact" class="text-gray-700 hover:text-blue-900 transition-colors duration-300 font-medium">Contact</a>
            </div>
            <div class="hidden md:block">
                <a href="https://www.pogisostours.co.za/booking/" class="bg-blue-900 text-white px-6 py-2 rounded-lg font-semibold hover:bg-blue-800 transition-colors duration-300">
                    Book Now
                </a>
            </div>
        </nav>
    </header>

    <!-- Main Content -->
    <section class="py-24 bg-white">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8">Terms of Service</h1>
            
            <div class="prose prose-lg max-w-none">
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">1. Agreement to Terms</h2>
                <p class="text-gray-700 leading-relaxed mb-6">
                    By accessing and using this website and our services, you accept and agree to be bound by the terms and provision of this agreement. If you do not agree to abide by the above, please do not use this service.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">2. Use License</h2>
                <p class="text-gray-700 leading-relaxed mb-6">
                    Permission is granted to temporarily download one copy of the materials (information or software) on Pogiso Tours' website for personal, non-commercial transitory viewing only. This is the grant of a license, not a transfer of title, and under this license you may not:
                </p>
                <ul class="list-disc list-inside space-y-3 mb-6 text-gray-700">
                    <li>Modifying or copying the materials</li>
                    <li>Using the materials for any commercial purpose or for any public display</li>
                    <li>Attempting to decompile or reverse engineer any software contained on the website</li>
                    <li>Removing any copyright or other proprietary notations from the materials</li>
                    <li>Transferring the materials to another person or "mirroring" the materials on any other server</li>
                </ul>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">3. Booking and Cancellation Policy</h2>
                <p class="text-gray-700 leading-relaxed mb-6">
                    Bookings made through our service are subject to our cancellation and modification policy:
                </p>
                <ul class="list-disc list-inside space-y-3 mb-6 text-gray-700">
                    <li>Cancellations made 24 hours or more in advance receive a full refund</li>
                    <li>Cancellations within 24 hours are subject to a 50% charge</li>
                    <li>Modifications can be made free of charge up to 12 hours before pickup</li>
                </ul>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">4. Limitation of Liability</h2>
                <p class="text-gray-700 leading-relaxed mb-6">
                    In no event shall Pogiso Tours or its suppliers be liable for any damages (including, without limitation, damages for loss of data or profit, or due to business interruption) arising out of the use or inability to use the materials on the website, even if we or an authorized representative has been notified orally or in writing of the possibility of such damage.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">5. Accuracy of Materials</h2>
                <p class="text-gray-700 leading-relaxed mb-6">
                    The materials appearing on the website could include technical, typographical, or photographic errors. Pogiso Tours does not warrant that any of the materials on its website are accurate, complete, or current. Pogiso Tours may make changes to the materials contained on its website at any time without notice.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">6. Contact Us</h2>
                <p class="text-gray-700 leading-relaxed">
                    If you have any questions about these Terms of Service, please contact us at:
                </p>
                <p class="text-gray-700 leading-relaxed mt-4">
                    Email: <a href="mailto:info@pogisostours.co.za" class="text-blue-900 hover:underline">info@pogisostours.co.za</a>
                </p>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 py-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center">
                <p class="text-gray-400 mb-4">
                    &copy; <span id="year"></span> Pogiso Tours. All rights reserved.
                </p>
                <div class="flex space-x-6 justify-center">
                    <a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a>
                    <a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a>
                </div>
            </div>
        </div>
    </footer>

    <script>
        document.getElementById('year').textContent = new Date().getFullYear();
    </script>
</body>
</html>
```

#### Step 3: Create the Blog Page

1. In your project folder, create a new file called `blog.html`
2. Use this template:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Blog - Pogiso Tours">
    <title>Blog | Pogiso Tours</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
</head>
<body class="bg-white text-gray-900 font-sans">
    <!-- Header Navigation -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
            <div class="flex items-center space-x-2">
                <i class="fas fa-shuttle-van text-blue-900 text-3xl"></i>
                <span class="text-xl md:text-2xl font-bold text-blue-900">Pogiso Tours</span>
            </div>
            <div class="hidden md:flex items-center space-x-8">
                <a href="index.html#home" class="text-gray-700 hover:text-blue-900 transition-colors duration-300 font-medium">Home</a>
                <a href="index.html#features" class="text-gray-700 hover:text-blue-900 transition-colors duration-300 font-medium">Features</a>
                <a href="index.html#contact" class="text-gray-700 hover:text-blue-900 transition-colors duration-300 font-medium">Contact</a>
            </div>
            <div class="hidden md:block">
                <a href="https://www.pogisostours.co.za/booking/" class="bg-blue-900 text-white px-6 py-2 rounded-lg font-semibold hover:bg-blue-800 transition-colors duration-300">
                    Book Now
                </a>
            </div>
        </nav>
    </header>

    <!-- Main Content -->
    <section class="py-24 bg-white">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8">Our Blog</h1>
            
            <div class="text-center py-12">
                <p class="text-xl text-gray-600">Blog posts coming soon. Check back for updates on corporate transportation tips and industry insights.</p>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 py-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center">
                <p class="text-gray-400 mb-4">
                    &copy; <span id="year"></span> Pogiso Tours. All rights reserved.
                </p>
                <div class="flex space-x-6 justify-center">
                    <a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a>
                    <a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a>
                </div>
            </div>
        </div>
    </footer>

    <script>
        document.getElementById('year').textContent = new Date().getFullYear();
    </script>
</body>
</html>
```

#### Step 4: Verify Links in index.html

The links in `index.html` should already be correct:

**Location:** Lines 649-653

```html
<a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a>
<a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a>
<a href="blog.html" class="text-gray-400 hover:text-white transition-colors duration-300">Blog</a>
```

These links are already set up correctly and will work once you create the files.

### File Structure After Setup

```
project-root/
├── index.html          ✅ Main landing page
├── privacy.html        ✅ Privacy Policy page
├── terms.html          ✅ Terms of Service page
├── blog.html           ✅ Blog page
└── css/
    └── custom.css      (Optional)
```

### Testing the Links

1. Save all files in the same folder
2. Open `index.html` in your browser
3. Click the "Privacy Policy" link in the footer
4. You should be taken to `privacy.html`
5. Click "Terms of Service" - you should be taken to `terms.html`
6. Click "Blog" - you should be taken to `blog.html`
7. From any policy page, click the Pogiso Tours logo to return to the home page

### Customizing Policy Content

Once you create the policy pages, you can customize them:

**In `privacy.html`:**
- Replace "Pogiso Tours" with your company name
- Update the email address to your contact email
- Add your specific privacy practices
- Add information about how you collect and use customer data

**In `terms.html`:**
- Update company name and contact information
- Modify cancellation policies to match your actual policy
- Add any specific terms relevant to your business
- Include liability disclaimers specific to your services

---

## Common Customizations

### Change Company Name Throughout the Page

This requires updating multiple locations:

1. **Logo/Header** (Line 67):
```html
<span class="text-xl md:text-2xl font-bold text-blue-900">Your Company Name</span>
```

2. **Page Title** (Line 16):
```html
<title>Corporate Shuttle & Tour Experts Nationwide | Your Company Name</title>
```

3. **Meta Description** (Line 14):
```html
<meta name="description" content="Your service description - Your Company Name">
```

4. **OG Title** (Line 18):
```html
<meta property="og:title" content="Your Headline | Your Company Name">
```

5. **Footer** (Line 540):
```html
<span class="text-xl font-bold text-white">Your Company Name</span>
```

6. **Footer Copyright** (Line 648):
```html
&copy; <span id="year"></span> Your Company Name. All rights reserved.
```

7. **All policy pages** - Same locations as above

### Change Primary Color from Blue to Another Color

**Find and Replace Method:**

1. Open the file in your code editor
2. Press `Ctrl+H` (Windows) or `Cmd+H` (Mac)
3. Find: `blue-900`
4. Replace: `green-900` (or your chosen color)
5. Click "Replace All"

**Then repeat for other blue shades:**
- Find `blue-800` → Replace with `green-800`
- Find `blue-100` → Replace with `green-100`
- Find `blue-50` → Replace with `green-50`
- Find `blue-400` → Replace with `green-400`

### Add a New Feature Card

1. Find the Features section (Line 136)
2. Find the last feature card (Nationwide Service)
3. Copy the entire `<div class="bg-white border-2...">` block
4. Paste it after the last card
5. Update the icon, title, and description:

```html
<!-- New Feature Card -->
<div class="bg-white border-2 border-gray-200 rounded-xl p-8 transition-all duration-300 hover:shadow-xl hover:scale-105 hover:border-blue-900 cursor-pointer">
    <div class="bg-blue-100 w-16 h-16 rounded-full flex items-center justify-center mb-6 mx-auto">
        <i class="fas fa-award text-3xl text-blue-900"></i>  <!-- Change icon -->
    </div>
    <h3 class="text-2xl font-bold text-gray-900 mb-3 text-center">Your Feature Title</h3>
    <p class="text-gray-600 leading-relaxed text-center">
        Your feature description goes here. Explain the benefit clearly and concisely.
    </p>
</div>
```

**Important:** If you add a 4th feature card, the grid will wrap to 2 columns on some screens. To keep 3 columns, you may need to adjust the grid class.

### Add a New Testimonial

1. Find the Testimonials section (Line 318)
2. Find the last testimonial card
3. Copy the entire testimonial `<div>` block
4. Paste it after the last testimonial
5. Update the stars, quote, name, and title:

```html
<!-- New Testimonial -->
<div class="bg-white rounded-xl p-8 shadow-lg transition-all duration-300 hover:shadow-xl hover:scale-105">
    <div class="flex items-center mb-4">
        <div class="flex text-yellow-400">
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
        </div>
        <span class="ml-2 text-gray-600 font-semibold">(5.0)</span>
    </div>
    <p class="text-gray-700 leading-relaxed mb-6">
        "Your testimonial quote goes here. Make it authentic and specific to your service."
    </p>
    <div class="border-t border-gray-200 pt-4">
        <p class="font-bold text-gray-900">Person's Name</p>
        <p class="text-gray-600 text-sm">Job Title, Company Name</p>
    </div>
</div>
```

### Update Contact Form Action

The contact form (Lines 519-533) currently doesn't send anywhere. To make it functional:

**Option 1: Use Formspree (Recommended for beginners)**

1. Go to [formspree.io](https://formspree.io)
2. Sign up for a free account
3. Create a new form and get your form ID
4. Update the form tag:

```html
<!-- Before -->
<form class="space-y-4">

<!-- After -->
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST" class="space-y-4">
```

Replace `YOUR_FORM_ID` with the ID from Formspree.

**Option 2: Use a Backend Service**

If you have a backend/server, update the form to point to your endpoint:

```html
<form action="https://yourserver.com/send-email" method="POST" class="space-y-4">
```

### Change Hero Background Image

The hero image is located at Line 110:

```html
<img src="https://images.unsplash.com/photo-1504093376055-b3094b674dcb?w=1600&h=900&fit=crop&q=80" alt="Corporate Shuttle Service" class="w-full h-full object-cover">
```

**To change it:**

1. Find a new image URL (from Unsplash, Pexels, etc.)
2. Replace the entire URL:

```html
<img src="https://images.unsplash.com/photo-YOUR-NEW-IMAGE-ID?w=1600&h=900&fit=crop&q=80" alt="Corporate Shuttle Service" class="w-full h-full object-cover">
```

### Change Benefit Section Images

There are three benefit section images at:
- Line 218 (Cost-Effective image)
- Line 232 (Professional Chauffeurs image)
- Line 258 (Reliable Nationwide image)

Update them the same way as the hero image.

### Adjust Mobile Menu Behavior

The mobile menu is controlled by JavaScript (Line 656):

```javascript
document.querySelector('.mobile-menu-button').addEventListener('click', function() {
    document.querySelector('.mobile-menu').classList.toggle('hidden');
});
```

This is already set up and working. No changes needed unless you want to modify the behavior.

---

## Troubleshooting

### Common Issues and Solutions

#### Links Not Working

**Problem:** Clicking a link doesn't go anywhere

**Solutions:**
1. Check if the `href` attribute is correct
2. Make sure the file path is correct (e.g., `privacy.html` not `privacy.html.html`)
3. Verify the file exists in the same folder
4. For external links, ensure the full URL is used (e.g., `https://example.com`)

**Debug:** Right-click the link → "Inspect" → Check the `href` value

#### Styling Looks Broken

**Problem:** Colors, spacing, or layout looks wrong

**Solutions:**
1. Check that you didn't accidentally delete a `class` attribute
2. Verify Tailwind CSS CDN is still loading (Line 12):
```html
<script src="https://cdn.tailwindcss.com"></script>
```
3. Clear your browser cache (Ctrl+Shift+Delete)
4. Try opening in a different browser

#### Text Isn't Updating

**Problem:** You changed text in the HTML but it's not showing on the page

**Solutions:**
1. Save the file (Ctrl+S or Cmd+S)
2. Refresh the browser (F5 or Cmd+R)
3. Do a hard refresh to clear cache (Ctrl+Shift+R)
4. Check you edited the correct file

#### Mobile Menu Not Working

**Problem:** Hamburger menu doesn't open on mobile

**Solutions:**
1. Check JavaScript is enabled in your browser
2. Verify the script section (Lines 656-680) is intact
3. Open browser console (F12) and check for JavaScript errors
4. Test on actual mobile device (not just browser resize)

#### Icons Not Showing

**Problem:** Font Awesome icons appear as boxes or don't display

**Solutions:**
1. Check Font Awesome CDN is loading (Line 13):
```html
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
```
2. Verify icon class is correct (e.g., `fas fa-car` not `fas fa-cars`)
3. Clear browser cache
4. Check [Font Awesome documentation](https://fontawesome.com/icons) for correct icon names

#### Responsive Design Not Working

**Problem:** Page doesn't look good on mobile

**Solutions:**
1. Check viewport meta tag is present (Line 11):
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```
2. Test on actual mobile device
3. Use browser DevTools (F12) → Toggle device toolbar
4. Check that Tailwind responsive classes are correct (e.g., `md:`, `lg:`)

#### Form Not Submitting

**Problem:** Contact form doesn't send emails

**Solutions:**
1. Check if form action is set up (see "Update Contact Form Action" above)
2. Verify all required fields have `required` attribute
3. Check browser console for errors
4. Test with Formspree or another form service

---

## Best Practices

### Code Organization

1. **Keep related elements together** - Don't scatter sections around
2. **Maintain consistent indentation** - Use 4 spaces or 1 tab per level
3. **Use meaningful comments** - Add `<!-- Section Name -->` comments for major sections
4. **Back up your work** - Save copies before major changes

### Maintenance Tips

1. **Test after every change** - Refresh browser and verify nothing broke
2. **Use version control** - Use Git to track changes
3. **Keep a changelog** - Document what you changed and when
4. **Test on multiple devices** - Check mobile, tablet, and desktop
5. **Test different browsers** - Check Chrome, Firefox, Safari, Edge

### SEO Best Practices

1. **Update meta tags** (Lines 14-20):
   - `meta name="description"` - Appears in search results
   - `og:title` and `og:description` - For social sharing

2. **Use descriptive alt text** for all images:
```html
<!-- Good -->
<img src="image.jpg" alt="Professional chauffeur in uniform">

<!-- Bad -->
<img src="image.jpg" alt="image">
```

3. **Use proper heading hierarchy** - Don't skip from `<h1>` to `<h3>`

4. **Include relevant keywords** in headings and descriptions

### Performance Tips

1. **Optimize images** - Use compressed images to reduce file size
2. **Minimize redirects** - Use direct links when possible
3. **Lazy load images** - Add `loading="lazy"` for images below the fold
4. **Minimize external requests** - Only load necessary libraries

### Security Tips

1. **Validate form inputs** - Check data before sending to server
2. **Use HTTPS** - Ensure booking link uses `https://`
3. **Keep dependencies updated** - Tailwind and Font Awesome should be current
4. **Sanitize user data** - Never display user input without validation

### Accessibility Tips

1. **Use descriptive link text** - Avoid "click here"
2. **Include alt text** for all images
3. **Use semantic HTML** - Use `<button>` for buttons, `<nav>` for navigation
4. **Ensure color contrast** - Text should be readable
5. **Make forms accessible** - Use `<label>` tags for form inputs

### Code Quality Checklist

Before deploying, verify:

- [ ] All links work (internal and external)
- [ ] All images load correctly
- [ ] Mobile menu opens and closes
- [ ] FAQ accordion expands and collapses
- [ ] Contact form submits (or shows error)
- [ ] Page loads quickly
- [ ] No JavaScript errors in console
- [ ] Looks good on mobile, tablet, desktop
- [ ] All text is correct and up-to-date
- [ ] Colors are consistent with brand
- [ ] No broken images or icons
- [ ] Footer links work
- [ ] Header navigation works
- [ ] CTA buttons go to correct URL
- [ ] Email links work
- [ ] Social media links (if present) work

---

## Additional Resources

### Learning Resources

- [HTML Basics](https://developer.mozilla.org/en-US/docs/Web/HTML)
- [CSS Basics](https://developer.mozilla.org/en-US/docs/Web/CSS)
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [Font Awesome Icons](https://fontawesome.com/icons)
- [Web Accessibility Guidelines](https://www.w3.org/WAI/)

### Tools

- [Code Editor: VS Code](https://code.visualstudio.com/)
- [Browser DevTools](https://developer.chrome.com/docs/devtools/)
- [Image Optimizer: TinyPNG](https://tinypng.com/)
- [Color Picker: Coolors](https://coolors.co/)
- [Responsive Tester: Responsively App](https://responsively.app/)

### Getting Help

If you encounter issues:

1. Check the [Troubleshooting](#troubleshooting) section above
2. Open browser console (F12) and look for error messages
3. Use [Stack Overflow](https://stackoverflow.com/) to search for solutions
4. Check [Tailwind documentation](https://tailwindcss.com/) for CSS issues
5. Consult [MDN Web Docs](https://developer.mozilla.org/) for HTML/CSS questions

---

## Support and Questions

This landing page is designed to be maintainable and customizable. If you have questions about specific sections or need clarification on any instructions, refer back to the relevant section in this guide.

For technical support with Tailwind CSS or general web development questions, consult the official documentation linked in the Additional Resources section.

---

**Document Version:** 1.0  
**Last Updated:** 2024  
**Page Type:** Landing Page  
**Built With:** HTML5, Tailwind CSS, Font Awesome, Vanilla JavaScript