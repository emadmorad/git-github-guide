# How to Create a Repository and Upload It to GitHub from Scratch

## Prerequisites

- [Git](https://git-scm.com/downloads) installed on your machine
- A [GitHub](https://github.com) account
- A terminal / command prompt

---

## Step 1 — Configure Git (first-time setup)

Before anything else, tell Git who you are. These details are attached to every commit.

```bash
git config --global user.name  "Your Name"
git config --global user.email "you@example.com"
```

---

## Step 2 — Create a local project folder

```bash
mkdir my-project
cd my-project
```

---

## Step 3 — Initialize a Git repository

```bash
git init
```

This creates a hidden `.git/` folder — that's the repository engine. Don't touch it directly.

---

## Step 4 — Add your files

Create or copy your project files into the folder, then stage them:

```bash
git add .          # stage everything
git add README.md  # or stage a specific file
```

> **Tip:** Create a `.gitignore` file to exclude things you never want to commit, like `node_modules/`, `.env`, or build output folders.

---

## Step 5 — Make your first commit

```bash
git commit -m "Initial commit: add project scaffold and README"
```

Write **descriptive** commit messages — explain *what* changed and *why*.

| ✅ Good | ❌ Bad |
|---|---|
| `feat: add user authentication module` | `update stuff` |
| `fix: resolve null pointer in payment service` | `bug fix` |
| `docs: add installation steps to README` | `readme` |

---

## Step 6 — Create a new repository on GitHub

1. Go to [github.com](https://github.com) and sign in.
2. Click the **+** icon (top-right) → **New repository**.
3. Give it a name (e.g. `my-project`).
4. Leave **"Initialize this repository with a README"** **unchecked** — you already have files locally.
5. Click **Create repository**.

---

## Step 7 — Link your local repo to GitHub

Copy the remote URL shown on GitHub and run:

```bash
# HTTPS
git remote add origin https://github.com/your-username/my-project.git

# SSH (recommended if you have SSH keys set up)
git remote add origin git@github.com:your-username/my-project.git
```

Verify it was added:

```bash
git remote -v
```

---

## Step 8 — Push to GitHub

```bash
git push -u origin main
```

The `-u` flag sets `origin/main` as the default upstream, so future pushes only need `git push`.

---

## Step 9 — Verify on GitHub

Refresh your GitHub repository page — your files should now be visible. 🎉

---

## Handy follow-up commands

```bash
git status                        # show working directory state
git log --oneline                 # compact commit history
git pull                          # fetch + merge latest from GitHub
git checkout -b feature/my-thing  # create and switch to a new branch
```
