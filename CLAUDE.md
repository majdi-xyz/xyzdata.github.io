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
2. Hero - Direct value proposition with client logos and free audit offer
3. Expertise - Three core capabilities cards (what I do)
4. About - Personal story section (who I am, why I do this)
5. Services - Six service offerings in a grid
6. Approach - Three-step timeline showing methodology (includes free audit mention)
7. Contact - Two-column layout with free audit mention and Formspree form
8. Footer - Personal branding with "I get things done" tagline

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
- Background: Grew up in Paris ghetto, studied statistics at NUS Singapore, French engineering at ENSTA
- Experience: Founded Fairphonic, worked with Givaudan, Mooncard, lemlist, BGC Partners, Capitalab
- Expertise: Data engineering, Python pipelines, cloud infrastructure, AI/ML
- Philosophy: Problem-solver, not data enthusiast. Data is a tool, not a passion
- Approach: Hands-on builder who writes code and transfers knowledge
- Offer: First 30min audit call is free
- Based in Paris, works globally

**Writing Style:**
- Very short sentences. Fragment sentences are fine.
- No adjectives unless necessary. No adverbs ever.
- Concrete examples over abstract concepts
- "Build" not "architect", "fix" not "optimize", "works" not "solution"
- Remove words like "actually", "really", "truly", "innovative", "cutting-edge", "leverage"
- If it sounds like AI wrote it or like corporate marketing, delete it and start over
- Write like you're texting a friend, not pitching a client
