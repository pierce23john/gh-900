# Week 6 — Security, Administration & GitHub Community

> **Exam Domains:** Domain 6 — Privacy, Security & Administration (~10%), Domain 7 — Benefits of the GitHub Community (~10%)

---

## Theory Goals

- Know authentication methods: username/password, PATs, SSH keys, SAML SSO
- Understand 2FA and why it's required for certain orgs
- Know repository roles: Read, Triage, Write, Maintain, Admin
- Understand organisation roles: Owner, Member, Outside Collaborator
- Know security features: Dependabot alerts/updates, secret scanning, security advisories; secure repo best practices (code scanning covered in Week 4)
- Understand InnerSource programme management: discoverability (topics, README, CONTRIBUTING.md), guidance (issue templates, review standards), maintenance metrics
- Understand open source licensing and GitHub Sponsors
- Know GitHub Marketplace: Actions, Apps

---

## Daily Breakdown

| Day | Topic | Resources |
|---|---|---|
| Mon | Auth: PATs (classic vs. fine-grained), SSH keys, OAuth Apps, GitHub Apps | [MS Learn — Authenticate & Authorize](https://learn.microsoft.com/en-us/training/modules/authenticate-authorize-user-identities-github/) · [GitHub Docs — Auth](https://docs.github.com/en/authentication) |
| Tue | 2FA; SAML SSO; SCIM provisioning (Enterprise) | [GitHub Docs — Security](https://docs.github.com/en/authentication/securing-your-account-with-two-factor-authentication-2fa) |
| Wed | Repo & org permissions model; team permissions; GitHub administration overview | [MS Learn — GitHub Administration](https://learn.microsoft.com/en-us/training/modules/github-introduction-administration/) · [GitHub Docs — Permissions](https://docs.github.com/en/organizations/managing-user-access-to-your-organizations-repositories/repository-roles-for-an-organization) |
| Thu | Dependabot alerts/updates; secret scanning; security advisories; **secure repo best practices**: security policies, SECURITY.md, dependency review | [MS Learn — Maintain Secure Repo](https://learn.microsoft.com/en-us/training/modules/maintain-secure-repository-github/) · [GitHub Docs — Security Features](https://docs.github.com/en/code-security) |
| Fri | InnerSource programme management (discoverability, guidance, maintenance); contributing to open source; GitHub Sponsors; GitHub Marketplace | [MS Learn — Manage InnerSource](https://learn.microsoft.com/en-us/training/modules/manage-innersource-program-github/) · [MS Learn — Contribute to Open Source](https://learn.microsoft.com/en-us/training/modules/contribute-open-source/) · [GitHub Docs — Community](https://docs.github.com/en/communities) |
| Sat | **Practical Lab 6** (see below) | |
| Sun | Full mock exam + review (see below) | |

---

## Practical Lab 6 — Security & Administration

1. Generate a **fine-grained PAT** scoped to only your `gh-900-practice` repo with `Contents: Read and Write` permission. Test it with a `curl` call to the GitHub API.
2. Enable **Dependabot alerts** and **Dependabot version updates** on your repo (`Settings → Code security`).
3. Enable **secret scanning** on the repo. (Try committing a fake API key string and observe the alert.)
4. Review the **security policy** tab and add a `SECURITY.md` file.
5. Navigate to an open-source repo you use (e.g., `dotnet/aspnetcore`) and explore: fork count, contributor graph, open issues vs. PRs, release history.

---

## Full Mock Exam (Sunday, Week 6)

- Use the Microsoft Learn practice assessment: https://learn.microsoft.com/en-us/credentials/certifications/github-foundations/
- Time yourself: 75 questions in 120 minutes
- Review every wrong answer against the official docs
- Aim for >80% before scheduling the real exam

---

← [[Week-5-Actions-and-Project-Management]] | [[Home]] | Next: [[Quick-Reference]] →
