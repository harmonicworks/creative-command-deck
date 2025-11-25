# Creative Command Deck — Silent Library Edition

The **Creative Command Deck** is a lightweight personal dashboard built with plain HTML, CSS, and JavaScript.  
It provides a simple and fast way to choose your daily focus — **Learn**, **Create**, or **Research** — and then shows only the tools relevant to that mode.

Below the cockpit are the **Silent Library Shelves**: always-available reference links such as AI assistants, writing tools, study music, learning platforms, and general utilities.  
The entire project is designed to be quiet, minimal, and distraction-free — a small start page for personal flow.

---

## ✨ Features

- Three-mode cockpit: **Learn**, **Create**, **Research**
- Clean and minimal interface optimized for focus
- Silent Library shelves for background and reference tools
- Responsive layout without external frameworks
- Local “Next step” notes stored automatically in the browser
- Zero-dependency design — just one HTML file

---

## 📁 File Structure

```

course-start-page.html   → Main dashboard
CHANGELOG.md             → Version notes and edits
README.md                → Project documentation
.gitignore               → Standard ignore file

````

You can rename `course-start-page.html` to `index.html` if you want GitHub Pages to load it directly.  
(Or set a custom source in **Settings → Pages**.)

---

## 🚀 Usage

### Open locally
1. Clone or download the repository  
2. Open `course-start-page.html` in your browser  
3. Select **Learn**, **Create**, or **Research**  
4. Use the Silent Library Shelves for quick access to tools and platforms

### GitHub Pages
This repository is already deployed via GitHub Pages.  
Any changes you push will appear live once GitHub Pages rebuilds.

---

## 🛠 Customizing the Deck

All customization happens directly inside `course-start-page.html`.

### 1. Change mode links  
Inside the `<script>` section you will find the `MODES` object:

```js
const MODES = {
  learn: {
    title: "📚 Learn",
    lead: "Open your learning cockpit: languages, coding, ethics, and more.",
    links: [
      { label:"Learn Dashboard (Notion)", href:"#", tag:"l-brand" },
      { label:"Course Overview (Docs)", href:"#", tag:"l-accent" },
      // ...
    ],
    noteKey: "next_learn"
  },
  // create, research ...
};
````

* Change `label` to update the button text
* Change `href` to link to your page or tool
* Change `tag` to adjust the visual style

  * `l-brand` – primary accent
  * `l-accent` – secondary accent
  * `l-dark` – neutral
  * `l-music` – warm accent

### 2. Edit the Silent Library Shelves

These shelves live in a `<section>` block near the bottom of the HTML:

```html
<div class="tile">
  <h3>🧘 Focus</h3>
  <ul>
    <li><a href="https://chatgpt.com/">ChatGPT</a></li>
    <li><a href="https://gemini.google.com/">Google Gemini</a></li>
    <!-- ... -->
  </ul>
</div>
```

You can freely add or remove `<li>` links or entire shelf tiles.

### 3. Modify styles

At the top of the file in `<style>`, you can adjust:

* Color variables
* Spacing
* Shadows
* Dark/light mode overrides

Everything is self-contained and easy to tweak.

---

## 💾 Local “Next Step” Notes

Each mode has a **Next step** field at the bottom of its cockpit. Notes are:

* Saved using `localStorage`
* Stored per browser and device
* Not synced or uploaded anywhere
* Meant to be *one small nudge*, not a to-do list

---

## 📌 Roadmap / Ideas (Optional)

* Config file for links
* Screenshot header banner
* Compact or mobile-first variants
* Keyboard shortcuts
* Additional themes

---

## 🤝 Contributing / Forking

This project is intentionally simple and meant to be customized.

Feel free to:

* Fork it
* Change the shelves
* Replace links and tools
* Edit styles or mode labels

If you publish a fork, a small mention of the original Creative Command Deck is appreciated but optional.

---

## 📄 License

You’re free to adapt, reuse, or publish variants of this dashboard for personal or public use.

```

