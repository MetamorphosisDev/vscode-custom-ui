<div align="center">

![Preview](https://upload.wikimedia.org/wikipedia/commons/thumb/9/9a/Visual_Studio_Code_1.35_icon.svg/500px-Visual_Studio_Code_1.35_icon.svg.png)

# ✦ VSCode Custom UI

**A hand-crafted Visual Studio Code reskin — cleaner, rounder, and more alive.**

[![License: MIT](https://img.shields.io/badge/License-MIT-a78bfa?style=flat-square)](LICENSE)
[![VS Code](https://img.shields.io/badge/VS%20Code-1.85%2B-7c6af7?style=flat-square&logo=visualstudiocode&logoColor=white)](https://code.visualstudio.com/)
[![Extension](https://img.shields.io/badge/Requires-Custom%20CSS%20%26%20JS%20Loader-5a4fcf?style=flat-square)](https://marketplace.visualstudio.com/items?itemName=be5invis.vscode-custom-css)
[![Stars](https://img.shields.io/github/stars/your-username/vscode-custom-ui?style=flat-square&color=f9a8d4)](https://github.com/your-username/vscode-custom-ui)

</div>

---

## ✦ What's Inside

A set of carefully crafted CSS (and optional JS) injections that transform the default VSCode interface into something worth staring at all day.

| Area | What Changed |
|------|-------------|
| **Activity Bar** | Floating pill icons, smooth hover lift, animated active indicator |
| **Command Palette** | Slide-in entrance, layered shadow, input focus glow |
| **Notifications** | Toast slide-in, severity-colored borders, fade-in toolbar |
| **Editor Watermark** | Replaced with custom SVG on empty editor |
| **Global** | Rounded corners, improved spacing, subtle borders |

---

## ✦ Project Structure

```
vscode-custom-ui/
│
├── css/
│   └── custom.css          # All UI overrides
│
├── js/
│   └── script.js           # Optional JS tweaks
│
├── assets/
│   ├── welcome.svg         # Custom editor watermark
│   └── images/             # Additional assets
│
└── README.md
```

---

## ✦ Installation

### 1 — Install the extension

Search for **Custom CSS and JS Loader** in the VS Code Extensions panel, or install via CLI:

```bash
code --install-extension be5invis.vscode-custom-css
```

### 2 — Clone this repo

```bash
git clone https://github.com/your-username/vscode-custom-ui.git
```

### 3 — Point VSCode to the files

Open your `settings.json` (`Ctrl+Shift+P` → *Open User Settings JSON*) and add:

```jsonc
"vscode_custom_css.imports": [
  "file:///absolute/path/to/vscode-custom-ui/css/custom.css",
  "file:///absolute/path/to/vscode-custom-ui/js/script.js"
]
```

> **Windows example**
> ```jsonc
> "vscode_custom_css.imports": [
>   "file:///C:/Users/yourname/vscode-custom-ui/css/custom.css"
> ]
> ```

> **macOS / Linux example**
> ```jsonc
> "vscode_custom_css.imports": [
>   "file:///home/yourname/vscode-custom-ui/css/custom.css"
> ]
> ```

### 4 — Enable & restart

Open the Command Palette (`Ctrl+Shift+P`) and run:

```
Enable Custom CSS and JS
```

Then **fully restart** VS Code. If prompted about a corrupted installation — that's normal, click **Don't Show Again**.

---

## ✦ Snippet Highlights

### Custom Editor Watermark
```css
.editor-group-watermark .letterpress {
  background-image: url("file:///path/to/assets/welcome.svg") !important;
  background-repeat: no-repeat !important;
  background-position: center;
  background-size: contain;
}
```

### Activity Bar — Floating Pills
```css
.monaco-workbench .activitybar > .content
  :not(.monaco-menu) > .monaco-action-bar .action-item {
  border-radius: 12px;
  border: 1.5px solid transparent;
  transition: background 0.18s ease, transform 0.14s ease;
}
```

### Custom Editor Font
```css
.monaco-editor {
  font-family: "MesloLGS NF", "Hack Nerd Font", monospace !important;
}
```

---

## ✦ Recommended Fonts

For the best experience, install one of these Nerd Fonts:

- [MesloLGS NF](https://github.com/romkatv/powerlevel10k#meslo-nerd-font-patched-for-powerlevel10k)
- [Hack Nerd Font](https://www.nerdfonts.com/font-downloads)

These include extra programming ligatures and symbols used throughout the UI.

---

## ✦ Notes

> CSS selectors may break after a VS Code update since they target internal class names.
> If something stops working, open an issue or check the selector in DevTools (`Help → Toggle Developer Tools`).

---

## ✦ License

Released under the [MIT License](LICENSE). Use it, fork it, make it yours.

---

<div align="center">
  <sub>made with obsession · <a href="https://github.com/your-username">your-username</a></sub>
</div>
