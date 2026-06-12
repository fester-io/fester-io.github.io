# Sakiina's Portfolio Website

A portfolio website built with Hugo and Tailwind CSS, deployed automatically to GitHub Pages.

**Your live site:** https://fester-io.github.io/

Every change you save to the `main` branch goes live automatically in about 2 minutes. You never need to "deploy" anything yourself.

---

## How to Edit Your Site (pick the option you like best)

### Option 1: Visual editor — easiest, no technical knowledge needed ⭐

This site works with [Pages CMS](https://pagescms.org), a free visual editor:

1. Go to **https://app.pagescms.org**
2. Click **Sign in with GitHub** (one-time: allow it to access this repository)
3. Pick this repository (`fester-io.github.io`)

You'll see a friendly editor with your **Projects**, **Homepage**, **About**, **Contact**, and **Resume** pages. You can:

- ✏️ Edit any page with a normal text editor (bold, headings, lists — no code)
- ➕ Add a new project with the **Add entry** button — fill in the form, write your story, done
- 🖼️ Upload images straight from your computer (they land in the right folder automatically)
- 💾 Click **Save** — your change is live on the website ~2 minutes later

That's it. No Git, no terminal, no installing anything.

### Option 2: Edit on the GitHub website

1. Open the repository on github.com
2. Browse to the `content/` folder and click any `.md` file
3. Click the **pencil icon** (top right of the file) to edit
4. Make your changes, then click **Commit changes...** → **Commit changes**
5. The site rebuilds and goes live automatically in ~2 minutes

To add a new project this way: open `content/projects/`, click **Add file → Create new file**, name it something like `my-new-project.md`, and paste the template below.

### Option 3: On your computer (for technical users)

```
Edit files → commit → push to main → live in ~2 minutes
```

Local preview: `pnpm install` once, then `pnpm dev` and open http://localhost:1313 (requires Hugo extended ≥ 0.148.2 and Node 22).

---

## Project Template

When creating a project file by hand (Options 2 and 3), start with this:

```markdown
---
title: "My Project Name"
description: "A short description for the project card"
date: 2026-06-01
weight: 10
image: "/images/my-project-image.png"
link: "https://link-to-live-project.com"
tags: ["tag1", "tag2"]
---

Write your full project description here using Markdown.

## What I Did

- Describe your work
- Add as much detail as you want
```

- **weight** controls the order on the projects page: lower numbers show first.
- **image** and **link** are optional — leave them as `""` if you don't have them yet. Projects without an image get a colorful placeholder automatically.

---

## Images

- In the visual editor (Option 1): just upload them where you see an image field.
- By hand: put image files in `static/images/` and reference them as `/images/your-filename.png`.

---

## Changing the Text on the Homepage

The big greeting on the homepage (name, tagline, intro) lives in `content/_index.md` — editable under **Homepage** in the visual editor, or by editing that file directly.

Other site-wide settings live in `hugo.yaml` (rarely needed):

- `title` — site name shown in the browser tab and navigation
- `params.social_media` — your social links (GitHub, LinkedIn, Instagram, Twitter)
- `menu` — the navigation links

---

## Previewing Big Changes Safely (optional)

If you're nervous about a big change, use a Pull Request instead of saving straight to `main`:

```
Create a branch → edit files → open a Pull Request → check the build passes → merge → live
```

The build check runs automatically on every Pull Request.

---

## One-Time Setup (already done for you)

If you ever need to set the site up on a new GitHub account:

1. Create a new repository on GitHub and push this code to the `main` branch
2. Go to **Settings → Pages → Source** and select **"GitHub Actions"**
3. Wait for the first build to finish (check the Actions tab)
4. Your site is live at `https://your-username.github.io/`
5. If the username changed, update `baseURL` in `hugo.yaml` to match

---

## What's Safe to Edit

| Safe to edit | What it is |
|---|---|
| `content/` | All your pages and projects (Markdown) |
| `static/images/` | Your images |
| `hugo.yaml` | Site settings (title, social links, menus) |

**Leave these alone** (they make the site work): `layouts/`, `assets/`, `.github/`, `.pages.yml`, `vite.config.mjs`, `postcss.config.js`, `package.json`.

---

## File Structure

```
content/
├── _index.md          ← Homepage text (greeting, name, tagline)
├── about.md           ← About page
├── contact.md         ← Contact page
├── resume.md          ← Resume/CV page
└── projects/
    ├── _index.md      ← Projects page title and intro
    ├── project-one.md ← Individual project
    └── project-two.md ← Individual project

static/
└── images/            ← Your images go here

hugo.yaml              ← Site settings (title, social links, menus)
.pages.yml             ← Visual editor configuration (Pages CMS)
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

- [Pages CMS documentation](https://pagescms.org/docs/)
- [Markdown Guide](https://www.markdownguide.org/basic-syntax/)
- [Hugo Documentation](https://gohugo.io/documentation/)
