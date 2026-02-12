# Swatch Switcher

Switch color variable themes instantly in Sketch. Auto-detects your library structure — no configuration needed.

## Installation

1. [Download the latest release](../../releases/latest)
2. Unzip the downloaded file
3. Double-click `Swatch Switcher.sketchplugin` to install

## Usage

1. Select one or more layers that use color variables from a Library
2. Run **Plugins → Swatch Switcher → Switch Theme...**
3. Choose your target theme from the dropdown
4. Done! All matching colors are switched instantly

### Smart Features

- **Auto-detection**: The plugin finds where "Light" or "Dark" appears in your color paths and switches at that position
- **Partial matching**: If only some colors have counterparts, you'll see a count like `Dark (8/10)` showing how many will switch
- **Multi-library support**: Works with any enabled Sketch Library
- **Symbol overrides**: Switches colors inside Symbol instances too

## Supported Library Structures

The plugin works with any folder organization. Just include "Light" or "Dark" somewhere in your color variable names:

```
Light/Background        ↔  Dark/Background
Colors/Light/Primary    ↔  Colors/Dark/Primary
Accents/Light/Red       ↔  Accents/Dark/Red
Background/Light        ↔  Background/Dark
UI/Buttons/Light/CTA    ↔  UI/Buttons/Dark/CTA
```

## Best Practices for Libraries

### Naming Convention

Include **Light** or **Dark** (case-insensitive) somewhere in your color variable path. The plugin will find it automatically.

Variations that work:
- `Light`, `light`, `LIGHT`
- `Dark`, `dark`, `DARK`
- `Light - Base`, `Dark - Elevated` (compound names work too)

### Folder Structure Examples

**Theme First**
```
Light/
├── Background
├── Text/Primary
└── Text/Secondary
Dark/
├── Background
├── Text/Primary
└── Text/Secondary
```

**Category First**
```
Background/
├── Light
└── Dark
Text/
├── Light/Primary
├── Light/Secondary
├── Dark/Primary
└── Dark/Secondary
```

**Theme in Middle**
```
Accents/
├── Light/Red
├── Light/Blue
├── Dark/Red
└── Dark/Blue
Fills/
├── Light/Base
└── Dark/Base
```

### Tips for Best Results

1. **Keep names consistent** — `Light/Background` should pair with `Dark/Background`, not `Dark/BG`
2. **Match folder depth** — if Light colors are 2 levels deep, Dark should be too
3. **Use the same parent folders** — `Accents/Light/Red` pairs with `Accents/Dark/Red`

## Requirements

- Sketch 70 or later

## License

[MIT](LICENSE) — free to use, modify, and distribute.

---

Made by [Raul](https://github.com/raul)
