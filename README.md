# Church Study Guide Maker

A simple, no-install tool for building your weekly study-group guide. It has your
sections and styling built in, comes pre-filled with an editable example, and turns
what you type into a clean, print-ready handout — with a horizontal line between
every block, just like you asked.

## How to open it

Download or clone this folder and **double-click `index.html`**. It opens in any web
browser (Chrome, Safari, Edge, Firefox) on a computer, tablet, or phone. Nothing to
install, and it works offline.

## How to use it

The screen is split in two: **editor on the left, live guide on the right.** As you
type on the left, the guide updates instantly on the right.

Toolbar buttons (top of the screen):

| Button | What it does |
| --- | --- |
| **Load Example** | Fills every field with the sample guide so you can see the format. Great starting point each week. |
| **New / Clear** | Wipes everything for a blank guide. |
| **Open…** | Opens a `.json` guide you saved before (e.g. `template-example.json`) so you can edit it. |
| **Save Guide** | Downloads this week's guide as a `.json` file. Reopen it next week with **Open…** to reuse or tweak it. |
| **Print / PDF** | Opens your browser's print dialog. Choose your printer, or **"Save as PDF"** to get a shareable file. |

Your work also **auto-saves in the browser**, so if you close the tab by accident,
it's still there when you come back.

## The sections (in order)

1. **Title** — what you're studying, the week, and a short description of the night.
2. **Weekly Updates** — church announcements (add as many as you need), an ice
   breaker, and last week's inward & outward growth focus.
3. **Body** — one or more scripture segments. Each has the passage to read, a
   summary, key notes for leaders (shown in a highlighted box), a transition into
   the questions, the questions, and related verses.
4. **Closing Prayer Points**
5. **Growth Steps for Next Week** — the inward & outward steps you're setting.

Every one of these blocks is separated by a horizontal line in the finished guide.

## The template file

`template-example.json` is the editable template. You can:

- Open it in the app (**Open…**) and edit it there, or
- Open it in any text editor to tweak the example wording directly.

When you **Save Guide**, the app writes the same kind of `.json` file (named after
your study and week), which becomes both your saved guide and a template you can
pull from next time.

## Changing the styling

All colors, fonts, and spacing live in one place: the `:root { ... }` block near the
top of `index.html`. Change a value there (for example `--primary` for the heading
color) and the whole guide restyles to match.
