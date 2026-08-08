# Church Study Guide Maker

A single-page HTML form for building your weekly study-group guide. Fill in the
fields, click one button, and it downloads a finished **Word document** (`.doc`) with
your sections and styling already applied — and a horizontal line between every block,
just like you asked.

## How to open it

Download or clone this folder and **double-click `index.html`**. It opens in any web
browser (Chrome, Safari, Edge, Firefox) on a computer, tablet, or phone. Nothing to
install, and it works offline.

The page has two tabs — **Guide Content** and **Styling** — and a compactness slider
along the bottom.

## How to use it

1. On the **Guide Content** tab, the form is pre-filled with an example so you can see
   what goes in each field. Replace the example text with your own.
2. Need more of something? Use the **+ Add** buttons for extra announcements, scripture
   segments, questions, related verses, or prayer points.
3. (Optional) Open the **Styling** tab to change fonts, sizes, colors, and bolding, and
   save the look as a profile — see below.
4. (Optional) Drag the **Compactness** slider at the bottom to tighten or loosen the
   spacing so you don't waste paper.
5. Click **⬇ Download Word Document**.
6. The finished `.doc` lands in your Downloads folder, named after your study and week
   (e.g. `the-book-of-james_week-3.doc`). Open it in **Microsoft Word or Google Docs**
   to print, share, or make final tweaks.

## The sections (in order)

1. **Title** — what you're studying, the week, and a short description of the night.
2. **Weekly Updates** — church announcements (as many as you need), an ice breaker,
   and last week's inward & outward growth focus.
3. **Body** — one or more scripture segments. Each has the passage to read, a box for
   the **actual scripture text**, a summary, key notes for leaders (in a highlighted
   box), a transition into the questions, the questions, and related verses.
4. **Closing Prayer Points**
5. **Growth Steps for Next Week** — the inward & outward steps you're setting.

Every one of these blocks is separated by a horizontal line in the finished document.

## Styling & profiles

The **Styling** tab lets you set — with a live preview:

- **Title, section headings, and body text** — font, size, color, and bold.
- **Accent color** — used for labels, dividers, and the leader-notes box.

Save a look you like as a **profile** with **Save as new…**; it's stored in your
browser, so it's there next time. Switch profiles from the dropdown, update one with
**Save**, or remove one with **Delete**. Three profiles come built in:

- **Classic** — the default.
- **Ink Saver** — smaller, black, tightly spaced to save toner and paper.
- **Large Print** — bigger type and roomier spacing for easier reading.

The **Compactness** slider (bottom of the page) controls margins, line spacing, and the
gaps between blocks. It's saved as part of each profile.

## How the Word file is made

The page builds a Word-compatible document right in your browser — no server, no
account, no internet needed. The `.doc` opens natively in Microsoft Word and Google
Docs, where it stays fully editable. The example scripture text uses the public-domain
King James Version; replace it with whatever translation your group uses.

## For developers — editing defaults

- **Example wording:** edit the `EXAMPLE = { ... }` object in the `<script>` section.
- **Default styles / built-in profiles:** edit `DEFAULT_STYLE` and `BUILTIN_PROFILES`.
- **Word output structure:** see `buildContent()` / `buildDocHtml()`.
- **Look of the form page itself:** edit the `:root { ... }` CSS block at the top.
