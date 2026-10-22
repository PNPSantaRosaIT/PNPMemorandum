# Memorandum System

PNP memorandum generator (Santa Rosa CPS template). Runs entirely in the browser: no server, no installation.

```
memorandum-system/
  index.html   the page
  style.css    all styles (app screen + the memorandum page and print layout)
  script.js    all code (editor, page layout, PDF, History, phone support)
  images/      app icons and a copy of the logos used on the memorandum
```

## Put it on GitHub Pages

1. Create a **Public** repository on github.com.
2. Upload everything inside this folder (`index.html`, `style.css`, `script.js`, `images`), not the folder itself, then **Commit changes**.
3. **Settings > Pages > Deploy from a branch > main > / (root) > Save**.
4. Open the link GitHub shows (`https://YOUR-NAME.github.io/REPO-NAME/`). On a phone use **Add to Home Screen** inside the app.

To update later, upload the changed files again with the same names. If a phone still shows the old version, change the number after `?v=` in `index.html` (both lines), upload, and reopen the page.

## Lists and tables (how they work)

- **Lists** behave like Word / Google Docs: Tab / Shift+Tab change the level (1. then a. then i.), choosing a different style on an item nests it under the item above, Enter on an empty item or Backspace at the start moves it up a level.
- **Tables:** drag a column border to resize. Drag across cells and press **Merge Cells**, or use **Merge Right / Merge Down**; **Split Cell** undoes a merge.

## Notes

- Drafts and History are kept in each person's own browser. Nothing is uploaded anywhere.
- The logos are built into `script.js` so PDF export works even when `index.html` is opened straight from a file. The PNG copies in `images/` are for reference or editing.
- To change the letterhead text, search `script.js` for `UNIT_HEADER`. For layout measurements (in points, taken from the Word template) search `style.css` for `.hdw`, `.ft` and `.row`.

## Pages

The form has one group per page (**Page 1 Body Text**, **Page 2 Body Text**, ...). **+ Add Page** starts a new page, **Delete Page** removes one, and each page has its own **+ Add Body Text**. Every page always starts on a new sheet; a long page still continues onto the next sheet by itself.
