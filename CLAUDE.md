# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

A static portfolio website for Nguyễn Phạm Duy Mạnh, a web developer. Built as a single `code.html` file using vanilla HTML/CSS/JS with TailwindCSS via CDN. No framework, no bundler, no build step.

## Development

- **Run locally**: Open `code.html` with VS Code Live Server (configured on port 5501 in `.vscode/settings.json`)
- **No build/lint/test commands** — everything is in one self-contained HTML file
- **Dependencies**: TailwindCSS (CDN), Google Fonts (Space Grotesk, Manrope), Material Symbols — all loaded externally, no npm install needed

## Architecture

The entire site lives in **`code.html`** with three inline sections:

1. **Tailwind config** (`<script id="tailwind-config">`) — custom color tokens, border radii, font families, letter spacing
2. **Custom CSS** (`<style>`) — fixed background gradients, glow effects, scroll-reveal animation classes, chip asymmetry
3. **HTML body** — semantic sections (hero, projects, skills, experience, education, contact) with anchor-based navigation
4. **JavaScript** (inline `<script>` at bottom) — Intersection Observer for scroll-reveal animations

## Design System ("Kinetic Archive")

The design system is documented in **`DESIGN.md`**. Key rules that must be followed when editing:

- **Color**: Black `#000` background with gold `#ffe792` accents used sparingly. No white for body text — use `#ababab` (`on-surface-variant`)
- **No borders**: Never use 1px solid borders. Separate sections via tonal surface shifts (e.g., `surface-dim` `#0e0e0e` → `surface-container-low` `#131313`)
- **No drop shadows**: Use gold-tinted ambient glow (`primary` color at low opacity) instead of dark shadows
- **Typography**: Space Grotesk for headlines/labels, Manrope for body. Labels in all-caps with `0.1em` tracking
- **Layout**: Asymmetrical margins, non-standard grid offsets (5 or 7 column). Reject template conventions
- **Components**: Chips have asymmetric rounding (full left, sharp right). Cards use full-bleed images with gradient overlays
