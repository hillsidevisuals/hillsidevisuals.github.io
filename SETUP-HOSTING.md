# Mockup hosting — hillsidevisuals.github.io

**Status: live as of 2026-08-31.** Outreach emails link to `hillsidevisuals.github.io/<prospect>`
instead of `claude.ai`.

## How it is set up

- Separate GitHub account **`hillsidevisuals`** (a standalone account, not an org, which works the
  same for Pages). `gh` on this Mac is authenticated as it.
- Public repo **`hillsidevisuals/hillsidevisuals.github.io`**, GitHub Pages serving `/` on `main`.
- This local folder (`~/Hillside Brand/Prospecting/_mockup-site/`) is that repo. `origin` points at it.
- Each prospect: `<slug>/index.html`, one self-contained file. `robots.txt` + a `noindex` meta on
  every page keep them out of search. Unlisted, not secret: anyone with the link can open them, same
  as the old Artifact links. Root `index.html` is a plain Hillside card, no prospect list.

## Publishing changes

```
~/.claude/skills/lv-prospecting/publish-mockup.sh <slug>     # one prospect
~/.claude/skills/lv-prospecting/publish-mockup.sh --all      # every prospect in the latest month
```

Copies `Prospecting/<latest-month>/<slug>/website/index.html` in, commits, pushes. Pages redeploys
in about a minute. `/lv-prospecting` runs this automatically for new packages.

If `gh` ever logs out: `gh auth login` (GitHub.com, HTTPS, web browser), pick the `hillsidevisuals`
account.

## Later: a real domain

Buy `hillsidevisuals.com` (~$12/yr), add it under the repo Settings, Pages, Custom domain, and set
the DNS records GitHub shows. Links become `hillsidevisuals.com/beach-cafe`. Tell Claude when the
domain exists to switch the drafts and the script.
