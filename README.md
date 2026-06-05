# Sakiina's Portfolio Website

A simple portfolio website built with Hugo and Tailwind CSS, deployed automatically to GitHub Pages.

## How It Works

1. You write content in Markdown files (in the `content/` folder)
2. You push your changes to GitHub
3. The site automatically builds and goes live within 2-3 minutes

**Your live site:** https://fester-io.github.io/

---

## How to Edit Your Site

### Edit existing pages

1. Open any `.md` file in the `content/` folder
2. Edit the text (it's plain Markdown — like writing notes)
3. Save, commit, and push to GitHub

### Add a new project

1. Create a new file in `content/projects/` (for example: `content/projects/my-new-project.md`)
2. Copy this template at the top of the file:

```markdown
---
title: "My Project Name"
description: "A short description for the project card"
date: 2026-06-01
image: "/images/my-project-image.png"
link: "https://link-to-live-project.com"
tags: ["tag1", "tag2"]
---

Write your full project description here using Markdown.

## What I Did

- Describe your work
- Add as much detail as you want
```

3. Save, commit, and push — your new project will appear on the site!

### Add images

1. Put your image files in the `static/images/` folder
2. Reference them in your Markdown as `/images/your-filename.png`

### Edit your personal info

Open `hugo.yaml` and update these sections:
- `params.hero` — Your name, tagline, and intro text on the homepage
- `params.social_media` — Your social media links
- `title` — Your site title (shown in the browser tab and navigation)

---

## How Publishing Works

**Simple path (recommended):**
```
Edit a file → Commit → Push to main → Site is live in ~2 minutes
```

**Safe path (preview before publishing):**
```
Create a branch → Edit files → Open a Pull Request → Check that the build passes → Merge → Site goes live
```

The safe path is useful when you're making big changes and want to verify everything looks right before publishing.

---

## One-Time Setup (already done for you)

If you ever need to set up the site on a new GitHub account:

1. Create a new repository on GitHub
2. Push this code to the `main` branch
3. Go to **Settings > Pages > Source** and select **"GitHub Actions"**
4. Wait for the first build to complete (check the Actions tab)
5. Your site will be live at `https://your-username.github.io/`

If using a different username, update `baseURL` in `hugo.yaml` to match.

---

## What NOT to Touch

These folders contain the site's theme and build system. You don't need to edit them:

- `layouts/` — HTML templates (the site's structure)
- `assets/` — CSS and JavaScript source files
- `.github/` — Deployment automation
- `node_modules/` — Build dependencies (not in the repo, created during build)
- `vite.config.mjs` — Build tool configuration
- `postcss.config.js` — CSS processing configuration

**Safe to edit:**
- `content/` — All your pages and projects (Markdown)
- `static/images/` — Your images
- `hugo.yaml` — Site configuration (title, social links, etc.)

---

## File Structure

```
content/
├── _index.md          ← Homepage (minimal, uses hero config from hugo.yaml)
├── about.md           ← About page
├── contact.md         ← Contact page
├── resume.md          ← Resume/CV page
└── projects/
    ├── _index.md      ← Projects listing page intro
    ├── project-one.md ← Individual project
    └── project-two.md ← Individual project

static/
└── images/            ← Your images go here

hugo.yaml              ← Site settings (name, social links, hero text)
```

---

## Quick Markdown Reference

```markdown
# Big Heading
## Medium Heading
### Small Heading

Regular paragraph text.

**Bold text** and *italic text*

- Bullet point
- Another bullet

1. Numbered item
2. Another item

[Link text](https://url.com)

![Image description](/images/filename.png)
```

---

## Need Help?

- [Markdown Guide](https://www.markdownguide.org/basic-syntax/)
- [Hugo Documentation](https://gohugo.io/documentation/)
