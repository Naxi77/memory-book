# Memory Book 📖

An interactive, hand-crafted **flip-book** that turns your paintings, sketches, and travel photos into a realistic 3D memory book — right in the browser.

**Live site:** https://jayrorotang.github.io/Memory-Book/

<p align="center">
  <em>Click the cover to open · turn pages with a real page-flip · a vintage postage stamp bookmark carries each spread's photo</em>
</p>

---

## ✨ Features

- **Realistic 3D page turns** — GPU-accelerated flips with gloss shading, lift shadows, and flash-free image decoding.
- **Kraft-paper "V2" theme** — warm paper background, decorative corner stamp, and a handwritten *My Memory Book* title.
- **Vintage stamp bookmark** — tucks behind the book and slides out on hover to reveal each spread's photo.
- **Closed-book intro** — a real page-turn opens the cover directly onto the first spread; the first/last page folds the book shut again.
- **Batch image upload** — a **+** button on the right edge lets you replace the whole book from your own images (see naming rules below).
- **Flexible page layouts** — one full cross-page artwork *or* two portrait photos side-by-side per spread.
- **Fully responsive** — the book scales uniformly and re-centers for tablet and mobile screens.
- **Self-contained** — a single `index.html` with all images embedded; no build step, no dependencies.

---

## 🚀 Usage

Just open the live site, or download `index.html` and open it in any modern browser.

- **Click the cover** to open the book.
- **Arrow keys ← / →** or **click a page** to turn.
- **Hover the stamp** on the right to slide the photo bookmark out.

### Replacing images (the `+` button)

Click the **+** button on the right edge, then select multiple files at once. Files are matched by name (case-insensitive, leading zeros OK):

| File name | What it becomes |
| --- | --- |
| `page1.png` | Spread 1's artwork (one big image spanning both pages) |
| `page1-1.png` + `page1-2.png` | Two portrait photos on spread 1 (left / right). Also accepts `-a/-b`, `-l/-r`, `-left/-right` |
| `picture1.jpg` | Spread 1's postage-stamp photo (`background1.jpg` also works) |
| `cover.jpg` | The book cover photo (does **not** change the page count) |

**How the page count works:** uploading page/picture files **rebuilds the book** to exactly the highest page number provided (e.g. `page1 … page8` → an 8-page book), after a confirmation prompt. Spreads without a `pictureN` photo fall back to a built-in default placeholder so the stamp bookmark still appears. Uploading only a `cover` image swaps the cover without touching your pages.

---

## 🛠️ Tech

- Vanilla **HTML / CSS / JavaScript** — no frameworks.
- CSS 3D transforms (`preserve-3d`, `rotateY`) for the page-turn physics.
- Images embedded as base64 data URLs and kept in a decode cache for smooth flips.
- Hosted on **GitHub Pages**.

---

## 📄 License

Created by **Jaymee** · © 2026. Personal creative project.
