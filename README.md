# Church Study Guide Maker

A single-page HTML form for building your weekly study-group guide. Fill in the
fields, click one button, and it downloads a finished **Word document** (`.doc`) with
your sections and styling already applied — and a horizontal line between every block,
just like you asked.

## How to open it

Download or clone this folder and **double-click `index.html`**. It opens in any web
browser (Chrome, Safari, Edge, Firefox) on a computer, tablet, or phone. Nothing to
install, and it works offline.

## How to use it

1. The form is pre-filled with an **example** so you can see exactly what goes in each
   field. Replace the example text with your own.
2. Need more of something? Use the **+ Add** buttons to add extra announcements,
   scripture segments, questions, related verses, or prayer points.
3. Click **⬇ Download Word Document** at the bottom.
4. The finished `.doc` lands in your Downloads folder, named after your study and week
   (e.g. `the-book-of-james_week-3.doc`). Open it in **Microsoft Word or Google Docs**
   to print, share, or make final tweaks.

## The sections (in order)

1. **Title** — what you're studying, the week, and a short description of the night.
2. **Weekly Updates** — church announcements (as many as you need), an ice breaker,
   and last week's inward & outward growth focus.
3. **Body** — one or more scripture segments. Each has the passage to read, a summary,
   key notes for leaders (in a highlighted box), a transition into the questions, the
   questions, and related verses.
4. **Closing Prayer Points**
5. **Growth Steps for Next Week** — the inward & outward steps you're setting.

Every one of these blocks is separated by a horizontal line in the finished document.

## How the Word file is made

The page builds a Word-compatible document right in your browser — no server, no
account, no internet needed. The `.doc` opens natively in Microsoft Word and Google
Docs, where it stays fully editable.

## Editing the example / styling

- **Example wording:** edit the `EXAMPLE = { ... }` block near the top of the
  `<script>` section in `index.html`. Whatever you put there becomes the default the
  form loads with each time.
- **Colors & fonts of the Word output:** edit the `C = { ... }` color values and the
  inline styles inside `buildDocHtml()` in `index.html`.
- **Look of the form page itself:** edit the `:root { ... }` block of CSS at the top.
