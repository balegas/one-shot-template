# Vendored skills

These skills were vendored from upstream Electric SQL packages on
2026-05-03. They contain library-author-maintained instructions for
agents (Claude, Copilot, Cursor, etc.) on how to use the corresponding
libraries correctly.

| Skill | Source package | Source path |
|-------|---------------|-------------|
| electric-debugging | @electric-sql/client | electric/packages/typescript-client/skills/electric-debugging |
| electric-deployment | @electric-sql/client | electric/packages/typescript-client/skills/electric-deployment |
| electric-new-feature | @electric-sql/client | electric/packages/typescript-client/skills/electric-new-feature |
| electric-orm | @electric-sql/client | electric/packages/typescript-client/skills/electric-orm |
| electric-postgres-security | @electric-sql/client | electric/packages/typescript-client/skills/electric-postgres-security |
| electric-proxy-auth | @electric-sql/client | electric/packages/typescript-client/skills/electric-proxy-auth |
| electric-schema-shapes | @electric-sql/client | electric/packages/typescript-client/skills/electric-schema-shapes |
| electric-shapes | @electric-sql/client | electric/packages/typescript-client/skills/electric-shapes |
| electric-yjs | @electric-sql/y-electric | electric/packages/y-electric/skills/electric-yjs |

## Auto-update path

The template's `package.json` runs `intent install --no-prompt || true`
on `postinstall`. When upstream packages start including `skills/` in
their published tarballs (via the `files` field in their `package.json`),
those skills will start flowing in automatically — overriding (or sitting
beside) these vendored copies. At that point, this README + the vendored
copies should be removed in favor of the auto-installed versions.

## Skills NOT vendored (no upstream skills exist yet)

- `@durable-streams/client` — no `skills/` directory in source
- `@tanstack/db` / `@tanstack/electric-db-collection` — no `skills/` in source
- AI durable transport — package not yet identified
- (Future) Durable Streams Yjs provider — separate from y-electric, not yet authored
