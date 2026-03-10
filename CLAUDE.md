# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is a single-file personal resume/portfolio website for a Java backend developer. The entire site lives in `resume.html` — no build tools, no dependencies, no package manager.

## Working with the File

Open `resume.html` directly in a browser to preview. There is no build or lint step.

## Structure

`resume.html` is self-contained with three sections inlined:

- **`<style>`** — All CSS using CSS custom properties (`--bg`, `--accent`, `--text`, etc. defined in `:root`)
- **`<body>`** — Four sections: Hero (`#about`), Skills (`#skills`), Experience (`#experience`), Education/Certs (`#edu`)
- **`<script>`** — Scroll-triggered fade-in animation via `IntersectionObserver`

## Design Conventions

- Dark theme with a blue accent palette; color tokens defined in `:root`
- Three fonts: `Playfair Display` (headings), `JetBrains Mono` (labels/code), `Noto Sans KR` (body)
- Skill categories use modifier classes (`.cat-java`, `.cat-infra`, `.cat-db`, `.cat-front`, `.cat-ai`, `.cat-tools`) for color-coding the left border and title
- Scroll animation: add class `fade-in` to an element; JS adds `visible` when it enters the viewport
- Responsive breakpoint at `768px`; mobile hides nav links and the hero years element
