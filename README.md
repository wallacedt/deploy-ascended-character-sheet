# Ascended Character Sheet Deployment

This folder contains a standalone static build of the Ascended Character Sheet.

## Files

- `index.html` - the deployment-ready character sheet.
- `deployment-checklist.md` - a quick manual check for hosted deployments.

The sheet is designed to run as a static HTML app. It does not require a build step, server-side code, passwords, tokens, or Squarespace credentials.

## Repository Access

Deployment repository:

```text
https://github.com/wallacedt/deploy-ascended-character-sheet
```

Hosted character sheet URL:

```text
https://wallacedt.github.io/deploy-ascended-character-sheet/
```

Git and GitHub CLI access have been verified locally with:

```powershell
git --version
gh --version
gh auth status
gh repo view wallacedt/deploy-ascended-character-sheet
```

Expected GitHub CLI status:

```text
Logged in to github.com account wallacedt
Git operations protocol: https
Token scopes include: repo, workflow
```

Do not paste GitHub tokens into files, commit secrets, or share login credentials. Codex should not push changes unless explicitly instructed.

## Open Locally

Open `index.html` directly in a browser:

```text
deploy/character-sheet/index.html
```

Browser save/load uses `localStorage`, so saved test data is stored only in the browser and origin where the sheet is opened.

## Deploy To GitHub Pages

These instructions use the public repository `wallacedt/deploy-ascended-character-sheet`.

1. Commit the static deployment files to the repository.
2. In GitHub, open `wallacedt/deploy-ascended-character-sheet`.
3. Go to **Settings**.
4. Go to **Pages**.
5. Under **Build and deployment**, choose **Deploy from a branch**.
6. Select the `main` branch.
7. If the deployment files are committed at the repository root, choose `/root`.
8. If the deployment files are committed under `/deploy/character-sheet`, use a GitHub Actions workflow that publishes that folder.
9. After GitHub provides the Pages URL, open it and run `deployment-checklist.md`.

Do not commit secrets, tokens, or passwords to use GitHub Pages.

## Deploy To Netlify By Drag And Drop

1. Open Netlify in your browser.
2. Use Netlify's manual deploy or drag-and-drop deploy flow.
3. Drag the `deploy/character-sheet` folder into the deploy area.
4. After Netlify provides the hosted URL, open it and run `deployment-checklist.md`.

Do not share Netlify login credentials with this project or store credentials in repository files.

## Embed In Squarespace With Iframe

Add a Squarespace embed/code block and paste this snippet after replacing the URL:

```html
<iframe
  src="https://wallacedt.github.io/deploy-ascended-character-sheet/"
  style="width:100%; min-height:1400px; border:0;"
  loading="lazy"
  title="Ascended Character Sheet">
</iframe>
```

## Link From Squarespace With A Button

Add a Squarespace code block or button/link area and use this snippet after replacing the URL:

```html
<a
  href="https://wallacedt.github.io/deploy-ascended-character-sheet/"
  target="_blank"
  rel="noopener"
  style="display:inline-block;padding:12px 18px;border-radius:12px;background:#b9924a;color:#1a140c;text-decoration:none;font-weight:bold;">
  Open Ascended Character Sheet
</a>
```

## Deployment Safety Notes

- Keep the character sheet as a standalone static HTML app.
- Do not convert it to React or split files unless there is a specific deployment requirement.
- Do not remove or alter persistence, validation, Action Scene, Arcane, Divine, Psionic, AP, or race logic.
- Do not automate destructive Squarespace or website changes.
