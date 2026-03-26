# Personal Resume — Single Page HTML

A modern, self-contained resume website built with a single HTML file. No frameworks, no build tools, no external CSS — just open and go.

## Features

- **Dark / Light Mode** — toggle with the ☀️/🌙 button (persists across page refreshes via localStorage)
- **Responsive Design** — sidebar nav on desktop, stacked layout on mobile
- **Active Section Highlighting** — nav links highlight as you scroll
- **Smooth Scrolling** — click any nav link for animated scroll
- **Experience Cards** — hover effects, gradient borders, tech badges
- **Print Friendly** — nav and controls hidden automatically when printing
- **Zero Dependencies** — no Bootstrap, no jQuery, no build step

## File Structure

```
├── index.html                  # The entire resume (HTML + CSS + JS)
├── assets/
│   └── img/
│       └── my_new_pic.jpeg     # Profile photo (120x120, circular crop)
└── README.md
```

## Setup

1. Clone or download this repo
2. Add your profile photo at `assets/img/my_new_pic.jpeg`
3. Open `index.html` in a browser

That's it. No `npm install`, no server required.

## Customization

### Edit Content
All content is plain HTML in `index.html`. Each section (`#about`, `#experience`, `#education`, `#skills`, `#interests`, `#awards`) is clearly labeled with comments.

### Change Colors
Edit the CSS variables at the top of the `<style>` block:

```css
:root {
  --bg: #0f172a;        /* dark mode background */
  --accent: #38bdf8;    /* primary accent color */
  --accent2: #818cf8;   /* secondary accent (gradient) */
}
.light-theme {
  --bg: #f8fafc;        /* light mode background */
  --accent: #0284c7;    /* light mode accent */
}
```

### Change Fonts
The page loads two Google Fonts:
- **Inter** — body text
- **JetBrains Mono** — dates, tech badges

Swap them by editing the `<link>` tag and `font-family` values in CSS.

### Add a New Experience Entry
Copy an existing `exp-card` div and update the content:

```html
<div class="exp-card">
  <div class="exp-header">
    <div>
      <div class="exp-title">Job Title</div>
      <div class="exp-company">Company · Location</div>
    </div>
    <span class="exp-date">Start – End</span>
  </div>
  <ul>
    <li>Accomplishment or responsibility</li>
  </ul>
  <div class="exp-tech">
    <span class="tech-badge">Skill</span>
  </div>
</div>
```

### Profile Photo
- Place at `assets/img/my_new_pic.jpeg`
- Recommended: square image, at least 240x240px
- Automatically displayed as a circle in the sidebar

## External Resources

The only external loads are:
| Resource | Purpose | Required? |
|----------|---------|-----------|
| Google Fonts (Inter, JetBrains Mono) | Typography | Optional — falls back to system fonts |
| Font Awesome 5 | Section & nav icons | Optional — remove `<script>` tag if not needed |
| `assets/img/my_new_pic.jpeg` | Profile photo | Optional — sidebar shows without it |

## Browser Support

Works in all modern browsers (Chrome, Firefox, Safari, Edge). No IE support.

## License

All rights reserved. This repository is for personal portfolio use only. You may view the source code for reference, but copying, modifying, or redistributing the content is not permitted without prior written consent.
