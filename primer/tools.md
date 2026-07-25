# Tools

The tools Artifact builds with, grouped by area — what each one is used for, not a sales pitch.

## Development

- **Claude Code** — primary tool for agent-assisted development, following the Superpowers plugin conventions for skills and workflows.
- **GitHub** (`gh` CLI) — hosts every repo; issues, pull requests, and Actions runs are usually driven through the `gh` CLI.
- **Wrangler** — Cloudflare's CLI for local development and deployment of Worker and Pages projects.
- **Eleventy** — static site generator behind the Catalogue Raisonné template.
- **Xcode** — builds and ships the Swift-based iOS, watchOS, and macOS apps.
- **Gradle** — builds the Kotlin-based Android app.
- Typical stacks lean on TypeScript/JavaScript running on Cloudflare Workers, with SolidJS, Three.js, or PixiJS where a frontend framework is needed.

## Tracking

- **Linear** (workspace `arfct`) — issue tracking and project status. See [linear.md](linear.md) for how Artifact uses it.

## Design

- **Figma** — design and prototyping for product UI and marketing.

## Infrastructure

- **Cloudflare Workers** — serverless compute behind most apps and sites.
- **Cloudflare Pages** — hosts static site deployments.
- **Cloudflare R2** — object storage for media and other project assets.
- **Cloudflare Durable Objects** — stateful coordination for realtime and multiplayer features.
- **Cloudflare D1** — SQL database for projects that need relational storage.
- **Netlify** — hosts a small number of legacy sites that predate the move to Cloudflare.
- **GitHub Actions** — builds and deploys the public Catalogue Raisonné template to GitHub Pages.
