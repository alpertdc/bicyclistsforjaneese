# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

A single-page advocacy website at `cyclistsforjaneese.com` making the case for why DC cyclists should vote for Janeese Lewis George for mayor. The companion long-form case is at the Substack post linked in the footer.

## Tech Stack

Plain HTML/CSS/vanilla JS — no build step, no framework, no dependencies besides Google Fonts (loaded via CDN). Everything lives in `index.html`.

## Deployment

GitHub Pages with a custom domain. The `CNAME` file contains `cyclistsforjaneese.com`. To deploy, just push to `main` — GitHub Pages serves the root `index.html` automatically.

To configure the custom domain for the first time:
1. Push the `CNAME` file to the repo
2. In repo Settings → Pages, set the custom domain to `cyclistsforjaneese.com`
3. Add a CNAME DNS record at your registrar pointing `cyclistsforjaneese.com` to `<username>.github.io`

## Key Links (do not change without verifying with owner)

- **Donate (tracked):** `https://secure.actblue.com/donate/jlg-do-20251201?refcode=jlg-ms-do-20251201-id-87`
- **Volunteer:** `https://www.mobilize.us/janeesefordc/`
- **Campaign site:** `https://janeesefordc.com/`
- **Substack source post:** `https://moderatesforjaneese.substack.com/p/janeese-lewis-george-will-keep-my`
- **Hero photo:** `https://substack-post-media.s3.amazonaws.com/public/images/f494171a-5cd1-4e20-a946-af7ce11d274b_900x876.jpeg` — replace when better Janeese-on-a-bike photos are available

## Design System

Defined as CSS custom properties in `:root`:
- `--purple-dark` / `--purple-mid` / `--purple` / `--purple-light` — brand purple scale
- `--lime` / `--lime-dark` — cyclist accent color
- `--off-white` — light purple-tinted background for alternating sections

Scroll animations use `.fade-up` + `.delay-1` / `.delay-2` classes toggled by an `IntersectionObserver` in the inline script.
