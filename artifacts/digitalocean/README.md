# artifacts/digitalocean

UBI-240 slice 6: the canonical home for this provider's own docs/codegen
artifacts, moved here from `ubiquex-docs`. See `ubx-sdk-kubernetes`'s
own `artifacts/kubernetes/README.md` for the full account of why this
moved (UBI-102's own comment thread) and how the files divide.

- **`descriptions.json`** / **`intros.json`** / **`categories.json`** —
  real source of truth, read by `ubx-docs-providers` at build time.
  No `exclusions.json` yet -- this provider genuinely has none authored
  in `ubiquex-docs` either; `ubx-docs-providers` never reads it, so its
  absence is not a gap.
- **`digitalocean.json`** — codegen-ready export (`{resource: {relPath:
  text}}`, qualifier-stripped, HTML-unescaped). What `ubx sdk gen
  --descriptions-dir artifacts/digitalocean` actually reads. Never
  edited directly.

To update: edit `descriptions.json` here, then regenerate
`digitalocean.json` from a sibling `ubiquex-docs` checkout:

```bash
ubx sdk gen --only digitalocean --dump-ir /tmp/dump --out /tmp/unused
cd ~/Ubiquex/ubiquex-docs/scripts/resource-reference-gen
python3 export_raw_descriptions.py digitalocean DigitalOcean \
    --dump-root /tmp/dump/digitalocean \
    --descriptions-path ~/Ubiquex/ubx-sdk-digitalocean/artifacts/digitalocean/descriptions.json \
    --nested-out ~/Ubiquex/ubx-sdk-digitalocean/artifacts/digitalocean/digitalocean.json
```

Commit both files together.
