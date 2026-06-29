# NANZE — The Scent of What's Next

A luxury futuristic perfume e-commerce single-page application with hand-crafted SVG bottles, light mode design, and responsive product pagination.

## Features

- **20 Unique Perfume Products** — each with a custom SVG bottle design and animated interactions
- **Light Mode Design** — cream background, dark text, vibrant accent colors (purple, teal, pink)
- **Responsive Pagination** — browse products across multiple pages (6 per page by default)
- **Interactive Cart System** — add items, view cart drawer, live item count
- **Smooth Animations** — morphing orb hero, floating bottles, scroll-triggered reveals
- **Pure HTML/CSS/JS** — no frameworks, no external images, all SVG

## Quick Start

### 1. Open in Browser

Simply open `index.html` in any modern web browser:

```bash
open index.html
# or on Windows:
start index.html
```

### 2. With Local Server (Recommended)

For best results, serve the file over HTTP:

#### Using Node.js/npm:
```bash
npm install -g serve
serve .
# Open http://localhost:3000
```

#### Using Python 3:
```bash
python -m http.server 8000
# Open http://localhost:8000
```

#### Using Python 2:
```bash
python -m SimpleHTTPServer 8000
# Open http://localhost:8000
```

## Usage

### Browsing Products

- Scroll down to see the **Collection** section (6 products per page)
- Use the **pagination controls** at the bottom to navigate between pages
- Hover over a product card to see the bottle glow intensify and the "Add to Cart" button slide up

### Adding to Cart

1. Click **"Add to Cart"** on any product
2. The cart pill in the top-right corner updates with the item count
3. The **cart drawer** slides in from the right automatically
4. Close the drawer by clicking the **×** button or the overlay

### Viewing Philosophy & Formula

- Scroll to the **"Fragrance is not worn. It is activated."** section for brand philosophy
- Continue scrolling to the **Formula** section to see the 10 key ingredients
- All sections fade in as you scroll down

### Cart

- Click the **CART** button in the top-right to open/close the cart drawer
- Cart persists during your session (refreshing clears it)
- Press **Escape** to close the drawer

## Project Structure

```
nanze/
├── index.html          # Single-file application (all HTML, CSS, JS)
├── README.md           # This file
└── .git/               # Git repository
```

## Browser Support

Works in all modern browsers:
- Chrome/Edge 90+
- Firefox 88+
- Safari 14+

## Customization

### Adjusting Products Per Page

Edit the JavaScript section at the bottom of `index.html`. Find:
```javascript
const productsPerPage = 6;
```

Change `6` to any number (e.g., `4`, `8`, `12`).

### Changing Accent Colors

Edit the CSS tokens at the top:
```css
:root {
  --violet:  #9966CC;  /* Change to your purple */
  --teal:    #00A89F;  /* Change to your cyan */
  --pink:    #E91E63;  /* Change to your magenta */
}
```

### Adding New Products

Each product is an `<article class="product-card">` with:
- A `<div class="bottle-stage">` containing an SVG bottle
- Product info (label, name, notes, price)
- An "Add to Cart" button with `data-name` and `data-price` attributes

## Performance Notes

- All animations respect `prefers-reduced-motion` for accessibility
- Scroll reveal animations use `IntersectionObserver` for efficiency
- Cart state is stored in-memory (no backend or storage)

## License

© 2089 NANZE — All frequencies reserved.

---

**Built with:** Pure HTML, CSS, and vanilla JavaScript — no dependencies.
