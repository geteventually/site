# Eventually — Tokens

Canonical values for the marketing site and brand surfaces. Prefer these names over raw hex in new CSS.

## Color

| Token | Value | Usage |
|-------|-------|-------|
| `color-bg` | `#ffffff` | Page background (stark white — locked) |
| `color-fg` | `#000000` | Primary text, CTAs fill, rules |
| `color-accent` | `#fffd01` | Highlighter — selection, rare emphasis |
| `color-fg-muted` | `rgba(0, 0, 0, 0.6)` | Tagline, copyright (~opacity 0.6) |
| `color-fg-subtle` | `rgba(0, 0, 0, 0.4)` | Blurbs under hero (~opacity 0.4) |
| `color-surface-soft` | `rgba(0, 0, 0, 0.02)` | Soft pads / bands only if needed |
| `color-cta-fg` | `#ffffff` | Text on black buttons |
| `color-cta-bg` | `#000000` | Primary button fill |

### Rules

- **Core triad only:** white, black, highlighter yellow.  
- Do **not** introduce sky blue (`#0ea5e9`) or other accents on legal/support pages — match this palette.  
- Accent is scarce: selection + intentional moments, not large fills.  
- Body text on white and white text on black CTA meet strong contrast; never put `#fffd01` text on white for small copy.

## Typography

Open Sans is **retired** for brand work. Use:

| Token | Value | Role |
|-------|-------|------|
| `font-sans` | `"DM Sans", system-ui, sans-serif` | Primary UI + marketing type (calm, sharp) |
| `font-brand` | `"Instrument Serif", Georgia, serif` | Wordmark / `<brand>` — italic signature |
| `font-weight-regular` | `400` | Body, notes |
| `font-weight-medium` | `500` | Masthead, emphasis |
| `font-weight-semibold` | `600` | Headlines (replace invalid `599`) |
| `font-weight-bold` | `700` | CTA labels |

### Scale (marketing)

| Token | Value | Usage |
|-------|-------|-------|
| `text-masthead` | `27px` / `1.19` | Top wordmark area |
| `text-hero` | `clamp(3.75rem, 1.0714rem + 8.5714vw, 7.5rem)` / `1.05` / `-1.2px` tracking | Hero only |
| `text-display` | `clamp(2.75rem, 1.0714rem + 5.7143vw, 5.5rem)` / `1.05` / `-0.78px` | Mid-page display beats (use sparingly) |
| `text-body` | `16px` / `1.5` | Blurbs, notes, footer |
| `text-cta` | `22px` / weight `700` / `1px` tracking | Buttons |

**Hierarchy rule:** Hero uses `text-hero`. At most **one** mid-page band at `text-display`. Supporting beats step down to `text-body` or a modest larger body (~20–24px), not five identical display blocks.

## Spacing & layout

| Token | Value | Usage |
|-------|-------|-------|
| `shell-max` | `1236px` | Content max width |
| `space-masthead-top` | `20vh` | Breath above masthead |
| `space-masthead-bottom` | `4vh` | Masthead → hero |
| `space-display-pad` | `80px` | Vertical pad for display sections |
| `space-cta-block` | `20px` | CTA stack rhythm |
| `radius-cta` | `20px` | Primary buttons |
| `radius-pad` | `60px` | Soft band corners (if used) |

## Motion

| Token | Value | Usage |
|-------|-------|-------|
| `motion-cta` | `transform 0.17s ease-out` | Button hover scale |
| `motion-cta-hover-scale` | `1.05` | Hover |

Keep motion small and purposeful (CTA + prop states). No ambient glow loops.

## Imagery

| Token / rule | Spec |
|--------------|------|
| `prop-size` | `110×110px` (inline balloons / saved badge) |
| Props | Real photos, object-fit contain; signature forever |
| Alt text | Descriptive; decorative props may use short labels but prefer meaningful alts |

## CSS variables (implement)

```css
:root {
  --color-bg: #ffffff;
  --color-fg: #000000;
  --color-accent: #fffd01;
  --color-fg-muted: rgba(0, 0, 0, 0.6);
  --color-fg-subtle: rgba(0, 0, 0, 0.4);
  --color-surface-soft: rgba(0, 0, 0, 0.02);
  --color-cta-fg: #ffffff;
  --color-cta-bg: #000000;

  --font-sans: "DM Sans", system-ui, sans-serif;
  --font-brand: "Instrument Serif", Georgia, serif;

  --shell-max: 1236px;
  --radius-cta: 20px;
  --radius-pad: 60px;
  --motion-cta: transform 0.17s ease-out;
}
```

## Downloads / platforms

| Platform | Status |
|----------|--------|
| Chrome | Primary CTA (URL TBD — wire real store link) |
| Safari | Coming soon |
| Firefox | Coming soon |

## Legal

Marketing: **Eventually**.  
Entity line (later): Becomes Tech LLC — footer/legal only when added.

## Related

`mood.md` · `voice.md`
