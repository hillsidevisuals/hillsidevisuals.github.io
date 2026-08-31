# hillsidevisuals.github.io

Client-facing preview mockups for Hillside Visuals cold outreach.

- Each prospect gets a folder: `/<slug>/index.html` served at `https://hillsidevisuals.github.io/<slug>`
- Every page is a single self-contained HTML file (images inlined as data URIs).
- `robots.txt` + a `noindex` meta on every page keep these out of search. They are unlisted, not
  secret: anyone with the link can open them (same as the old Claude Artifact links).
- The root `index.html` is a plain Hillside card, no list of prospects.

## Updating

From a machine with `gh` authenticated:

```
~/.claude/skills/lv-prospecting/publish-mockup.sh <slug>     # one prospect
~/.claude/skills/lv-prospecting/publish-mockup.sh --all      # every prospect in the latest month
```

The script copies `Prospecting/<latest-month>/<slug>/website/index.html` into this repo, commits, and
pushes. GitHub Pages redeploys in about a minute.
