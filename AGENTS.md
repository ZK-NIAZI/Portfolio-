## Agent Instructions for Portfolio Website

This is a single-page portfolio website for Zeeshan Khan, a Flutter Developer.

**Project Structure:**
- `index.html`: Main HTML file containing all content.
- `styles.css`: Main stylesheet.
- `animations.js`: Handles JavaScript-based animations, smooth scrolling, and mobile menu functionality.
- `logo.png`: Profile image used as the logo and in the "About Me" section.
- `linkedin-icon.svg`, `github-icon.svg`: SVG icons used in the contact section.

**Key Considerations When Modifying:**

1.  **Responsiveness:** The site uses CSS flexbox, grid, and media queries for responsiveness. Ensure any new sections or style changes are tested across common breakpoints (mobile, tablet, desktop). Media queries are primarily in `styles.css` towards the end.
2.  **JavaScript Animations:**
    *   Scroll-triggered animations are handled by an IntersectionObserver in `animations.js`. New elements that need to be animated on scroll should be added to the `animatedElements` querySelectorAll list and have the initial `opacity: 0; transform: translateY(30px);` style applied (as seen in `styles.css` for existing animated elements). The `.visible` class will be added by JS.
    *   Smooth scrolling is implemented for navigation links. If new sections are added, ensure their IDs match the `href` in the navigation.
3.  **Navigation:**
    *   The main navigation is in `index.html` within the `<nav class="navbar">`.
    *   Mobile navigation is handled by JS toggling an `.active` class on `.nav-links` and `.hamburger-menu`.
    *   Active link highlighting based on scroll position is also handled in `animations.js`.
4.  **Content Updates:**
    *   Personal details, project descriptions, and experience are directly in `index.html`.
    *   Project and experience dates were intentionally set to future dates as per user request. If this needs to be changed to past dates, update the relevant text in `index.html`.
5.  **Image Optimization:** The `logo.png` image could be further optimized. If replaced or new images are added, ensure they are optimized for the web to maintain fast loading times.
6.  **CSS Variables:** Colors and some common properties are defined as CSS variables at the root of `styles.css`. Utilize these for consistency.

**Validation:**
- Before submitting changes, it's good practice to validate HTML and CSS using online tools (e.g., W3C validators).

Following these guidelines will help maintain the integrity and functionality of the website.
