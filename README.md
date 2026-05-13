# George-Sodini Archive

## Overview

This repository is a **static archival website** preserving material related to George Sodini, including:

- A reproduction of diary-style blog entries (`index.htm`)
- A compiled biographical/research page (`me.htm`)
- An archival publication page for two YouTube videos with embedded playback, transcripts, and metadata (`publication.htm`)
- Supporting image and video assets under `imgs/` and `videos/`

The site appears intended for historical/archival reference and documentation of events around the August 4, 2009 LA Fitness shooting in Pennsylvania.

---

## Content Warning

This repository contains material that may be distressing, including:

- Graphic and explicit misogynistic language
- Discussions of violence, suicide, and mass shooting
- Victim details and post-incident reporting

Please use discretion.

---

## Repository Contents

### Top-level files

- `index.htm` — Archive-style diary page with dated entries and maintainer note
- `me.htm` — "About" page with biography, timeline, references, and image galleries
- `publication.htm` — Video archive page for two YouTube uploads, each with metadata and transcript
- `LICENSE` — The Unlicense (public domain dedication)

### Asset directories

- `imgs/` — Still images used by `me.htm` and visual context graphics
- `videos/` — Two MP4 files embedded in `publication.htm`

---

## Detailed Page Map

### 1) `index.htm` (Diary Archive)

Primary features:

- Header summary (age, DOB/DOD, location, basic profile)
- Navigation links:
  - `Me` → `me.htm`
  - `Videos` → `publication.htm`
- Long sequence of dated diary entries (late 2008 to August 2009)
- Maintainer-added note exposing a commented-out original entry
- Footer preserving original reproduction language and intent

Technical notes:

- Entirely static HTML
- Minimal inline styling for responsive layout (`max-width`, `overflow-x` protection)

---

### 2) `me.htm` (Biography / Context Page)

Primary features:

- Introductory note that original `me.htm` could not be located
- Structured sections with headings, including:
  - Personal background
  - Online presence and writings
  - Planning and preparation
  - Shooting incident
  - Immediate aftermath
  - References
- Multiple interactive image galleries (thumbnail strip + main image switch)
- Reference list with external links (news and archival sources)

Client-side behavior:

- Inline JavaScript function `switchGallery(...)` updates the main image and active thumbnail class

Styling/layout:

- Inline CSS defines infobox and gallery components
- Mobile fallback for infobox at narrow widths (`@media (max-width: 500px)`)

---

### 3) `publication.htm` (Video Archive)

Primary features:

- Header and back navigation links to `index.htm` and `me.htm`
- Two embedded videos (local MP4 sources)
- For each video:
  - Metadata summary (upload date, duration, codec, bitrate, container, URL)
  - Expandable raw metadata JSON (`<details>` + `<textarea readonly>`)
  - Full transcript block
  - Narrative summary paragraph
- Concluding archival context note about discovery/investigation

Video files referenced:

- `videos/How George Pittsburgh Lives.mp4`
- `videos/Hide from Emotion.mp4`

---

## Asset Inventory

### `imgs/`

Repository image assets currently include:

- `elizabeth_gannon.jpg`
- `heidi_overmier.jpg`
- `jody_billingsley.jpg`
- `shooting_graphic.gif`
- `sodini_000.jpg`
- `sodini_001.jpg`
- `sodini_002.jpg`
- `sodini_003.jpg`
- `sodini_004.jpg`
- `sodini_005.jpg`
- `sodini_006.jpg`
- `sodini_101.jpg`
- `sodini_102.jpg`
- `sodini_103.jpg`
- `sodini_104.jpg`
- `sodini_105.jpg`
- `sodini_106.jpg`
- `sodini_107.jpg`
- `sodini_video.jpg`
- `.keep`

### `videos/`

- `How George Pittsburgh Lives.mp4`
- `Hide from Emotion.mp4`
- `.keep`

---

## How to View Locally

Because this is a static site, you can open it directly in a browser or serve it locally.

### Option A: Open directly

Open:

- `index.htm`

in your browser.

### Option B: Run a local static server

From the repository root:

```bash
python3 -m http.server 8000
```

Then visit:

- `http://localhost:8000/index.htm`

Using a local server is recommended for consistent media loading and relative path behavior.

---

## Navigation Flow

- `index.htm` → `me.htm`
- `index.htm` → `publication.htm`
- `me.htm` → `index.htm` and `publication.htm`
- `publication.htm` → `index.htm` and `me.htm`

This creates a closed three-page archival navigation loop.

---

## Technical Characteristics

- No build step
- No package manager metadata (`package.json`, `pyproject.toml`, etc.)
- No test or lint configuration in repository
- No framework dependency; plain HTML/CSS/JS
- Inline styles/scripts (no external CSS/JS bundles)

---

## Provenance and Framing

This archive combines:

- Apparent original/quoted diary-style material
- Maintainer-added contextual notes
- Reconstructed/compiled biographical content from cited external reports
- Preserved video transcripts and extracted metadata

Users should treat all claims as archival material that may require independent source verification.

---

## Legal / License

This repository is licensed under **The Unlicense** (`LICENSE`), placing contents in the public domain where legally recognized.

Key point: content is provided **"AS IS"** without warranty.

---

## Maintenance Notes

If you plan to update this archive:

- Keep relative paths intact (`imgs/...`, `videos/...`)
- Preserve cross-page links between the three HTML files
- Verify media filenames exactly match references in HTML
- Preserve or clearly annotate any editorial additions vs. original archival text

