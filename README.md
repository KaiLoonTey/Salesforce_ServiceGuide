# Trimble Documentation Site Template

Starter template for building Trimble-branded documentation websites with **MkDocs** + **Material for MkDocs**, published free on **GitHub Pages**.

Content is written in Markdown. No HTML, CSS, or JavaScript knowledge required.

## Start here

**Read `SETUP-GUIDE.md`.** It covers the whole process from installing Python to publishing your first live page.

## Quick reference

```powershell
pip install -r requirements.txt     # once per machine
python -m mkdocs serve              # preview at http://127.0.0.1:8000
python -m mkdocs build --strict     # check for errors before pushing

git add .
git commit -m "Describe the change"
git push                            # publishes automatically
```

## What's in the box

| Path | Purpose |
|---|---|
| `SETUP-GUIDE.md` | Full setup walkthrough — read this first |
| `mkdocs.yml` | Site name, URL, and navigation |
| `docs/` | All content |
| `docs/assets/trimble-theme.css` | Trimble branding — do not edit |
| `docs/assets/images/` | Screenshots |
| `docs/guide/` | How to write and publish — delete when live |
| `docs/example/` | Example page layouts — delete when live |
| `.github/workflows/deploy.yml` | Automatic publishing — do not edit |
| `requirements.txt` | Software versions — do not edit |

## Two rules that prevent most problems

1. **A page not listed in `nav:` will not appear on the site.** Create the file, then register it in `mkdocs.yml`.
2. **A red cross in the Actions tab means nothing was published.** The live site still shows the previous version.

## Before going live

- Update `site_name`, `site_description`, and `site_url` in `mkdocs.yml`
- Delete `docs/guide/` and `docs/example/`, and remove them from `nav:`
- Delete `SETUP-GUIDE.md`
