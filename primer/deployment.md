# Deployment

Where Artifact software runs — hosting targets, app stores, and domains.

## Targets

| Repo | Deploys to | URL / Store | How |
|---|---|---|---|
| subpixel | Cloudflare Workers | [subpixel.app](https://subpixel.app) | `npm run deploy` (`wrangler deploy`) |
| minder | internal — see `arfct/internal` | — | — |
| villainy | Cloudflare Workers | [play.villainy.app](https://play.villainy.app) | `npm run deploy` (`wrangler deploy`) |
| catalogue | GitHub Pages | [arfct.github.io/catalogue](https://arfct.github.io/catalogue/) | GitHub Actions (`deploy-github-pages.yml`) |
| catalogue-artifact | Cloudflare Pages | [catalogue-artifact.pages.dev](https://catalogue-artifact.pages.dev) | `npm run deploy` (`wrangler pages deploy`) |
| web | unverified (no deploy config in-repo; possibly Cloudflare) | [artifact.com](https://artifact.com) | unverified |
| hourglass | internal — see `arfct/internal` | — | — |
| chronograph | internal — see `arfct/internal` | — | — |
| size.fyi | Cloudflare Workers | [size.fyi](https://size.fyi) | `npm run deploy` (`wrangler deploy`) |
| timezone.fyi | Netlify (unverified as sole/active host) | timezone.fyi (unverified) | Netlify Functions |
| itty-bitty | Netlify or Firebase Hosting (unverified) | [itty.bitty.site](https://itty.bitty.site) | unverified |

Rows marked "internal" are private repos with no confirmed public distribution — deployment detail for those lives in `arfct/internal`, not here. Rows marked "unverified" reflect what the repo itself doesn't confirm; treat them as best-guess, not fact.

## Cloudflare

Most Artifact products run on Cloudflare Workers or Cloudflare Pages. The convention is a `deploy` script in `package.json` that wraps the Wrangler CLI — `wrangler deploy` for Workers, `wrangler pages deploy` for Pages — so deploying is always `npm run deploy`.

Which Cloudflare account, zone, and bucket/database bindings back each project is inventory, not process — see `arfct/internal`'s `accounts.md`.

## Secrets

Three kinds of secrets, three homes — nothing secret ever lives in git:

- **Production runtime secrets** (API keys a Worker reads at runtime) — Workers secrets, set with `wrangler secret put` or the Cloudflare dashboard.
- **Shared CI tokens** (e.g. a Cloudflare deploy token used by GitHub Actions) — org-level Actions secrets on GitHub, scoped to the repos that need them. Set once, rotate once.
- **Everything humans handle** (account credentials, personal API tokens, local `.dev.vars` values) — the shared password manager. Repos commit a `.dev.vars.example` template with names only; real values come from the vault.

Which vault and which accounts: see `arfct/internal`'s `accounts.md`.

## App stores

Native apps ship through the platform stores: iOS via App Store Connect, Android via Google Play Console. Bundle/package IDs follow `com.artifact.<product>` — confirmed for Villainy (`com.artifact.villainy`).

Store listing status for Artifact's other native projects isn't confirmed publicly yet; a product's own repo docs are the source of truth for whether it's actually published.

## Domains

Product domains follow short, product-named patterns: `subpixel.app`, `size.fyi`, `timezone.fyi`, `itty.bitty.site`, plus the primary `artifact.com`. The registrar and DNS inventory lives in `arfct/internal`, not here.
