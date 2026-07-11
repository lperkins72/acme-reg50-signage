# Acme Signage REG50 Signage

## Purpose

This repository is the generated frontend deployment package for:

- tenant: `acme`
- region: `reg50`

It was generated from the neutral `BDN-region-template` source.

That template uses `BDN-Next` as its shell baseline, then resolves tenant, region, and device placeholders during generation.

## Identity Model

This region expects screen identity from the URL query string:

```text
?tenant=acme&region=reg50&device=nuc-001
```

Example:

```text
https://<deployment-domain>/?tenant=acme&region=reg50&device=nuc-001
```

## Included

- `index.html`
- `primary.html`
- `secondary.html`
- `footer.html`
- `primaryending.html`
- `secondary-footer-overlay.html`
- `assets/`
- `data/`
- `regions/reg50/`
- `devices/reg50/`
- `sw.js`
- `robots.txt`
- `wrangler.jsonc`

## Device Naming Rule

This region currently includes `25` generated NUC launcher pages.

Device values are unique inside this region and tenant.

Examples:

- `acme / reg50 / nuc-001`
- `acme / reg50 / nuc-002`

## Control Plane Pairing

This generated frontend is configured to use:

- `https://acme-control-plane.example.workers.dev`

That base URL is written into:

- `data/sync.json`

## Next Steps

1. create the GitHub repo for this generated region
2. push this folder as its own repo
3. create the Cloudflare Pages project
4. confirm the tenant control plane origin rules include this region domain
5. test one launcher such as `/devices/reg50/nuc-001.html`
