# Publishing to GitHub

This folder contains a minimal Python + pytest project for E2E testing of the datacurve QA pipeline. To use it as the example repository, push it to a **public** GitHub repo.

## Option 1: GitHub CLI

```bash
cd e2e-example-repo
git init
git add .
git commit -m "Initial commit: minimal pytest example"
gh repo create datacurve-qa-example --public --source=. --push
```

## Option 2: Manual

1. Create an empty repository on GitHub (e.g. `datacurve-qa-example`).
2. From this directory:

```bash
cd e2e-example-repo
git init
git add .
git commit -m "Initial commit: minimal pytest example"
git branch -M main
git remote add origin https://github.com/<your-username>/datacurve-qa-example.git
git push -u origin main
```

## Usage in E2E Test

After publishing, use the repo URL in your E2E test:

- **Repo URL:** `https://github.com/<your-username>/datacurve-qa-example.git`
- **Branch:** `main`
