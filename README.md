# ShivaOps Project Portfolio

This repository contains the source for my **account-level GitHub Pages site**:

**Live site:** `https://shivaops.github.io/`

Built with **MkDocs** and **Material for MkDocs**, this portfolio brings together my main showcase areas:

- **Smart Trip** — AI-Assisted Airline Booking Simulator
- **DevOps Lab** — CI/CD, Docker and Kubernetes Practice Platform
- **GRPF** — Runtime Oracle Report Parameter Form Builder with AI-Assisted Design

## What this repository contains

This is the **source repository** for the website.

Main folders and files:

- `docs/` — markdown pages, images, files and site content
- `mkdocs.yml` — site navigation and theme configuration
- `requirements.txt` — Python packages used for local preview and deployment

## Run locally

```bash
pip install -r requirements.txt
mkdocs serve
```

Then open:

```text
http://127.0.0.1:8000
```

## Build the site

```bash
mkdocs build
```

## Deploy to GitHub Pages

This site is published from the **`gh-pages`** branch using:

```bash
mkdocs gh-deploy
```

Typical update flow:

```bash
git add .
git commit -m "Update portfolio site"
git push
mkdocs gh-deploy
```

## Repository and live site

- **Repository:** `https://github.com/shivaops/shivaops.github.io`
- **Live site:** `https://shivaops.github.io/`

## Notes

- Edit content in the source files under `docs/`
- Do not manually edit generated files in the `gh-pages` branch
- Preview locally before deploying changes
