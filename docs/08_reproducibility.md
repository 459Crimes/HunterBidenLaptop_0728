# 8. How to verify the published tables

> **Encyclopedia.** The articles are the entry point; the [evidence catalog](catalog/README.md) names the files behind them. Historical claims are cited public sources; they are not generated from SHA-256.

This repository is a **metadata and hash witness**. A reader can check that the published tables match the checksums in this tree. A reader **cannot** re-open Extra Found Files bytes from this GitHub checkout.

## Two evidence layers

1. **Inventory layer** — paths, hashes, timestamps, category rollups, published under `build/` and listed in the catalogs.
2. **Historical-source layer** — call, FBI photos, court, news chronology in [Timeline and handling](06_timeline_and_handling.md) and [Source matrix](09_source_matrix.md).

## Checksums

| File | Role |
|---|---|
| [`build/manifest.tsv`](../build/manifest.tsv) | Path, size, SHA-256, and data-row count for every published `build/` object |
| [`build/manifest.sha256`](../build/manifest.sha256) | Same hashes in `sha256sum` form |

To verify a checkout, recompute SHA-256 of each path in `manifest.tsv` and compare.

## Claim → catalog

| Public claim | Catalog | File |
|---|---|---|
| 480,039 paths / 317,319 hashes | [Corpus identity](catalog/corpus_info.md) | `01_acquisition.tsv` |
| Extra Found Files 479,584 | [File tree](catalog/file_tree.md) | `01_top_level_summary.tsv` |
| Category populations | [File tree](catalog/file_tree.md) | `02_category_distribution.tsv` |
| Extension populations | [Metadata](catalog/metadata.md) | `02_extension_distribution.tsv` |
| 70.2% / 29.8% primary overlap | [Hash manifest](catalog/hash_manifest.md) | `04_coverage.tsv` |
| 2021 vs 2026 mtime years | [Metadata](catalog/metadata.md) | `01_time_distribution.tsv` |
| R-00014 audio SHA-256 | [Exhibits](catalog/exhibits.md) | `docs/exhibits/audio/` |

## Claims that rest on historical sources

Ziegler MEGA hop, Hayes carving words, Mesa County badge facts, FD-597 photographs, and the FBI referral are **not** filesystem derivations. They are sourced in [Source matrix](09_source_matrix.md).

## Reproduce from PostgreSQL (operator)

On a machine with `rhb_forensics`:

```sql
SELECT COUNT(*), COUNT(DISTINCT sha256), SUM(size)
FROM files
WHERE source_id = 2 AND relative_path LIKE '0728/%';
```

Expected: `480039` / `317319` / `336321196441`.

Scripts live in gitignored `.local-use-only/scripts/`.

## What “reproducible” means without source bytes

Checking checksums and re-reading the published TSVs can show that two analysts reach the same structural and overlap conclusions from the same reports.

It does **not** prove this GitHub checkout independently re-hashed every Extra Found Files object.
