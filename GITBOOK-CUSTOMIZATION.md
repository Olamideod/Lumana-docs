# GitBook customization for Lumana

Follow this guide to brand and customize your Lumana docs site in the [GitBook dashboard](https://gitbook.com/docs/publishing-documentation/customization). These settings apply in **Customize** (or **Settings** → **Customization**).

## 1. Title, icon, and logo

- **Title:** Lumana Docs (or your preferred name)
- **Icon:** Upload the Lumana logo or use a book/camera emoji as favicon
- **Custom logo (Premium/Ultimate):** Upload `lumana-docs-header.png` as the custom logo to replace the title in the header. Add separate versions for light and dark mode if needed.

## 2. Themes and Lumana brand colors

- **Theme:** Choose **Muted** or **Clean** for a professional look. **Bold** (Premium) works well with dark mode.
- **Primary color:** Use your Lumana brand color here. This affects buttons, links, and highlighted UI. For dark mode:
  - If Lumana has a defined accent (e.g., from [lumana.ai](https://lumana.ai)), use that hex
  - Otherwise try `#FFFFFF` (white) or `#E5E5E5` (light gray) for good contrast
  - In GitBook: **Customize** → **Themes** → **Primary color** → enter hex or pick from palette
- **Tint color:** Subtly changes text and icons. For dark Lumana theme:
  - Use `#FFFFFF` or `#F5F5F5` for crisp text, or a subtle brand tint
  - Try the **BOLD** suggested swatches (`#2E2E2E`, `#222222`, `#161616`) for background depth

## 3. Black/dark background (Lumana theme)

- Under **Modes** → **Default mode:** Select **Dark**
- Optionally enable **Show mode toggle** if readers should switch between light and dark

## 4. Page icons (sidebar and page headers)

GitBook uses built-in icons (book, lightning, lightbulb, chain link, etc.) for pages. To add them:

1. In the space, go to the table of contents
2. Hover over a page title
3. Click **Add icon** or the emoji button next to the title
4. Choose an icon (or emoji) for each page

Suggested icons by section:

| Section | Icon suggestion |
|---------|-----------------|
| Quickstart / Getting started | Lightning bolt |
| What's new | Document / newspaper |
| Configuration | Gear / settings |
| System administration | People / users |
| Live monitoring | Video / camera |
| Alerts and AI detection | Bell |
| Databases and search | Magnifying glass / database |
| Software integrations | Link / chain |
| Troubleshooting | Wrench / tools |
| Monitoring services | Broadcast / antenna |
| FAQ and reference | Question mark / help |
| Concepts | Lightbulb |

## 5. Card icons

The welcome page cards already include icons via `data-card-cover` in the README. Icons live in `.gitbook/assets/` (rocket, file-text, settings, users, video, bell, search, link, wrench, radio, help-circle, lightbulb). To change or replace them, edit the card table in the README or add new SVG/PNG files to `.gitbook/assets/`.

## 6. Page cover for welcome page

To use the Lumana header as a full page cover:

1. Open the welcome page
2. Hover over the page title and open **Page options**
3. Select **Page cover**
4. Upload or select `lumana-docs-header.png` (1990×480 px recommended)

## 7. Additional customization (Premium/Ultimate)

- **Custom fonts:** Upload Lumana brand fonts
- **Footer:** Add Lumana logo, copyright, and links
- **Semantic colors:** Style hint blocks and code blocks
- **Code theme:** Match code blocks to dark Lumana theme
