# Deployment Checklist

Run this check after opening the hosted character sheet URL.

Repository:

```text
https://github.com/wallacedt/deploy-ascended-character-sheet
```

Hosted URL:

```text
https://wallacedt.github.io/deploy-ascended-character-sheet/
```

Before deployment, confirm local GitHub access:

- [ ] `git --version` works.
- [ ] `gh --version` works.
- [ ] `gh auth status` shows `wallacedt` logged in.
- [ ] `gh repo view wallacedt/deploy-ascended-character-sheet` works.
- [ ] No passwords, tokens, or secrets are stored in repo files.

- [ ] Open hosted URL.
- [ ] Confirm all tabs render: Identity, Attributes, Skills, Inventory, Arcane, Divine, Psionic, Action Scene, Notes.
- [ ] Fill Character Name.
- [ ] Select Handedness.
- [ ] Click Save to Browser.
- [ ] Reload page.
- [ ] Click Load from Browser.
- [ ] Confirm data restores.
- [ ] Click Export JSON.
- [ ] Confirm JSON appears in the import/export text area.
- [ ] Clear or change the Character Name.
- [ ] Paste the exported JSON if needed.
- [ ] Click Import JSON.
- [ ] Confirm data restores.

Notes:

- Browser saves use `localStorage` and are scoped to the hosted URL.
- Test data saved on a local file URL will not automatically appear on the hosted URL.
- Do not store passwords, tokens, or secrets in the character sheet or repository files.
