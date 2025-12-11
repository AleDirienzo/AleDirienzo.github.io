# Copilot Instructions for AleDirienzo.github.io

## Project Overview
This is a minimal, design-focused portfolio website for Max Ricci (designer/artist based in Lugano, Switzerland). Built with vanilla HTML/CSS/JavaScript—no frameworks or build tools. The site showcases 3 selected works with interactive hover effects.

## Architecture & Key Patterns

### File Structure
- **index.html** — Main portfolio page (only fully implemented page)
- **about.html, contact.html** — Currently empty placeholder files
- **README.md** — Minimal project description

### Design System (in index.html `<style>`)
- **Color scheme**: Dark theme (#0a0a0a background, #e0e0e0 text, #333 accents)
- **Typography**: Monospace font ('Helmet', 'Courier New') with consistent letter-spacing for uppercase text
- **Layout patterns**:
  - Fixed navigation bar (top, z-index: 1000)
  - Full-viewport hero section with large typography
  - Grid-based project list with fixed-position preview on desktop
  - Responsive breakpoints: 1024px (hide project previews), 768px (mobile refinements)

### JavaScript Interaction Pattern
- Simple event listener approach on `.project-item` elements
- Hover triggers opacity transitions on `#projectVisual` preview box
- Uses emoji icons (🕒, 🏛️, ✨) mapped by project index
- Mobile detection: `window.innerWidth > 1024` check disables visual preview

## Development Conventions

### HTML Structure
- Single-page semantic layout with `<nav>`, `<section>`, `<footer>`
- Data organization: Project info encoded in nested `<div>` classes (`.project-number`, `.project-title`, etc.)
- No templating—content is hardcoded

### Styling Approach
- Inline `<style>` block (no external CSS)
- CSS Grid for project list alignment (`grid-template-columns: 60px 1fr 200px 100px`)
- Extensive use of transitions (0.3s standard duration)
- Design tokens embedded: 2px letter-spacing for uppercase, 1px borders with #333 color
- Consistent padding: 5% horizontal margins, 4-8rem vertical sections

### Interactive Patterns
- Hover effects use `opacity` transitions and width expansion (nav underlines)
- DOM queries cached in variables (`.project-item`, `#projectVisual`)
- No external dependencies—vanilla DOM manipulation

## Common Tasks

**Update project list**: Modify `.project-item` divs in projects-section; add corresponding emoji to `icons` array in script.

**Adjust responsive breakpoints**: Edit `@media` queries in style block (currently 1024px and 768px).

**Complete placeholder pages**: about.html and contact.html are empty—use same nav/footer structure from index.html for consistency.

**Change color palette**: Update #0a0a0a, #e0e0e0, #333, #666, #888 values in CSS variables throughout style block.

## Notes for AI Agents
- This is a static site with no build process or dependencies—changes are immediately visible
- The GitHub Pages deployment model (.github.io repo) means changes to main branch auto-deploy
- About/contact pages need implementation but should mirror index.html's design system
- No version control workflow complexity expected
