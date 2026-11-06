# Publishing this repository to GitHub

GitHub CLI authentication was unavailable in the analysis environment (`gh auth status` → not logged in). Use one of the options below on your machine.

## Option A — GitHub CLI (recommended)

```bash
cd ~/Public/Jupiter-Educational-Platform

# 1) Authenticate (browser or token)
gh auth login

# 2) Create PUBLIC repo (no license flag on purpose)
gh repo create Jupiter-Educational-Platform \
  --public \
  --description "Case study: Jupiter Educational Platform — Angular + ASP.NET Core full-stack EdTech system" \
  --source . \
  --remote origin \
  --push

# 3) Topics for discoverability
gh repo edit amiragomaa2597/Jupiter-Educational-Platform \
  --add-topic angular \
  --add-topic aspnetcore \
  --add-topic csharp \
  --add-topic sql-server \
  --add-topic edtech \
  --add-topic full-stack \
  --add-topic portfolio \
  --add-topic educational-platform
```

## Option B — GitHub website + git push

1. Create a new **public** repository named `Jupiter-Educational-Platform` (do **not** initialize with a license unless you explicitly want one).
2. Then:

```bash
cd ~/Public/Jupiter-Educational-Platform
git add .
git commit -m "Add Jupiter Educational Platform portfolio case study"
git remote add origin https://github.com/amiragomaa2597/Jupiter-Educational-Platform.git
git push -u origin main
```

## Do not

- Push private `JupiterFront` or `JupiterBackendOmar` source into this repo
- Add secrets, dumps, or unredacted screenshots
- Change visibility of the private source repositories
