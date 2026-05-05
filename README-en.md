# Lightmind

> A calm, mountain-inspired Typora theme — forest greens, cream paper, deep-navy code. **Light** and **Dark**.

**[中文版 README →](./README.md)**

---

A lightweight Typora theme designed for long-form writing in mixed Chinese/English contexts. Body text is set in **LXGW WenKai (霞骛文楷)**, code in **JetBrains Mono**.

Two variants are included:

- **Lightmind** (`lightmind.css`) — warm cream paper with deep forest accents
- **Lightmind Dark** (`lightmind-dark.css`) — dark forest night with brighter green accents and the same navy code blocks

> ⚠️ **Tested only on Windows (Typora 1.13.4).** macOS and Linux **have not been tested**. Most things should work — Typora's renderer is consistent across platforms — but font rendering, sidebar metrics, and shadow rendering may differ. Reports / PRs welcome.

## Preview

See [`showcase-en.md`](./showcase/showcase-en.md) (English) or [`showcase.md`](./showcase/showcase-zh.md) (Chinese) for a full demo of every Markdown element rendered under this theme.

The sample exercises:

- All heading levels (H1–H6)
- Paragraphs · bold · italic · strikethrough · inline code · `<kbd>` · `<abbr>` · sub / sup · marks
- Blockquotes (regular & nested)
- All five GitHub-style alerts (`> [!NOTE]`, `> [!TIP]`, `> [!IMPORTANT]`, `> [!WARNING]`, `> [!CAUTION]`)
- Lists (unordered, ordered, nested, task lists)
- Tables (basic, alignment, complex cells)
- Code blocks across **Rust / C# / TypeScript** with One Dark-style syntax colors
- Inline math + display math (rounded cream cards)
- 14 Mermaid diagram types: flowchart, sequence, class, state-v2, ER, gantt, pie, journey, mindmap, gitGraph, xychart, sankey, packet, zenUML

## Design

### Light variant (`lightmind.css`)

| Token | Color | Where it shows |
| :--- | :--- | :--- |
| `--bg-page` | `#f4f1e8` | Outer page (warm cream paper) |
| `--bg-write` | `#faf7ef` | Writing surface (slightly brighter) |
| `--bg-formula` | `#f7f3e8` | Math block backgrounds |
| `--accent` | `#4a7c59` | Mid mountain green — links, accents |
| `--accent-deep` | `#2f5a40` | Shadowed pines — headings, strong |
| `--accent-soft` | `#8fb39b` | Hazy ridge — soft borders |
| `--accent-warm` | `#c2a878` | Sun glow — highlights, marks |
| `--code-bg` | `#1e2330` | Code block deep navy |
| `--code-fg` | `#c8cfd9` | Code text light gray |

### Dark variant (`lightmind-dark.css`)

| Token | Color | Where it shows |
| :--- | :--- | :--- |
| `--bg-page` | `#161d1a` | Outer page (deep forest night) |
| `--bg-write` | `#1d2622` | Writing surface (a touch lighter) |
| `--bg-formula` | `#1f2823` | Math block backgrounds |
| `--accent` | `#7fbe92` | Brighter mountain green — accents |
| `--accent-deep` | `#a8d4b6` | Moonlit jade — headings, strong |
| `--accent-soft` | `#5a7d68` | Soft mist — borders |
| `--accent-warm` | `#d8bd86` | Warm gold — highlights |
| `--code-bg` | `#14181f` | Code block (darker than page for contrast) |
| `--code-fg` | `#c8cfd9` | Code text light gray |

Code-block syntax colors in **both variants** follow the **One Dark** palette: purple keywords, golden types, green strings, soft red variables, blue function names.

## Installation

1. Copy `lightmind.css` (and optionally `lightmind-dark.css`) into your Typora themes folder:

   - **Windows** (tested): `%APPDATA%\Typora\themes\`
   - **macOS** (untested): `~/Library/Application Support/abnerworks.Typora/themes/`
   - **Linux** (untested): `~/.config/Typora/themes/`

   Or open Typora → `Preferences` → `Appearance` → click **Open Theme Folder**.

2. Restart Typora, then choose **Lightmind** or **Lightmind Dark** from the `Theme` menu.

> When you change the CSS files, Typora doesn't always hot-reload. Switch to a different theme then back, or restart Typora.

## Recommended Fonts

The theme works without anything installed (it falls back to system fonts), but for the intended look install:

- **[LXGW WenKai](https://github.com/lxgw/LxgwWenKai)** — body / Chinese text
- **[JetBrains Mono](https://www.jetbrains.com/lp/mono/)** — code

Both are open-source and free.

> **Note**: JetBrains Mono has no CJK glyphs, so Chinese characters inside code blocks fall back to LXGW WenKai (kai-style, not strictly monospaced). If you prefer strict monospace alignment for CJK, install **[Sarasa Mono SC](https://github.com/be5invis/Sarasa-Gothic)** and add it to the `--font-mono` chain.

## Customization

Key tokens are defined in `:root` at the top of `lightmind.css`. Override them by editing the file directly, or by adding a custom CSS file in Typora. Examples:

```css
:root {
    /* warmer paper background */
    --bg-page: #f7f3e3;

    /* punchier accent green */
    --accent: #2f8246;

    /* lighter code block */
    --code-bg: #2a3142;
}

#write {
    /* wider writing area */
    max-width: 960px;

    /* larger body font */
    font-size: 18px;
}
```

## Compatibility

- **Tested platform**: Typora 1.13.4 on Windows 10/11.
- **Untested platforms**: macOS, Linux. Likely works (Typora is Electron-based and CSS rules are platform-agnostic), but the author hasn't verified. Submit issues if anything breaks.
- **GFM-style alerts** (`> [!NOTE]` etc.) require Typora 1.7+ — older versions render them as plain blockquotes.
- **Mermaid diagrams** target Typora's current SVG renderer; minor visual differences may appear on older Typora releases.
- The theme uses CSS `:has()` selectors, which require recent Chromium-based Electron (bundled with Typora ≥ ~1.5).

## Credits

- **Code palette** — the One Dark theme by Atom
- **Fonts** — LXGW WenKai by [lxgw](https://github.com/lxgw), JetBrains Mono by JetBrains
- **GitHub alert classes** — Typora 1.13+ native `md-alert` rendering

## License

MIT — feel free to fork, modify, and share.

---

> Made with `lightmind.css` · words growing among the mountains.
