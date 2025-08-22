# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is the Sintra Labs website repository (sintra-labs.github.io) - a minimal, vision-focused landing page that communicates the company's transformative approach to AI-powered software delivery.

## Project Structure

```
/
├── index.html      # Main page with inspirational quote
├── vision.html     # Vision page detailing company philosophy
├── logo.svg        # Hexagonal tessellation logo
├── styles.css      # Minimal, futuristic styling
└── LANDING_PAGE_SPEC.md  # Original specification document
```

## Key Design Decisions

1. **Extreme Minimalism**: Focus on content with generous whitespace
2. **No JavaScript**: Pure HTML/CSS for fastest loading
3. **Two-page Structure**: Home (quote) and Vision pages only
4. **Color Scheme**: 
   - Primary: #1e3a8a (Midnight Blue) - conveys trust and technological depth
   - Accent: #06b6d4 (Cyan) - adds modern technological edge
   - Background alt: #f0f9ff (Ice Blue)
5. **Typography**: Inter font family throughout
6. **Logo**: Hexagonal tessellation pattern without padding, uses primary color
7. **No Tagline**: Removed to maintain cleaner design

## Commands

Since this is a static website:
- **Local Development**: Use `python -m http.server` or `npx serve` to preview
- **Deployment**: Push to main branch to deploy via GitHub Pages
- **No Build Process**: Direct HTML/CSS editing

## Architecture & Philosophy

- **Content-First**: The vision and message take precedence over visual effects
- **Fast Loading**: No frameworks, minimal dependencies
- **Responsive Design**: Mobile-first approach with clean breakpoints
- **Accessible**: Semantic HTML, proper contrast ratios, keyboard navigation
- **Visual Hierarchy**: Strategic use of color to guide attention

## Company Vision Context

Sintra Labs believes in the transformation of software delivery through AI, where:
- The 10x developer becomes the 100x developer
- Traditional software stacks collapse into cloud platform + AI flows
- One person with the right tools can outperform entire teams
- Focus on AI adoption for creating business value and insights

## Visual Design Elements

- **Navigation**: Animated underline on hover using accent color
- **Quote**: Displayed in primary color with decorative cyan quotation marks
- **Vision Page**: Section headings with cyan accent borders
- **Interactive Elements**: Cyan focus states and text selection
- **Subtle gradient background**: Midnight blue to cyan at low opacity

## Development Guidelines

1. Maintain extreme simplicity - resist adding complexity
2. Any changes should support the core message, not distract from it
3. Performance is critical - keep load times minimal
4. The vision content is the centerpiece - design serves the message
5. Color usage should reinforce hierarchy and guide user attention
6. Preserve the clean, professional aesthetic