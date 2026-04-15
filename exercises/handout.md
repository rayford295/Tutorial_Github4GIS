# Hands-On Exercise: Launch Your Academic Website

**GIS Practicum · April 15, 2026 · CSA 303**

---

## Part 1 — Your First Git Repository (Local)

Open a terminal and run these commands one by one:

```bash
# 1. Create a project folder
mkdir my-first-repo
cd my-first-repo

# 2. Initialize Git
git init

# 3. Create a file
echo "# My First Repo" > README.md

# 4. Check what Git sees
git status

# 5. Stage the file
git add README.md

# 6. Save the snapshot
git commit -m "Initial commit"

# 7. View history
git log --oneline
```

---

## Part 2 — Launch Your Website on GitHub Pages

### Step 1 — Create a GitHub Account
Go to **github.com** and sign up (free).

### Step 2 — Create Your Repository
- Click **New repository**
- Name it exactly: `your-username.github.io` (replace with your actual GitHub username)
- Set to **Public**
- Check **Initialize this repository with a README**
- Click **Create repository**

### Step 3 — Enable GitHub Pages
- Go to **Settings** → **Pages** (left sidebar)
- Under **Source**, select `main` branch → click **Save**
- Wait ~60 seconds

### Step 4 — Edit Your Content
Click the pencil icon on `README.md` and add:

```markdown
# Your Name

PhD Student in [Your Field] at [Your University]

## Research Interests
- Topic 1
- Topic 2

## Contact
- Email: you@university.edu
- GitHub: github.com/your-username
```

Click **Commit changes**.

### Step 5 — Visit Your Live Site
Open your browser and go to: `https://your-username.github.io`

🎉 **You are live on the internet!**

---

## Bonus — Add a Theme

1. Go to **Settings → Pages**
2. Click **Choose a theme**
3. Pick any theme you like → click **Select theme**
4. Your site will update in ~30 seconds

---

## Key Commands Reference

| Command | What it does |
|---------|--------------|
| `git init` | Create a new repository |
| `git status` | See what has changed |
| `git add <file>` | Stage a file |
| `git add .` | Stage all changed files |
| `git commit -m "message"` | Save a snapshot |
| `git log --oneline` | View compact history |
| `git clone <url>` | Copy a remote repo locally |
| `git push origin main` | Upload local commits to GitHub |
| `git pull origin main` | Download latest changes from GitHub |

---

## Useful Resources

- **Git Book (free):** git-scm.com/book
- **Interactive Git tutorial:** learngitbranching.js.org
- **GitHub Pages docs:** pages.github.com
- **al-folio (academic template):** github.com/alshedivat/al-folio
- **Git cheat sheet (PDF):** education.github.com/git-cheat-sheet
