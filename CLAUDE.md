# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is the personal website for Majdi Rabia (xyzdata), a freelance data engineering and analytics consultant. The site is a static, single-page application built with vanilla HTML and CSS (no build tools or frameworks).

**Brand Voice:** Direct, conversational, first-person ("I" not "we"). Majdi's tagline is "I get things done"—the site should reflect action-oriented pragmatism with technical credibility. No corporate speak or marketing fluff.

## Architecture

**Static Single-Page Site:**
- `index.html` - Main HTML file containing all page sections
- `styles.css` - Complete stylesheet with responsive design
- SVG/PNG assets for branding

**Page Structure:**
The site follows a single-page layout with anchor navigation:
1. Header - Sticky navigation with logo and section links
2. Hero - Main value proposition with client logos
3. Expertise - Three core capabilities cards
4. Services - Six detailed service offerings in a grid
5. Approach - Three-step timeline showing methodology
6. Contact - Two-column layout with info and Formspree form
7. Footer - Branding and copyright

**Design System:**
CSS custom properties in `:root` define the color palette and design tokens:
- Primary blue (`--primary: #0066FF`) for CTAs and accents
- Dark theme (`--dark: #0A0A0F`) for text and backgrounds
- Gray scale system (`--gray-50` through `--gray-900`)
- Accent colors for hover states (purple, pink)

**Responsive Breakpoints:**
- Desktop: Default (1280px max-width container)
- Tablet: 1024px and below
- Mobile: 768px and below
- Small mobile: 480px and below

## Development

**Local Development:**
This is a static site with no build process. Open `index.html` directly in a browser or use a local server:
```bash
# Python 3
python3 -m http.server 8000

# Node (if http-server is installed)
npx http-server -p 8000
```

**Contact Form:**
The contact form submits to Formspree at `https://formspree.io/f/xblvdnrq`. Form handling is external; no backend code in this repository.

## Key Patterns

**CSS Organization:**
Styles are organized by component/section with clear comment headers. Each section follows the pattern:
- Reset/base styles at top
- Component-specific styles grouped together
- Responsive overrides at bottom in media queries

**Hover Interactions:**
Most interactive elements use subtle transforms and shadows:
- Cards: `translateY(-8px)` on hover with shadow
- Buttons: `translateY(-2px)` with colored glow
- Icons: Background color transitions

**Gradient Effects:**
- Hero section uses animated radial gradient blob (`.hero-gradient`) with CSS keyframe animation
- Timeline connectors use vertical gradients fading to transparent

## Content Guidelines

**Voice & Tone:**
- Always use first-person "I" (Majdi speaking directly)
- Direct and conversational—like talking to a colleague, not a client
- Action-oriented: focus on what gets done, not what could be done
- Honest and pragmatic: acknowledge tradeoffs, no overselling
- Technical credibility without jargon

**About Majdi:**
- Background: Statistics (NUS Singapore) + French engineering (ENSTA)
- Experience: Founder (Fairphonic), consultant to Givaudan, Looping Group
- Expertise: Data engineering, Python pipelines, cloud infrastructure, AI/ML
- Approach: Hands-on builder who writes code and transfers knowledge
- Based in Paris, works globally

**Writing Style:**
- Short, punchy sentences
- Concrete examples over abstract concepts
- "Build" not "architect", "fix" not "optimize", "works" not "solution"
- If it sounds like corporate marketing, rewrite it
