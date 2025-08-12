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
4. **Brand Colors**: Primary color #4338ca (deep indigo)
5. **Typography**: Inter font family throughout
6. **Logo**: Hexagonal tessellation pattern without padding

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

## Company Vision Context

Sintra Labs believes in the transformation of software delivery through AI, where:
- The 10x developer becomes the 100x developer
- Traditional software stacks collapse into cloud platform + AI flows
- One person with the right tools can outperform entire teams
- Tagline: "Where AI thinking becomes business value."

## Development Guidelines

1. Maintain extreme simplicity - resist adding complexity
2. Any changes should support the core message, not distract from it
3. Performance is critical - keep load times minimal
4. The vision content is the centerpiece - design serves the message