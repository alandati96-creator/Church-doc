# Church Study Guide Maker

A single-page HTML form for building your weekly study-group guide. Fill in the
fields and export a finished document — **Word (`.docx`)**, the older **`.doc`**, or a
**PDF** — with your sections and styling already applied, and a horizontal line between
every block.

## How to open it

Download or clone this folder and **double-click `index.html`**. It opens in any web
browser (Chrome, Safari, Edge, Firefox) on a computer, tablet, or phone. Nothing to
install, and it works offline (the only feature that needs internet is scripture lookup).

The page has two tabs — **Guide Content** and **Styling** — and three layout sliders
along the bottom next to the export buttons.

## How to use it

1. On the **Guide Content** tab, the form is pre-filled with an example so you can see
   what goes in each field. Replace the example text with your own.
2. Need more of something? Use the **+ Add** buttons for extra announcements, scripture
   segments, questions, related verses, or prayer points, and the **↑ ↓** arrows to
   reorder them.
3. (Optional) Open the **Styling** tab to change fonts, sizes, colors, and bolding, and
   save the look as a profile — see below.
4. (Optional) Use the **sliders** at the bottom to tighten spacing and save paper.
5. Export with the buttons at the bottom right:
   - **⬇ Word (.docx)** — a true modern Word file (recommended).
   - **.doc** — the older Word-compatible format, if you need it.
   - **🖨 PDF** — opens a print view; choose your printer or "Save as PDF".
6. Word files land in your Downloads folder, named after your study and week
   (e.g. `the-book-of-james_week-3.docx`), and open in **Microsoft Word or Google Docs**.

## Saving your work

- Your typing **auto-saves in this browser**, so closing the tab won't lose it.
- **Save Guide** downloads the whole guide as a small `.json` file. **Open Guide** loads
  one back in — so you can keep last week's guide and reuse it as a starting point.
- **Load Example** restores the built-in sample; **Clear** empties the form.

## The sections (in order)

1. **Title** — what you're studying, the week, and a short description of the night.
2. **Weekly Updates** — church announcements (as many as you need), an ice breaker,
   and last week's inward & outward growth focus.
3. **Body** — one or more scripture segments. Each has the passage to read, a box for
   the **actual scripture text** (with a **Get text** button — see below), a summary,
   key notes for leaders (in a highlighted box), a transition into the questions, the
   questions, and related verses.
4. **Closing Prayer Points**
5. **Growth Steps for Next Week** — the inward & outward steps you're setting.

Every one of these blocks is separated by a horizontal line in the finished document.

## Scripture lookup ("Get text")

Each segment has a translation dropdown (**NIV, NLT, ESV, NASB, KJV**) and a **Get text**
button next to the passage reference:

- **KJV** is public domain, so it's **fetched automatically** and dropped into the box.
- **NIV, NLT, ESV, and NASB** are copyrighted and have no free lookup service, so
  **Get text** opens that passage on **Bible Gateway** in a new tab — copy the text into
  the box. (Please follow your translation's usage terms when reproducing it.)

Scripture lookup needs an internet connection; everything else works offline.

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

**Moving profiles between computers:** profiles live in one browser on one device. Use
**Export…** to download all your profiles as a small `.json` file, and **Import…** on
another computer (or browser) to load them back in. Import adds the profiles to whatever
you already have.

### Paper-saving sliders (bottom of the page)

Three sliders control how much paper the guide uses — tighten them to fit more on each
page. They're saved as part of each profile.

- **Compactness** — the gaps between blocks and around each element.
- **Line spacing** — how tall each line of text is (1.0 = single-spaced).
- **Margins** — the white border around the page, in inches.

The **Ink Saver** profile sets all three tight; **Large Print** loosens them.

## How the documents are made

Everything is built right in your browser — no server, no account. The **`.docx`** is a
real Office Open XML package assembled by hand (a tiny built-in zip writer), so it opens
cleanly in Microsoft Word and Google Docs. The **`.doc`** is a Word-compatible HTML file,
and **PDF** comes from your browser's print dialog. The example scripture text uses the
public-domain King James Version; replace it with whatever translation your group uses.

## For developers — editing defaults

- **Example wording:** edit the `EXAMPLE = { ... }` object in the `<script>` section.
- **Default styles / built-in profiles:** edit `DEFAULT_STYLE` and `BUILTIN_PROFILES`.
- **`.doc` / PDF output structure:** see `buildContent()` / `buildDocHtml()`.
- **`.docx` output:** see `buildDocumentXml()` (WordprocessingML) and `zipStore()`.
- **Scripture lookup:** see `fetchScripture()` (KJV via `bible-api.com`, others via
  Bible Gateway).
- **Look of the form page itself:** edit the `:root { ... }` CSS block at the top.
