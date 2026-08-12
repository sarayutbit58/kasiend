# KasienD Design System (Master)

Source: ui-ux-pro-max guidelines + product constraints (static HTML, Thai Sarabun, vibrant/friendly, mobile-first).

## Product
- Personal finance education tool (Thailand)
- Single-page journey: EF → Compound → Retirement + knowledge tools
- Audience: non-technical Thai users, mobile primary

## Style
- Friendly / soft-trust finance (not dark bank terminal)
- Vibrant accents on calm surfaces
- Soft cards, 12–20px radius, light elevation

## Tokens
| Token | Value | Use |
|---|---|---|
| `--brand` | #0f766e | Primary brand / success path |
| `--brand-soft` | #ccfbf1 | Brand backgrounds |
| `--accent` | #2563eb | Interactive primary |
| `--bg` | #f0f4f8 | Page background |
| `--surface` | #ffffff | Cards |
| `--text` | #0f172a | Body |
| `--muted` | #475569 | Secondary (≥3:1 on surface) |
| `--space-1..6` | 4/8/12/16/24/32 | 4–8 rhythm |
| `--radius` | 14px | Cards |
| `--touch` | 44px | Min control height |
| `--font` | Sarabun, system-ui | Thai-first |

## Layout
- Max content width 640px
- Mobile-first; sticky bottom nav ≤5 items
- Safe-area padding on fixed nav
- Progressive disclosure: core 3 stages always visible; knowledge tools grouped

## Motion
- 150–250ms ease
- `prefers-reduced-motion: reduce` disables non-essential animation

## A11y
- Focus ring 3px brand
- Labels on all inputs
- Skip link to main
- Color not sole status indicator (text + icons)
