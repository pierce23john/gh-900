# Week 1 — Git Fundamentals & GitHub Basics

> **Exam Domain:** Domain 1 — Introduction to Git and GitHub (~22%)

---

## Theory Goals

- Understand what version control is and why it matters
- Distinguish between centralised (SVN) vs. distributed (Git) VCS
- Learn the Git object model: blobs, trees, commits, tags
- Know the three Git states: working directory, staging area, repository
- Understand the GitHub platform: GitHub.com vs. GitHub Enterprise Cloud vs. Server vs. AE
- Know GitHub account types: personal, organisation, and enterprise
- Know GitHub plan tiers: Free, Team, Enterprise — key feature differences and billing
- Know GitHub Desktop and GitHub Mobile as access options

---

## Daily Breakdown

| Day | Topic | Resources |
|---|---|---|
| Mon | What is version control? History of Git | [MS Learn — Intro to Git](https://learn.microsoft.com/en-us/training/modules/intro-to-git/) · [Git SCM Book Ch.1](https://git-scm.com/book/en/v2) |
| Tue | Git internals: commits, branches, HEAD | [Git SCM Book Ch.2–3](https://git-scm.com/book/en/v2) |
| Wed | GitHub overview: repos, stars, forks, watch | [MS Learn — Intro to GitHub](https://learn.microsoft.com/en-us/training/modules/introduction-to-github/) · [GitHub Docs — Getting Started](https://docs.github.com/en/get-started) |
| Thu | GitHub account types & plan tiers (Free/Team/Enterprise); GitHub Desktop & Mobile overview | [MS Learn — GitHub Products](https://learn.microsoft.com/en-us/training/modules/github-introduction-products/) · [GitHub CLI Manual](https://cli.github.com/manual/) |
| Fri | Review + quiz yourself | |
| Sat | **Practical Lab 1** (see below) | |
| Sun | Rest or catch-up | |

---

## Practical Lab 1 — Git & GitHub Basics

```bash
# 1. Configure Git locally
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
git config --global init.defaultBranch main

# 2. Create and initialise a local repo
mkdir gh-900-practice && cd gh-900-practice
git init
echo "# GH-900 Practice" > README.md
git add README.md
git commit -m "Initial commit"

# 3. Push to GitHub using GitHub CLI
gh auth login
gh repo create gh-900-practice --public --source=. --push

# 4. Explore the Git object model
git cat-file -t HEAD        # Should print "commit"
git cat-file -p HEAD        # Inspect the commit object
git ls-tree HEAD            # Inspect the tree object
```

**Exercise:** Make 3 more commits changing the README. Use `git log --oneline --graph` to visualise history.

---

← [[Pre-Study-Setup]] | [[Home]] | Next: [[Week-2-Working-with-Repositories]] →
