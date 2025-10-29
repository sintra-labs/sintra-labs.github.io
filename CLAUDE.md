# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is the Sintra Labs website repository (sintra-labs.github.io) - a minimal, vision-focused landing page that communicates the company's transformative approach to AI-powered software delivery. Features a complete dark/light mode implementation with theme-aware logo switching.

## Project Structure

```
/
├── index.html              # Main page with inspirational quote
├── vision.html             # Vision page detailing company philosophy
├── public/                 # Static assets folder
│   ├── css/
│   │   └── styles.css      # Minimal, futuristic styling with dark mode support
│   ├── js/
│   │   └── theme.js        # JavaScript theme management with persistence
│   └── images/
│       ├── logo.svg               # Logo icon only - light mode (midnight blue)
│       ├── logo-dark.svg          # Logo icon only - dark mode (light blue)
│       ├── logo-with-text.svg     # Logo with "Sintra Labs" text - light mode
│       ├── logo-dark-with-text.svg # Logo with "Sintra Labs" text - dark mode
│       ├── logo.png               # Legacy square PNG version
│       ├── logo-light.png         # PNG icon only - light (500px, transparent)
│       ├── logo-dark.png          # PNG icon only - dark (500px, transparent)
│       ├── logo-with-text.png     # PNG with text - light (1200px, transparent)
│       ├── logo-dark-with-text.png # PNG with text - dark (1200px, transparent)
│       ├── favicon.svg            # SVG favicon
│       ├── favicon-32x32.png
│       └── favicon-16x16.png
├── misc/                   # Miscellaneous files (ignored by git)
│   └── Inter.zip           # Inter font for logo text rendering
├── LANDING_PAGE_SPEC.md    # Original specification document
└── CLAUDE.md               # This file - development guidelines
```

## Key Design Decisions

1. **Extreme Minimalism**: Focus on content with generous whitespace
2. **JavaScript-Powered Dark Mode**: Clean theme switching with localStorage persistence
3. **Two-page Structure**: Home (quote) and Vision pages only
4. **Organized Assets**: All static assets in `/public` folder (css, js, images)
5. **Color Scheme**:
   - Light: Primary #1e3a8a (midnight blue), accent #06b6d4 (cyan)
   - Dark: Primary #60a5fa (light blue), accent #06b6d4 (cyan)
   - Backgrounds adapt accordingly for optimal contrast
6. **Typography**: Inter font family throughout
7. **Theme-Aware Logo**: Automatically switches between light/dark versions
8. **Clickable Branding**: Logo and title link to home page

## Commands

Since this is a static website:
- **Local Development**: Use `python -m http.server` or `npx serve` to preview
- **Deployment**: Push to main branch to deploy via GitHub Pages
- **No Build Process**: Direct HTML/CSS editing
- **Asset Organization**: All static assets organized in `/public` folder (css, js, images)

## Dark Mode Implementation

### Theme Management (public/js/theme.js):
- **ThemeManager class**: Handles all theme logic
- **Smart initialization**: Checks localStorage → system preference → defaults to light
- **Persistence**: User preference saved across page navigation
- **System awareness**: Responds to OS theme changes when no manual preference set

### CSS Structure (public/css/styles.css):
- **CSS Custom Properties**: All colors defined as variables in `:root`
- **Dark theme override**: `[data-theme="dark"]` selector updates all variables
- **Logo switching**: Uses `content: url('../images/logo-dark.svg')` to swap SVG files
- **Smooth transitions**: All theme changes are animated (0.3s ease)

### Theme Toggle:
- **Visual design**: Pill-shaped toggle with sliding indicator
- **Icons**: Sun/moon icons with opacity changes
- **Accessibility**: Proper ARIA labels and keyboard support

## Architecture & Philosophy

- **Content-First**: The vision and message take precedence over visual effects
- **Fast Loading**: Minimal JavaScript, no frameworks, optimized assets
- **Responsive Design**: Mobile-first approach with clean breakpoints
- **Accessible**: Semantic HTML, proper contrast ratios, keyboard navigation
- **Visual Hierarchy**: Strategic use of color and typography to guide attention
- **Theme Consistency**: All elements adapt seamlessly between light/dark modes

## Company Vision Context

Sintra Labs believes in the transformation of software delivery through AI, where:
- The 10x developer becomes the 100x developer
- Traditional software stacks collapse into cloud platform + AI flows
- One person with the right tools can outperform entire teams
- Focus on AI adoption for creating business value and insights

## Visual Design Elements

### Light Mode:
- **Navigation**: Animated cyan underlines on hover
- **Quote**: Midnight blue text with subtle cyan quotation marks
- **Vision sections**: Midnight blue headings with cyan accent borders
- **Logo**: Midnight blue hexagonal tessellation

### Dark Mode:
- **Backgrounds**: Deep navy (#0f172a) with subtle texture
- **Text**: Light colors for optimal readability
- **Accents**: Cyan (#06b6d4) maintains consistency across themes
- **Logo**: Light blue hexagonal tessellation for contrast

### Interactive Elements:
- **Hover effects**: Subtle opacity and color changes
- **Focus states**: Cyan outline for accessibility
- **Text selection**: Cyan background
- **Smooth transitions**: All state changes are animated

## Development Guidelines

1. **Maintain extreme simplicity** - resist adding complexity
2. **Theme-aware development** - ensure all new elements work in both themes
3. **Test both themes** - always verify light and dark mode appearance
4. **Preserve performance** - keep load times minimal
5. **Logo consistency** - use appropriate logo version for each theme
6. **Color usage** - stick to CSS custom properties for theme compatibility
7. **Accessibility first** - maintain proper contrast ratios in both themes

## File Management Notes

- **Active logos**:
  - **Icon only**:
    - SVG: `public/images/logo.svg` (light mode), `public/images/logo-dark.svg` (dark mode)
    - PNG: `public/images/logo-light.png` (light mode, 500px, transparent), `public/images/logo-dark.png` (dark mode, 500px, transparent)
  - **With text "Sintra Labs"**:
    - SVG: `public/images/logo-with-text.svg` (light mode), `public/images/logo-dark-with-text.svg` (dark mode)
    - PNG: `public/images/logo-with-text.png` (light mode, 1200px, transparent), `public/images/logo-dark-with-text.png` (dark mode, 1200px, transparent)
    - Text specs: Inter font, weight 600, size 36px, letter-spacing -0.02em
  - **Legacy**: `public/images/logo.png` (original square version)
- **Favicons**: All favicon files stored in `public/images/`
- **Asset paths**: All HTML files reference assets via `public/` folder structure
- **CSS paths**: Use relative paths from CSS location (e.g., `../images/logo-dark.svg`)
- **Theme persistence**: Handled entirely by JavaScript, no server-side requirements
- **Asset optimization**: All SVGs are optimized and use semantic markup
- **PNG generation**:
  - **Simple conversion**: `npx @resvg/resvg-js-cli --fit-width 500 <input.svg> <output.png>`
  - **With Inter font** (for logos with text):
    ```bash
    npx @resvg/resvg-js-cli \
      --font-file ~/Library/Fonts/Inter_24pt-SemiBold.ttf \
      --font-file ~/Library/Fonts/Inter_24pt-Bold.ttf \
      --font-default-family "Inter" \
      --font-sans-serif-family "Inter" \
      --no-system-font \
      --fit-width 1200 \
      <input.svg> <output.png>
    ```
  - **Inter font installation**: Inter font must be installed from `misc/Inter.zip` to `~/Library/Fonts/` for correct text rendering