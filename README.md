# cssreel

A curated collection of CSS animations and effects — ready to drop into any project. Customize live (color, speed, size, opacity, radius) and copy the exact code you need.

**No npm. No build step. No dependencies. Just CSS.**

---

## Features

- **39 effects** across 10 categories
- Live editor — tweak every parameter and see results instantly
- Copy button generates a clean, self-contained snippet with your exact values
- Single HTML file — open it in any browser, no server needed
- Fully responsive

---

## Categories

| Category | Effects |
|---|---|
| **loaders** | spin loader, pulse dot, wave bars, dots bounce, ring pulse |
| **keyframes** | bounce, float & rotate, 3d cube spin |
| **hover** | lift button, underline reveal, glow card, flip 360, border draw, fill sweep, 3d tilt |
| **text** | blinking cursor, typing reveal, shimmer skeleton |
| **glassmorphism** | glass card |
| **transforms** | slide in, shake, pendulum, orbit, spring pop |
| **metallic** | chrome shine, gold text, brushed steel, liquid metal |
| **neon** | neon glow, neon flicker, neon border, laser scan |
| **glitch** | glitch text, crt scanlines, chromatic shift |
| **cards** | portfolio card, glass profile, stat card, gradient border |

---

## Usage

```bash
git clone https://github.com/andrewavilan/cssreel.git
cd cssreel
open index.html   # or just double-click it
```

1. Browse effects and click any card to open the live editor
2. Adjust color, speed, size, opacity and border-radius in real time
3. Hit **copy code** — the snippet includes your exact custom values

---

## How effects are built

Each effect is a plain JavaScript object in the `EFFECTS` array inside `index.html`:

```js
{
  id: 1,
  cat: 'loader',           // category slug
  name: 'spin loader',
  desc: 'Short description shown on the card.',
  defaults: { color: '#22C55E', duration: 0.9, size: 36, radius: 50, opacity: 1 },

  // Returns a live DOM element for the card/modal preview
  buildPreview(cfg) { ... },

  // Returns the HTML snippet string
  html: (cfg) => `...`,

  // Returns the CSS snippet string
  css: (cfg) => `...`,
}
```

To add a new effect, append an object to the array following the same shape — the grid, modal, and copy button all work automatically.

---

## Design tokens

```
--bg-base      #080E09   base background
--bg-surface   #0F1A11   cards / surfaces
--green        #22C55E   primary accent
--text-primary #E8F5EA   main text
font: DM Mono (Google Fonts)
```

---

## Contributing

Pull requests welcome. Keep effects self-contained (no external dependencies), and make sure the `css()` function generates a complete, copy-pasteable snippet.

---

## Author

**Andrew Avilan** — Frontend developer, Medellín, Colombia

- GitHub: [@andrewavilan](https://github.com/andrewavilan)
- LinkedIn: [andrewavilan](https://linkedin.com/in/andrewavilan)
- Email: hello@andrewavilan.dev

---

## License

MIT
