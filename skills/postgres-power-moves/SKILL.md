---
name: postgres-power-moves
description: Uses the PostgreSQL features most people miss, like JSONB, arrays, generated columns, partial indexes, and window functions, to make your database simpler and faster.
---

# Postgres Power Moves

Use this when designing tables, writing queries, or tuning performance on PostgreSQL
(including Supabase and Neon).

## Reach for these when they fit

- **JSONB** for flexible, rarely-filtered attributes. Index with GIN if you query inside it.
  Don't hide core fields in JSON; give them real columns.
- **Arrays** for short lists like tags (`text[]`), with a GIN index for `@>` lookups.
- **Generated columns** for values derived from other columns (full names, search vectors).
- **CHECK constraints and enums/domains** so bad data can't get in, instead of only
  validating in the app.
- **Partial indexes** for common filters: `create index … where deleted_at is null`.
- **Expression indexes** for queries like `lower(email)`.
- **Window functions** (`row_number`, `rank`, `lag`, running totals) instead of loops in
  app code.
- **CTEs** (`with …`) to make long queries readable.
- **Upserts** with `insert … on conflict … do update`.
- **Full-text search** with `tsvector` and `to_tsquery` before adding a search service.
- **`returning`** on insert/update/delete to avoid a second query.

## Habits

- Use `timestamptz`, not `timestamp`. Use `uuid` or `bigint identity` keys.
- Add an index for every foreign key you join or filter on.
- Check slow queries with `explain analyze` before guessing.
- Make schema changes as migrations, never by hand in production.
- If the app exposes tables to users (like Supabase), turn on row-level security and write
  policies before shipping.

## Output

When suggesting a change, show the SQL, explain why it helps in one line, and note any
migration or locking risk on large tables.
