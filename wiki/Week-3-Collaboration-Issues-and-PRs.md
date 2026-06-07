# Week 3 — Collaboration: Issues, PRs, and GitHub Flow

> **Exam Domain:** Domain 3 — Collaboration Features (~30%), Part 1

---

## Theory Goals

- Understand GitHub Flow: branch → commit → PR → review → merge → deploy
- Know the difference between merge strategies: merge commit, squash merge, rebase merge
- Understand pull requests: draft PRs, reviewers, required reviews, auto-merge
- Know Issues: labels, milestones, assignees, issue templates, closing keywords (`Fixes #123`)
- Understand Discussions vs. Issues

---

## Daily Breakdown

| Day | Topic | Resources |
|---|---|---|
| Mon | GitHub Flow explained end-to-end | [GitHub Flow Guide](https://docs.github.com/en/get-started/using-github/github-flow) |
| Tue | Pull requests: creation, anatomy, review process | [GitHub Docs — Pull Requests](https://docs.github.com/en/pull-requests) |
| Wed | Merge strategies: merge commit vs. squash vs. rebase | [GitHub Docs — Merging](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/incorporating-changes/about-pull-request-merges) |
| Thu | Issues: templates, labels, milestones, closing keywords | [GitHub Docs — Issues](https://docs.github.com/en/issues) |
| Fri | Discussions: when to use vs. Issues | [GitHub Docs — Discussions](https://docs.github.com/en/discussions) |
| Sat | **Practical Lab 3** (see below) | |
| Sun | Rest or catch-up | |

---

## Practical Lab 3 — GitHub Flow End-to-End

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

← [[Week-2-Working-with-Repositories]] | [[Home]] | Next: [[Week-4-Code-Review-and-Modern-Development]] →
