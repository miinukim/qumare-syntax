
# QuMaRE Syntax Extension – Installation Guide

Enables syntax‑highlighting, bracket matching and snippets for **`.qmr`** experiment files.

---

## 1 · Install from the Marketplace  *(easiest)*

1.  Open VS Code or Cursor.  
2.  Press **⌘ ⇧ X** (macOS) or **Ctrl Shift X** (Windows/Linux) to open the *Extensions* view.  
3.  Search for **“QuMaRE Syntax”** or the full identifier **`quiqcl.qumare-syntax`**.  
4.  Click **Install**.  
5.  Reopen a `.qmr` file – colours and snippets are now active!

---

## 2 · Offline / local installation (VSIX)

If you downloaded `qumare-syntax-x.y.z.vsix` from CI or GitHub Releases:

```bash
# VS Code CLI
code --install-extension qumare-syntax-x.y.z.vsix

# Cursor CLI
cursor --install-extension qumare-syntax-x.y.z.vsix
```

Or via the GUI:  
*Extensions ▸ … ▸ Install from VSIX…* and select the file.

---

## 3 · Minimum VS Code version

The extension requires **VS Code 1.90 or newer** _(package.json → `"engines": { "vscode": "^1.90.0" }`)_.  
Update your editor if installation is refused.

---

## 4 · File association

Files ending in **`.qmr`** are detected automatically.  
If you use another extension such as `.qmc`, add this to *settings.json*:

```jsonc
"files.associations": {
  "*.qmc": "qumare"
}
```

---

## 5 · Troubleshooting

| Symptom                                   | Fix |
|-------------------------------------------|-----|
| **No colouring** for `.qmr`               | Check the status‑bar language mode—should read *QuMaRE*. Click it to change if needed. |
| *VSIX too large* when sideloading         | Use the Marketplace version or a minimal VSIX without sample data. |
| “Not compatible with VS Code” error       | Update VS Code / Cursor to ≥ 1.90 or lower the `engines.vscode` field before packaging. |

---

*Open issues or contribute at **<https://github.com/miinukim/qumare-syntax>***.
