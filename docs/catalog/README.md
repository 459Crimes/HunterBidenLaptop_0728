# Evidence catalog

This encyclopedia publishes **derived forensic tables and reports**, not Extra Found Files bytes. Each catalog page lists one family of files, what it measures, and how it relates to the articles.

Checksums for every published `build/` object: [`build/manifest.tsv`](../../build/manifest.tsv) · [`build/manifest.sha256`](../../build/manifest.sha256).

| Catalog | What it covers | Typical articles |
|---|---|---|
| [Corpus identity](corpus_info.md) | Tree kind, URI, delivery fields | [What is 0728?](../01_what_is_0728.md) |
| [File tree](file_tree.md) | Top-level and R-Studio category rollups | [What is in the corpus](../04_what_is_in_the_corpus.md) |
| [Hash manifest](hash_manifest.md) | SHA-256 overlap vs APFS / GAI / JPMI | [Integrity](../INTEGRITY.md) |
| [Metadata](metadata.md) | Extension and mtime-year summaries | [Timestamps](../TIMESTAMPS.md) |
| [Reports](reports.md) | Generated forensic summaries | [Timeline](../TIMELINE.md) |
| [Exhibits](exhibits.md) | R-00014 audio, FBI document photos, Hayes signed affidavit | [Exhibits](../EXHIBITS.md) |

## How to read a table

TSV files are UTF-8, tab-separated, with a header row. Path count and distinct SHA-256 are **different identity systems** — see [Glossary](../GLOSSARY.md) and [Sourcing](../MANUAL_OF_STYLE.md).

The articles state a claim in prose. The catalog names the file that holds the rows. The TSV is the appendix.

## What is not here

- Extra Found Files source bytes (`source/recovered/`)
- Full per-path SHA-256 dumps (local `build/deep/`)
- Rebuild scripts (`.local-use-only/`)
