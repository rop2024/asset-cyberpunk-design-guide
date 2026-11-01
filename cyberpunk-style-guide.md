# Cyberpunk Style Guide

## Design intent

Cyberpunk is a reusable dark interface system for products that need to feel precise, technical, fast, and slightly mechanical. It combines an almost-black canvas with controlled neon accents, condensed display type, monospace metadata, angular surfaces, and dense but readable information layouts.

The visual language is intentionally product-agnostic. It works for dashboards, developer tools, games, analytics, operations consoles, and other interfaces where status and hierarchy need to be scannable.

## Core tokens

### Color

| Token | Value | Use |
|---|---|---|
| `--bg` | `#080A0F` | Page background |
| `--surface-1` | `#0E1119` | Sidebar and recessed areas |
| `--surface-2` | `#141925` | Cards and panels |
| `--surface-3` | `#1B2230` | Hover surfaces and tracks |
| `--line` | `#293244` | Borders, rules, and chart grids |
| `--text` | `#F2F5F7` | Primary text |
| `--muted` | `#8D98A8` | Supporting text |
| `--dim` | `#566173` | Low-emphasis metadata |
| `--cyan` | `#00E5FF` | Information and links |
| `--yellow` | `#FCEE09` | Primary action and selection |
| `--green` | `#5DFF6A` | Healthy and successful states |
| `--magenta` | `#C44DFF` | Advanced or system content |
| `--pink` | `#FF3B7A` | Warning, negative, or destructive states |
| `--orange` | `#FF9F43` | Secondary comparison data |

Use one accent as the semantic identity of a component. Neon color should communicate meaning, not decorate every surface.

### Typography

- **Display:** Rajdhani, `500` and `700`; headings, navigation, values, and interface text.
- **Technical:** JetBrains Mono, `400` and `700`; labels, statuses, buttons, codes, filters, and measurements.
- Fallbacks: `Bahnschrift`, `Arial Narrow`, `Consolas`, or `Cascadia Mono`.
- Page titles: `clamp(2rem, 4vw, 3.5rem)`, uppercase, tight line-height.
- Technical labels: `0.68rem`, uppercase, `0.16em` tracking.
- Body copy: `1rem` to `1.15rem`; never uppercase long explanatory text.

Technical labels use the `// label` convention to establish a command-line voice.

### Shape and spacing

- Base spacing unit: `4px`.
- Standard panel padding: `20px`.
- Standard layout gap: `16px`.
- Panel corner cut: `14px` bottom-right.
- Focus ring: `2px solid var(--cyan)`, offset `3px`.
- Avoid soft rounded cards. Use angular corners, left-edge accents, and rules.

## Component rules

### Panels

Panels use `--surface-2`, a `1px` `--line` border, and a clipped bottom-right corner. A colored `4px` left rule identifies the panel's purpose. Every panel should contain a technical label, a clear content hierarchy, and optional metadata.

### Buttons and controls

- Primary action: yellow fill, dark text, bold monospace label, clipped corner.
- Secondary action: transparent background, `--line` border, cyan label.
- Selected control: cyan border and yellow text.
- Hover: increase border contrast; avoid large filled neon blocks.
- Focus: always provide a visible cyan outline.

### Status

Never communicate state by color alone. Pair color with a text label such as `ONLINE`, `QUEUED`, `SYNCED`, or `ERROR`.

### Data visualization

Use dashed `--line` grid lines, a single accent line, and a yellow current-value marker. Progress bars use a `6px` track, segmented dark separators, and a restrained accent glow.

## Layout patterns

The default shell is a two-column workspace: a `240px` navigation rail and a flexible content region. Use a four-column KPI row on wide screens, a `2fr 1fr` split for primary and secondary content, and consistent left alignment throughout.

At `900px` and below, collapse multi-column grids, wrap controls, and let the navigation rail become a compact top bar or drawer. Never remove active indicators, status text, or focus states.

## Quality checklist

- Contrast remains readable against dark surfaces.
- Headings follow a semantic order.
- Interactive elements use native buttons and links.
- Charts have an accessible label or adjacent summary.
- Status is communicated with text as well as color.
- Motion respects `prefers-reduced-motion`.
- Texture and glow remain subtle enough that they never compete with content.
