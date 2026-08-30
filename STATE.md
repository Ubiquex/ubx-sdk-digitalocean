# STATE.md -- current state

> Rewritten, not appended, as the LAST act of every session. See `HISTORY.md`
> for the narrative.

## In flight

Real first commit (generated bindings + scaffold) pushed to a branch,
PR open, not yet merged. Not published to any registry yet -- publish
only happens after merge, per `CLAUDE.md`'s own publishing discipline.

## Blocked

Nothing blocked once the PR merges.

## Current state

No tags exist yet. `VERSION` at repo root: fetched 2026-08-29 from
DigitalOcean's own real, public OpenAPI 3.0 spec, bundled via
`ubx-provider-dynamic`'s own `redocly_bundle` mechanism, generated
against the real, pinned `ubx-schema-digitalocean` v1.0.0 release.

## Before touching anything

- Never self-merge here. See `CLAUDE.md`.
- Never hand-edit generated bindings -- fix the generator or the upstream
  schema, then regenerate.
