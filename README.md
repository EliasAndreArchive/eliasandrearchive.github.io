<p align="center">
  <img src="visual-field-notes-mark.svg" width="72" alt="Visual Field Notes logo">
</p>

<h1 align="center">Visual Field Notes</h1>

<p align="center">
  A personal cinematography archive by Elias Andre.<br>
  <a href="https://eliasandre.space/#home"><strong>Visit eliasandre.space →</strong></a>
</p>

## About

Visual Field Notes documents real scenes as they unfold through a raw, grounded and artistic perspective. The archive brings together short cinematic observations shaped by documentary framing, expressive color and the character of the equipment used to capture them.

## The experience

- A free-moving visual canvas on desktop and an organic vertical layout on mobile
- Continuously playing video previews with full-quality playback on focus
- A Performance mode for lighter, faster loading on lower-end devices
- Animated collection changes and focused clip views
- Shareable links for individual collections and clips
- A responsive About page with contact and production information

## How it is built

The site is a lightweight static project built with HTML, CSS and JavaScript. Clip metadata, labels, collection placement and display sizes are managed in [`media.json`](media.json). Video files and their smaller performance previews are stored in Cloudflare R2.

The source lives in this GitHub repository. The public website is deployed through Cloudflare Pages and served from **[eliasandre.space](https://eliasandre.space/#home)**. The repository name is retained from the site's earlier GitHub Pages version.

Instructions for adding new work are available in [`ADDING_MEDIA.md`](ADDING_MEDIA.md).

---

© 2026 Elias Andre. All rights reserved.
