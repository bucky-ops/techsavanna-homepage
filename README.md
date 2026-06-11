# TechSavanna Homepage

> Enhanced homepage for TechSavanna Kenya, featuring 3D design, interactive cards, mouse tracking effects, and customer-centric UI.

**Live Demo:** [techsavanna-homepage.vercel.app](https://techsavanna-homepage.vercel.app) | **Original Site:** [techsavanna.co.ke](https://techsavanna.co.ke/)

---

## Overview

This is the enhanced, standalone homepage for TechSavanna Kenya. Built as a single self-contained HTML file with embedded CSS and JavaScript, it features cutting-edge web design patterns including 3D transformations, interactive card animations, custom cursor effects, and a fully responsive layout. The page follows a customer-centric design philosophy, leading with visitor pain points and outcomes rather than company features.

---

## Features

### Visual and 3D Effects
- **Custom Cursor:** Ring and dot cursor with smooth easing that reacts to interactive elements
- **Mouse Glow Trail:** Subtle radial glow that follows cursor movement
- **Interactive Particle Network:** Canvas-based particle system that responds to mouse proximity
- **3D Tilt Cards:** All card elements tilt in 3D space based on mouse position
- **Hero 3D Parallax:** Hero section content shifts with mouse movement for depth
- **Floating 3D Geometric Shapes:** Rotating, floating geometric shapes with CSS 3D transforms
- **Magnetic Buttons:** Buttons subtly attract toward the cursor on hover

### Interactive Components
- **3D Flip Success Story Cards:** Hover to flip and reveal client testimonials (Safaricom, Equity, Britam, Stanbic)
- **Animated Stats Counter:** Numbers count up when scrolled into view (500+ Projects, 150+ Clients, 12+ Years, 50+ Team)
- **Interactive FAQ Accordion:** Smooth expand/collapse with rotating icons
- **Solution Category Tabs:** Filter solutions by category (All / Enterprise / Management / Industry)
- **Ripple Effect:** Material Design-inspired ripple on all interactive buttons
- **Animated Progress Bars:** Work Routine section with animated step indicators
- **Customer Pain Points Section:** Highlighting challenges visitors face with clear CTAs

### Layout and UX
- **Customer-Centric Flow:** Problem, Solution, Proof, Process, Action
- **Scroll Reveal Animations:** Elements animate in as you scroll (fade-up, slide-left, slide-right)
- **Header Scroll Effect:** Transparent header transitions to frosted glass on scroll
- **Lazy-loaded Iframes:** Videos and embeds load only when visible
- **Fully Responsive:** Optimized for mobile, tablet, and desktop
- **Mobile Menu:** Slide-out offcanvas navigation for smaller screens

### Page Sections (Customer Journey Order)
1. Hero with customer-focused messaging and animated typing effect
2. Trust Bar with social proof stats
3. Pain Points: challenges customers face
4. Solutions carousel with category filtering
5. Success Stories with 3D flip cards
6. Client Testimonials
7. How It Works: customer journey process
8. Partner ecosystem logos
9. Video showcase
10. FAQ with customer-focused questions
11. Call-to-action section
12. Blog insights
13. Credentials and certifications
14. Footer with newsletter signup

---

## Tech Stack

| Technology | Purpose |
|-----------|---------|
| HTML5 | Semantic markup |
| CSS3 | Custom properties, 3D transforms, animations, Grid, Flexbox |
| JavaScript (Vanilla) | Intersection Observer, Canvas API, requestAnimationFrame |
| Bootstrap 5.3 | Grid system and responsive utilities |
| Font Awesome 6.5 | Icons |
| Google Fonts | Poppins and Lato typography |
| Swiper 11 | Carousel/slider functionality |

---

## Project Structure

```
techsavanna-homepage/
├── index.html          # Complete enhanced homepage (self-contained)
├── vercel.json         # Vercel deployment configuration
├── .gitignore          # Git ignore rules
├── LICENSE             # MIT License
└── README.md           # Project documentation
```

---

## Deployment

### Vercel (Current)
The site is deployed on Vercel and auto-deploys on every push to `main`.

1. Push changes to the `main` branch
2. Vercel automatically detects and deploys
3. Live at `techsavanna-homepage.vercel.app`

### Other Static Hosts
This project works with any static site host (Netlify, GitHub Pages, etc.). Just serve the root directory. The `index.html` file is self-contained with all CSS and JS inline.

---

## Development

Since this is a single self-contained HTML file:

1. Clone the repository
2. Open `index.html` in any browser
3. Edit the file directly
4. Push changes to deploy

No build tools, no npm install, no bundlers needed.

---

## Version History

| Version | Changes |
|---------|---------|
| v4.0 | Customer-centric redesign: reorganized sections, customer-focused copy, new Pain Points and CTA sections |
| v3.0 | 3D effects, interactive cards, mouse tracking, content accuracy |
| v2.0 | Interactive cards, enhanced UX, animated stats |
| v1.0 | Initial enhanced homepage |

---

## Credits

- **Design and Development:** TechSavanna Kenya
- **Original Site:** [techsavanna.co.ke](https://techsavanna.co.ke/)

---

## License

This project is proprietary. All rights reserved by TechSavanna Kenya.
