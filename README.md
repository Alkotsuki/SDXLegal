# SDXLegal

Public legal documents for SDX apps, served as a GitHub Pages site.

**Live site:** https://alkotsuki.github.io/SDXLegal/

| Document | Source | URL |
| --- | --- | --- |
| Evoke — Privacy Policy | [`evoke/privacy.md`](evoke/privacy.md) | https://alkotsuki.github.io/SDXLegal/evoke/privacy/ |
| Evoke — Support & FAQ | [`evoke/support.md`](evoke/support.md) | https://alkotsuki.github.io/SDXLegal/evoke/support/ |
| Clarta — Privacy Policy | [`clarta/privacy.md`](clarta/privacy.md) | https://alkotsuki.github.io/SDXLegal/clarta/privacy/ |
| Clarta — Support & FAQ | [`clarta/support.md`](clarta/support.md) | https://alkotsuki.github.io/SDXLegal/clarta/support/ |

`evoke/support.md` is the **Support URL** on Evoke's App Store product page. App Review checks that
it loads and that it offers a way to contact support, so it must stay reachable and must keep the
contact button (`evoke.support@gmail.com`).

## Publishing

GitHub → **Settings → Pages → Build and deployment**: source *Deploy from a branch*, branch `main`,
folder `/ (root)`. GitHub builds it with Jekyll (`_config.yml`, `jekyll-theme-primer`). Each document
sets its own `permalink` in front matter, so URLs stay stable even if files move.

There is no local build step. Pushing to `main` republishes.

## Editing rules

- **The policy describes the shipped app, not intentions.** Every factual claim in
  `evoke/privacy.md` — the 1024 px downscale, `store: false`, "no raw decimal can be sent to
  analytics", the Keychain sync behaviour — is a property of code in the Evoke repo. If that code
  changes, this page changes in the same PR.
- **The FAQ answers describe the shipped app too** — the three free cloud edits, the 1024 px cloud
  copy, refinements being free, restore living in Settings. If that behaviour changes in the Evoke
  repo, `evoke/support.md` changes with it.
- Bump both **Last updated** and, for material changes, **Effective date** in the front matter block
  at the top of the document.
- Keep the plain-English summary at the top in sync with the numbered sections. Users read the
  summary; regulators read the sections.
