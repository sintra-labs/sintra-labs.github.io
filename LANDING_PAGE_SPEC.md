# Sintra Labs Landing Page Specification

## Overview
A minimal landing page for Sintra Labs, focused on the transformative vision of AI-powered software delivery and the Agentic Data Platform.

## Page Structure

### Navigation Order
Home | Vision | Product | About Us | Contact

### 1. Home Page (index.html)
- **Header**:
  - "Sintra Labs" (logo + text)
  - Navigation: Home | Vision | Product | About Us | Contact
  - Dark mode toggle
- **Quote Section**:
  - Inspirational quote: "The best way to predict the future is to invent it." - Alan Kay
  - Quote attribution
  - Takes up 60vh (60% of viewport height)
  - Centered vertically and horizontally
  - Appears above card stack as introduction
- **Page Previews Section**:
  - Three cards stacked vertically with scroll-triggered animations:
    - **Our Vision**: Comprehensive description of AI transformation (2 paragraphs, slides in from left)
    - **Our Product**: Detailed Agentic Data Platform overview (2 paragraphs, slides in from right)
    - **About Us**: Full team introduction and expertise (2 paragraphs, slides in from left)
  - Cards appear on scroll with horizontal slide animation
  - Uses Intersection Observer API for scroll detection
  - Smooth transitions with cubic-bezier easing
  - Cards start hidden and animate to visible when scrolled into view
  - Each card has expanded content with multiple paragraphs
  - Call-to-action links: "Explore our vision →", "Discover the platform →", "Meet the team →"
- **Footer**: Enhanced footer (see below)

### 2. Vision Page (vision.html)
- **Header**: Same as home page (Navigation: Home | Vision | Product | About Us | Contact)
- **Content Structure**:
  - **Page Title**: "Our Vision"
  - **Opening Statement**: The transformation of software delivery
  - **Core Vision**:
    - The dramatic transformation in software delivery
    - From 10x to 100x developers
    - Automation of entire software layers
  - **The New Paradigm**:
    - Traditional stack collapse
    - Two-layer future: cloud platform + AI flows
    - Natural language to custom applications
  - **Our Approach**:
    - Building the software stack that builds software
    - Guiding customers through the shift
    - The power of interdisciplinary expertise
  - **Closing**: "Where AI thinking becomes business value."
- **Footer**: Enhanced footer (see below)

### 3. Product Page (product.html)
- **Header**: Same as home page (Navigation: Home | Vision | Product | About Us | Contact)
- **Content Structure**:
  - **Page Title**: "Agentic Data Platform"
  - **Subtitle**: "Autonomous Enterprise Intelligence"
  - **The Problem**:
    - Enterprise data projects are expensive and time-consuming
    - Require large teams for manual data integration
    - Traditional ETL processes take months
  - **The Solution**:
    - AI-powered autonomous data engineering
    - Fully automated Extract, Transform, Load processes
    - Business experts focus on decisions, not engineering
  - **Key Benefits**:
    - Light-Speed to Insights: Days instead of months
    - Radical Cost Optimization: AI automates integration work
    - Adaptive & Secure: Self-contained, self-managed system
    - Broadening Access: Makes analytics economically viable
- **Footer**: Enhanced footer (see below)

### 4. About Us Page (about.html)
- **Header**: Same as home page
- **Content Structure**:
  - **Page Title**: "About Us"
  - **Our Team**:
    - Founded by experts in technology and data
    - 3 Founders with deep tech and data backgrounds
    - 1 Advisor with extensive IBM sales and HR experience
    - Combined expertise in engineering, product, and AI
  - **Our Mission**:
    - Building the future of autonomous enterprise intelligence
    - Transforming how businesses leverage their data
- **Footer**: Enhanced footer (see below)

### 5. Contact Page (contact.html)
- **Header**: Same as home page (Navigation: Home | Vision | Product | About Us | Contact)
- **Content Structure**:
  - **Page Title**: "Get in Touch"
  - **Sections**:
    - General Inquiries: info@sintralabs.com
    - Business & Partnerships: business@sintralabs.com
    - Legal & Compliance: legal@sintralabs.com
    - Location: Portugal
- **Footer**: Enhanced footer (see below)

### 6. Legal Terms Page (legal.html)
- **Header**: Same as home page (Navigation: Home | Vision | Product | About Us | Contact)
- **Content Structure**:
  - **Page Title**: "Legal Terms"
  - **Sections**:
    - Terms of Service (placeholder)
    - Privacy Policy (placeholder)
    - Data Processing Terms (placeholder)
    - Security Policy (placeholder)
    - Contact information
- **Footer**: Enhanced footer (see below)

## Enhanced Footer

All pages include an enhanced footer with three columns:

**Product Section:**
- Agentic Data Platform
- Our Vision

**Company Section:**
- About Us
- Contact

**Legal Section:**
- Terms & Privacy

**Footer Bottom:**
- Copyright © 2025 Sintra Labs. All rights reserved.

## Design Requirements

### Visual Style
- **Aesthetic**: Minimal, futuristic, confident
- **Color Scheme**: 
  - Primary: Deep blue or purple (suggesting depth/intelligence)
  - Accent: Bright accent for CTAs
  - Background: White/off-white
  - Text: Near-black for readability
- **Typography**:
  - Modern sans-serif (e.g., Inter, SF Pro)
  - Large, confident sizing
  - Generous line-height
  - Strategic use of bold

### Layout Principles
- Extreme minimalism
- Focus on whitespace
- Content-first approach
- No unnecessary elements

### Responsive Design
- Mobile-first
- Single column on mobile
- Readable without horizontal scrolling
- Touch-friendly navigation

## Technical Requirements
- Pure HTML/CSS (no frameworks needed)
- Blazing fast load times
- Semantic HTML5
- CSS Grid/Flexbox for layout
- SSL/HTTPS required

## Content Guidelines
- **Tone**: Visionary yet grounded, confident but not arrogant
- **Language**: Clear, direct, avoiding jargon where possible
- **Focus**: The transformation, not the technology
- **Message**: One person with the right tools can change everything

## Implementation Notes
- Start with the vision as the centerpiece
- Let the content breathe with ample whitespace
- Navigation should be subtle, not distract from content
- Consider subtle animations on scroll (optional)
- Ensure the revolutionary nature of the vision comes through