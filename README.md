# Git, GitHub & Personal Websites for GIS Researchers

> Guest lecture materials for **GIS Practicum** · Texas A&M University
> April 15 & 20, 2026 · CSA 303 · 4:10–5:25 PM

**Instructor:** [Yifan Yang](https://rayford295.github.io) — PhD Student, GIScience & GeoAI, Texas A&M University

---

## What You Will Learn

By the end of this session, you will be able to:

- Understand what Git is and why version control matters for research
- Use the six core Git commands that cover 90% of real workflows
- Create a GitHub repository and push your work online
- Launch a live personal academic website at `your-username.github.io` in under 10 minutes
- Know when and how to collaborate using branches and pull requests

---

## Materials

| File | Description |
|------|-------------|
| [`git-github-lecture.pptx`](git-github-lecture.pptx) | 17-slide lecture deck (concepts + live demo) |
| [`exercises/handout.md`](exercises/handout.md) | Step-by-step in-class exercise — start here |
| [`exercises/github-pages-guide.md`](exercises/github-pages-guide.md) | Detailed website setup guide (3 difficulty paths) |
| [`Yifan Yang-4.20-GIS Practicum.pdf`](Yifan%20Yang-4.20-GIS%20Practicum.pdf) | Session slides as PDF |

---

## Lecture Outline (75 min)

| Time | Topic |
|------|-------|
| 0–15 min | **Why version control?** — The problem Git solves; the 3 states (working / staged / committed) |
| 15–30 min | **Core Git commands** — `init`, `add`, `commit`, `log`, `clone`, `push`, `pull` |
| 30–45 min | **GitHub** — Git vs GitHub, remote repos, push/pull workflow, collaboration with branches |
| 45–60 min | **GitHub Pages** — Free hosting, three setup paths (template / Jekyll / custom HTML) |
| 60–75 min | **Hands-on** — Every student launches a live site at `username.github.io` |

---

## Quick Start (In-Class Exercise)

Open a terminal and run:

```bash
# 1. Create and initialize a repo
mkdir my-first-repo && cd my-first-repo
git init

# 2. Create a file, stage, and commit
echo "# My First Repo" > README.md
git add README.md
git commit -m "Initial commit"
```

Then follow [`exercises/handout.md`](exercises/handout.md) to push it to GitHub and turn it into a live website.

---

## Launch Your Academic Website in 3 Steps

1. **Fork the template:** Go to [github.com/rayford295/academic-website-template](https://github.com/rayford295/academic-website-template) → click **Use this template** → name your repo `your-username.github.io`
2. **Enable Pages:** Settings → Pages → Source: `main` branch → Save
3. **Edit your info:** Open `index.html`, search for `EDIT`, and fill in your name, affiliation, and links

Your site goes live at `https://your-username.github.io` within ~60 seconds.

> Full setup guide with 3 difficulty paths: [`exercises/github-pages-guide.md`](exercises/github-pages-guide.md)

---

## Essential Commands Reference

| Command | What it does |
|---------|-------------|
| `git init` | Create a new repository in the current folder |
| `git status` | Show what has changed since the last commit |
| `git add <file>` | Stage a specific file |
| `git add .` | Stage all changed files |
| `git commit -m "message"` | Save a snapshot with a description |
| `git log --oneline` | View compact history |
| `git clone <url>` | Copy a remote repository to your machine |
| `git push origin main` | Upload local commits to GitHub |
| `git pull origin main` | Download the latest changes from GitHub |
| `git branch <name>` | Create a new branch |
| `git checkout <name>` | Switch to a branch |
| `git merge <name>` | Merge a branch into the current branch |

---

## Resources

| Resource | Link |
|----------|------|
| Interactive Git tutorial | [learngitbranching.js.org](https://learngitbranching.js.org) |
| Official Git documentation | [git-scm.com/doc](https://git-scm.com/doc) |
| Pro Git Book (free) | [git-scm.com/book](https://git-scm.com/book) |
| GitHub Pages documentation | [pages.github.com](https://pages.github.com) |
| Class website template | [github.com/rayford295/academic-website-template](https://github.com/rayford295/academic-website-template) |
| al-folio (advanced academic template) | [github.com/alshedivat/al-folio](https://github.com/alshedivat/al-folio) |
| GitHub Desktop (GUI) | [desktop.github.com](https://desktop.github.com) |
| Git cheat sheet (PDF) | [education.github.com/git-cheat-sheet](https://education.github.com/git-cheat-sheet-education.pdf) |

---

## About the Instructor

**Yifan Yang** is a PhD student in GIScience and GeoAI at Texas A&M University (GEAR Lab, advised by Prof. Lei Zou).
His research focuses on autonomous GeoAI agents for geospatial scientific discovery.

- Website: [rayford295.github.io](https://rayford295.github.io)
- GitHub: [github.com/rayford295](https://github.com/rayford295)
- Email: yyang48@tamu.edu

---

*Materials are freely reusable for educational purposes.*
