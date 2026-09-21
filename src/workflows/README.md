# Workflows

The workflows subject contains automation scripts that support GitHub Actions workflows, CLI tools, and repository automation. These scripts handle tasks like PR labeling, cache purging, content change analysis, and repository maintenance.

## Purpose & Scope

This subject is responsible for:
- PR and issue automation (labeling, metadata, reviewer assignment)
- Cache management (Fastly edge cache purging)
- Content validation and reporting (content type checking, change tables)
- Repository maintenance (orphan file cleanup, syncing)
- Husky git hooks (pre-commit checks)
- GitHub Actions support scripts

Note: This directory does not contain a `scripts/` folder since every file here would belong in `scripts/`. Files are organized flat at the top level with supporting utilities in `lib/`.

## Setup & Usage

### Running workflow scripts locally

Scripts are registered in `package.json`:

| Script | Command | Purpose |
|--------|---------|---------|
| content-changes-table-comment | `npm run content-changes-table-comment` | Analyzes content changes in PRs |
| check-content-type | `npm run check-content-type` | Validates content types |
| delete-orphan-translation-files | `npm run delete-orphan-translation-files` | Removes orphaned translations |
| enable-automerge | `npm run enable-automerge` | Enables PR automerge |
| purge-fastly | `npm run purge-fastly` | Purges Fastly CDN cache (per-language, single-key, or entire cache) |
| prevent-pushes-to-main | (Husky hook) | Prevents pushing to main |

### Running tests

```bash
npm run test -- src/workflows/tests
```
