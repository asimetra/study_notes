# Study Notes — Project Rules

## File Format

Notes are written in **pure HTML**. No Markdown.

- Naming: `{number}-{topic-name}.html` (e.g. `1-matris-Giris.html`)
- Each HTML file runs standalone — no external CDN or library dependencies
- KaTeX, MathJax and similar math renderers are **not used** (require internet, unreliable offline)

---

## Math Notation

**No LaTeX.** Use instead:

| Need | Method |
|------|--------|
| Variable name | `<i>x</i>` or `.var` class |
| Multiplication | `&times;` |
| Minus sign | `&minus;` |
| Subscript | `<sub>ij</sub>` |
| Superscript | `<sup>2</sup>` |
| Arrow | `&rarr;` |
| Matrix | `.mat` + `.mat-cells` CSS classes (see below) |

### Matrix Structure

Matrices use CSS `border-left` + `border-right` for brackets:

```html
<span class="mat">
  <span class="mat-cells" style="grid-template-columns: repeat(3, auto)">
    <span>1</span><span>2</span><span>3</span>
    <span>4</span><span>5</span><span>6</span>
  </span>
</span>
```

Elements are written **row by row** (left to right, top to bottom).
`grid-template-columns: repeat(N, auto)` — N = number of columns.

---

## CSS Class System (Bash-doc Style)

Every HTML file must define these classes:

| Class | Usage | Example |
|-------|-------|---------|
| `.var` | Variable name | `<span class="var">A</span>` |
| `.eq` | Equation line | `<span class="eq">3x &minus; 2y = 10</span>` |
| `.kw` | Key term | `<span class="kw">Row count</span>` |
| `.dim` | Dimension label | `<span class="dim">3×3</span>` |
| `.def` | Definition box | `<div class="def">...</div>` |
| `.note` | Warning/note box (red tint) | `<div class="note">...</div>` |
| `.mat` | Matrix wrapper | see above |
| `.mat-eq` | Matrix equation row | flex container |
| `.ex-row` | Side-by-side example | flex container |

### `.dim` CSS — important

Use `position: relative` + `top`, **not** `vertical-align: sub` (inconsistent across browsers):

```css
.dim {
  font-family: "Courier New", monospace;
  font-size: 0.72em;
  position: relative;
  top: 0.4em;
  color: #444;
}
```

---

## Page Structure

```
h1       → Course name (e.g. "Lineer Cebir")
nav.toc  → Table of contents (linked topics only — no placeholders)
h2       → Topic heading (with id, linked from toc)
h3       → Sub-section (italic + bold)
```

`<nav class="toc">` lists only finished (linkable) topics.
Topics not yet written are **not** added to the list.

---

## Design Decisions

- **Background:** `#fffff8` (cream)
- **Font:** `"Times New Roman", Times, serif` — old HTML document feel
- **Max width:** `720px`, centered
- **h2:** bottom border only, no top line or background color
- **h3:** italic + bold, plain text only, no box or background
- **No `<table>`** — use `display: grid` or `display: flex` for layout
- **Mobile:** grid collapses to single column below 500px

---

## Known Issues (Don't Repeat)

1. **Markdown + LaTeX mix doesn't work.** `$...$` inside HTML tags is not rendered.
   → Fix: use pure HTML — `.var`, `<i>`, `<sub>`.

2. **`$$...$$` breaks flex/grid layout.** Block math causes the markdown parser to inject `<p>` tags, breaking the layout.
   → Fix: not an issue in HTML files; LaTeX is not used anyway.

3. **`<table>` doesn't work for matrices, looks bad too.**
   → Fix: use `.mat` + `.mat-cells` (CSS grid).

4. **Boxed grid examples make the page too long.**
   → Fix: use `.ex-row` for side-by-side, `.ex-note` for short label.

5. **`vertical-align: sub` on `.dim` renders inconsistently.**
   → Fix: use `position: relative; top: 0.4em` instead.
