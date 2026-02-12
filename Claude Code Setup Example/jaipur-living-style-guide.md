# Jaipur Living Design System & Brand Voice
## LLM Context Document for Web Design Consistency

**Purpose:** This document provides comprehensive design specifications for Claude or any LLM to create web pages, components, and marketing materials that precisely match the Jaipur Living brand aesthetic.

**Last Updated:** January 2026
**Source:** Live website analysis (www.jaipurliving.com) + Figma Design System

---

## Table of Contents
1. [Brand Overview](#brand-overview)
2. [Typography System](#typography-system)
3. [Color Palette](#color-palette)
4. [Spacing & Layout](#spacing--layout)
5. [Component Library](#component-library)
6. [Brand Voice & Messaging](#brand-voice--messaging)
7. [Photography & Image Guidelines](#photography--image-guidelines)
8. [Code Implementation Examples](#code-implementation-examples)
9. [Anti-Patterns to Avoid](#anti-patterns-to-avoid)

---

## Brand Overview

### Brand Positioning
Jaipur Living is a **luxury handmade rug and home decor** company specializing in artisan-crafted rugs from India. The brand positions itself at the intersection of:
- **Artisanal Craftsmanship** - Handmade quality, traditional techniques
- **Modern Luxury** - Contemporary aesthetics, elevated design
- **Sustainability** - Ethical production, natural materials
- **Accessibility** - Bringing designer-quality pieces to discerning consumers

### Design Philosophy
The visual identity embodies **"refined minimalism"** - a design approach characterized by:
- **Restraint over excess** - Generous whitespace, limited color palette
- **Typography as hero** - Light weights, elegant letter-spacing
- **Product-forward** - Design recedes to let products shine
- **Warmth within minimalism** - Soft backgrounds, inviting neutrals

### Target Aesthetic Keywords
When generating designs, aim for: `elegant`, `refined`, `artisanal`, `warm minimalist`, `sophisticated`, `understated luxury`, `timeless`, `curated`

---

## Typography System

### Primary Font Family: Inter (Google Web Font)

**IMPORTANT:** The site has migrated from Helvetica to Inter. All typography must use Inter font variants. Never reference Helvetica.

```css
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap');

font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
```

### Type Scale

| Element | Size | Weight | Line Height | Letter Spacing | Transform |
|---------|------|--------|-------------|----------------|-----------|
| H1 (Hero) | 36px | 300 (Light) | 38px (1.06) | -0.72px | None |
| H2 (Section) | 28px | 300 (Light) | 32px (1.14) | -0.56px | None |
| H3 (Subsection) | 22px | 400 (Regular) | 28px (1.27) | -0.44px | None |
| H4 (Card Title) | 18px | 500 (Medium) | 24px (1.33) | -0.36px | None |
| Body Large | 16px | 400 (Regular) | 26px (1.63) | 0 | None |
| Body | 14px | 400 (Regular) | 22px (1.57) | 0 | None |
| Body Small | 12px | 400 (Regular) | 18px (1.5) | 0 | None |
| Label/Badge | 10px | 500 (Medium) | 14px (1.4) | 2px | Uppercase |
| Caption | 11px | 400 (Regular) | 16px (1.45) | 0.5px | None |
| Button | 12px | 500 (Medium) | 16px (1.33) | 1.5px | Uppercase |

### Typography CSS Variables

```css
:root {
  /* Font Family */
  --font-primary: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;

  /* Font Sizes */
  --text-xs: 10px;
  --text-sm: 12px;
  --text-base: 14px;
  --text-lg: 16px;
  --text-xl: 18px;
  --text-2xl: 22px;
  --text-3xl: 28px;
  --text-4xl: 36px;

  /* Font Weights */
  --font-light: 300;
  --font-regular: 400;
  --font-medium: 500;
  --font-semibold: 600;
  --font-bold: 700;

  /* Letter Spacing */
  --tracking-tight: -0.02em;
  --tracking-normal: 0;
  --tracking-wide: 0.1em;
  --tracking-wider: 0.15em;
}
```

### Typography Guidelines

1. **Headers use light weight (300)** - Creates elegant, airy feel
2. **Body uses regular weight (400)** - Ensures readability
3. **Labels are ALWAYS uppercase** - With generous letter-spacing (2px)
4. **Negative letter-spacing for large text** - Tightens headlines
5. **Positive letter-spacing for small text** - Improves legibility
6. **Line heights are generous** - 1.5+ for body text

---

## Color Palette

### Primary Colors

| Name | Hex | RGB | Usage |
|------|-----|-----|-------|
| Charcoal | `#393939` | rgb(57, 57, 57) | Primary text, headers |
| Off-White | `#f6f5f4` | rgb(246, 245, 244) | Page backgrounds |
| Pure White | `#ffffff` | rgb(255, 255, 255) | Cards, overlays, contrast areas |
| Dark | `#282828` | rgb(40, 40, 40) | Footer, dark sections |
| Near Black | `#1f1e1e` | rgb(31, 30, 30) | Hover states, emphasis |

### Neutral Palette

| Name | Hex | Usage |
|------|-----|-------|
| Gray 100 | `#f6f5f4` | Backgrounds |
| Gray 200 | `#e8e6e3` | Subtle backgrounds |
| Gray 300 | `#ddd8d0` | Borders, dividers |
| Gray 400 | `#d8d6cf` | Accent backgrounds |
| Gray 500 | `#b5b3ae` | Disabled text |
| Gray 600 | `#8a8885` | Secondary text |
| Gray 700 | `#5c5a57` | Body text alternate |
| Gray 800 | `#393939` | Primary text |
| Gray 900 | `#1f1e1e` | Headlines, emphasis |

### Accent Colors (Use Sparingly)

| Name | Hex | Usage |
|------|-----|-------|
| Error Red | `#ff0101` | Error messages, alerts |
| Success Green | `#2d7d46` | Success states |
| Link Blue | `#2563eb` | Text links (rare) |

### Color CSS Variables

```css
:root {
  /* Primary */
  --color-text-primary: #393939;
  --color-text-secondary: #5c5a57;
  --color-text-muted: #8a8885;
  --color-text-disabled: #b5b3ae;

  /* Backgrounds */
  --color-bg-primary: #f6f5f4;
  --color-bg-secondary: #e8e6e3;
  --color-bg-card: #ffffff;
  --color-bg-dark: #282828;
  --color-bg-darker: #1f1e1e;

  /* Borders */
  --color-border-light: #ddd;
  --color-border-medium: #d8d6cf;
  --color-border-dark: #b5b3ae;

  /* Interactive */
  --color-hover: #ddd8d0;
  --color-active: #1f1e1e;

  /* Status */
  --color-error: #ff0101;
  --color-success: #2d7d46;
}
```

### Color Usage Guidelines

1. **Minimal color palette** - Rely on neutrals; color is an accent
2. **Warm neutrals preferred** - Use warm grays (#f6f5f4) over cool grays
3. **High contrast for text** - #393939 on #f6f5f4 maintains readability
4. **No gradients** - Flat colors only
5. **Borders are subtle** - Use #ddd or lighter
6. **Dark mode sparingly** - Only for footer and special sections

---

## Spacing & Layout

### Spacing Scale

```css
:root {
  --space-1: 4px;
  --space-2: 8px;
  --space-3: 12px;
  --space-4: 16px;
  --space-5: 20px;
  --space-6: 24px;
  --space-8: 32px;
  --space-10: 40px;
  --space-12: 48px;
  --space-16: 64px;
  --space-20: 80px;
  --space-24: 96px;
}
```

### Container Widths

| Size | Width | Usage |
|------|-------|-------|
| Small | 640px | Single-column content |
| Medium | 960px | Blog posts, about pages |
| Large | 1200px | Product grids, main content |
| Full | 1440px | Hero sections, max width |

### Grid System

```css
/* Product Grid */
.product-grid {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
}

.product-card {
  flex: 1 0 254px;
  max-width: 254px;
  padding: 5px;
}

/* Responsive Breakpoints */
--breakpoint-sm: 576px;
--breakpoint-md: 768px;
--breakpoint-lg: 992px;
--breakpoint-xl: 1200px;
--breakpoint-xxl: 1440px;
```

### Layout Patterns

1. **Header Height:** 72px (fixed/sticky)
2. **Sidebar Width:** Variable, sticky at `top: 70px`
3. **Content Padding:** 16px-20px standard
4. **Section Spacing:** 64px-96px between major sections
5. **Card Padding:** 16px-24px internal padding
6. **Product Image Max Width:** 248px

---

## Component Library

### Buttons

#### Primary Button
```css
.btn-primary {
  background-color: transparent;
  color: #393939;
  border: 1px solid #393939;
  padding: 12px 24px;
  font-family: 'Inter', sans-serif;
  font-size: 12px;
  font-weight: 500;
  letter-spacing: 1.5px;
  text-transform: uppercase;
  cursor: pointer;
  transition: all 0.2s ease;
}

.btn-primary:hover {
  background-color: #393939;
  color: #ffffff;
}
```

#### Secondary Button
```css
.btn-secondary {
  background-color: #ffffff;
  color: #393939;
  border: 1px solid #ddd;
  padding: 10px 20px;
  font-family: 'Inter', sans-serif;
  font-size: 12px;
  font-weight: 500;
  letter-spacing: 1.5px;
  text-transform: uppercase;
  cursor: pointer;
  transition: all 0.2s ease;
}

.btn-secondary:hover {
  border-color: #393939;
}
```

#### Button Guidelines
- **No shadows or depth effects** - Flat design only
- **Rectangular shape** - No rounded corners (or minimal: 2px max)
- **Uppercase text** - Always with letter-spacing
- **Transparent backgrounds preferred** - Border-only aesthetic
- **Subtle hover transitions** - Color changes, not transforms

### Navigation

#### Header
```css
.header {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  height: 72px;
  background-color: #ffffff;
  border-bottom: 1px solid #ddd;
  z-index: 50;
  display: flex;
  align-items: center;
  padding: 0 20px;
}
```

#### Breadcrumbs
```css
.breadcrumb {
  font-size: 11px;
  font-weight: 400;
  color: #8a8885;
  letter-spacing: 0.5px;
}

.breadcrumb a {
  color: #5c5a57;
  text-decoration: none;
}

.breadcrumb a:hover {
  color: #393939;
}

.breadcrumb-separator {
  margin: 0 8px;
  color: #b5b3ae;
}
```

### Product Cards

```css
.product-card {
  background: #ffffff;
  text-align: center;
  padding: 5px;
  cursor: pointer;
}

.product-card-image {
  max-width: 248px;
  width: 100%;
  aspect-ratio: 1 / 1;
  object-fit: cover;
}

.product-card-title {
  font-size: 10px;
  font-weight: 500;
  letter-spacing: 2px;
  text-transform: uppercase;
  color: #393939;
  margin-top: 12px;
}

.product-card-badge {
  font-size: 10px;
  font-weight: 500;
  letter-spacing: 2px;
  text-transform: uppercase;
  color: #8a8885;
}
```

### Form Elements

#### Input Fields
```css
.form-input {
  width: 100%;
  height: 44px;
  padding: 0 16px;
  font-family: 'Inter', sans-serif;
  font-size: 14px;
  color: #393939;
  background-color: #ffffff;
  border: 1px solid #ddd;
  outline: none;
  transition: border-color 0.2s ease;
}

.form-input:focus {
  border-color: #393939;
}

.form-input::placeholder {
  color: #b5b3ae;
}
```

#### Select/Dropdown
```css
.form-select {
  height: 34px;
  padding: 3px 10px;
  font-family: 'Inter', sans-serif;
  font-size: 12px;
  color: #393939;
  background-color: #ffffff;
  border: 1px solid #ddd;
  cursor: pointer;
}
```

#### Labels
```css
.form-label {
  display: block;
  font-size: 11px;
  font-weight: 500;
  letter-spacing: 1px;
  text-transform: uppercase;
  color: #5c5a57;
  margin-bottom: 8px;
}
```

### Filter Sidebar

```css
.filter-sidebar {
  position: sticky;
  top: 70px;
  max-height: calc(100vh - 96px);
  overflow-y: auto;
  background-color: #f6f5f4;
  padding: 20px;
}

.filter-section {
  border-bottom: 1px solid #ddd;
  padding: 16px 0;
}

.filter-title {
  font-size: 11px;
  font-weight: 500;
  letter-spacing: 1.5px;
  text-transform: uppercase;
  color: #393939;
  margin-bottom: 12px;
}
```

---

## Brand Voice & Messaging

### Tone Characteristics

| Attribute | Description | Example |
|-----------|-------------|---------|
| **Refined** | Sophisticated without being pretentious | "Artisan-crafted rugs" not "Amazing rugs!" |
| **Warm** | Inviting and approachable | "Welcome to your home" not "Shop now" |
| **Confident** | Assured quality without overselling | "Handmade with care" not "Best rugs ever!" |
| **Understated** | Let products speak; minimal hype | "Explore the collection" not "Don't miss out!" |
| **Authentic** | Genuine story of craftsmanship | "Made by artisans in Jaipur" |

### Writing Guidelines

1. **Avoid superlatives** - No "best," "amazing," "incredible"
2. **Favor active voice** - "Artisans weave" not "Woven by artisans"
3. **Short sentences** - Elegant brevity over lengthy descriptions
4. **No exclamation marks** - Confident tone doesn't need them
5. **Lowercase when possible** - "explore collection" not "EXPLORE COLLECTION" (except for UI labels)

### Headline Examples

| Do | Don't |
|----|-------|
| "Handcrafted Beauty" | "Amazing Handcrafted Rugs!" |
| "The Art of Home" | "Transform Your Home Today!" |
| "Timeless Design" | "Best Designs Ever" |
| "Explore Our Collection" | "Shop Now!!!" |
| "Artisan Made" | "Incredible Quality" |

### CTA Button Text

| Context | Preferred | Avoid |
|---------|-----------|-------|
| Product view | "View Details" | "Buy Now!" |
| Collection | "Explore" | "Shop Now!" |
| Cart | "Proceed to Checkout" | "Checkout Now!" |
| Newsletter | "Subscribe" | "Sign Up Now!" |
| Contact | "Send Message" | "Submit!" |

### Product Description Voice

```
Example Product Description:

"The Solana rug brings warmth to any space with its hand-knotted
wool construction and subtle geometric pattern. Crafted by artisans
in Jaipur using traditional techniques passed down through generations."

- No hyperbole
- Focus on craftsmanship
- Mention origin and technique
- Describe rather than sell
```

---

## Photography & Image Guidelines

### Product Photography

1. **Clean backgrounds** - White or light neutral (#f6f5f4)
2. **Natural lighting** - Soft, diffused light; no harsh shadows
3. **Straight-on angles** - Products shown flat or at slight angle
4. **Consistent framing** - Centered, equal padding on all sides
5. **No props clutter** - Minimal styling; product is hero

### Lifestyle Photography

1. **Warm tones** - Natural wood, soft textiles, warm lighting
2. **Aspirational but attainable** - Luxury that feels accessible
3. **Real spaces** - Authentic interiors, not sterile showrooms
4. **Subtle product placement** - Rug as part of scene, not focal point
5. **Neutral color palette** - Complements the product range

### Image Specifications

| Usage | Dimensions | Format | Notes |
|-------|------------|--------|-------|
| Product Grid | 254px wide | WebP/JPG | Square aspect ratio |
| Product Detail | 800px+ | WebP/JPG | Allow zoom |
| Hero Banner | 1440px wide | WebP/JPG | Optimize for speed |
| Thumbnails | 100px | WebP/JPG | Consistent sizing |

---

## Code Implementation Examples

### Tailwind CSS Configuration

```javascript
// tailwind.config.js
module.exports = {
  theme: {
    extend: {
      fontFamily: {
        sans: ['Inter', '-apple-system', 'BlinkMacSystemFont', 'Segoe UI', 'Roboto', 'sans-serif'],
      },
      colors: {
        'jl-charcoal': '#393939',
        'jl-offwhite': '#f6f5f4',
        'jl-dark': '#282828',
        'jl-border': '#ddd',
        'jl-hover': '#ddd8d0',
        'jl-muted': '#8a8885',
        'jl-secondary': '#5c5a57',
      },
      fontSize: {
        'xs': ['10px', { lineHeight: '14px', letterSpacing: '2px' }],
        'sm': ['12px', { lineHeight: '18px' }],
        'base': ['14px', { lineHeight: '22px' }],
        'lg': ['16px', { lineHeight: '26px' }],
        'xl': ['18px', { lineHeight: '24px' }],
        '2xl': ['22px', { lineHeight: '28px', letterSpacing: '-0.44px' }],
        '3xl': ['28px', { lineHeight: '32px', letterSpacing: '-0.56px' }],
        '4xl': ['36px', { lineHeight: '38px', letterSpacing: '-0.72px' }],
      },
      spacing: {
        '18': '72px', // Header height
      },
    },
  },
}
```

### React Component Example

```jsx
// ProductCard.jsx
import React from 'react';

const ProductCard = ({ image, title, category, code }) => {
  return (
    <div className="bg-white text-center p-1 cursor-pointer group">
      <div className="overflow-hidden">
        <img
          src={image}
          alt={title}
          className="w-full max-w-[248px] mx-auto aspect-square object-cover
                     transition-transform duration-300 group-hover:scale-105"
        />
      </div>
      <h3 className="mt-3 text-[10px] font-medium tracking-[2px] uppercase text-jl-charcoal">
        {title}
      </h3>
      {category && (
        <p className="text-[10px] font-medium tracking-[2px] uppercase text-jl-muted">
          {category}
        </p>
      )}
      {code && (
        <p className="text-[10px] tracking-[2px] uppercase text-jl-muted">
          {code}
        </p>
      )}
    </div>
  );
};

export default ProductCard;
```

### Button Component

```jsx
// Button.jsx
import React from 'react';

const Button = ({ variant = 'primary', children, ...props }) => {
  const baseStyles = `
    px-6 py-3
    font-medium text-xs tracking-[1.5px] uppercase
    transition-all duration-200
    cursor-pointer
  `;

  const variants = {
    primary: `
      bg-transparent text-jl-charcoal
      border border-jl-charcoal
      hover:bg-jl-charcoal hover:text-white
    `,
    secondary: `
      bg-white text-jl-charcoal
      border border-jl-border
      hover:border-jl-charcoal
    `,
    dark: `
      bg-jl-charcoal text-white
      border border-jl-charcoal
      hover:bg-jl-dark
    `,
  };

  return (
    <button className={`${baseStyles} ${variants[variant]}`} {...props}>
      {children}
    </button>
  );
};

export default Button;
```

---

## Anti-Patterns to Avoid

### Typography Don'ts

- Never use Helvetica (always use Inter)
- No Comic Sans, Papyrus, or decorative fonts
- Avoid bold weights (700) for headers - use light (300)
- Don't use font sizes smaller than 10px
- Never use more than 2 font weights on a page
- Avoid centered body text (except for short captions)

### Color Don'ts

- No bright, saturated colors
- No gradients or color transitions
- Avoid pure black (#000000) - use #393939 or #1f1e1e
- No neon or fluorescent accents
- Don't use more than 3-4 colors total

### Layout Don'ts

- No cluttered layouts - embrace whitespace
- Avoid shadow effects on cards
- No rounded corners larger than 2px
- Don't overlap elements or use complex z-index stacking
- Avoid full-width colored sections (except footer)

### Brand Voice Don'ts

- No exclamation marks!
- Avoid ALL CAPS (except UI labels)
- No aggressive CTAs ("BUY NOW!", "DON'T MISS OUT!")
- Avoid hyperbole ("amazing", "incredible", "best")
- No emoji in professional contexts
- Don't use slang or overly casual language

### Visual Don'ts

- No stock photos with obvious watermarks
- Avoid busy patterns or textures
- No animated GIFs or flashy effects
- Don't use icons as decorative elements
- Avoid parallax scrolling effects

---

## Quick Reference Card

### Font
```
Family: Inter
Headers: 300 weight, negative letter-spacing
Body: 400 weight
Labels: 500 weight, 2px letter-spacing, uppercase
```

### Colors (Most Used)
```
Text: #393939
Background: #f6f5f4
White: #ffffff
Border: #ddd
Muted: #8a8885
Dark: #282828
```

### Spacing
```
Base unit: 4px
Standard padding: 16-20px
Section gap: 64-96px
Header height: 72px
```

### Voice
```
Tone: Refined, warm, confident, understated
Avoid: Exclamation marks, superlatives, urgency
CTAs: "Explore", "View Details", "Subscribe"
```

---

## Version History

| Version | Date | Changes |
|---------|------|---------|
| 1.0 | Jan 2026 | Initial document creation |

---

*This document should be referenced whenever creating new pages, components, or marketing materials for Jaipur Living to ensure brand consistency.*
