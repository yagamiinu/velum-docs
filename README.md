# Velum Docs

The dedicated Velum documentation site, built with [Mintlify](https://mintlify.com).
This is the "real" reference (protocol, integration, security) — the marketing
copy on `site/` stays simple and separate.

## Structure

```
docs-site/
├─ docs.json              # Mintlify config: nav, theme, colors, links
├─ introduction/          # What is Velum, How it works, Privacy model
├─ using-velum/           # Add funds, Request, Cash out, Multichain
├─ protocol/              # Architecture, Circuits, Relayer, Compliance, Contracts
├─ build/                 # SDK quickstart, Integrate
├─ security/              # Audits & trusted setup, Threat model
└─ logo/                  # favicon + light/dark logos
```

## Local preview

```bash
npm i -g mint      # Mintlify CLI
cd docs-site
mint dev           # serves at http://localhost:3000
```

Validate links and config before shipping:

```bash
mint broken-links
```

## Deploy

Connect this repo to Mintlify (GitHub app) and set the content root to
`docs-site/`. Pushes to the default branch auto-deploy. Point a custom domain
(e.g. `docs.velum.finance`) at it from the Mintlify dashboard.

## Editing notes

- Pages are `.mdx`. Frontmatter `title` + `description` is required.
- Nav order is controlled by `docs.json` → `navigation.groups`, not the filesystem.
- Voice: honest, cypherpunk, the HTTPS analogy is the centerpiece. Keep the
  security/caveats pages candid — that honesty is the brand.
- Update `protocol/contracts.mdx` and `using-velum/multichain.mdx` as testnet
  deployments and (eventually) mainnet addresses land.
```
