# The Ledger

A private, single-file link archive. Save links with a title, description, category, and subcategory, and browse them back organized by folder-style tabs — no server, no database, no build step. Just one `index.html` file that runs entirely in your browser.

## Features

- **Add links manually** — title, URL, description, category, and subcategory, with autocomplete from what you've already typed
- **Organized homepage** — a tab per category across the top, grouped into subcategory sections underneath, links shown as cards
- **Open, Edit, Delete** on every card — Open launches the link in a new tab
- **Letter avatars** — each category gets a consistent colored initial (e.g. "P" for Polity) so cards and tabs are easy to scan
- **Favicons** — each card shows the site's icon next to its URL
- **Import Bookmarks HTML** — drop in a bookmarks export from Chrome, Firefox, Safari, etc. Every link lands in a **Pending** tab with its original folder name suggested as a category. Review, edit, and **Approve & File** each one (or discard it) before it joins your main archive
- **Search** — live filter across titles, descriptions, URLs, categories, and subcategories
- **Export / Import data** — download a JSON snapshot of your whole archive and import it on another device or browser to keep them in sync (duplicate URLs are skipped automatically)
- **Light and dark themes** — light is the default; toggle from the header, and your choice is remembered

## Getting started

No installation, no dependencies, no build step.

1. Download `index.html` from this repo (or clone it)
2. Open it directly in any modern browser — double-click the file, or drag it into a browser tab
3. Start adding links

To use it like a real "site," you can also host it for free:

- **GitHub Pages** — push `index.html` to a repo, enable Pages in Settings, and visit the generated URL
- **Any static host** — Netlify, Vercel, Cloudflare Pages, etc. all work by just serving the single file

## How your data is stored

Everything is saved to your browser's `localStorage`, scoped to whatever URL you're opening the file from. That means:

- Your data is private — nothing is sent to a server
- Data does **not** automatically sync between devices or browsers
- Clearing your browser's site data will erase your archive

To move your archive between devices, use **Export Data** to download a `.json` snapshot, then **Import Data** on the other device to bring it in. Imports merge with what's already there and skip anything with a duplicate URL, so it's safe to import the same file more than once.

## Importing existing bookmarks

Most browsers can export your bookmarks as an HTML file:

- **Chrome / Edge**: Bookmark Manager → ⋮ menu → Export bookmarks
- **Firefox**: Bookmarks → Manage Bookmarks → Import and Backup → Export Bookmarks to HTML
- **Safari**: File → Export Bookmarks

Click **Import Bookmarks HTML** in The Ledger and select that file. Every bookmark is added to the **Pending** tab with its original bookmark folder pre-filled as a suggested category. From there you can edit the title, description, category, and subcategory for each one, then **Approve & File** it into your main archive, or **Discard** anything you don't want to keep.

## Project structure

```
index.html   ← the entire application (HTML, CSS, and JavaScript)
```

Everything lives in one file on purpose — copy it, host it, or drop it into any folder and it just works.

## Browser support

Works in any modern browser (Chrome, Firefox, Safari, Edge). Relies on `localStorage`, the File API, and `DOMParser` — all standard and widely supported.

## License

Use, modify, and share freely.
