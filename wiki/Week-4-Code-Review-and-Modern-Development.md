# Week 4 — Collaboration: Code Review & Modern Development

> **Exam Domains:** Domain 3 — Collaboration Features (~30%), Domain 4 — Modern Development (~13%)

---

## Theory Goals

- Understand code review best practices: commenting on specific lines, suggesting changes
- Know protected branches: required status checks, required reviews, dismiss stale reviews
- Know what GitHub Codespaces is and when to use it
- Understand GitHub Copilot: what it does, what models power it, subscription tiers
- Know GitHub Actions at a conceptual level (workflows, jobs, steps, triggers — detail in Week 5)
- Understand code scanning: CodeQL, third-party tools, and integration with GitHub Actions

---

## Daily Breakdown

| Day | Topic | Resources |
|---|---|---|
| Mon | Code review features: line comments, suggested changes, CODEOWNERS | [GitHub Docs — Reviewing PRs](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/reviewing-changes-in-pull-requests) |
| Tue | Branch protection rules: required reviews, status checks | [GitHub Docs — Protected Branches](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-protected-branches) |
| Wed | GitHub Codespaces: what it is, dev container, prebuilds | [MS Learn — Code with Codespaces](https://learn.microsoft.com/en-us/training/modules/code-with-github-codespaces/) · [GitHub Docs — Codespaces](https://docs.github.com/en/codespaces) |
| Thu | GitHub Copilot: overview, tiers, privacy settings; configure code scanning with CodeQL & third-party tools | [MS Learn — Intro to Copilot](https://learn.microsoft.com/en-us/training/modules/introduction-to-github-copilot/) · [MS Learn — Configure Code Scanning](https://learn.microsoft.com/en-us/training/modules/configure-code-scanning/) · [GitHub Copilot Docs](https://docs.github.com/en/copilot) |
| Fri | GitHub Actions: concepts (workflow, trigger, job, step, runner) | [GitHub Docs — Actions](https://docs.github.com/en/actions) |
| Sat | **Practical Lab 4** (see below) | |
| Sun | Rest or catch-up | |

---

## Practical Lab 4 — Code Review & Codespaces

1. On your `gh-900-practice` repo, configure a **branch protection rule** on `main`:
   - Require 1 PR review before merging
   - Require status checks to pass (add a simple CI check in Week 5)
2. Add a `CODEOWNERS` file at `.github/CODEOWNERS` assigning yourself as owner of `*.md` files.
3. Open a Codespace on your repo from the GitHub UI (green "Code" button → Codespaces tab). Explore the web editor.
4. If you have GitHub Copilot access, open your .NET project and observe inline suggestions.

> **Note for .NET developers:** The MS Learn GitHub Foundations path includes a "Using GitHub Copilot with Python" module. Apply the exact same concepts in C# — ghost text completions, multi-line suggestions, and Copilot Chat explaining existing code work identically across languages.

---

← [[Week-3-Collaboration-Issues-and-PRs]] | [[Home]] | Next: [[Week-5-Actions-and-Project-Management]] →
