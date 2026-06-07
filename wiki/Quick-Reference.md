# Quick Reference

Cheat sheets for the most commonly tested concepts.

---

## Git Commands You Must Know

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

---

## GitHub Permissions Quick Reference

| Role | Can push | Can merge PRs | Manage settings | Manage members |
|---|---|---|---|---|
| Read | No | No | No | No |
| Triage | No | No | No | No |
| Write | Yes | Yes | No | No |
| Maintain | Yes | Yes | Partial | No |
| Admin | Yes | Yes | Yes | Yes |

---

## Security Features Cheat Sheet

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

[[Home]] | [[Study-Resources]] | [[Exam-Day-Checklist]]
