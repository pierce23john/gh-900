# Week 5 — Modern Dev, GitHub Actions & Project Management

> **Exam Domains:** Domain 4 — Modern Development (~13%), Domain 5 — Project Management (~7%)

---

## Theory Goals

- Understand GitHub Actions YAML structure: `on`, `jobs`, `steps`, `uses`, `run`
- Know starter workflows and the GitHub Marketplace
- Know GitHub Packages: what it is, supported package types
- Understand GitHub Projects (v2): boards, roadmaps, custom fields, automation
- Know GitHub Insights: pulse, contributors, traffic

---

## Daily Breakdown

| Day | Topic | Resources |
|---|---|---|
| Mon | GitHub Actions: YAML syntax deep dive; workflow triggers | [GitHub Docs — Workflow Syntax](https://docs.github.com/en/actions/writing-workflows/workflow-syntax-for-github-actions) |
| Tue | Actions: secrets, environment variables, contexts | [GitHub Docs — Contexts](https://docs.github.com/en/actions/writing-workflows/choosing-what-your-workflow-does/accessing-contextual-information-about-workflow-runs) |
| Wed | GitHub Packages: publish/consume packages | [GitHub Docs — Packages](https://docs.github.com/en/packages) |
| Thu | GitHub Projects (v2): boards, automation, roadmaps | [GitHub Docs — Projects](https://docs.github.com/en/issues/planning-and-tracking-with-projects) |
| Fri | GitHub Insights: traffic, contributors, pulse | [GitHub Docs — Insights](https://docs.github.com/en/repositories/viewing-activity-and-data-for-your-repository) |
| Sat | **Practical Lab 5** (see below) | |
| Sun | Rest or catch-up | |

---

## Practical Lab 5 — GitHub Actions & Projects

### Create Your First Workflow

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

### Steps

1. Commit the workflow and watch it run in the **Actions** tab.
2. Add a failing step, observe the failed run, then fix it.
3. Add a **repository secret** (`Settings → Secrets and variables → Actions`) and reference it in a step using `${{ secrets.MY_SECRET }}`.
4. Create a **GitHub Project (v2)** linked to your repo. Add your open issues to it. Set up a "Todo → In Progress → Done" board view.

---

← [[Week-4-Code-Review-and-Modern-Development]] | [[Home]] | Next: [[Week-6-Security-Administration-and-Community]] →
