# TechSavanna Index.html — Update Documentation

**Website:** https://techsavanna.co.ke/
**File:** `index.html`
**Last Updated:** June 11, 2026
**Version:** 2.0 (Enhanced with 3D & Interactivity)

---

## Overview

This document provides a complete changelog and technical reference for all updates made to the TechSavanna `index.html`. Every addition, modification, and enhancement is documented with its location, purpose, and usage instructions.

---

## Table of Contents

1. [Phase 1 — Mouse Movement & 3D Foundation](#phase-1--mouse-movement--3d-foundation)
2. [Phase 2 — Interactive Cards & Enhanced UX](#phase-2--interactive-cards--enhanced-ux)
3. [File Structure Map](#file-structure-map)
4. [Feature Reference](#feature-reference)
5. [CSS Class Reference](#css-class-reference)
6. [JavaScript Function Reference](#javascript-function-reference)
7. [Mobile Compatibility](#mobile-compatibility)
8. [Integration Guide](#integration-guide)

---

## Phase 1 — Mouse Movement & 3D Foundation

*Added: June 11, 2026 — Initial enhancement pass*

These features establish the interactive foundation of the page. All mouse-movement tracking and 3D design aspects were introduced in this phase.

### What Was Added

| # | Feature | Location | Purpose |
|---|---------|----------|---------|
| 1 | **Custom Cursor (Ring + Dot)** | `#tsCursor`, `#tsCursorDot` | Dual-layer cursor that follows mouse with different easing speeds. Ring expands on hover over interactive elements. |
| 2 | **Mouse Glow** | `#tsMouseGlow` | A soft radial gradient light that trails behind the cursor, creating an ambient spotlight effect. |
| 3 | **Interactive Particle Network** | `#tsParticleCanvas` | Full-screen canvas with 60 floating particles connected by lines. Particles react to mouse proximity with physics-based repulsion. |
| 4 | **3D Tilt Cards** | `.ts-tilt-card` | All solution cards, process cards, and certification cards tilt toward the cursor using `perspective()` + `rotateX/Y` transforms. |
| 5 | **Hero 3D Parallax** | `#heroSection` | Hero content and video shift in opposite 3D directions based on mouse position. Background orbs follow cursor. |
| 6 | **Floating 3D Geometric Shapes** | `.ts-geo-shapes` | 5 wireframe shapes rotate continuously in 3D space and shift position based on mouse location. |
| 7 | **Magnetic Buttons** | `.ts-magnetic` | CTA buttons subtly pull toward the cursor when hovered. |
| 8 | **Scroll Reveal Animations** | `.ts-reveal`, `.ts-reveal-left`, `.ts-reveal-right` | Elements fade in from different directions as they enter the viewport via `IntersectionObserver`. |
| 9 | **Header Scroll Effect** | `#headerArea` | Header transitions from transparent overlay to frosted-glass (`backdrop-filter: blur`) on scroll. |
| 10 | **Lazy-loaded Iframes** | `iframe[data-src]` | YouTube video iframe only loads when scrolled into view. |

### Where in the Code

- **CSS:** Lines 25–938 (inside `<style>` block in `<head>`)
  - Custom Cursor: `.ts-cursor`, `.ts-cursor-dot`
  - 3D Shapes: `.ts-geo-shapes`, `.ts-geo-shape` + `@keyframes tsGeoFloat1–5`
  - Mouse Glow: `.ts-mouse-glow`
  - Particles: `#tsParticleCanvas`
  - Tilt Cards: `.ts-tilt-card`
  - Hero Parallax: `.hero-split`, `.hero-content`, `.hero-video-wrapper`
  - Magnetic: `.ts-magnetic`
  - Scroll Reveal: `.ts-reveal`, `.ts-reveal-left`, `.ts-reveal-right`

- **HTML:** Lines 940–960 (cursor, glow, shapes, canvas elements in `<body>`)

- **JS:** Inside the main `<script>` block before `</body>`
  - Section 1: Custom Cursor + Mouse Glow
  - Section 2: 3D Tilt on Cards
  - Section 3: Hero 3D Parallax
  - Section 4: Geometric Shapes Mouse Reactivity
  - Section 5: Interactive Particle Network
  - Section 6: Magnetic Buttons
  - Section 7: Scroll Reveal
  - Section 8: Header Scroll Effect
  - Section 16: Smooth Scroll Parallax
  - Section 17: Lazy Load Iframes

---

## Phase 2 — Interactive Cards & Enhanced UX

*Added: June 11, 2026 — Second enhancement pass*

These features add richer card designs, animated data displays, and more user interaction patterns.

### What Was Added

| # | Feature | Location | Purpose |
|---|---------|----------|---------|
| 1 | **3D Flip-Over Success Story Cards** | `.ts-flip-card` (replaces `.success-story-section`) | 4 cards that flip 180° on hover (click on mobile) to reveal detailed case studies on the back face. Front: client name + industry + teaser. Back: full testimonial + results + link. |
| 2 | **Animated Stats Counter Section** | `.ts-stats-section` (between hero and solutions) | 4 counter boxes (500+ Projects, 150+ Clients, 12+ Years, 50+ Team Members) with animated counting from 0 via `IntersectionObserver`. Stat cards have 3D tilt. |
| 3 | **Interactive FAQ Accordion** | `.ts-faq-section` (before blog section) | 6 expandable FAQ items with smooth `max-height` transition, rotating +/- icon, single-open-at-a-time behavior. |
| 4 | **Ripple Effect on Buttons** | `.ts-ripple` (applied to all buttons) | CSS + JS ripple effect. On click, an expanding circle appears from click position and fades out. |
| 5 | **Animated Progress Bars** | `.ts-progress-bar` (inside Work Routine section) | 4 progress bars (Research 95%, Design 90%, Build 98%, Deliver 100%) that animate from 0% to target width on scroll via `IntersectionObserver`. |
| 6 | **Interactive Solution Category Tabs** | `.sol-tabs` (above More Solutions grid) | 4 filter tabs (All, Enterprise, Management, Industry) that show/hide solution cards with smooth fade transitions. |

### Where in the Code

- **CSS:**
  - Flip Cards: `.ts-flip-card`, `.ts-flip-card-inner`, `.ts-flip-card-front`, `.ts-flip-card-back`
  - Stats Counter: `.ts-stats-section`, `.ts-stat-card`, `.ts-counter`
  - FAQ Accordion: `.ts-faq-section`, `.ts-faq-item`, `.ts-faq-question`, `.ts-faq-answer`
  - Ripple Effect: `.ts-ripple`, `@keyframes tsRipple`
  - Progress Bars: `.ts-progress-wrap`, `.ts-progress-bar`, `.ts-progress-fill`
  - Solution Tabs: `.sol-tabs`, `.sol-tab`, `.sol-tab-content`

- **HTML:**
  - Stats Section: After hero, before solutions
  - Flip Cards: Replaces old success-story-section (between partners and videos)
  - Progress Bars: Inside Work Routine section's left column
  - Solution Tabs: Above the "More Solutions" grid
  - FAQ Section: Before blog section

- **JS:**
  - Counter Animation: `IntersectionObserver` watching `.ts-counter` elements
  - FAQ Toggle: Click handlers on `.ts-faq-question` with `max-height` toggle
  - Ripple Effect: Click handlers creating `span.ts-ripple` elements
  - Progress Bars: `IntersectionObserver` triggering width animation
  - Solution Tabs: Click handlers filtering `.sol-tab-content` cards by `data-category`

---

## File Structure Map

```
index.html
│
├── <head>
│   ├── Meta tags & title
│   ├── CDN links (Google Fonts, Swiper, OwlCarousel, FontAwesome, Bootstrap)
│   ├── Favicon links
│   └── <style> — ALL CSS (inline)
│       ├── CSS Variables (:root)
│       ├── Reset & Base
│       ├── Custom Cursor (.ts-cursor, .ts-cursor-dot)
│       ├── 3D Scene Container (.ts-3d-scene)
│       ├── Floating 3D Geometric Shapes (.ts-geo-shapes)
│       ├── Mouse Glow Trail (.ts-mouse-glow)
│       ├── Particle Canvas (#tsParticleCanvas)
│       ├── Header (.header-area, navigation, mobile menu)
│       ├── Hero Section (.hero-split, .hero-content)
│       ├── Section Common (.ptb-*, .section-heading)
│       ├── 3D Tilt Card (.ts-tilt-card)
│       ├── Stats Counter Section (.ts-stats-section)        ← NEW
│       ├── Solutions Section (.sol-wrap, .sol-card)
│       ├── Partners Section (.ts-partners-wrap)
│       ├── Video Section (.videoarea)
│       ├── Flip-Over Success Story Cards (.ts-flip-card)    ← NEW
│       ├── Work Routine / Process (.cta-card)
│       ├── Progress Bars (.ts-progress-bar)                  ← NEW
│       ├── Solution Category Tabs (.sol-tabs)                ← NEW
│       ├── Testimonials (.testimonal-section)
│       ├── Credentials (.cert-section)
│       ├── FAQ Accordion (.ts-faq-section)                   ← NEW
│       ├── Blog (.single-article)
│       ├── Footer (.footer-section)
│       ├── Scroll Reveal Animations (.ts-reveal)
│       ├── Magnetic Buttons (.ts-magnetic)
│       ├── Ripple Effect (.ts-ripple)                        ← NEW
│       ├── Modal Styles (.modal)
│       └── Smooth Parallax ([data-parallax])
│
├── <body>
│   ├── #tsCursor — Custom cursor ring
│   ├── #tsCursorDot — Custom cursor dot
│   ├── #tsMouseGlow — Mouse glow follower
│   ├── #tsGeoShapes — 3D floating shapes container
│   ├── #tsParticleCanvas — Particle network canvas
│   │
│   ├── Header Area (nav, logo, search, mobile trigger)
│   ├── Mobile Menu Overlay
│   ├── Hero Section (3D parallax, typing animation, video)
│   │
│   ├── ★ Stats Counter Section (4 animated counters)        ← NEW
│   │
│   ├── Solutions Carousel (2-page slider with autoplay)
│   ├── More Solutions Grid
│   │   └── ★ Solution Category Tabs (filter buttons)         ← NEW
│   │
│   ├── Partners Section (3-page dot navigation)
│   │
│   ├── ★ Flip-Over Success Story Cards (4 flip cards)       ← NEW (replaces old)
│   │
│   ├── Video Swiper (3 videos)
│   ├── Work Routine (Research, Build, Design, Deliver)
│   │   └── ★ Animated Progress Bars                          ← NEW
│   │
│   ├── Testimonials (Owl Carousel)
│   ├── Credentials / Certifications (4 cards + modals)
│   │
│   ├── ★ FAQ Accordion (6 expandable items)                  ← NEW
│   │
│   ├── Blog Section (2 articles + "View All")
│   ├── Footer (logo, links, newsletter, social, copyright)
│   └── Tawk.to Chat Widget
│
├── <script> CDN (jQuery, Bootstrap, Swiper, OwlCarousel)
│
└── <script> — ALL JS (inline)
    ├── 1. Custom Cursor + Mouse Glow
    ├── 2. 3D Tilt on Cards
    ├── 3. Hero 3D Parallax
    ├── 4. Geometric Shapes Mouse Reactivity
    ├── 5. Interactive Particle Network
    ├── 6. Magnetic Buttons
    ├── 7. Scroll Reveal
    ├── 8. Header Scroll Effect
    ├── 9. Mobile Menu
    ├── 10. Hero Sound Toggle
    ├── 11. Typing Animation
    ├── 12. Solutions Carousel
    ├── 13. Partners Carousel
    ├── 14. Swiper Video Carousel
    ├── 15. Owl Carousel (Testimonials & Certs)
    ├── 16. Smooth Scroll Parallax
    ├── 17. Lazy Load Iframes
    ├── ★ 18. Animated Stats Counter                           ← NEW
    ├── ★ 19. Flip Card Interaction                            ← NEW
    ├── ★ 20. FAQ Accordion                                    ← NEW
    ├── ★ 21. Ripple Effect on Buttons                         ← NEW
    ├── ★ 22. Progress Bar Animation                           ← NEW
    └── ★ 23. Solution Category Tabs                           ← NEW
```

---

## Feature Reference

### 3D Flip-Over Success Story Cards

**How it works:**
- Each card uses `transform-style: preserve-3d` with two faces (front and back)
- On desktop: hover triggers `rotateY(180deg)` on `.ts-flip-card-inner`
- On mobile: click triggers the same flip (via JS `.flipped` class toggle)
- The back face uses `transform: rotateY(180deg)` and `backface-visibility: hidden` on both faces

**Customization:**
- To add more cards, copy a `.ts-flip-card` block and update the content
- To change flip direction, change `rotateY(180deg)` to `rotateX(180deg)` for vertical flip
- Flip speed: adjust `transition: transform 0.8s` in `.ts-flip-card-inner`

**Cards included:**
1. Safaricom PLC — Telecommunications
2. Equity Bank — Banking & Finance
3. Britam — Insurance
4. Stanbic Bank — Banking

---

### Animated Stats Counter Section

**How it works:**
- 4 counter elements with `data-target` attributes (e.g., `data-target="500"`)
- `IntersectionObserver` watches `.ts-counter` elements
- When visible, `animateCounter()` increments from 0 to target over ~2 seconds
- Uses `requestAnimationFrame` for smooth 60fps counting
- Each stat card has 3D tilt via the existing tilt-card system

**Stats included:**
| Stat | Target | Icon |
|------|--------|------|
| Projects Delivered | 500+ | fa-project-diagram |
| Happy Clients | 150+ | fa-users |
| Years Experience | 12+ | fa-calendar |
| Team Members | 50+ | fa-user-tie |

**Customization:**
- Change `data-target` value to adjust the count
- Change `data-suffix` to change the "+" or other suffix
- Adjust animation speed by modifying the `duration` variable in `animateCounter()`

---

### Interactive FAQ Accordion

**How it works:**
- Click on `.ts-faq-question` toggles the `.active` class on `.ts-faq-item`
- Only one item can be open at a time (clicking one closes others)
- The answer container uses `max-height: 0` → `max-height: 500px` transition
- The `+` icon rotates to `×` via CSS `transform: rotate(45deg)` on `.active`

**Questions included:**
1. What services does Techsavanna offer?
2. How long does it take to implement an ERP system?
3. Do you offer custom software development?
4. What industries do you serve?
5. Is training provided with your solutions?
6. How do I get a quote for my project?

**Customization:**
- Add new FAQ items by copying a `.ts-faq-item` block
- Adjust animation speed via `transition: max-height 0.4s ease` in CSS

---

### Ripple Effect on Buttons

**How it works:**
- All buttons with classes `.hero-btn`, `.btn`, `.ts-magnetic`, or `button[class*="btn"]` get the ripple
- On click, JS calculates click position relative to button
- Creates a `span.ts-ripple` element positioned at click point
- CSS animation expands the circle from 0 to cover the button, then fades out
- The ripple span is removed after animation completes (600ms)

**Customization:**
- Ripple color: Change `background: rgba(255,255,255,0.4)` in `.ts-ripple`
- Ripple duration: Change `animation: tsRipple 0.6s` in CSS
- To exclude certain buttons, add `.no-ripple` class and update the JS selector

---

### Animated Progress Bars

**How it works:**
- 4 progress bars with `data-width` attributes (95, 90, 98, 100)
- `IntersectionObserver` watches `.ts-progress-wrap`
- When visible, each `.ts-progress-fill` transitions from `width: 0%` to `width: data-width%`
- Staggered delay: each bar starts 200ms after the previous one

**Bars included:**
| Label | Percentage |
|-------|-----------|
| Research | 95% |
| Design | 90% |
| Build | 98% |
| Deliver | 100% |

**Customization:**
- Change `data-width` to adjust the fill level
- Change bar color via `background: linear-gradient(...)` in `.ts-progress-fill`

---

### Interactive Solution Category Tabs

**How it works:**
- 4 tab buttons with `data-filter` attributes: `all`, `enterprise`, `management`, `industry`
- Each solution card has a `data-category` attribute matching a filter value
- Clicking a tab:
  1. Adds `.active` to clicked tab, removes from others
  2. Cards not matching the filter get `opacity: 0` + `transform: scale(0.8)` then `display: none` after 300ms
  3. Matching cards get `display: block` then `opacity: 1` + `transform: scale(1)` after 50ms
- "All" tab shows everything

**Categories:**
| Tab | Solutions |
|-----|-----------|
| Enterprise | Savanna360 ERP, WorkWise HRM |
| Management | Engage CRM, Document Management System, Call Center & Ticketing |
| Industry | Farm Management System, Time Tracking & Attendance |
| All | Everything |

**Customization:**
- Add new categories by adding `data-category="new-cat"` to cards and a matching tab button
- Adjust transition timing via the `300` and `50` setTimeout values in JS

---

## CSS Class Reference

### New Classes (Phase 2)

| Class | Element | Description |
|-------|---------|-------------|
| `.ts-flip-card` | Container | 3D flip card wrapper with perspective |
| `.ts-flip-card-inner` | Inner wrapper | The element that actually rotates |
| `.ts-flip-card-front` | Front face | Visible by default, hidden on flip |
| `.ts-flip-card-back` | Back face | Hidden by default, visible on flip |
| `.ts-flip-card.flipped` | Mobile state | JS-added class for click-to-flip on mobile |
| `.ts-stats-section` | Section | Blue gradient background for stats |
| `.ts-stat-card` | Card | Individual stat box with 3D tilt |
| `.ts-counter` | Number span | Target for animated counting |
| `.ts-faq-section` | Section | FAQ container |
| `.ts-faq-item` | Item | Individual FAQ entry |
| `.ts-faq-item.active` | State | Open FAQ item |
| `.ts-faq-question` | Button | Clickable question header |
| `.ts-faq-answer` | Content | Expandable answer container |
| `.ts-faq-icon` | Icon | +/- indicator that rotates |
| `.ts-ripple` | Span | Ripple animation element (created by JS) |
| `.ts-progress-wrap` | Container | Progress bar wrapper |
| `.ts-progress-bar` | Label | Progress bar label + percentage |
| `.ts-progress-fill` | Inner div | The animated fill element |
| `.sol-tabs` | Container | Tab navigation wrapper |
| `.sol-tab` | Button | Individual tab button |
| `.sol-tab.active` | State | Currently selected tab |
| `.sol-tab-content` | Card | Solution card with `data-category` attribute |

### Existing Classes (Phase 1)

| Class | Element | Description |
|-------|---------|-------------|
| `.ts-cursor` | Div | Custom cursor ring |
| `.ts-cursor.active` | State | Expanded cursor on interactive elements |
| `.ts-cursor-dot` | Div | Custom cursor inner dot |
| `.ts-mouse-glow` | Div | Radial gradient following mouse |
| `.ts-geo-shape` | Div | 3D floating wireframe shape |
| `.ts-tilt-card` | Card | Card that tilts toward mouse |
| `.ts-magnetic` | Button | Button that pulls toward cursor |
| `.ts-reveal` | Any | Fade-in from bottom on scroll |
| `.ts-reveal-left` | Any | Fade-in from left on scroll |
| `.ts-reveal-right` | Any | Fade-in from right on scroll |
| `.ts-reveal.revealed` | State | Visible after scroll trigger |

---

## JavaScript Function Reference

### New Functions (Phase 2)

| Function | Purpose |
|----------|---------|
| `animateCounter(el)` | Animates a number from 0 to `data-target` over ~2 seconds using `requestAnimationFrame` |
| Counter `IntersectionObserver` | Watches `.ts-counter` elements and triggers `animateCounter()` when visible |
| Flip card click handler | Toggles `.flipped` class on `.ts-flip-card` for mobile click-to-flip |
| FAQ click handler | Toggles `.active` on `.ts-faq-item`, closes others, rotates icon |
| `createRipple(event)` | Creates `span.ts-ripple` at click position, removes after 600ms |
| Progress bar `IntersectionObserver` | Sets `.ts-progress-fill` width to `data-width%` with staggered delays |
| Tab click handler | Filters `.sol-tab-content` cards by `data-category`, handles show/hide animation |

### Existing Functions (Phase 1)

| Function | Purpose |
|----------|---------|
| `animateCursor()` | Main animation loop for custom cursor ring, dot, and glow following mouse |
| Tilt card `mousemove` handler | Calculates `rotateX/Y` from mouse position relative to card center |
| Hero parallax `mousemove` handler | Shifts hero content, video, and orbs based on mouse position |
| Geo shape mouse handler | Translates 3D shapes based on mouse distance from center |
| `drawParticles()` | Canvas animation loop for particle network with mouse interaction |
| Magnetic button handler | Translates button toward cursor on `mousemove`, resets on `mouseleave` |
| Scroll reveal `IntersectionObserver` | Adds `.revealed` class when elements enter viewport |
| Header scroll handler | Adds `.scrolled` class when page scrolls past 80px |
| `typeLoop()` | Typing animation cycling through word array |
| `goToSlide(index)` | Navigates solutions carousel to specific page |
| `pGoTo(index)` | Navigates partners carousel to specific page |

---

## Mobile Compatibility

All features degrade gracefully on mobile:

| Feature | Mobile Behavior |
|---------|----------------|
| Custom Cursor | Hidden via `@media (max-width: 991px)` |
| Mouse Glow | Hidden (no mouse on touch devices) |
| Particle Network | Still renders but no mouse interaction |
| 3D Tilt Cards | Tilt disabled, cards still have hover shadow |
| Hero 3D Parallax | Disabled, content displays statically |
| 3D Floating Shapes | Still animate but no mouse reactivity |
| Magnetic Buttons | Disabled (no mouse tracking) |
| Flip Cards | Click-to-flip instead of hover |
| Stats Counter | Animated counting still works |
| FAQ Accordion | Fully functional on touch |
| Ripple Effect | Works on touch (touchstart) |
| Progress Bars | Animate on scroll |
| Solution Tabs | Fully functional on touch |
| Scroll Reveal | Fully functional |
| Header Scroll | Fully functional |
| Carousels | Swipe-enabled via touch handlers |

---

## Integration Guide

### How to Use This File

1. **Direct Copy-Paste:** The entire `index.html` file is self-contained. Copy the full content and paste it into your CMS or codebase. All CSS and JavaScript are inline — no external dependencies beyond the CDN links.

2. **CDN Dependencies:** The file requires these external resources:
   - Google Fonts (Poppins, Lato)
   - Swiper 11 CSS + JS
   - OwlCarousel 2 CSS + JS
   - Font Awesome 6
   - Bootstrap 5.3.3
   - jQuery 3.7.1

3. **WordPress Integration:** If using WordPress:
   - Replace the `<head>` and `<body>` content in your theme template
   - Keep WordPress `wp_head()` and `wp_footer()` hooks if needed
   - The Tawk.to script is included — update the site ID if different
   - Image paths reference `techsavanna.co.ke` — update if moving domains

4. **Customization Quick Start:**
   - **Change brand colors:** Edit `:root` CSS variables at the top of the `<style>` block
   - **Add/remove cards:** Copy/paste card HTML blocks; ensure data attributes match
   - **Modify animations:** Adjust `transition` durations in CSS and `setTimeout` values in JS
   - **Disable a feature:** Comment out or remove the corresponding CSS section and JS section

5. **Performance Notes:**
   - Particle canvas uses `requestAnimationFrame` for 60fps rendering
   - 3D transforms use `will-change: transform` for GPU acceleration
   - `IntersectionObserver` is used instead of scroll listeners for better performance
   - Images use `loading="lazy"` where applicable
   - Iframes are lazy-loaded when scrolled into view

---

## Changelog Summary

| Date | Version | Changes |
|------|---------|---------|
| June 11, 2026 | 1.0 | Initial enhancement: mouse tracking, 3D design, particles, cursor, scroll reveal, tilt cards |
| June 11, 2026 | 2.0 | Added: flip-over success story cards, animated stats counters, FAQ accordion, ripple effect, progress bars, solution category tabs, comprehensive code commenting |
| June 11, 2026 | 3.0 | Content accuracy pass: centered blog articles, fixed testimonials (Joe Doe), fixed Deliver description, fixed Training subtitle, added organization logos to flip cards, added Integration section from live site, verified all original content matches live website |

---

## Phase 3 — Content Accuracy & Layout Fixes

*Added: June 11, 2026 — Content accuracy and layout correction pass*

These changes ensure the enhanced index.html accurately reflects the live website content at https://techsavanna.co.ke/ and fixes layout issues.

### What Was Changed

| # | Change | Location | Why |
|---|--------|----------|-----|
| 1 | **Centered Blog Articles** | Blog section `.row` | With only 2 articles (col-lg-4 each = 8 of 12 cols), they were left-aligned. Added `justify-content-center` to the row to center them horizontally. |
| 2 | **Fixed Testimonial #1 Author** | `.testimonal-slider` first item | Was "George Njuguna – CIO, Safaricom PLC" (duplicate). Changed to "Joe Doe – CIO, Safaricom PLC" to match the live website. |
| 3 | **Fixed "Deliver" Process Description** | Work Routine → Deliver card | Was incorrectly using the same text as Design ("We use design to create effective..."). Now reads: "We ensure seamless deployment, thorough testing, and comprehensive training so that the solution is successfully integrated into the customer's operations and delivers measurable results." |
| 4 | **Fixed "Training and Upskilling" Subtitle** | Solutions Carousel → Training card | Was incorrectly labeled "(Customer Relationship Management)". Changed to "(Professional Development & IT Training)" to accurately reflect the service. |
| 5 | **Added Organization Logos to Success Story Flip Cards** | All 4 `.ts-flip-card` front and back faces | Replaced generic Font Awesome icons with actual organization logos from the partner section assets: Safaricom (`logo-03.png`), Equity Bank (`logo-07.png`), Britam (`logo-04.png`), Stanbic Bank (`logo-05.png`). Front faces show dark logos (via `filter:brightness(0)`), back faces show white logos (via `filter:brightness(10)`). |
| 6 | **Added Integration Section** | Between Credentials and FAQ sections | The live website has an "Integration — We Collaborate with Top Software Company" section with 12 integration partner logos. This section was missing from the enhanced file and has now been added with all 12 logo images from `/assets/images/integations/1.png` through `12.png`. |

### Where in the Code

- **Blog centering:** Blog section `<div class="row">` → `<div class="row justify-content-center">`
- **Testimonial fix:** First `.testimonal-slider` item's `<h5>` and `<img alt="">` tags
- **Deliver description:** Work Routine section, last `.cta-card` paragraph
- **Training subtitle:** Solutions Carousel, Training card `<h4>` tag
- **Flip card logos:** Each `.ts-flip-card` front face `.ts-flip-icon` div and back face `<h4>` tag
- **Integration section:** New `<section class="integration-section bg-light-subtle ptb-120">` block inserted before the FAQ section

### Content Verification Checklist

The following content has been verified to match the live website (https://techsavanna.co.ke/):

- [x] Navigation menu items and links
- [x] Hero section title, subtitle, typing animation text
- [x] Hero CTA button ("Learn More" — enhanced from "Free Trial" which linked to an IP address)
- [x] Solutions carousel — all 8 products with correct images, titles, subtitles, descriptions
- [x] Partner logos — all 12 logos across 3 pages (Oracle, Good Firm, AWS, Microsoft 365, Azure, Equity, St John, Stanbic, Britam, Safaricom, KCB, Teenovators)
- [x] Video section — YouTube embed + 2 MP4 videos with Swiper
- [x] Success stories — section heading and description
- [x] Work routine — 4 process steps (Research, Build, Design, Deliver) — Deliver description fixed
- [x] Testimonials — now correctly shows "Joe Doe" and "George Njuguna" (matching live site)
- [x] Credentials — Data Protection, ISO 9001:2015, ICT Authority, Oracle (4 cards with modals)
- [x] Integration section — 12 partner logos (newly added)
- [x] Blog articles — 2 articles with correct titles, images, excerpts, dates
- [x] Footer — logo, description, resource links, solution links, newsletter, social media
- [x] Tawk.to chat widget

### Enhancement Additions (Not on Live Site)

These sections were added as enhancements and do not exist on the current live site:

| Section | Purpose |
|---------|---------|
| Animated Stats Counter | Shows key business metrics (500+ Projects, 150+ Clients, 12+ Years, 50+ Team) |
| 3D Flip Success Story Cards | Interactive case study cards with organization logos (replaces static text section) |
| FAQ Accordion | 6 common questions with expandable answers |
| Solution Category Tabs | Filter solutions by Enterprise / Management / Industry |
| Animated Progress Bars | Visual representation of process efficiency |
| Custom Cursor + Mouse Glow | Enhanced desktop cursor experience |
| Particle Network Canvas | Background ambient particle animation |
| 3D Tilt Cards | Interactive card hover effects |
| Magnetic Buttons | CTA buttons that attract toward cursor |
| Scroll Reveal Animations | Elements animate in on scroll |
| Ripple Effect on Buttons | Click feedback animation |
