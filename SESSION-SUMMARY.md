# Buachie Entertainment — Session Summary
**Date:** October 12, 2026  
**Project:** Million Dollar Musician — Buachie Entertainment Web & Marketing Assets

---

## What We Built

### 1. Mobile-First Website Redesign (`index.html`)

**Goal:** Reformat the existing desktop site into a clean, mobile-friendly single-column "steady roll" layout.

**Key changes made:**
- Replaced the multi-column grid layout with a single-column responsive design
- Added a **hamburger menu** with a CSS/JS slide-down drawer for mobile navigation
- Stacked all package cards vertically (name on left, price on right in each card header)
- Made every form field full-width (removed all two-column form rows)
- Set `font-size: 1rem` (16px minimum) on all form inputs — prevents iOS auto-zoom
- Used CSS custom properties (tokens) for light/dark theme support
- Loaded Google Fonts: **Playfair Display** (headings) + **Inter** (body)

**Contact info updated to:**
- Phone: **757-606-0878**
- Email: **buachieent@gmail.com**

**Live URL:** https://joshbuachie.github.io/buachie-entertainment  
**Custom domain:** https://buachie-ent.com  
**GitHub repo:** https://github.com/joshbuachie/buachie-entertainment

---

### 2. Showbride Platinum Sponsor Banner (`buachie-banner-final.png`)

**Spec:** 1170 × 300 px at 300 dpi — Showbride banner ad format

**Design elements:**
- Dark near-black background with warm gold gradient accents (`#0a0a0a` → `#161208`)
- Gold color palette: `#8B6E2A` / `#C9A84C` / `#E8C96A`
- Left panel: stylized piano keyboard illustration
- Center panel: "BUACHIE ENTERTAINMENT" title + "Virginia Beach Wedding Keyboardist" tagline + website/contact line
- Right panel: musical staff with **4 evenly spaced notes** (no treble clef)
- QR code (bottom right) linking to site

**Contact line on banner:**
```
buachie-ent.com
757-606-0878  ·  buachieent@gmail.com
```

**Iterations during session:**
1. Added phone number to same line as email ✓
2. Treble clef attempted (Unicode `𝄞` — failed in cairosvg, no music font)
3. Hand-drawn SVG path attempted — looked "smashed together" per Joshua's feedback
4. Treble clef **removed entirely** per request
5. Added a **4th note** and spaced all 4 evenly across the staff (60px spacing, cx = 916, 976, 1036, 1096)

**File:** `buachie-banner-final.png` — delivered for download

---

## GitHub Setup

**Repo:** `joshbuachie/buachie-entertainment`  
**Branch:** `main`  
**Commit:** `9edbcf6` — "Mobile-first redesign: single-column layout, hamburger nav, updated contact info"

**Authorization process:**
- GitHub connected in Claude settings, but the Claude GitHub App was not yet installed
- Navigated to **github.com/apps/claude** → Install → configured access for `buachie-entertainment` repo
- After authorization, `git clone` and `git push` succeeded

---

## Technical Notes

| Topic | Detail |
|---|---|
| Banner tool | `cairosvg` Python library — SVG → PNG at specified DPI |
| Unicode issue | `𝄞` (treble clef) renders blank in cairosvg — no music font support |
| iOS form zoom | Set `font-size: 1rem` on inputs — 16px minimum prevents auto-zoom |
| Mobile layout | `flexbox` + `gap`, single column, min 16px side gutter |
| Theme support | CSS custom properties with `prefers-color-scheme` dark/light blocks |

---

## Files Reference

| File | Location | Purpose |
|---|---|---|
| `index.html` | `/home/claude/buachie-entertainment/` | Live website (GitHub Pages) |
| `buachie-banner-final.png` | Delivered to user | Showbride 300dpi banner |
| `buachie-banner-300dpi.svg` | Scratchpad | Banner source SVG |
| `buachie-mobile-preview.html` | Scratchpad | Preview before GitHub push |

---

## Buachie Entertainment Business Context

- **Business:** Wedding keyboardist / entertainment — Virginia Beach, VA
- **Owner:** Joshua Seth-Buachie
- **Goal:** $1M in annual revenue milestone; near-term: surpass $79K/year current salary
- **Platform:** Showbride (wedding expo / vendor platform) — Platinum Sponsor level
- **Band (2027 goal):** Full band with Mike (drums), Isaac Jemes & Shafone (vocals)
- **Target:** 1 wedding gig per month by 2027
