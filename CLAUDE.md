# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is the Sintra Labs website repository (sintra-labs.github.io) - a minimal, vision-focused landing page that communicates the company's transformative approach to AI-powered software delivery. Features a complete dark/light mode implementation with theme-aware logo switching.

## Project Structure

```
/
├── index.html              # Main page with inspirational quote
├── vision.html             # Vision page detailing company philosophy
├── styles.css              # Minimal, futuristic styling with dark mode support
├── theme.js                # JavaScript theme management with persistence
├── logo.svg                # Original logo (midnight blue) for light mode
├── logo-dark.svg           # Dark mode logo (light blue)
├── logo.png                # Square PNG version for external use
├── LANDING_PAGE_SPEC.md    # Original specification document
└── [legacy logo files]    # Various logo experiments (can be cleaned up)
```

## Key Design Decisions

1. **Extreme Minimalism**: Focus on content with generous whitespace
2. **JavaScript-Powered Dark Mode**: Clean theme switching with localStorage persistence
3. **Two-page Structure**: Home (quote) and Vision pages only
4. **Color Scheme**: 
   - Light: Primary #1e3a8a (midnight blue), accent #06b6d4 (cyan)
   - Dark: Primary #60a5fa (light blue), accent #06b6d4 (cyan)
   - Backgrounds adapt accordingly for optimal contrast
5. **Typography**: Inter font family throughout
6. **Theme-Aware Logo**: Automatically switches between light/dark versions
7. **Clickable Branding**: Logo and title link to home page

## Commands

Since this is a static website:
- **Local Development**: Use `python -m http.server` or `npx serve` to preview
- **Deployment**: Push to main branch to deploy via GitHub Pages
- **No Build Process**: Direct HTML/CSS editing

## Dark Mode Implementation

### Theme Management (theme.js):
- **ThemeManager class**: Handles all theme logic
- **Smart initialization**: Checks localStorage → system preference → defaults to light
- **Persistence**: User preference saved across page navigation
- **System awareness**: Responds to OS theme changes when no manual preference set

### CSS Structure:
- **CSS Custom Properties**: All colors defined as variables in `:root`
- **Dark theme override**: `[data-theme="dark"]` selector updates all variables
- **Logo switching**: Uses `content: url()` to swap SVG files
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

- **Active logos**: `logo.svg` (light mode), `logo-dark.svg` (dark mode), `logo.png` (external use)
- **Legacy files**: Several experimental logo files exist and can be cleaned up
- **Theme persistence**: Handled entirely by JavaScript, no server-side requirements
- **Asset optimization**: All SVGs are optimized and use semantic markup