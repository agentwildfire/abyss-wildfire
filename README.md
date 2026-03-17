# Obsidian for Jellyfin

A clean, Apple-inspired dark theme for [Jellyfin](https://jellyfin.org): frosted glass surfaces, refined typography, smooth transitions, and a minimal aesthetic drawing from iOS and macOS design language.

---

## Quick Install

Paste this single line into **Dashboard > Branding > Custom CSS** and save:

```css
@import url('https://cdn.jsdelivr.net/gh/AumGupta/obsidian-jellyfin@main/obsidian.css');
```

---

## Preview


---

## Features

- **Frosted glass UI**: header, drawer, dialogs, and footer all use `backdrop-filter` blur
- **Apple-style typography**: Google Sans throughout, matching iOS/macOS weight and spacing
- **Smooth transitions**: all interactions use Apple's `cubic-bezier(0.25, 0.46, 0.45, 0.94)` ease curve at 150ms
- **Floating sidebar**: pill-shaped drawer with rounded corners and a subtle border
- **Pill tab bar**: active tab highlighted with a filled pill indicator
- **Clean home page**: My Media section shows covers only, no text labels **\***
- **Responsive**: mobile layout tweaks, ultrawide support, and cast thumbnail scaling across all breakpoints
- **Customisable**: three CSS variables let you retheme without touching the rest of the file

> [!CAUTION]  
> **\*** Make sure that you set `My Media` as your "Home screen section 1" if not go in `Settings>Home>Home screen` section 1 select `My Media`.

---

## Customisation

Override any of these variables at the top of your **Custom CSS** field, after the `@import` line:

```css
@import url('https://raw.githubusercontent.com/AumGupta/obsidian-jellyfin/main/obsidian.css');

:root {
    /* Accent colour: R, G, B only, no rgb() wrapper */
    --obsidian-accent: 245, 245, 247;   /* default: near-white */

    /* Corner rounding applied globally */
    --obsidian-radius: 12px;            /* default: 12px */

    /* Episode count / indicator pill background */
    --obsidian-indicator: 55, 55, 55;   /* default: dark grey */
}
```

### Example accent colours

| Look | Value |
|---|---|
| Default (near-white) | `245, 245, 247` |
| Warm white | `255, 250, 240` |
| Soft blue | `100, 160, 255` |
| Teal | `50, 200, 180` |
| Rose | `255, 100, 120` |

> [!NOTE]
> You can also change the font by adding a *Google Fonts* (or any other source) `@import` and overriding the `body` font-family after your theme import. For example, to use [Inter](https://fonts.google.com/specimen/Inter):

> ```css
> @import url('https://cdn.jsdelivr.net/gh/AumGupta/obsidian-jellyfin@main/obsidian.css');
> @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600&display=swap');
> 
> body {
>     font-family: "Inter", sans-serif;
>     font-optical-sizing: auto;
>     font-style: normal;
>     font-variation-settings: "GRAD" 0;
> }
> ```
> Browse fonts at [fonts.google.com](https://fonts.google.com), replace `"Inter"` with any family name you pick.
---

## Compatibility

| Jellyfin version | Status |
|---|---|
| 10.10.x | ✅ Tested |
| 10.9.x | ✅ Should work |
| Earlier | ⚠️ Untested |

> Obsidian targets the **desktop web client**. Mobile layout tweaks are included but the experience is optimised for desktop.

---


## Contributing

Pull requests are welcome. If you find a broken selector after a Jellyfin update, open an issue with your Jellyfin version and a screenshot.

---

## License

Obsidian Jellyfin is licensed under the [LICENSE](LICENSE)

---

## Credits

- Built with inspiration from [Ultrachromic](https://github.com/CTalvio/Ultrachromic) by CTalvio, which provided several foundational patterns for Jellyfin CSS theming.
- [Google Sans](https://fonts.google.com/specimen/Google+Sans) by Google, served via Google Fonts
- [Material Icons Round](https://fonts.google.com/icons) by Google, served via Google Fonts CDN


## Support & Feedback
For suggestions, feature requests, or bug reports, open an issue on the [Issues](https://github.com/AumGupta/obsidian-jellyfin/issues) page.
