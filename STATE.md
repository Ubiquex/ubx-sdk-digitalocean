# STATE.md -- current state

> Rewritten, not appended, as the LAST act of every session. See `HISTORY.md`
> for the narrative.

## In flight

Nothing in flight as of 2026-09-04. This file's own "PR open, not yet
merged, no tags exist yet" claim above was stale -- this repo has
since published for real multiple times; don't trust an unrewritten
STATE.md's own age claims, re-check.

## Blocked

Nothing blocked. Zero open PRs.

## Current state

**`translator-watch.yml` is now live (UBI-249).** This repo's own
`hash-watch.yml` already auto-regenerates and correctly commits
`PROVENANCE.json` on real spec drift; `translator-watch.yml` adds the
other, independent trigger (a translator-tag move) that path never
covered -- regenerates holding the schema fixed at this repo's own
pinned version, self-heals (`PROVENANCE.json` only) on an empty diff,
opens a real review PR on a genuine one. Never auto-merges.

This repo's own `--descriptions-dir` fix (a session-wide gap: every
hand regeneration had omitted the flag) and `PROVENANCE.json` bootstrap
(this repo never had one before) both merged this same arc. This
regeneration was also verified to be generated after the earlier
accelerator/dedicated-inference-accelerator path-collision fix (both
now real, separate files).

Published: npm/PyPI `1.0.1` (verified directly against the registries).
Committed: `1.0.2` (ahead, not yet published -- no bump needed until a
real publish is dispatched). `PROVENANCE.json` records a real, verified
`ubx-provider-dynamic` commit (`dba9b68`, tag `v1.0.13`).

`VERSION` at repo root: fetched 2026-08-29 from
DigitalOcean's own real, public OpenAPI 3.0 spec, bundled via
`ubx-provider-dynamic`'s own `redocly_bundle` mechanism, generated
against the real, pinned `ubx-schema-digitalocean` v1.0.0 release.

## Before touching anything

- Never self-merge here. See `CLAUDE.md`.
- Never hand-edit generated bindings -- fix the generator or the upstream
  schema, then regenerate.
