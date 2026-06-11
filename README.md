# TechSavanna Homepage

> Enhanced homepage for [TechSavanna Kenya](https://techsavanna.co.ke/) — featuring 3D design, interactive cards, mouse tracking effects, and modern UI.

## Overview

This is the enhanced, standalone homepage for TechSavanna Kenya. Built as a single self-contained HTML file with embedded CSS and JavaScript, it features cutting-edge web design patterns including 3D transformations, interactive card animations, custom cursor effects, and a fully responsive layout.

**Live Site:** [techsavanna.co.ke](https://techsavanna.co.ke/)

## Features

### Visual & 3D Effects
- **Custom Cursor** — Ring + dot cursor with smooth easing that reacts to interactive elements
- **Mouse Glow Trail** — Subtle radial glow that follows cursor movement
- **Interactive Particle Network** — Canvas-based particle system that responds to mouse proximity
- **3D Tilt Cards** — All card elements tilt in 3D space based on mouse position
- **Hero 3D Parallax** — Hero section content shifts with mouse movement for depth
- **Floating 3D Geometric Shapes** — Rotating, floating geometric shapes with CSS 3D transforms
- **Magnetic Buttons** — Buttons subtly attract toward the cursor on hover

### Interactive Components
- **3D Flip Success Story Cards** — Hover to flip and reveal client testimonials (Safaricom, Equity, Britam, Stanbic)
- **Animated Stats Counter** — Numbers count up when scrolled into view (500+ Projects, 150+ Clients, 12+ Years, 50+ Team)
- **Interactive FAQ Accordion** — Smooth expand/collapse with rotating icons
- **Solution Category Tabs** — Filter solutions by category (All / Enterprise / Management / Industry)
- **Ripple Effect** — Material Design-inspired ripple on all interactive buttons
- **Animated Progress Bars** — Work Routine section with animated step indicators

### Layout & UX
- **Scroll Reveal Animations** — Elements animate in as you scroll (fade-up, slide-left, slide-right)
- **Header Scroll Effect** — Transparent header transitions to frosted glass on scroll
- **Lazy-loaded Iframes** — Videos and embeds load only when visible
- **Fully Responsive** — Optimized for mobile, tablet, and desktop
- **Mobile Menu** — Slide-out offcanvas navigation for smaller screens

### Content Sections
- Hero with animated text typing effect
- Solutions carousel with category filtering
- Partner logos grid with pagination
- Video showcase section
- Success stories with 3D flip cards
- Stats counter section
- Work routine / process section
- Testimonials carousel
- Credentials & certifications
- Blog articles
- FAQ accordion
- Newsletter signup & footer

## Tech Stack

- **HTML5** — Semantic markup
- **CSS3** — Custom properties, 3D transforms, animations, Grid, Flexbox
- **JavaScript (Vanilla)** — Intersection Observer, Canvas API, requestAnimationFrame
- **Bootstrap 5.3** — Grid system and responsive utilities
- **Font Awesome 6.5** — Icons
- **Google Fonts** — Poppins + Lato
- **Swiper 11** — Carousel/slider functionality

## Deployment

This project is designed for static hosting and works with any static site host:

### Vercel (Recommended)
1. Push this repo to GitHub
2. Import the repo on [vercel.com](https://vercel.com)
3. Framework: **Other**
4. Deploy — `index.html` at root is auto-detected

### Netlify / GitHub Pages / Any Static Host
Just serve the root directory. The `index.html` file is self-contained.

## File Structure

```
techsavanna-homepage/
├── index.html          # Complete enhanced homepage (self-contained)
├── vercel.json         # Vercel deployment configuration
└── README.md           # This file
```

## Credits

- **Design & Development:** TechSavanna Kenya
- **Original Site:** [techsavanna.co.ke](https://techsavanna.co.ke/)
- **Enhanced Version:** v3.0 with 3D effects, interactive cards, and mouse tracking

## License

&copy; TechSavanna Kenya. All rights reserved.
