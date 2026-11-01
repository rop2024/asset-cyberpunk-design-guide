# Cyberpunk Style Guide

A reusable dark interface design system for products that need to feel precise, technical, fast, and slightly mechanical.

## Files

| File | Purpose |
|------|---------|
| `cyberpunk-style-guide.html` | Live visual reference of colors, typography, components, states, and layout patterns |
| `cyberpunk-style-guide.css` | All design tokens (colors, type, spacing) and component styles |
| `cyberpunk-style-guide.md` | Written design intent, token table, component rules, layout patterns, and quality checklist |

## How to use

1. Open `cyberpunk-style-guide.html` in a browser to see the live style guide.
2. Reference `cyberpunk-style-guide.md` for design decisions and token definitions.
3. Copy variables from `cyberpunk-style-guide.css` into your own project to apply the cyberpunk visual language.

## Core tokens

- Background: `#080A0F`
- Primary text: `#F2F5F7`
- Cyan accent: `#00E5FF` (information, links)
- Yellow accent: `#FCEE09` (primary action, selection)
- Green: `#5DFF6A` (healthy states)
- Magenta: `#C44DFF` (system content)
- Pink: `#FF3B7A` (warning/danger)
- Orange: `#FF9F43` (secondary data)

Use one accent as the semantic identity of a component. Neon color communicates meaning, not decoration.

## Layout

Default shell is a two-column workspace: `240px` navigation rail plus flexible content region. At `900px` and below, grids collapse to a single column and the rail becomes a compact top bar or drawer.
