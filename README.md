# SÂN/06 — Volleyball E-commerce UI Concept & Prototype

[![Deploy to GitHub Pages](https://github.com/datmnt-dev/volleyball-ecommerce-prototype/actions/workflows/deploy.yml/badge.svg)](https://github.com/datmnt-dev/volleyball-ecommerce-prototype/actions/workflows/deploy.yml)

🌐 **Live Demo:** [https://datmnt-dev.github.io/volleyball-ecommerce-prototype/](https://datmnt-dev.github.io/volleyball-ecommerce-prototype/)  
📄 **Campaign Landing Page:** [https://datmnt-dev.github.io/volleyball-ecommerce-prototype/landing.html](https://datmnt-dev.github.io/volleyball-ecommerce-prototype/landing.html)

A responsive two-page e-commerce prototype for a modern volleyball brand and apparel concept.

## 🏐 Project Structure

```text
san06-volleyball-ecommerce-prototype/
└── volleyball-store/
    ├── assets/             # Vector SVGs for jerseys, balls, gear, and court scene
    ├── index.html          # Homepage & Storefront with product grid, filter, cart simulation
    ├── landing.html        # Campaign landing page for Drop 01 narrative
    ├── styles.css          # Shared responsive design system
    ├── app.js              # Shared client-side interaction & localStorage cart
    ├── generate_assets.py  # Helper script to generate SVG mock assets
    ├── DESIGN-BRIEF.md     # Design rationale, tone of voice, visual direction
    └── README.md           # Detailed documentation
```

## 🚀 Quick Start

Open `volleyball-store/index.html` or `volleyball-store/landing.html` directly in any modern browser, or run a local static HTTP server:

```bash
cd volleyball-store
python -m http.server 8000
```

Visit:
- Homepage: [http://localhost:8000/](http://localhost:8000/)
- Landing Page: [http://localhost:8000/landing.html](http://localhost:8000/landing.html)

No build tools or heavy dependencies required.
