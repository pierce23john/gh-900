# GH-900 GitHub Foundations — Study Plan

> **Exam:** GitHub Foundations Certification (GH-900)
> **Duration:** 6 weeks (~1–1.5 hrs/day on weekdays, ~2–3 hrs on weekends)
> **Goal:** Pass the exam with confidence, backed by hands-on experience — not just memorisation.

---

## Exam Domain Breakdown

| Domain | Weight | Week Focus |
|---|---|---|
| 1. Introduction to Git and GitHub | ~22% | Week 1 |
| 2. Working with GitHub Repositories | ~8% | Week 2 |
| 3. Collaboration Features | ~30% | Week 3–4 |
| 4. Modern Development | ~13% | Week 4–5 |
| 5. Project Management | ~7% | Week 5 |
| 6. Privacy, Security & Administration | ~10% | Week 5–6 |
| 7. Benefits of the GitHub Community | ~10% | Week 6 |

---

## Pre-Study Setup (Before Week 1)

- [ ] Create a free GitHub account (if you don't have one): https://github.com
- [ ] Install Git locally: https://git-scm.com/downloads
- [ ] Install GitHub CLI (`gh`): https://cli.github.com
- [ ] Install GitHub Desktop (optional, but good to know for the exam): https://desktop.github.com
- [ ] Install **GitHub Mobile** on your phone (iOS/Android) — it's covered in the GitHub Products module on the exam: https://github.com/mobile
- [ ] Bookmark the official study guide: https://examregistration.github.com/certification/GHF
- [ ] Create a **practice repository** called `gh-900-practice` — you'll use this throughout the plan

---

## Week 1 — Git Fundamentals & GitHub Basics (Domain 1)

### Theory Goals
- Understand what version control is and why it matters
- Distinguish between centralised (SVN) vs. distributed (Git) VCS
- Learn the Git object model: blobs, trees, commits, tags
- Know the three Git states: working directory, staging area, repository
- Understand the GitHub platform: GitHub.com vs. GitHub Enterprise Cloud vs. Server vs. AE
- Know GitHub account types: personal, organisation, and enterprise
- Know GitHub plan tiers: Free, Team, Enterprise — key feature differences and billing
- Know GitHub Desktop and GitHub Mobile as access options

### Daily Breakdown

| Day | Topic | Resources |
|---|---|---|
| Mon | What is version control? History of Git | [MS Learn — Intro to Git](https://learn.microsoft.com/en-us/training/modules/intro-to-git/) · [Git SCM Book Ch.1](https://git-scm.com/book/en/v2) |
| Tue | Git internals: commits, branches, HEAD | [Git SCM Book Ch.2–3](https://git-scm.com/book/en/v2) |
| Wed | GitHub overview: repos, stars, forks, watch | [MS Learn — Intro to GitHub](https://learn.microsoft.com/en-us/training/modules/introduction-to-github/) · [GitHub Docs — Getting Started](https://docs.github.com/en/get-started) |
| Thu | GitHub account types & plan tiers (Free/Team/Enterprise); GitHub Desktop & Mobile overview | [MS Learn — GitHub Products](https://learn.microsoft.com/en-us/training/modules/github-introduction-products/) · [GitHub CLI Manual](https://cli.github.com/manual/) |
| Fri | Review + quiz yourself | |
| Sat | **Practical Lab 1** (see below) | |
| Sun | Rest or catch-up | |

### Practical Lab 1 — Git & GitHub Basics
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

## Week 2 — Working with GitHub Repositories (Domain 2)

### Theory Goals
- Know repo visibility: public vs. private vs. internal (Enterprise)
- Understand README, `.gitignore`, and `LICENSE` purpose and best practices
- Master GitHub Flavored Markdown (GFM): tables, task lists, code fences, @mentions, issue/PR cross-references, Mermaid diagrams
- Know what GitHub Pages is and how to enable it
- Understand wikis and their use cases
- Learn about repo templates and how to create one
- Know how to search and filter repository history: by author, date, keyword; understand `git blame` and commit cross-linking

### Daily Breakdown

| Day | Topic | Resources |
|---|---|---|
| Mon | Repository creation options; visibility levels | [GitHub Docs — Repositories](https://docs.github.com/en/repositories) |
| Tue | GitHub Flavored Markdown deep dive: tables, task lists, code fences, @mentions, issue/PR/commit references, Mermaid diagrams | [MS Learn — Communicate with Markdown](https://learn.microsoft.com/en-us/training/modules/communicate-using-markdown/) · [GitHub Docs — Markdown](https://docs.github.com/en/get-started/writing-on-github) |
| Wed | `.gitignore` patterns; `LICENSE` types (MIT, Apache, GPL); README best practices | [choosealicense.com](https://choosealicense.com) |
| Thu | GitHub Pages; GitHub Desktop & Mobile walkthrough | [GitHub Docs — Pages](https://docs.github.com/en/pages) |
| Fri | Wikis; repo templates; search & filter repo history: `git blame`, author/date filters, cross-linking issues and commits | [MS Learn — Search & Organize History](https://learn.microsoft.com/en-us/training/modules/search-organize-repository-history-github/) · [GitHub Docs — Wikis](https://docs.github.com/en/communities/documenting-your-project-with-wikis) |
| Sat | **Practical Lab 2** (see below) | |
| Sun | Rest or catch-up | |

### Practical Lab 2 — Repository Features
1. Enable **GitHub Pages** on your `gh-900-practice` repo (branch: `main`, folder: `/ (root)`). Verify the published URL.
2. Add a **Wiki** page titled "Study Notes" and write a summary of Week 1.
3. Create a second repo **from a template** — use any public template repo on GitHub.
4. Add a `.gitignore` for a .NET project (use the GitHub-provided template when creating the repo).
5. Star 5 repos relevant to your interests and observe how Stars/Watch/Fork counts work.
6. In the README, practice GitHub Flavored Markdown: add a task list `- [ ]`, a table, a fenced code block, and a Mermaid diagram (` ```mermaid `).
7. Run `git blame README.md` locally — observe line-by-line author and commit attribution.
8. In the GitHub UI, click a file → **History** to see per-file commit log. Switch to the **Blame** view and explore the annotation panel.

---

## Week 3 — Collaboration: Issues, PRs, and GitHub Flow (Domain 3, Part 1)

### Theory Goals
- Understand GitHub Flow: branch → commit → PR → review → merge → deploy
- Know the difference between merge strategies: merge commit, squash merge, rebase merge
- Understand pull requests: draft PRs, reviewers, required reviews, auto-merge
- Know Issues: labels, milestones, assignees, issue templates, closing keywords (`Fixes #123`)
- Understand Discussions vs. Issues

### Daily Breakdown

| Day | Topic | Resources |
|---|---|---|
| Mon | GitHub Flow explained end-to-end | [GitHub Flow Guide](https://docs.github.com/en/get-started/using-github/github-flow) |
| Tue | Pull requests: creation, anatomy, review process | [GitHub Docs — Pull Requests](https://docs.github.com/en/pull-requests) |
| Wed | Merge strategies: merge commit vs. squash vs. rebase | [GitHub Docs — Merging](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/incorporating-changes/about-pull-request-merges) |
| Thu | Issues: templates, labels, milestones, closing keywords | [GitHub Docs — Issues](https://docs.github.com/en/issues) |
| Fri | Discussions: when to use vs. Issues | [GitHub Docs — Discussions](https://docs.github.com/en/discussions) |
| Sat | **Practical Lab 3** (see below) | |
| Sun | Rest or catch-up | |

### Practical Lab 3 — GitHub Flow End-to-End
```bash
# 1. Create a feature branch
git checkout -b feature/add-about-page

# 2. Make changes and commit
echo "## About" >> README.md
git add README.md
git commit -m "Add about section to README"

# 3. Push and open a pull request via CLI
git push origin feature/add-about-page
gh pr create --title "Add about page" --body "Closes #1" --base main
```

4. On the GitHub UI: add a label, request a reviewer (even yourself via another account or a collaborator).
5. Create an **Issue template** in `.github/ISSUE_TEMPLATE/bug_report.md`.
6. Open 2 issues. Close one using a commit message with `Fixes #<issue-number>`.
7. Enable **Discussions** on the repo and create one discussion post.

---

## Week 4 — Collaboration: Code Review & Modern Development (Domains 3 & 4)

### Theory Goals
- Understand code review best practices: commenting on specific lines, suggesting changes
- Know protected branches: required status checks, required reviews, dismiss stale reviews
- Know what GitHub Codespaces is and when to use it
- Understand GitHub Copilot: what it does, what models power it, subscription tiers
- Know GitHub Actions at a conceptual level (workflows, jobs, steps, triggers — detail in Week 5)
- Understand code scanning: CodeQL, third-party tools, and integration with GitHub Actions (MS Learn Part 1 gives this a full dedicated module)

### Daily Breakdown

| Day | Topic | Resources |
|---|---|---|
| Mon | Code review features: line comments, suggested changes, CODEOWNERS | [GitHub Docs — Reviewing PRs](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/reviewing-changes-in-pull-requests) |
| Tue | Branch protection rules: required reviews, status checks | [GitHub Docs — Protected Branches](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-protected-branches) |
| Wed | GitHub Codespaces: what it is, dev container, prebuilds | [MS Learn — Code with Codespaces](https://learn.microsoft.com/en-us/training/modules/code-with-github-codespaces/) · [GitHub Docs — Codespaces](https://docs.github.com/en/codespaces) |
| Thu | GitHub Copilot: overview, tiers, privacy settings; configure code scanning with CodeQL & third-party tools | [MS Learn — Intro to Copilot](https://learn.microsoft.com/en-us/training/modules/introduction-to-github-copilot/) · [MS Learn — Configure Code Scanning](https://learn.microsoft.com/en-us/training/modules/configure-code-scanning/) · [GitHub Copilot Docs](https://docs.github.com/en/copilot) |
| Fri | GitHub Actions: concepts (workflow, trigger, job, step, runner) | [GitHub Docs — Actions](https://docs.github.com/en/actions) |
| Sat | **Practical Lab 4** (see below) | |
| Sun | Rest or catch-up | |

### Practical Lab 4 — Code Review & Codespaces
1. On your `gh-900-practice` repo, configure a **branch protection rule** on `main`:
   - Require 1 PR review before merging
   - Require status checks to pass (add a simple CI check in Week 5)
2. Add a `CODEOWNERS` file at `.github/CODEOWNERS` assigning yourself as owner of `*.md` files.
3. Open a Codespace on your repo from the GitHub UI (green "Code" button → Codespaces tab). Explore the web editor.
4. If you have GitHub Copilot access, open your .NET project and observe inline suggestions.

> **Note for .NET developers:** The MS Learn GitHub Foundations path includes a "Using GitHub Copilot with Python" module. Apply the exact same concepts in C# — ghost text completions, multi-line suggestions, and Copilot Chat explaining existing code work identically across languages.

---

## Week 5 — Modern Dev, GitHub Actions & Project Management (Domains 4 & 5)

### Theory Goals
- Understand GitHub Actions YAML structure: `on`, `jobs`, `steps`, `uses`, `run`
- Know starter workflows and the GitHub Marketplace
- Know GitHub Packages: what it is, supported package types
- Understand GitHub Projects (v2): boards, roadmaps, custom fields, automation
- Know GitHub Insights: pulse, contributors, traffic

### Daily Breakdown

| Day | Topic | Resources |
|---|---|---|
| Mon | GitHub Actions: YAML syntax deep dive; workflow triggers | [GitHub Docs — Workflow Syntax](https://docs.github.com/en/actions/writing-workflows/workflow-syntax-for-github-actions) |
| Tue | Actions: secrets, environment variables, contexts | [GitHub Docs — Contexts](https://docs.github.com/en/actions/writing-workflows/choosing-what-your-workflow-does/accessing-contextual-information-about-workflow-runs) |
| Wed | GitHub Packages: publish/consume packages | [GitHub Docs — Packages](https://docs.github.com/en/packages) |
| Thu | GitHub Projects (v2): boards, automation, roadmaps | [GitHub Docs — Projects](https://docs.github.com/en/issues/planning-and-tracking-with-projects) |
| Fri | GitHub Insights: traffic, contributors, pulse | [GitHub Docs — Insights](https://docs.github.com/en/repositories/viewing-activity-and-data-for-your-repository) |
| Sat | **Practical Lab 5** (see below) | |
| Sun | Rest or catch-up | |

### Practical Lab 5 — GitHub Actions & Projects

**Create your first workflow:**
```yaml
# .github/workflows/ci.yml
name: CI

on:
  push:
    branches: [main]
  pull_request:
    branches: [main]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - name: Print Hello
        run: echo "Hello from GitHub Actions!"
      - name: List files
        run: ls -la
```

1. Commit the workflow and watch it run in the **Actions** tab.
2. Add a failing step, observe the failed run, then fix it.
3. Add a **repository secret** (`Settings → Secrets and variables → Actions`) and reference it in a step using `${{ secrets.MY_SECRET }}`.
4. Create a **GitHub Project (v2)** linked to your repo. Add your open issues to it. Set up a "Todo → In Progress → Done" board view.

---

## Week 6 — Security, Administration & GitHub Community (Domains 6 & 7)

### Theory Goals
- Know authentication methods: username/password, PATs, SSH keys, SAML SSO
- Understand 2FA and why it's required for certain orgs
- Know repository roles: Read, Triage, Write, Maintain, Admin
- Understand organisation roles: Owner, Member, Outside Collaborator
- Know security features: Dependabot alerts/updates, secret scanning, security advisories; secure repo best practices (code scanning covered in Week 4)
- Understand InnerSource programme management: discoverability (topics, README, CONTRIBUTING.md), guidance (issue templates, review standards), maintenance metrics
- Understand open source licensing and GitHub Sponsors
- Know GitHub Marketplace: Actions, Apps

### Daily Breakdown

| Day | Topic | Resources |
|---|---|---|
| Mon | Auth: PATs (classic vs. fine-grained), SSH keys, OAuth Apps, GitHub Apps | [MS Learn — Authenticate & Authorize](https://learn.microsoft.com/en-us/training/modules/authenticate-authorize-user-identities-github/) · [GitHub Docs — Auth](https://docs.github.com/en/authentication) |
| Tue | 2FA; SAML SSO; SCIM provisioning (Enterprise) | [GitHub Docs — Security](https://docs.github.com/en/authentication/securing-your-account-with-two-factor-authentication-2fa) |
| Wed | Repo & org permissions model; team permissions; GitHub administration overview | [MS Learn — GitHub Administration](https://learn.microsoft.com/en-us/training/modules/github-introduction-administration/) · [GitHub Docs — Permissions](https://docs.github.com/en/organizations/managing-user-access-to-your-organizations-repositories/repository-roles-for-an-organization) |
| Thu | Dependabot alerts/updates; secret scanning; security advisories; **secure repo best practices**: security policies, SECURITY.md, dependency review | [MS Learn — Maintain Secure Repo](https://learn.microsoft.com/en-us/training/modules/maintain-secure-repository-github/) · [GitHub Docs — Security Features](https://docs.github.com/en/code-security) |
| Fri | InnerSource programme management (discoverability, guidance, maintenance); contributing to open source; GitHub Sponsors; GitHub Marketplace | [MS Learn — Manage InnerSource](https://learn.microsoft.com/en-us/training/modules/manage-innersource-program-github/) · [MS Learn — Contribute to Open Source](https://learn.microsoft.com/en-us/training/modules/contribute-open-source/) · [GitHub Docs — Community](https://docs.github.com/en/communities) |
| Sat | **Practical Lab 6** (see below) | |
| Sun | Full mock exam + review (see below) | |

### Practical Lab 6 — Security & Administration
1. Generate a **fine-grained PAT** scoped to only your `gh-900-practice` repo with `Contents: Read and Write` permission. Test it with a `curl` call to the GitHub API.
2. Enable **Dependabot alerts** and **Dependabot version updates** on your repo (`Settings → Code security`).
3. Enable **secret scanning** on the repo. (Try committing a fake API key string and observe the alert.)
4. Review the **security policy** tab and add a `SECURITY.md` file.
5. Navigate to an open-source repo you use (e.g., `dotnet/aspnetcore`) and explore: fork count, contributor graph, open issues vs. PRs, release history.

### Full Mock Exam (Sunday, Week 6)
- Use the Microsoft Learn practice assessment: https://learn.microsoft.com/en-us/credentials/certifications/github-foundations/
- Time yourself: 75 questions in 120 minutes
- Review every wrong answer against the official docs
- Aim for >80% before scheduling the real exam

---

## Quick-Reference: Key Concepts to Memorise

### Git Commands You Must Know
| Command | Purpose |
|---|---|
| `git init` | Initialise a new local repo |
| `git clone <url>` | Copy a remote repo locally |
| `git add <file>` | Stage changes |
| `git commit -m "msg"` | Commit staged changes |
| `git push` | Upload commits to remote |
| `git pull` | Fetch and merge from remote |
| `git fetch` | Fetch without merging |
| `git branch -b <name>` | Create and switch to branch |
| `git merge <branch>` | Merge a branch into current |
| `git rebase <branch>` | Reapply commits on top of another branch |
| `git stash` | Temporarily shelve uncommitted changes |
| `git log --oneline` | Compact commit history |
| `git diff` | Show unstaged changes |
| `git revert <hash>` | Create a new commit undoing a past commit |
| `git reset --hard <hash>` | Move HEAD (destructive — use with caution) |

### GitHub Permissions Quick Reference
| Role | Can push | Can merge PRs | Manage settings | Manage members |
|---|---|---|---|---|
| Read | No | No | No | No |
| Triage | No | No | No | No |
| Write | Yes | Yes | No | No |
| Maintain | Yes | Yes | Partial | No |
| Admin | Yes | Yes | Yes | Yes |

### Security Features Cheat Sheet
| Feature | What it does |
|---|---|
| Dependabot alerts | Notifies of vulnerable dependencies |
| Dependabot security updates | Auto-opens PRs to fix vulnerable deps |
| Dependabot version updates | Keeps deps up-to-date (not just security) |
| Secret scanning | Detects accidentally committed secrets |
| Code scanning (CodeQL) | Static analysis for security vulnerabilities |
| Security advisories | Private disclosure and CVE management |
| Private vulnerability reporting | Allows reporters to privately submit issues |

---

## Recommended Study Resources

| Resource | Type | Cost |
|---|---|---|
| [GitHub Docs](https://docs.github.com) | Official docs | Free |
| [MS Learn — GitHub Foundations Part 1](https://learn.microsoft.com/en-us/training/paths/github-foundations/) | Learning path (8 modules, ~6h 44m) | Free |
| [MS Learn — GitHub Foundations Part 2](https://learn.microsoft.com/en-us/training/paths/github-foundations-2/) | Learning path (8 modules, ~4h 57m) | Free |
| [GitHub Skills](https://skills.github.com) | Interactive labs | Free |
| [Git SCM Book (Pro Git)](https://git-scm.com/book/en/v2) | Book | Free |
| [GitHub Learning Lab (archived)](https://github.com/githubtraining) | Repos | Free |
| [Exam Registration + Study Guide](https://examregistration.github.com/certification/GHF) | Official | Free |

---

## Exam Day Checklist

- [ ] Booked via [PSI](https://examregistration.github.com) or Pearson VUE
- [ ] Valid government-issued ID ready
- [ ] Quiet room, stable internet, working webcam and microphone
- [ ] Know the format: ~75 multiple choice/multiple select questions, 120 minutes, passing ~68%
- [ ] Have reviewed the [exam guide](https://examregistration.github.com/certification/GHF) domain weightings one final time
- [ ] Slept well — no cramming on exam morning

---

> Good luck! The exam rewards understanding *how* GitHub is used in real workflows, not just memorising feature names. The labs throughout this plan are your most valuable prep tool.
