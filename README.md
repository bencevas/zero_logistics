# ZERO° LOGISTICS — Design System

A modern UI kit for cold-chain logistics applications featuring glassmorphism, clean typography, and an icy color palette.

## Quick Start

```html
<!-- 1. Add Google Fonts -->
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
<link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600;700;800;900&family=Open+Sans:ital,wght@0,300;0,400;0,600;1,300;1,400&family=Azeret+Mono:wght@300;400;500&display=swap" rel="stylesheet" />

<!-- 2. Import the design system -->
<link rel="stylesheet" href="zero-design-system.css" />
```

## Live Preview

View the full design system at: [zero-logistics.vercel.app](https://zero-logistics.vercel.app)

---

## Brand Identity

### Logo

The ZERO° LOGISTICS logo uses Montserrat Bold with a specific size ratio:

```html
<div class="logo-mark lm-blue">
  <span class="ln1">ZERO°</span>
  <span class="ln2">LOGISTICS</span>
</div>
```

| Element | Font | Size | Weight |
|---------|------|------|--------|
| ZERO° | Montserrat | 52px | 700 |
| LOGISTICS | Montserrat | 32px | 700 |

**Logo Variants:**
- `.lm-blue` — Primary blue (#0085CA)
- `.lm-white` — White (for dark backgrounds)
- `.lm-dark` — Carbon black (#0D0D0D)
- `.lm-grad` — Blue to glacier gradient

---

## Color Palette

### Primary Colors

| Name | Variable | Hex | Usage |
|------|----------|-----|-------|
| Blue | `--zero-blue` | `#0085CA` | Primary brand color, CTAs |
| Glacier | `--zero-glacier` | `#00B4E6` | Accents, gradients |
| Deep | `--zero-deep` | `#004E7C` | Hover states, contrast |

### Neutrals

| Name | Variable | Hex | Usage |
|------|----------|-----|-------|
| Carbon | `--zero-carbon` | `#0D0D0D` | Primary text |
| White | `--zero-white` | `#FFFFFF` | Backgrounds |
| Ice | `--zero-ice` | `#F0F7FB` | Light backgrounds, widgets |

### Text Colors

| Name | Variable | Value | Usage |
|------|----------|-------|-------|
| Text | `--zero-text` | `#0D0D0D` | Headings, primary text |
| Muted | `--zero-muted` | `rgba(0,0,0,0.52)` | Body text, descriptions |
| Dim | `--zero-dim` | `rgba(0,0,0,0.30)` | Labels, tertiary text |

### Status Colors

| Name | Variable | Hex | Usage |
|------|----------|-----|-------|
| Success | `--zero-success` | `#10B981` | In range, delivered |
| Warning | `--zero-warning` | `#F59E0B` | Attention needed |
| Danger | `--zero-danger` | `#EF4444` | Alerts, failures |

---

## Typography

### Font Stack

| Purpose | Font Family | Variable |
|---------|-------------|----------|
| Headings, Logo, Numbers | Montserrat | `--font-heading` |
| Body Text | Open Sans | `--font-body` |
| Labels, Technical Data | Azeret Mono | `--font-mono` |

### Type Scale

```css
--text-xs:    10px;   /* Labels */
--text-sm:    12px;   /* Small text */
--text-base:  14px;   /* Base size */
--text-md:    16px;   /* Body text */
--text-lg:    18px;   /* Large body */
--text-xl:    24px;   /* H4 */
--text-2xl:   32px;   /* H3 */
--text-3xl:   40px;   /* H2 */
--text-4xl:   52px;   /* H1 */
```

### Usage Examples

```html
<!-- Heading -->
<h2 style="font-family: var(--font-heading); font-weight: 700;">
  Cold-Chain Excellence
</h2>

<!-- Body text -->
<p style="font-family: var(--font-body); color: var(--zero-muted);">
  Real-time temperature monitoring across your supply chain.
</p>

<!-- Label -->
<span style="font-family: var(--font-mono); font-size: 10px; 
             letter-spacing: 0.14em; text-transform: uppercase;">
  SHIPMENT ID
</span>
```

---

## Glassmorphism

The signature effect of ZERO° UI. Use on light backgrounds for the frosted-glass look.

### Standard Glass

```html
<div class="glass">
  <!-- Content -->
</div>
```

```css
.glass {
  background: rgba(255,255,255,0.62);
  backdrop-filter: blur(20px);
  border: 1px solid rgba(255,255,255,0.88);
  border-radius: 16px;
  box-shadow: 0 8px 32px rgba(0,133,202,0.10);
}
```

### Dark Glass (on images/dark backgrounds)

```html
<div class="glass-dark">
  <!-- Content -->
</div>
```

```css
.glass-dark {
  background: rgba(255,255,255,0.05);
  backdrop-filter: blur(20px);
  border: 1px solid rgba(255,255,255,0.12);
}
```

---

## Components

### Buttons

```html
<!-- Primary -->
<button class="btn btn-primary">Track Shipment</button>

<!-- Ghost -->
<button class="btn btn-ghost">Learn More</button>
```

### Status Badges

```html
<div class="status-badge status-badge--primary">
  <span class="status-dot"></span>
  <span>In Transit</span>
</div>

<div class="status-badge status-badge--success">
  <span class="status-dot"></span>
  <span>Delivered</span>
</div>
```

### Dashboard Tiles

```html
<div class="dash-tile">
  <div class="dash-tile-label">Active Shipments</div>
  <div class="dash-tile-value">1,247</div>
</div>
```

### Widget Tiles (1:1)

```html
<div class="widget-tile">
  <div class="widget-bg"></div>
  <!-- Your content (map, chart, etc.) -->
  <div class="widget-info">
    <div>
      <div class="widget-info-label">Current</div>
      <div class="widget-info-value">Amsterdam Hub</div>
    </div>
    <div class="widget-info-badge">−20°C</div>
  </div>
</div>
```

---

## Spacing System

```css
--space-xs:   4px;
--space-sm:   8px;
--space-md:   16px;
--space-lg:   24px;
--space-xl:   32px;
--space-2xl:  48px;
--space-3xl:  64px;
--space-4xl:  100px;
```

---

## Border Radius

```css
--radius-sm:   8px;    /* Buttons, small cards */
--radius-md:   12px;   /* Medium cards */
--radius-lg:   16px;   /* Glass panels, widgets */
--radius-xl:   20px;   /* Large cards */
--radius-full: 9999px; /* Pills, badges */
```

---

## Layout

### Container

```html
<div class="container">
  <!-- Max-width: 1160px, padding: 48px -->
</div>
```

### Section Headers

```html
<p class="section-tag">01 — Overview</p>
<h2 class="section-title">Cold-Chain Excellence</h2>
<p class="section-desc">
  Real-time temperature monitoring across your entire supply chain.
</p>
```

---

## Responsive Breakpoints

| Breakpoint | Width | Adjustments |
|------------|-------|-------------|
| Desktop | > 1024px | Full layout |
| Tablet | ≤ 1024px | Reduced padding (32px) |
| Mobile | ≤ 768px | Compact layout (20px padding) |
| Small Mobile | ≤ 480px | Smallest type scale |

---

## File Structure

```
zero_logistics/
├── index.html              # Full design system showcase
├── zero-design-system.css  # Standalone CSS (import this)
├── README.md               # This file
└── assets/
    ├── containers-bg.png   # Hero container image
    ├── fleet-night.png     # Fleet night background
    └── reefer-warehouse.png
```

---

## Usage in New Projects

1. Copy `zero-design-system.css` to your project
2. Add the Google Fonts link to your HTML
3. Import the CSS file
4. Use the CSS variables and utility classes

```html
<!DOCTYPE html>
<html>
<head>
  <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600;700&family=Open+Sans:wght@400;600&family=Azeret+Mono:wght@400;500&display=swap" rel="stylesheet" />
  <link rel="stylesheet" href="zero-design-system.css" />
</head>
<body>
  <div class="container">
    <div class="glass" style="padding: 32px;">
      <h2>Welcome to ZERO°</h2>
      <p>Your shipment is on the way.</p>
      <button class="btn btn-primary">Track Now</button>
    </div>
  </div>
</body>
</html>
```

---

## AI Prompt Reference

When starting a new ZERO° Logistics project, use this prompt:

> Build a UI for ZERO° Logistics using their design system:
> - Primary blue: #0085CA, Glacier: #00B4E6
> - Fonts: Montserrat (headings), Open Sans (body), Azeret Mono (labels)
> - Use glassmorphism with backdrop-filter blur on white/light backgrounds
> - Logo: "ZERO°" at 52px and "LOGISTICS" at 32px, Montserrat Bold
> - Ice blue background for widgets: #F0F7FB
> - Status colors: Success #10B981, Warning #F59E0B, Danger #EF4444

---

**ZERO° LOGISTICS** — Cold-Chain Excellence
