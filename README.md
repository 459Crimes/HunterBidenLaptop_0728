# Extra Found Files (0728)

> This page is the **landing article** for the Extra Found Files corpus documented in this repository. Other laptop-data collections: [Scope](docs/SCOPE.md). How claims are labeled: [Sourcing and terminology](docs/MANUAL_OF_STYLE.md).

The **0728 Extra Found Files** corpus (**0728**) is one evidence lineage in the Hunter Biden laptop matter: a **recovery-tool export tree**, not a disk image, materialized around **28–29 July 2021**, delivered to this author in **August 2021** via a **MEGA** link from **Garrett Ziegler**, who attributed the files to **Conan James Hayes**. Hayes later said, on a recorded call, that he **carved** the Extra Files from **deleted / unallocated space**.

This GitHub repository is an **encyclopedia of that corpus**. It publishes tree identity, category inventories, SHA-256 overlap with other indexed sources, timestamps, and a sourced Hayes custody-and-method history. It does **not** publish the Extra Found Files bytes.

| | |
|---|---|
| **Lineage** | Hayes-attributed MEGA recovery export (R-Studio Known File Types tree) |
| **Stamp / burst** | 28 July 2021 local / **2021-07-29 04:19:09–04:46:08 UTC** (~27 minutes) |
| **Immediate provider** | Garrett Ziegler (MEGA, August 2021) |
| **Alleged upstream / method** | Conan James Hayes; carving claim on **R-00014** (17 April 2024) |
| **Tree kind** | File-category folders + synthetic names — **not** a mounted Mac volume |
| **PostgreSQL** | `rhb_forensics` source **2** (`0728 Extra Files`) |
| **Canonical paths** | **480,039** under `0728://` — [file-tree catalog](docs/catalog/file_tree.md) |
| **Extra Found Files / Root / Voice Memos** | 479,584 / 422 / 33 |
| **Distinct SHA-256 / logical bytes** | **317,319** / **336,321,196,441** (~313.2 GiB) — [hash catalog](docs/catalog/hash_manifest.md) |
| **Overlap vs APFS ∪ GAI ∪ JPMI** | **222,684** hashes (70.2%) match at least one; **94,635** (29.8%) match none |
| **This tree contains** | Articles, exhibits, derived tables — **not** the 313 GiB source files |
| **Author** | **459Crimes / Marc Aaron DeGiovanni**. [Author](docs/AUTHOR.md) · [*Beyond the Diary*](https://BeyondTheDiary.com) · [diary release](https://ShowersWithMy.Dad) |

## Start here

| If you want… | Open |
|---|---|
| A one-page definition | [What is 0728?](docs/01_what_is_0728.md) |
| The custody story | [Chain of custody](docs/03_chain_of_custody.md) · [MEGA delivery](docs/MEGA_DELIVERY.md) |
| What is in the tree | [What is in the corpus](docs/04_what_is_in_the_corpus.md) · [Contents census](docs/CONTENTS_CENSUS.md) |
| Conan James Hayes | [Conan Hayes](docs/CONAN_HAYES.md) · [People](docs/PEOPLE.md) |
| The recorded call | [R-00014 (17 Apr 2024)](docs/R00014_CALL.md) |
| Dates and later handling | [Timeline](docs/TIMELINE.md) · [Integrity](docs/INTEGRITY.md) |
| Every article | [Article index](docs/INDEX.md) |
| The TSV / report files | **[Evidence catalog](docs/catalog/README.md)** |
| Diagrams | [Diagrams](docs/diagrams/README.md) |

## Lead finding

The 0728 reporting shows a **signature-recovery export**: R-Studio-style category folders, seven-digit placeholder names, a high-rate **July 2021** write burst, and a bag of blobs that **both matches and fails to match** the three primary laptop-lineage inventories (APFS, GAI, JPMI).

It does **not** presently show a tool log, source-volume hash, or byte-offset map that would independently prove Hayes’s statement that the tree was carved only from unallocated space of the currently indexed APFS image.

> **0728 is not a clone of JPMI, APFS, or GAI.** Shared hashes prove shared content identity. Exclusive hashes are unexplained relative to those three catalogs. Unexplained ≠ named external origin.

Row-level overlap: [hash catalog](docs/catalog/hash_manifest.md) (`04_coverage.tsv`). Method claim: [Hayes carving claim](docs/HAYES_CARVING_CLAIM.md).

## What 0728 is

0728 is a **file tree**, not a hand-picked folder of documents and not a forensic E01.

```text
0728://
├── Extra Found Files/     479,584 paths, ~307 GiB
│     Document/            281,530
│     Graphics, Picture/   126,597
│     Internet related files/  61,439   (incl. ~43k “webarchive”)
│     Multimedia Video/    5,998        (~136 GiB)
│     Archive/             2,685
│     … other R-Studio type buckets
├── Root/                  422 paths (Spotlight / installer crumbs)
└── Voice Memos/           33 paths (2018–2019 content dates)
```

Most basenames are **synthetic**. Exact-hash matches to laptop-lineage files almost never keep the original filename. That is a recovery-mode property.

- Tooling: [R-Studio tree](docs/R_STUDIO.md) · [Filesystem for non-experts](docs/05_recovery_tree_for_non_experts.md)
- Other copies that are **not** this tree: [Copy lineages](docs/COPY_LINEAGES.md)

## Historical timeline

Full sourced narrative: [Timeline and handling](docs/06_timeline_and_handling.md). Claim-by-claim sources: [Source matrix](docs/09_source_matrix.md). Compact list: [Timeline (index)](docs/TIMELINE.md).

| When | What | Evidence class |
|---|---|---|
| **12–13 Apr 2019** | Mac Shop recovery (Wilmington). **Not** the 0728 export. | Court record — JPMI encyclopedia |
| **May 2021** | Mesa County trusted build: Hayes used Gerald Wood’s badge; imaged elections server. | Court-recited |
| **Jun 2021** | Marco Polo claimed receipt of a Hayes **bootable laptop** (**MPOLO**). Separate from 0728. | Marco Polo v4 |
| **28–29 Jul 2021** | 0728 tree materialized (local stamp 28 Jul; UTC burst ~27 min). | Direct 0728 mtime / burst analysis |
| **Aug 2021** | Author downloaded the MEGA share from **Ziegler**. | Author collection record |
| **13 Jun / 22 Jun 2022** | Hayes sent this author the APFS image (`RHB_Boot.imgc`) via MEGA. **Not 0728.** | Author receipt |
| **13 Sep 2022** | FBI Form **FD-597**: Hayes black iPhone “Received From”; SA **Calum Ramm** (Dallas). | Photographed FBI form — [Exhibits](docs/EXHIBITS.md) |
| **17 Apr 2024** | Recorded call **R-00014**: Hayes describes carving Extra Files from unallocated space. | Audio exhibit |
| **Aug 2024** | Tina Peters trial; informant theory excluded; prosecutor said FBI confirmed Hayes was never an informant. | Court / contemporaneous journalism |
| **28 Jul 2026** | Author FBI referral on 0728 as potentially hacked. | Project identity — [Author](docs/AUTHOR.md) |

## What is in the tree

The inventory contains **480,039** paths and **317,319** distinct SHA-256 values. Tables: [file-tree catalog](docs/catalog/file_tree.md).

| Category (Extra Found Files) | Paths | Distinct SHA-256 | Logical bytes |
|---|---:|---:|---:|
| `Document` | 281,530 | 205,136 | 7.24 GB |
| `Graphics, Picture` | 126,597 | 59,306 | 43.8 GB |
| `Internet related files` | 61,439 | 45,068 | 99.1 GB |
| `Multimedia Video` | 5,998 | 4,111 | 146.3 GB |
| `Archive` | 2,685 | 2,418 | 22.4 GB |

By extension, `.txt` dominates **count**; `.mp4` and `.webarchive` dominate **bytes**. Unmatched content is a **row-count minority but a byte majority**. See [Contents census](docs/CONTENTS_CENSUS.md).

## Evidence tables

Machine-readable appendix under `build/`. **Start with the catalogs**, then open the TSV:

| Catalog | Folder |
|---|---|
| [Corpus identity](docs/catalog/corpus_info.md) | `build/corpus_info/` |
| [File tree](docs/catalog/file_tree.md) | `build/file_tree/` |
| [Hash manifest](docs/catalog/hash_manifest.md) | `build/hash_manifest/` |
| [Metadata](docs/catalog/metadata.md) | `build/metadata/` |
| [Reports](docs/catalog/reports.md) | `build/reports/` |
| [Exhibits](docs/catalog/exhibits.md) | `docs/exhibits/`, R-00014 audio, FBI photos |

Checksum inventory: [`build/manifest.tsv`](build/manifest.tsv). How to check those files: [How to verify](docs/08_reproducibility.md).

## How to read this encyclopedia

Every public claim is traceable to 0728 path/hash/mtime reporting; a court opinion or pleading; an attributed participant account (including the R-00014 recording); a photographed FBI form; an independent news report; or a sourced public-record link.

> **Observed fact → interpretation → limitation**

Court-recited Mesa County facts, Hayes’s later technical account, 0728-internal measurements, and Ziegler’s MEGA handoff are **not interchangeable**. The [source matrix](docs/09_source_matrix.md) is the claim index.

## All articles

**Numbered narrative** (stable IDs):

1. [What is 0728?](docs/01_what_is_0728.md)
2. [Provenance — 5 Ws](docs/02_provenance_5ws.md)
3. [Chain of custody](docs/03_chain_of_custody.md)
4. [What is in the corpus](docs/04_what_is_in_the_corpus.md)
5. [Recovery tree for non-experts](docs/05_recovery_tree_for_non_experts.md)
6. [Timeline and handling](docs/06_timeline_and_handling.md)
7. [Limits and open questions](docs/07_limits_and_open_questions.md)
8. [How to verify](docs/08_reproducibility.md)
9. [Source matrix](docs/09_source_matrix.md)

**Companions:** [Author](docs/AUTHOR.md) · [People](docs/PEOPLE.md) · [Conan Hayes](docs/CONAN_HAYES.md) · [R-00014 call](docs/R00014_CALL.md) · [Phone seizure](docs/PHONE_SEIZURE.md) · [Tina Peters](docs/TINA_PETERS.md) · [Exhibits](docs/EXHIBITS.md) · [MEGA delivery](docs/MEGA_DELIVERY.md) · [R-Studio tree](docs/R_STUDIO.md) · [Carving claim](docs/HAYES_CARVING_CLAIM.md) · [Copy lineages](docs/COPY_LINEAGES.md) · [Diagrams](docs/diagrams/README.md) · [Timestamps](docs/TIMESTAMPS.md) · [Integrity](docs/INTEGRITY.md) · [Glossary](docs/GLOSSARY.md) · **[full index](docs/INDEX.md)**

---

**Categories:** 0728 · Extra Found Files · Conan James Hayes · MEGA recovery export · metadata/hash witness
