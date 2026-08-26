# Changelog

All notable changes to this project are documented here. The format is based on
[Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and this project
adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.2.0] - 2026-08-26

### Added

- `isNull(column)` and `isNotNull(column)` WHERE condition builders, emitting
  `"col" IS NULL` / `"col" IS NOT NULL` with no parameter bindings. Use these
  for null comparisons; `eq(column, null)` emits `"col" = ?`, which never
  matches in SQLite.

## [0.1.0]

### Added

- Initial release: typed `table`/`column` schema, `Database` CRUD over Durable
  Object SQLite, `eq`/`ne`/`lt`/`lte`/`gt`/`gte`/`and` conditions, `asc`/`desc`
  ordering, and a `migrate()` runner.
