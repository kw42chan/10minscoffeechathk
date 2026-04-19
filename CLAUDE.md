# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a single-file static personal branding website for **Clara Liu (劉克拉)**, a Hong Kong-based entrepreneur who offers personal branding courses, book clubs (讀書會), and growth journaling systems (成長手帳). The site is written in Traditional Chinese (zh-TW).

## Development

No build system, package manager, or server is needed. Open the file directly in a browser:

```
start 10minscoffeechat_hk-website.html   # Windows
open 10minscoffeechat_hk-website.html    # macOS/Linux
```

## Architecture

**Single file:** `10minscoffeechat_hk-website.html` (~920 lines) — all HTML, CSS, and JavaScript are self-contained.

**CSS custom properties** defined in `:root` control the entire color palette:
- `--teal` / `--teal-dark` / `--teal-light` / `--teal-pale` — primary brand color
- `--warm` / `--warm-mid` / `--warm-dark` — neutral warm grays
- `--ink` / `--ink-light` — text colors
- `--cream` — page background
- `--gold` — accent

**Google Fonts** (loaded via CDN): Noto Serif TC, Noto Sans TC, Playfair Display

**Page sections** (by ID, in order):
| ID | Content |
|----|---------|
| `#hero` | Main hero with photo, headline, CTA buttons |
| `.ticker-wrap` | CSS-animated scrolling testimonials |
| `#proof` | Student testimonial cards grid |
| `#about` | About Clara section |
| `#programs` | Three-tier course offerings |
| `#free` | Podcast episodes + free resource download cards |
| `#speaking` | Speaking engagement stats and topics |
| `#cta` | Final call-to-action band |
| footer | Links, socials, copyright |

**Hero photo** is an embedded base64 PNG (`data:image/png;base64,...`) inside an `<img>` tag within `.hero-photo-frame`.

**Contact email:** hello@claraliu.com (used in the speaking section mailto link)

All internal navigation uses anchor links (`href="#section-id"`). All external links (social media, programs, resources) currently use placeholder `href="#"`.
