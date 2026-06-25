# Optimized Kick Player

<div align="center">

**A clean, fast, and privacy-focused web player for Kick streams**

[![Live Demo](https://img.shields.io/badge/Live%20Demo-GitHub%20Pages-53fc18.svg)](https://onyx-i7.github.io/Optimized-Kick-Player/)
[![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)](https://github.com/Onyx-i7/Optimized-Kick-Player/releases)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![HTML5](https://img.shields.io/badge/HTML5-standards--compliant-orange.svg)](https://developer.mozilla.org/docs/Web/HTML)
[![No Tracking](https://img.shields.io/badge/tracking-none-brightgreen.svg)]()
[![No Ads](https://img.shields.io/badge/ads-none-brightgreen.svg)]()
[![GitHub Issues](https://img.shields.io/github/issues/Onyx-i7/Optimized-Kick-Player)](https://github.com/Onyx-i7/Optimized-Kick-Player/issues)
[![GitHub Stars](https://img.shields.io/github/stars/Onyx-i7/Optimized-Kick-Player)](https://github.com/Onyx-i7/Optimized-Kick-Player/stargazers)

[Live Demo](https://onyx-i7.github.io/Optimized-Kick-Player/) • [Installation](#installation) • [Features](#features) • [Usage](#usage) • [Technical Details](#technical-details) • [Contributing](#contributing)

</div>

---

## 🌐 Live Demo

**Try it now:** [https://onyx-i7.github.io/Optimized-Kick-Player/](https://onyx-i7.github.io/Optimized-Kick-Player/)

The live demo is hosted on GitHub Pages and runs entirely in your browser. No installation required just click and watch.

---

## Overview

Optimized Kick Player is a lightweight, self-contained web application that provides a clean and distraction-free viewing experience for [Kick.com](https://kick.com) live streams. Built with modern web standards, it strips away the clutter of the original platform while preserving full streaming functionality.

### Why Optimized Kick Player?

- **Privacy-first**: Zero tracking, zero analytics, zero third-party scripts
- **Ad-free experience**: No banner ads, no overlays, no sponsored interruptions
- **Performance-optimized**: Minimal DOM footprint, lazy initialization, efficient iframe handling
- **Clean UI**: Dark theme inspired by Kick's native aesthetic with a focus on content
- **Zero dependencies**: Pure HTML, CSS, and vanilla JavaScript — no frameworks, no build steps
- **Fully open source**: Transparent, auditable, and community-driven

---

## Features

### 🎥 Core Player

| Feature | Description |
|---------|-------------|
| **📺 Embedded Streaming** | Native Kick player integration via secure iframe embedding |
| **🔄 Player Reload** | One-click reload to recover from stream hiccups or buffering issues |
| **⚡ Instant Load** | No login wall, no splash screens — enter a channel and start watching |
| **🖥️ Fullscreen Support** | Native fullscreen capability with proper browser API integration |
| **📱 Responsive Layout** | Adapts seamlessly from mobile devices to ultrawide monitors |

### 🎯 Channel Management

| Feature | Description |
|---------|-------------|
| **🔍 Quick Search** | Type any Kick username and press Enter or click "Go" |
| **⭐ Quick Access List** | Pre-configured popular channels for one-click access |
| **🏷️ Visual Feedback** | Active channel is reflected in the input field |
| **📋 Dynamic List Rendering** | Channel buttons are generated on-the-fly with event delegation |

### 🛡️ Privacy & Performance

| Feature | Description |
|---------|-------------|
| **🚫 No Tracking Scripts** | No Google Analytics, no Facebook Pixel, no telemetry of any kind |
| **🚫 No Ad Containers** | No ad slots, no sponsored content, no affiliate links |
| **🔒 Sandboxed iframe** | Streams run in an isolated context with restricted permissions |
| **⚡ Zero External Dependencies** | No CDNs, no npm packages, no third-party libraries |
| **🪶 Lightweight** | Entire application is a single HTML file under 15 KB |

### 🎨 UI/UX Design

| Feature | Description |
|---------|-------------|
| **🌙 Dark Theme** | Kick-inspired color palette (`#0e0e10` / `#53fc18`) |
| **✨ Smooth Transitions** | Subtle hover and active states on interactive elements |
| **🎯 Focus States** | Clear visual indicators for keyboard navigation |
| **📐 Aspect Ratio Lock** | 16:9 player container maintains proper proportions |
| **🎭 Placeholder State** | Friendly empty state with icon and instructions |

---

## Installation

### Option 1: Live Demo (No Installation Required)

Visit the live demo hosted on GitHub Pages:  
**[https://onyx-i7.github.io/Optimized-Kick-Player/](https://onyx-i7.github.io/Optimized-Kick-Player/)**

### Option 2: Direct Download

1. Download the [`index.html`](index.html) file from this repository
2. Save it anywhere on your computer
3. Double-click to open it in your default browser
4. Done — no installation required

### Option 3: Clone the Repository

```bash
git clone https://github.com/Onyx-i7/Optimized-Kick-Player.git
cd Optimized-Kick-Player
# Open index.html in your browser
```

### Option 4: Self-Host

Deploy the single `index.html` file to any static hosting provider:

| Provider | Free Tier | Deploy Time |
|----------|-----------|-------------|
| **GitHub Pages** | ✅ Yes | ~2 minutes |
| **Netlify** | ✅ Yes | ~1 minute |
| **Vercel** | ✅ Yes | ~1 minute |
| **Cloudflare Pages** | ✅ Yes | ~2 minutes |
| **Any web server** | ✅ Yes | Drag & drop |

### Browser Compatibility

| Browser | Status | Notes |
|---------|--------|-------|
| Chrome | ✅ Fully supported | Recommended |
| Firefox | ✅ Fully supported | Recommended |
| Edge | ✅ Fully supported | Chromium-based |
| Safari | ✅ Fully supported | macOS / iOS |
| Opera | ✅ Fully supported | Chromium-based |
| Brave | ✅ Fully supported | Privacy-focused |

> **Note**: Since the player relies on Kick's embed endpoint, any browser that blocks third-party iframes by default may require you to allow them for `player.kick.com`.

---

## Usage

### Basic Usage

1. **Open the player** — Visit the [live demo](https://onyx-i7.github.io/Optimized-Kick-Player/) or launch `index.html`
2. **Enter a channel** — Type a Kick username in the input field (e.g., `xqc`)
3. **Start watching** — Press `Enter` or click the "Go" button
4. **Switch channels** — Enter a new username or click a quick-access button
5. **Reload if needed** — Click "Reload Player" to refresh the current stream

### Quick Access Channels

The player ships with a curated list of popular Kick channels for instant access:

- `xqc`
- `adinross`
- `trainwreckstv`
- `stake`
- `kick`
- `drdisrespect`
- `amouranth`
- `roshtein`

### Customizing the Quick Access List

Edit the `defaultChannels` array in the JavaScript section:

```javascript
const defaultChannels = [
    'yourfavorite',
    'channel1',
    'channel2'
];
```

---

## Technical Details

### Architecture

Optimized Kick Player follows a minimalist, single-file architecture:

```
index.html
├── <head>
│   ├── Meta tags (charset, viewport)
│   └── <style>          → All CSS (scoped, no external stylesheets)
└── <body>
    ├── Header (title + subtitle)
    ├── Player container (iframe host)
    ├── Controls (reload button)
    ├── Channels section (input + quick access)
    ├── Disclaimer
    └── <script>         → All JavaScript (vanilla ES6+)
```

### Core Components

| Component | Responsibility |
|-----------|---------------|
| **`loadChannel(channel)`** | Handles iframe creation, cleanup, and Kick embed URL generation |
| **`reloadPlayer()`** | Re-initializes the current channel's iframe |
| **`renderChannelList(channels)`** | Dynamically generates quick-access buttons with event delegation |
| **Event Listeners** | Manages user input (click, Enter key) and DOM ready state |

### Performance Considerations

- **Single HTTP request**: The entire app loads in one request (no CSS/JS files to fetch)
- **No render-blocking resources**: All styles and scripts are inline
- **Efficient DOM updates**: Iframe is replaced, not re-rendered on reload
- **Event delegation**: Channel buttons share a single listener pattern
- **Zero runtime dependencies**: No library overhead

### Security Model

| Concern | Mitigation |
|---------|-----------|
| **XSS** | No user input is rendered as HTML; channel names are sanitized via `.textContent` |
| **Iframe isolation** | Streams run in a sandboxed `<iframe>` with explicit `allow` directives |
| **No data collection** | No cookies, localStorage, or network requests beyond the Kick embed |
| **No external scripts** | Zero attack surface from third-party JavaScript |
| **HTTPS only** | Embed URL uses `https://player.kick.com/` |

### How It Works

```
User enters channel name
        ↓
Input sanitized (trimmed + lowercased)
        ↓
Existing iframe removed (if any)
        ↓
New iframe created with src:
  https://player.kick.com/{channel}
        ↓
iframe injected into player container
        ↓
Browser loads Kick's official player
        ↓
Stream plays natively
```

---

## Development

### Project Structure

```
Optimized-Kick-Player/
├── index.html       # Complete application (HTML + CSS + JS)
├── README.md        # This file
└── LICENSE          # MIT license
```

### Local Development

No build tools, no package managers, no compilers. Just open and edit:

```bash
# Clone the repo
git clone https://github.com/Onyx-i7/Optimized-Kick-Player.git
cd Optimized-Kick-Player

# Open in your favorite editor
code .

# Open in browser
open index.html          # macOS
xdg-open index.html      # Linux
start index.html         # Windows
```

### Testing Checklist

- [ ] Load a valid Kick channel
- [ ] Verify fullscreen works
- [ ] Test quick-access buttons
- [ ] Test Enter key submission
- [ ] Test player reload
- [ ] Verify responsive layout on mobile
- [ ] Confirm no console errors
- [ ] Check network tab for unwanted requests

---

## Contributing

Contributions are welcome! Here's how you can help:

### Reporting Bugs

1. Check existing [issues](https://github.com/Onyx-i7/Optimized-Kick-Player/issues) first
2. Create a new issue with:
   - Clear description of the problem
   - Steps to reproduce
   - Expected vs actual behavior
   - Browser and version
   - Screenshots if applicable

### Feature Requests

Have an idea? Open an issue and describe:

- The feature you'd like to see
- The use case and benefits
- Mockups or examples if possible

### Code Contributions

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/my-feature`
3. Make your changes
4. Test thoroughly across browsers
5. Commit with clear messages: `git commit -m 'Add feature'`
6. Push to your fork: `git push origin feature`
7. Open a Pull Request

### Code Style

- Use modern JavaScript (ES6+)
- Keep the single-file architecture
- No external dependencies
- Comment complex logic
- Test across multiple browsers

---

## Roadmap

### Completed ✅

- [x] Core iframe-based player
- [x] Channel input with Enter key support
- [x] Quick-access channel buttons
- [x] Player reload functionality
- [x] Responsive dark theme
- [x] Privacy-first design (no tracking, no ads)
- [x] Zero-dependency architecture
- [x] GitHub Pages deployment

### Planned Features

- [ ] **Channel history** — Remember recently watched channels (localStorage)
- [ ] **Custom quick-access list** — User-configurable favorites via UI
- [ ] **Picture-in-Picture** — Native PiP button for multitasking
- [ ] **Stream quality selector** — Expose quality options when available
- [ ] **Chat overlay** — Optional embedded Kick chat panel
- [ ] **Multi-stream view** — Watch up to 4 streams simultaneously
- [ ] **Custom themes** — User-selectable color schemes
- [ ] **Keyboard shortcuts** — Space to pause, F for fullscreen, etc.
- [ ] **PWA support** — Install as a standalone app
- [ ] **Offline placeholder** — Better UX when channel is offline

---

## FAQ

**Q: Is this legal?**  
A: Yes. The player uses Kick's official embed endpoint (`player.kick.com`), which is publicly available and designed for embedding. No streams are hosted, modified, or redistributed.

**Q: Does this bypass Kick's ads?**  
A: The player itself does not inject ad-blockers. Any ad-free experience depends on Kick's own embed behavior and your browser's settings.

**Q: Can I self-host this?**  
A: Absolutely. It's a single HTML file — drop it on any static host (GitHub Pages, Netlify, your own server).

**Q: Will this work with other streaming platforms?**  
A: Currently only Kick is supported. However, the architecture could be adapted for Twitch, YouTube Live, etc., with minor modifications.

**Q: Why doesn't the player load a specific channel?**  
A: Possible reasons:
- The channel name is misspelled
- The channel is currently offline
- Kick's embed endpoint is temporarily unavailable
- Your browser blocks third-party iframes

**Q: Does this collect any data?**  
A: **No.** Zero telemetry. Zero analytics. Zero cookies. The only network request is the iframe loading Kick's player.

**Q: Can I modify the quick-access channels?**  
A: Yes. Edit the `defaultChannels` array in the `<script>` section of `index.html`.

**Q: Why is this better than just visiting Kick.com?**  
A: No ads, no tracking, no clutter, no login wall. Just the stream.

**Q: How do I deploy my own version on GitHub Pages?**  
A: 
1. Fork this repository
2. Go to Settings → Pages
3. Select "Deploy from branch" → `main` → `/ (root)`
4. Your site will be live at `https://yourusername.github.io/Optimized-Kick-Player/`

---

## Credits

### Inspiration

- [Kick.com](https://kick.com) — Streaming platform and embed API
- Minimalist media player designs
- Privacy-first web applications

### Technologies

- **HTML5** — Semantic markup
- **CSS3** — Flexbox, Grid, custom properties
- **Vanilla JavaScript (ES6+)** — No frameworks, no libraries
- **Kick Player Embed** — Official streaming endpoint
- **GitHub Pages** — Free static hosting

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

```
MIT License

Copyright (c) 2026 Onyx-i7

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction...
```

---

## Support

If you find this project useful, consider:

- ⭐ **Starring the repository** — It helps others discover it
- 🌐 **Using the live demo** — [Try it now](https://onyx-i7.github.io/Optimized-Kick-Player/)
- 🐛 **Reporting bugs** — Help improve stability
- 💡 **Suggesting features** — Shape the roadmap
- 🔧 **Contributing code** — PRs are welcome

---

## Contact

- **GitHub**: [@Onyx-i7](https://github.com/Onyx-i7)
- **Repository**: [Optimized-Kick-Player](https://github.com/Onyx-i7/Optimized-Kick-Player)
- **Live Demo**: [GitHub Pages](https://onyx-i7.github.io/Optimized-Kick-Player/)
- **Issues**: [GitHub Issues](https://github.com/Onyx-i7/Optimized-Kick-Player/issues)

---

<div align="center">

**Built by [Onyx-i7](https://github.com/Onyx-i7)**

*Clean streams. Zero noise. Pure content.*

[🚀 Try the Live Demo](https://onyx-i7.github.io/Optimized-Kick-Player/)

</div>
