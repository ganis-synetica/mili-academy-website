# Mili Academy Website - EXACT CLONE

## Mission
Create an **exact clone** of https://www.superpath.io/ in Astro. Same design, same structure, same animations - just different branding for later.

## Stack (Same as SuperPath)
- **Framework:** Astro 5.x
- **Styling:** CSS (they use scoped Astro styles)
- **Font:** Plus Jakarta Sans (Google Fonts) - weights 400, 500, 600, 700, 800
- **Animations:** Lottie (for feature graphics)
- **No Tailwind** - they use custom CSS

## Design System (from SuperPath)

### Colors
| Color | Hex | Usage |
|-------|-----|-------|
| Navy/Purple | `#1E1A5C` | Primary text, headers, buttons |
| Magenta/Pink | `#EA1F67` | Primary CTA, accents |
| Light text | `#444F6F` | Secondary text |
| Gray | `#C3CAD2` | Muted text |
| Background | `#FFFFFF` | Main background |

### Typography
- Font: Plus Jakarta Sans
- H1: Bold, large
- Body: 400 weight
- Buttons: 700 weight

## Pages to Clone

### Priority 1 - Homepage
1. **Header** - Logo, nav with mega menus, Sign In, Book Demo CTA
2. **Hero** - Animated title with pills (create, deploy, automate, track), testimonial avatars, video
3. **Logo Slider** - Two-row infinite scroll
4. **Feature Block** - Lottie animation + text
5. **Micro Features** - Horizontal scroll tiles
6. **Features Accordion** - Two sections (Built for Admins, Built for HR)
7. **Track Everything** section
8. **CTA Section**
9. **Footer**

### Priority 2 - Other Pages
- /features (list all features)
- /pricing (Rp 20.000/bulan/orang)
- /contact
- /solutions (industry pages)

## Reference Files
- Homepage HTML saved at: reference/superpath/index.html
- Use this as reference for exact structure

## Key Components Needed

### Header.astro
- Fixed position
- Logo (use placeholder SVG for now)
- Navigation with dropdown mega menus
- Mobile hamburger menu
- Sign In link
- Book Demo button (pink gradient)

### Hero.astro
- Social proof (Capterra rating + avatar stack)
- Animated headline with colored pills
- Description text
- Pink gradient CTA button
- Video/animation placeholder

### LogoSlider.astro
- Two rows scrolling opposite directions
- Grayscale logos, color on hover
- Gradient fade edges

### FeatureBlock.astro
- Split layout (text + Lottie)
- Heading, rich text body, CTA

### FeaturesAccordion.astro
- Expandable feature items
- Lottie animations that change on selection

### Footer.astro
- Multi-column links
- Social icons
- Newsletter signup

## Installation

```bash
npm create astro@latest . -- --template minimal --typescript --no-install
npm install
npm install lottie-web
```

## CSS Setup
Add to global styles:
```css
@import url('https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700;800&display=swap');

:root {
  --color-navy: #1E1A5C;
  --color-pink: #EA1F67;
  --color-text: #444F6F;
  --color-muted: #C3CAD2;
  --font-family: 'Plus Jakarta Sans', sans-serif;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: var(--font-family);
  color: var(--color-text);
  background: #fff;
}
```

## Notes
- Keep SuperPath branding for now (we'll swap to Mili later)
- Focus on pixel-perfect recreation
- Use placeholder images/videos where needed
- Skip Lottie animations initially - use static images or placeholders
