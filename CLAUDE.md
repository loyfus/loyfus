# CLAUDE.md

Guidance for Claude Code and other AI assistants working in this repository.

## What this repository is

`loyfus/loyfus` is a **GitHub profile README repository** — the special repo whose
name matches its owner's username, so its `README.md` renders at the top of
<https://github.com/loyfus>.

**It is not a software project.** There is no application code, no build system, no
dependency manifest, no tests, and no CI. The entire repository is a single file:

```
.
└── README.md    # the rendered GitHub profile page (25 lines)
```

This has been true for every commit since the repo was created on 2021-08-01. Treat
the absence of tooling as intentional, not as something missing.

### Do not add

Unless the owner explicitly asks, do **not** introduce:

- `package.json`, lockfiles, or any dependency manifest
- linters, formatters, or pre-commit hooks
- GitHub Actions workflows (including README-stat auto-updaters)
- build scripts, bundlers, or a `src/` directory
- additional Markdown files, `.github/` metadata, or issue templates

The deliverable is one rendered page. Extra tooling adds maintenance cost and cannot
improve the output.

## The rendering surface

`README.md` is GitHub Flavored Markdown that also uses raw HTML. GitHub sanitizes
that HTML before rendering, which constrains what will actually work:

- **`<script>`, `<style>`, `<form>`, `<iframe>`, and event handlers are stripped.** Any
  suggestion involving JavaScript or custom CSS will silently do nothing.
- **`style` attributes are removed.** Layout must come from the allowed HTML subset
  (`<div>`, `<picture>`, `<img>`, `<a>`, tables, alignment attributes).
- **Images are proxied through GitHub's camo service.** They are fetched server-side
  and cached, so an updated remote image may not appear immediately, and any image
  host must be publicly reachable.
- **`<picture>` with `media` queries is supported** and is the standard way to serve
  light/dark variants — see the theming block below.
- Relative links resolve against this repo, so prefer absolute URLs.

## Current content structure

The file has three blocks, in order:

1. **Badge row** (lines 1–5) — a `<div>` holding three
   [shields.io](https://shields.io) badges linking to Instagram, email, and LinkedIn.
   Each badge is an `<img>` from `img.shields.io` wrapped in an `<a>`.
2. **Intro** (lines 7–13) — an `<h3>` greeting plus a three-item bullet list of
   background facts.
3. **Language stats card** (lines 15–25) — a `<picture>` element embedding the
   `github-readme-stats.vercel.app` top-languages card, with a dark-theme variant.

### Theming block — read before editing

The `<picture>` block works, but its second `media` query is not what it looks like:

```html
<source srcset="...&theme=dark" media="(prefers-color-scheme: dark)" />
<source srcset="..."            media="(prefers-color-scheme: dark), (prefers-color-scheme: no-preference)" />
<img    src="..." />
```

The second `<source>` repeats `dark` where `light` was almost certainly intended. It
still renders correctly by accident: the first `<source>` already claims dark mode, so
the duplicated clause is dead, `no-preference` gets the light card, and light mode
falls through to the `<img>` fallback — also the light card. If you touch this block,
fix the query to `(prefers-color-scheme: light)` rather than reproducing the
copy-paste. Keep the bare `<img>` as the final fallback; browsers and feed readers
that ignore `<picture>` depend on it.

## Content conventions

- **Language is Brazilian Portuguese.** All prose — headings, bullets, any new
  section — is written in pt-BR, first person, informal register. Do not translate
  existing content to English or add English sections unless asked.
- **The display name is "Luiz."** The README said "Felipe" until 2025-04-13, when it
  was deliberately changed. Git history still shows both `Felipe Penha` and
  `Luiz Penha` as commit authors. Do not "correct" Luiz back to Felipe.
- **Handles differ from the username.** GitHub is `loyfus`, Instagram is `loyfuss`
  (double s), LinkedIn is `feepenha`. These are not typos — verify against history
  before changing any of them.
- **The contact email is `felipepenha32@gmail.com`**, migrated from an iCloud address
  in 2025-08. The badge is labeled Gmail; keep the label and the address in sync.
- Badges use `style=for-the-badge` with brand colors. Match that style when adding one.
- Formatting is hand-written and slightly irregular — a trailing space on line 1, and
  `href = "mailto:..."` with spaces around the `=` on line 3. Both are harmless. Leave
  them alone unless you are editing that line anyway; a whitespace-only cleanup commit
  adds noise to a 25-commit history without changing the rendered page.
- The file is UTF-8 with LF endings and no BOM. Portuguese accents are stored
  literally (`informações`, not entities). Preserve that.

### Known issues

**The language-stats card is currently broken (verified 2026-07-31).** All three
`github-readme-stats.vercel.app` URLs in the `<picture>` block return HTTP 503
`DEPLOYMENT_PAUSED` — the upstream Vercel deployment is paused, not merely rate
limited. GitHub's camo proxy may still be serving a cached copy, so the profile page
may look fine for a while, but the origin is down and the card will break once the
cache expires.

If asked to fix it, the options are, in rough order of durability:

1. Self-host the [`github-readme-stats`](https://github.com/anuraghazra/github-readme-stats)
   project on your own Vercel instance and point the three URLs at it. The upstream
   README documents this precisely because the shared instance is unreliable.
2. Swap in a different stats provider.
3. Remove the block. The profile still reads fine without it.

Do not simply retry the existing URLs and call it fixed — the pause is on the
provider's side and nothing in this repo can change it.

**Two typos** are live in the intro bullet added on 2025-08-21 (line 12):

- `grduação` → `graduação`
- `Analise` → `Análise`

These are left as-is because no one has asked for them to be fixed. If you are editing
that line for another reason, fix them in the same commit; otherwise mention them
rather than opening a drive-by commit.

## Workflow

### Editing

Change `README.md` directly. There is nothing to install, compile, or run.

### Verifying a change

There is no test suite, so verification is visual and manual:

1. Render the Markdown locally or in an editor preview to confirm the structure holds.
   Note that a local preview will **not** reproduce GitHub's HTML sanitization — HTML
   that previews fine locally may be stripped once pushed.
2. Confirm every badge and image URL returns an image (`curl -I <url>`). The shields.io
   and `github-readme-stats.vercel.app` endpoints are third-party services; a broken
   or rate-limited URL renders as a broken image on the profile page.
3. Check both color schemes if the `<picture>` block changed.
4. After pushing, load <https://github.com/loyfus> to confirm the profile renders as
   expected. This is the only fully accurate check.

### Committing

- All 25 commits in history use GitHub's default web-editor message, `Update README.md`,
  which indicates edits have historically been made through github.com rather than
  locally. You do not need to imitate that — a short, specific message describing the
  change is more useful. Keep it in the imperative mood.
- The default branch is `main`.
- Commit only `README.md` unless the task genuinely calls for a new file.

## Sibling repository: `loyfus/hub-loyfus`

This session also has access to `loyfus/hub-loyfus`. **That repository is completely
empty** — zero commits and zero refs on the remote, as of 2026-07-31. It has no code
to document and no relationship to this repo's content. Do not assume the two share a
codebase, and do not use this file as guidance for it.
