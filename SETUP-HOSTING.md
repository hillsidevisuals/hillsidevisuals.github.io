# One-time setup: hillsidevisuals.github.io

Goal: outreach emails link to `hillsidevisuals.github.io/<prospect>` instead of `claude.ai`.
You do steps 1 and 2 in a browser, step 3 in your terminal. About 10 minutes. Free.

---

## 1. Create the GitHub organization (browser)

1. Sign in to GitHub as **hiletebisrat-cmyk**.
2. Go to https://github.com/organizations/plan
3. Pick **Free**. Organization name: **hillsidevisuals**  (must be exactly this, it becomes the URL).
   Contact email: hiletebisrat@gmail.com. Belongs to "my personal account".
4. Skip adding members. Finish.

If `hillsidevisuals` is taken, pick another name (e.g. `hillside-visuals-lv`) and tell me. The
mockup links then use that name and I will update the drafts and the script.

## 2. Create the Pages repo (browser)

1. https://github.com/organizations/hillsidevisuals/repositories/new
2. Repository name: **hillsidevisuals.github.io**  (exactly, including the `.github.io`).
3. **Public.** (Free orgs can only serve GitHub Pages from public repos. The pages are unlisted and
   carry a noindex tag, so they will not show up in search, but anyone with the link can open them,
   the same as the old Claude Artifact links.)
4. Do **not** add a README or license. Create the repo.

GitHub Pages turns on automatically for a repo named `<org>.github.io`. Nothing else to configure.

## 3. Push the mockups (terminal)

In this session you can prefix a line with `!` to run it here.

```
brew install gh
gh auth login          # GitHub.com, HTTPS, "Login with a web browser", paste the code
~/.claude/skills/lv-prospecting/publish-mockup.sh --all
```

That pushes the 5 current mockups. Give it about a minute, then open
https://hillsidevisuals.github.io/beach-cafe to confirm.

---

## After setup

- New prospect, or you edited a mockup:
  `~/.claude/skills/lv-prospecting/publish-mockup.sh <slug>`
- The `/lv-prospecting` skill now points new packages at this repo automatically.
- The local repo lives at `~/Hillside Brand/Prospecting/_mockup-site/`.

## Later, if you want a real domain

Buy `hillsidevisuals.com` (~$12/yr), add it under the repo's Settings, Pages, Custom domain, and
add the DNS records GitHub shows you. Links become `hillsidevisuals.com/beach-cafe`. Tell me when
the domain exists and I will switch the drafts and the script.
