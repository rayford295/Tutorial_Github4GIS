# Detailed Guide: Building Your Academic Website with GitHub Pages

**GIS Practicum · April 15, 2026**

---

## Overview

GitHub Pages turns any GitHub repository into a free, live website.  
Your site address: `https://your-username.github.io`

There are three paths — pick the one that fits your comfort level:

| Path | Time | Skill needed | Best for |
|------|------|--------------|----------|
| [A. Use the template](#path-a) | 5 min | None | Most students → start here |
| [B. Jekyll theme](#path-b) | 10 min | None | Want more design options |
| [C. Custom HTML](#path-c) | 30 min+ | Basic HTML/CSS | Full control |

---

<a id="path-a"></a>
## Path A — Use the Class Template (Recommended)

This is the fastest way. You get a professional site and only need to fill in your info.

### Step 1 — Fork the template

Go to: **https://github.com/rayford295/academic-website-template**

Click the green **"Use this template"** button → **"Create a new repository"**

Fill in:
- **Repository name:** `your-username.github.io`  
  *(Replace `your-username` with your actual GitHub username. Must match exactly.)*
- **Visibility:** Public
- Click **"Create repository"**

> ⚠️ The repo name **must** be `your-username.github.io` for GitHub Pages to work automatically.

---

### Step 2 — Enable GitHub Pages

In your new repo:

1. Click **Settings** (top menu bar)
2. Scroll down to **Pages** in the left sidebar
3. Under **Source**, select **Deploy from a branch**
4. Branch: `main` · Folder: `/ (root)`
5. Click **Save**

GitHub will show: *"Your site is ready to be published at https://your-username.github.io"*

Wait **1–2 minutes**, then visit the URL.

---

### Step 3 — Edit your content

Click on `index.html` in your repo, then click the **pencil icon** (✏) to edit.

Press `Ctrl+F` and search for **`✏️ EDIT`** — every line you need to change is marked.

**The 10 things to change:**

```
1.  <title>          → Your name and role
2.  .nav-name        → Your name in the navbar
3.  <h1>             → Your full name
4.  .position        → PhD Student · Your Department
5.  .university      → Your University · Advisor: Prof. X
6.  Hero links       → Your email, GitHub URL, Google Scholar URL
7.  YN in avatar     → Your initials (e.g., "JD" for Jane Doe)
8.  About section    → 2–3 sentences about your research
9.  Research tags    → Your actual research areas
10. Publications     → Copy the <li> block for each of your papers
```

After editing, scroll down and click **"Commit changes"** → **"Commit directly to main"**.

Your site updates automatically within 30–60 seconds.

---

### Step 4 — Add a profile photo (optional but recommended)

1. In your repo, click **"Add file"** → **"Create new file"**
2. Type `assets/photo.jpg` as the filename  
   *(This creates the `assets/` folder automatically)*
3. Click **"Choose your files"** and upload your photo
4. Commit the file

Then in `index.html`, inside `<div class="avatar">`:
- Delete the text `YN`
- Uncomment this line (remove `<!--` and `-->`):
  ```html
  <img src="assets/photo.jpg" alt="Your Name">
  ```

---

### Step 5 — Add your CV (optional)

1. Upload your PDF as `assets/cv.pdf` (same method as the photo)
2. The CV download link in the hero already points to `assets/cv.pdf` — nothing else to change

---

<a id="path-b"></a>
## Path B — Jekyll Theme (No Coding)

If you want more design variety without writing HTML, GitHub has built-in themes.

### Step 1 — Create the repo

- Go to **github.com** → click **"New repository"**
- Name: `your-username.github.io`
- Check **"Initialize with README"**
- Click **"Create repository"**

### Step 2 — Enable Pages with a theme

1. **Settings → Pages → Source:** main branch → Save
2. Click **"Choose a theme"**
3. Pick a theme (Cayman, Minimal, Slate, etc.) → click **"Select theme"**

GitHub automatically creates `_config.yml` in your repo with the theme set.

### Step 3 — Edit README.md

Your site renders from `README.md` (or `index.md`). Edit it with Markdown:

```markdown
# Jane Doe

PhD Student · Department of Geography · Texas A&M University  
Advisor: Prof. John Smith

---

## About Me

I study [your topic] using [your methods]. My current project focuses on ...

## Research Interests

- GIScience and GeoAI
- Remote sensing and satellite imagery  
- Natural hazard response

## Publications

**Doe, J.**, Smith, J. (2025). *Paper title.* Journal of Geography. [PDF](#) [DOI](#)

## Contact

- Email: jdoe@tamu.edu  
- GitHub: [github.com/janedoe](https://github.com/janedoe)
```

### Available themes

| Theme | Style |
|-------|-------|
| Cayman | Clean, green header — popular for researchers |
| Minimal | Extremely simple, just content |
| Slate | Dark theme |
| Midnight | Dark with sidebar |
| Dinky | Small header |
| Architect | Sidebar layout |

---

<a id="path-c"></a>
## Path C — Custom HTML from Scratch

For students who know (or want to learn) HTML/CSS. Full creative control.

### Minimum viable site

Create `index.html` in your repo:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Jane Doe | PhD Student</title>
  <style>
    body { font-family: sans-serif; max-width: 700px; margin: 60px auto; padding: 0 20px; }
    h1   { font-size: 2rem; }
    nav a { margin-right: 1rem; }
  </style>
</head>
<body>
  <h1>Jane Doe</h1>
  <p>PhD Student · Geography · Texas A&M</p>
  <nav>
    <a href="#about">About</a>
    <a href="#research">Research</a>
    <a href="mailto:jdoe@tamu.edu">Email</a>
  </nav>
  <section id="about">
    <h2>About Me</h2>
    <p>Your bio here.</p>
  </section>
</body>
</html>
```

Commit this file, enable Pages (same as above), and iterate from there.

---

## Updating Your Site Over Time

Whenever you want to update content:

1. Go to your repo on github.com
2. Click the file to edit (`index.html` or `README.md`)
3. Click the pencil ✏ icon
4. Make changes
5. Click **"Commit changes"**
6. Wait 30–60 seconds → your live site is updated

### Or update via Git locally

```bash
git clone https://github.com/your-username/your-username.github.io
cd your-username.github.io

# Edit index.html in your text editor

git add index.html
git commit -m "Update bio and add new publication"
git push origin main
```

---

## Custom Domain (Optional)

If you own a domain (e.g., `janedoe.com`), you can point it to your GitHub Pages site.

1. In your domain registrar, add a CNAME record: `www` → `your-username.github.io`
2. In your repo, create a file named `CNAME` containing just your domain:
   ```
   www.janedoe.com
   ```
3. In **Settings → Pages → Custom domain**, enter your domain → Save

---

## Troubleshooting

| Symptom | Cause | Fix |
|---------|-------|-----|
| Site shows 404 | Pages not enabled or repo name wrong | Check Settings → Pages; name must be `username.github.io` |
| Old content still showing | Browser cache | Hard refresh: `Ctrl+Shift+R` (Windows) / `Cmd+Shift+R` (Mac) |
| Photo not loading | Wrong file path or case | File must be at `assets/photo.jpg` exactly (case-sensitive) |
| Theme not applying | `_config.yml` missing `theme:` line | Add `theme: minima` (or other theme name) |
| Build failed | YAML syntax error in `_config.yml` | Check for missing quotes or indentation |

To see build errors: **Settings → Pages → scroll down** — GitHub shows build status with error details.

---

## Useful Resources

| Resource | Link |
|----------|------|
| GitHub Pages docs | pages.github.com |
| Class website template | github.com/rayford295/academic-website-template |
| Jekyll documentation | jekyllrb.com/docs |
| al-folio (advanced academic template) | github.com/alshedivat/al-folio |
| academicpages (simpler alternative) | academicpages.github.io |
| Markdown cheat sheet | markdownguide.org/cheat-sheet |
| GitHub Desktop (GUI app) | desktop.github.com |
