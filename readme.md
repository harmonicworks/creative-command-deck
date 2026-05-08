# Waypoint

**Waypoint** is a lightweight browser start page that helps you focus your day.

Choose a mode — **Daily**, **Learn**, **Create**, or **Explore** — and get instant access to the tools that matter for that moment.

Built with plain HTML, CSS, and JavaScript. No frameworks, no dependencies, no login required.

---

## Features

- Four focus modes: Daily, Learn, Create, Explore
- Clean dark interface designed to reduce distraction
- All links stored in a simple `links.json` file — no coding needed to edit
- Works on any device via GitHub Pages
- Zero dependencies — just two files

---

## File Structure

```
index.html    → The start page
links.json    → All your links, organized by tab and section
```

---

## How to use it as your browser start page

1. Go to the live page (see GitHub Pages link above)
2. Copy the URL
3. Set it as your browser's start page or new tab page

It works on any computer or device — just open the URL.

---

## How to customize your links

All links live in `links.json`. Open it and you will see a structure like this:

```json
{
  "tabs": [
    {
      "id": "daily",
      "label": "Daily",
      "sections": [
        {
          "title": "Email & Files",
          "links": [
            { "label": "Gmail", "href": "https://mail.google.com/" }
          ]
        }
      ]
    }
  ]
}
```

To add a link: copy an existing `{ "label": "...", "href": "..." }` line and change the values.

To remove a link: delete that line (and the comma before or after it).

To add a section: copy an entire `{ "title": "...", "links": [...] }` block.

Save and push — your page updates automatically.

---

## How to make your own version

1. Click **Fork** (top right on GitHub)
2. In your fork, edit `links.json` with your own links
3. Enable GitHub Pages in your fork's Settings → Pages
4. Use your own GitHub Pages URL as your start page

---

## License

Free to use, fork, and adapt for personal or public use.
