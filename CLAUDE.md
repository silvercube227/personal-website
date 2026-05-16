# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

Single-file static personal website for Bennett Ye, a JHU sophomore studying biomedical engineering and CS. Everything lives in `index.html` — HTML, CSS (inline `<style>`), and JS (inline `<script>`) in one file. No build system, no dependencies, no tests.

## Development

- **Preview locally**: open `index.html` directly in a browser, or run `python3 -m http.server` from the repo root and visit `http://localhost:8000`.
- **Deploy**: the repo is the site — push to `main` and whatever host serves it (e.g. GitHub Pages) picks it up. There is no build step.

## Structure notes

- Sections are hardcoded in `index.html`: intro, experience, projects, research & skills, awards, contact. Update copy directly inline; there is no templating or data file.
- Color palette and typography live in the `<style>` block at the top of `index.html`. The page uses a dark gradient background with `Courier New` monospace and blue (`#60a5fa`) accents.
- The name in the H1 (`#name-typewriter`) is rendered by the typewriter script at the bottom of the file — changing the displayed name means editing the `typeWriter(nameElement, 'bennett ye', 100)` call, not the H1 markup.
