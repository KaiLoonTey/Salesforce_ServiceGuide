# Setup Guide — From Template to Live Website

This template builds a Trimble-branded documentation website using **MkDocs** and the **Material for MkDocs** theme. It publishes free on **GitHub Pages** and rebuilds automatically every time you push a change.

You do not need to know HTML, CSS, or JavaScript. Content is written in Markdown — plain text with a few simple formatting marks.

**Time required:** about 30 minutes for the first setup. After that, publishing a change takes under a minute.

---

## What you will end up with

A live site at:

```
https://<your-github-username>.github.io/<your-repo-name>/
```

Tabs across the top, a sidebar, full-text search, click-to-zoom screenshots, and Trimble corporate styling applied automatically.

---

## Step 1 — Install the two tools you need

### 1.1 Install Python

Download from [python.org/downloads](https://www.python.org/downloads/) and run the installer.

> **Important:** on the first screen of the installer, tick **"Add Python to PATH"** before clicking Install. If you miss this, the commands later in this guide will not be recognised.

Verify it worked. Open **PowerShell** and run:

```powershell
python --version
```

You should see a version number such as `Python 3.12.4`.

### 1.2 Install Git

Download from [git-scm.com/downloads](https://git-scm.com/downloads) and run the installer. Accept all the default options.

Verify:

```powershell
git --version
```

You should see something like `git version 2.45.1`.

If either command returns *"is not recognized"*, close PowerShell completely, open it again, and retry. A fresh window is needed to pick up the new PATH.

---

## Step 2 — Unpack the template

1. Extract the template ZIP file.
2. Rename the extracted folder to your project name — for example `powerfab-training` or `tekla-structures-docs`.
3. Move it somewhere sensible, such as `D:\Websites\powerfab-training`.

Use lowercase letters and hyphens in the folder name, with no spaces. This name will appear in your public URL.

Inside you should see:

```
your-project-name/
├── .github/workflows/deploy.yml   Automatic publishing (do not edit)
├── docs/                          All your content lives here
│   ├── assets/                    Theme CSS and images
│   ├── guide/                     How-to pages (delete when you go live)
│   ├── example/                   Example pages (delete when you go live)
│   └── index.md                   Your home page
├── mkdocs.yml                     Site configuration and navigation
├── requirements.txt               Software versions (do not edit)
├── .gitignore                     Files to exclude (do not edit)
└── SETUP-GUIDE.md                 This file
```

---

## Step 3 — Preview the site on your own machine

Open PowerShell **inside your project folder**. The quickest way: open the folder in File Explorer, click the address bar, type `powershell`, and press Enter.

Install the software the site needs — this is a one-time step per machine:

```powershell
pip install -r requirements.txt
```

Start the preview server:

```powershell
python -m mkdocs serve
```

Open `http://127.0.0.1:8000` in your browser. The site is now running locally.

Leave this window running while you work. Every time you save a Markdown file, the browser refreshes automatically. Press **Ctrl+C** in PowerShell to stop it.

> **Always preview before publishing.** It takes seconds and catches most mistakes.

---

## Step 4 — Make it yours

### 4.1 Edit the site name

Open `mkdocs.yml` in any text editor (Notepad works, VS Code is better). Change the top three lines:

```yaml
site_name: PowerFab Training
site_description: Tekla PowerFab training documentation for the SEA region
site_url: https://taufiktrimble.github.io/powerfab-training/
```

The `site_url` must match the GitHub username and repository name you will create in Step 5. Get this right now and you will not have to revisit it.

### 4.2 Read the guide pages

The template ships with three pages under **Guide** and three under **Examples**. Read them in the browser preview — they explain page structure, callout boxes, tables, tabs, and screenshots, using real Tekla PowerFab content as the example.

### 4.3 Write your own content

1. Create a `.md` file inside `docs/`, in whatever subfolder makes sense.
2. Add that file to the `nav:` block at the bottom of `mkdocs.yml`.

**A page not listed in `nav:` will not appear on the site.** This is the single most common mistake.

### 4.4 Delete the template pages

Once you have your own content, delete the `docs/guide/` and `docs/example/` folders, and remove their entries from `nav:`. You can also delete `SETUP-GUIDE.md`.

---

## Step 5 — Create the GitHub repository

The repository must exist before you can publish. Nothing creates it automatically.

1. Go to [github.com](https://github.com) and sign in.
2. Click **+** in the top right, then **New repository**.
3. **Repository name:** use exactly the same name as your project folder, for example `powerfab-training`.
4. **Visibility:** choose **Public**. GitHub Pages on private repositories requires a paid plan.
5. **Do not tick** "Add a README file", "Add .gitignore", or "Choose a license". The repository must be completely empty — the template already contains these files, and pre-adding them causes a conflict on your first push.
6. Click **Create repository**.

Leave the resulting page open. You will need the URL shown on it.

---

## Step 6 — Push the template to GitHub

Back in PowerShell, inside your project folder. If the preview server is still running, press **Ctrl+C** first.

Run these commands one at a time:

```powershell
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git
git push -u origin main
```

Replace `YOUR-USERNAME` and `YOUR-REPO-NAME` with your actual values.

On the final command a browser window will open asking you to sign in to GitHub. Authorise it. This happens once per machine.

Refresh your GitHub repository page — your files should now be there.

---

## Step 7 — Turn on GitHub Pages

1. In your repository, go to **Settings**.
2. Select **Pages** from the left sidebar.
3. Under **Build and deployment**, set **Source** to **GitHub Actions**.

That is the only setting you need. **Do not** click **Configure** on the "GitHub Pages Jekyll" or "Static HTML" cards — the template already includes its own publishing workflow, and adding a second one causes conflicts.

---

## Step 8 — Confirm the first publish

1. Go to the **Actions** tab in your repository.
2. Find the run named **Deploy MkDocs to GitHub Pages**.

| What you see | Meaning | What to do |
|---|---|---|
| Yellow spinning circle | Building | Wait one to two minutes |
| Green tick | Published | Open your site |
| Red cross | Failed | See below |

**If the first run failed with a red cross,** this is normal and expected. It happens because you pushed before enabling Pages in Step 7, so the publishing step had nowhere to publish to.

Fix it: click the failed run, then click **Re-run all jobs** in the top right. It will pass now that Pages is enabled.

Your site is live at:

```
https://<your-github-username>.github.io/<your-repo-name>/
```

---

## Publishing changes from now on

This is the routine for everything you do afterwards. Three commands:

```powershell
git add .
git commit -m "Describe what you changed"
git push
```

Publishing starts automatically. The site updates in roughly 40 seconds.

If you still see the old content after the green tick appears, that is your browser cache. Press **Ctrl+Shift+R** to force a refresh.

### Editing directly on GitHub

For small corrections — a typo, one sentence, one table row — you do not need your PC at all:

1. Open the repository, navigate to the `.md` file.
2. Click the **pencil** icon (Edit this file).
3. Make the change.
4. Scroll down and click **Commit changes**.

Publishing triggers automatically.

> **If you edit on GitHub, your local folder is now out of date.** Before pushing from your PC again, run `git pull` first. Otherwise `git push` will be rejected.

---

## Troubleshooting

| Problem | Cause | Fix |
|---|---|---|
| `python` or `git` is not recognized | PATH not picked up | Close PowerShell, reopen, retry. If it persists, reinstall Python with "Add to PATH" ticked. |
| `mkdocs` is not recognized | Scripts folder not on PATH | Use `python -m mkdocs serve` instead of `mkdocs serve`. |
| `remote origin already exists` | `git remote add` was run twice | `git remote set-url origin https://github.com/USER/REPO.git` |
| `failed to push some refs` | Repository was created with a README | `git pull origin main --allow-unrelated-histories` then push again |
| Actions run fails at "build" | A page in `nav:` does not exist, or a link is broken | Open the failed run, read the red error line. It names the file. |
| Page written but not on the site | Not listed in `nav:` | Add it to `nav:` in `mkdocs.yml` |
| Site shows raw `.md` files | Pages Source set to a branch instead of GitHub Actions | Settings → Pages → Source → **GitHub Actions** |

### Why builds fail rather than publish quietly

The workflow runs `mkdocs build --strict`, which treats broken navigation entries and broken internal links as errors instead of warnings. A build that fails loudly is far better than a site that silently publishes with dead links — but it does mean that a red cross means *nothing was published*, and the live site still shows the previous version.

---

## Quick reference

| Task | Command |
|---|---|
| Install site software (once per machine) | `pip install -r requirements.txt` |
| Preview locally | `python -m mkdocs serve` |
| Check for errors without previewing | `python -m mkdocs build --strict` |
| Publish changes | `git add .` → `git commit -m "message"` → `git push` |
| Get latest changes made by others | `git pull` |
