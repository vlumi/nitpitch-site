# nitpitch.app

The website for **Nitpitch** — a tuner for violin, guitar, bass, and more, on iPhone, iPad, and Mac. Landing, support, and privacy pages.

The app itself is open source (MIT) at [github.com/vlumi/nitpitch](https://github.com/vlumi/nitpitch). **This site is not**: the marketing copy and artwork are all rights reserved. The repository is public for transparency, not for reuse.

## Build

Static site, built with [Hugo Extended](https://gohugo.io/). No JS, no external assets — plain HTML/CSS.

The Hugo version is **pinned** in [`.hugoversion`](.hugoversion). Hugo is a build-time tool, not a runtime — there's no security reason to chase updates, and a bump is the thing most likely to *break* the build. So pin it and update **deliberately**: bump `.hugoversion`, run a local build, and commit only if it's clean. (The box's nginx / OS / certbot are what stay current, not Hugo.)

```sh
hugo server        # local preview at http://localhost:1313
hugo               # one-off build into ./public
```

## Deploy

Served by nginx over HTTPS (Let's Encrypt / certbot) on the host for `nitpitch.app`. [`deploy.sh`](deploy.sh) does it in one step: it fetches the **pinned** Hugo Extended (cached per-version under `~/.local/share/nitpitch-hugo`, no root, never the system Hugo), pulls, and builds straight into the web root.

```sh
./deploy.sh                          # pull, build, publish to /var/www/nitpitch.app
WEBROOT=/some/other/path ./deploy.sh # override the publish dir
./deploy.sh --no-pull                # build the working tree as-is
```

[`nginx.conf.example`](nginx.conf.example) is the server block it's served from.

## Content

Four pages, all small:

- `layouts/index.html` — the landing page, written directly in the template since it's structure rather than prose.
- `content/support.md` — troubleshooting, aimed at the questions a tuner actually provokes ("it says play a note", "it disagrees with my other tuner").
- `content/privacy.md` — mirrors [PRIVACY.md](https://github.com/vlumi/nitpitch/blob/main/PRIVACY.md) in the app repo. **Keep the two in step**: App Store Connect points at one of them, and a privacy policy that contradicts itself is worse than either version alone.
- `content/guide.md` + `content/guide-watch.md` — the user guide, illustrated by real captures. The images live in `static/img/guide/` and come from the app repo's shot machinery, canonical names kept: `make shots` (the ASC set — the guide reuses launch/grid/string-view/presets/share), `make guide-shots` (the guide-only states), `make watch-shots` (the wrist, fully automatic). Re-run and re-copy when the UI changes; every illustration is a real detector reading by construction.

## Planned: the tuning collection

The app ships only the obvious tunings — standard, Drop D. The long tail (scordatura, open tunings, historical and regional setups) is meant to live *here*, as pages of preset links (`https://nitpitch.app/t#…` — the same links the app's own sharing emits), so the collection grows without an app update or a trip through App Review, and without bloating the picker for everyone who just wants standard.

The plumbing has shipped on both sides: the app emits and accepts these links as Universal Links, and `/t` is their landing page for anyone without the app. What's not built is the collection itself — the curated pages. See "nitpitch.app's tuning collection" in the app repo's ROADMAP (named, not numbered: the section numbers churn).

## Assets

`static/appicon.png` is generated from the app's own icon script (`Scripts/assets/make-icon.swift` in the app repo) rather than drawn separately, so the site and the App Store listing can't drift apart. Regenerate it there and copy it here.

## Styling

The app's language, not a separate brand: charcoal panel, the in-tune green from the icon's centre tick, and a shallow dial arc as the only ornament. Dark by default — the app is — with a light-appearance override.
