# Extra Found Files (0728)

> This page is the **landing article** for the Extra Found Files corpus documented in this repository. Other laptop-data collections: [Scope](docs/SCOPE.md). How claims are labeled: [Sourcing and terminology](docs/MANUAL_OF_STYLE.md).

On the night of **28 July 2021**, a computer began pouring files into a tree that still has no securely identified beginning. The burst lasted **27 minutes** by the wall clock. Strip away its pauses and the active output occupies roughly **20 minutes**: **177,488 recovered paths**, **295.76 GB of logical data**, and **105,654 distinct SHA-256 values**, divided into eight machine-like surges. That is not a person tidying a folder. It is the footprint of a recovery operation, and the first question is the one the files cannot answer for themselves: **what was scanned, and who made this cache?**

The **0728 Extra Found Files** corpus (**0728**) is a **recovery-tool export tree**, not a disk image. It materialized around **28–29 July 2021** and reached this author in **August 2021**, when **Garrett Ziegler** shared a **MEGA link that Hayes had given him**. The attributed upstream operator, **Conan James Hayes**, has described prior on-and-off assistance to the FBI and Homeland Security, an asset-like relationship in his own account, though this repository does not establish that he was a registered FBI confidential human source. Hayes later said, on a recorded call, that he **carved** the Extra Files from **deleted / unallocated space**. That explanation is under test: [Hayes carving claim](docs/HAYES_CARVING_CLAIM.md).

The cache carries the marks of a process designed, by accident or by choice, to shed identity. R-Studio-style category folders replace an ordinary filesystem tree. Synthetic names stand where original names should be. The export preserves hundreds of gigabytes of bytes while withholding the source medium, the operator's project file, the selection decisions, and the route by which the material entered circulation. It may be the lossy residue of raw carving. It may reflect staging or repackaging. It may conceal more than it reveals. The evidence does not yet select among those explanations.

This GitHub repository is an **encyclopedia of that corpus**. It publishes tree identity, category inventories, SHA-256 overlap with other indexed sources, timestamps, and a sourced Hayes custody-and-method history. It does **not** publish the Extra Found Files bytes.

## Criminal referral chronology

> **Project identity.** These are **author submissions**, not FBI or DOJ findings. The referral PDF is **not** hosted in this GitHub tree. See [Author](docs/AUTHOR.md) · [Integrity](docs/INTEGRITY.md).

| When | Event | Class |
|---|---|---|
| **3 Jun 2024** | On a preserved call, the author told **Kevin Morris** (Hunter Biden’s attorney) that additional files received in 2021 were retrieved from **iCloud without authorization** | Participant statement (author) |
| **Before 28 Jul 2026** | Author filed an **electronic tip** to federal authorities | Author collection record |
| **28 Jul 2026** | **Criminal referral** on the 0728 corpus submitted to the **FBI and DOJ** (`FBI_0728_Source_Attribution_Referral_FINAL_2026-07-28.pdf`) | Author advocacy |
| **30 Jul 2026** | Author sent **Robert Hunter Biden** the **same criminal referral package** that went to DOJ (counsel copied) | Author collection record |

The formal referral followed counsel notice and the electronic tip. It requests preservation and source-attribution investigation of the July 2021 Extra Found Files tree — especially the **94,635** hashes that match none of APFS, GAI, or JPMI.

## 459Crimes — Hunter Biden laptop forensics catalog

Rolling public encyclopedias from **459Crimes / Marc Aaron DeGiovanni**. Each volume is a **separate GitHub repository** with its own scope, hash tables, and integrity finding. They are designed to be read together; SHA-256 joins are how the volumes connect.

| Volume | Repository | Primary object | Role in the matter |
|---|---|---|---|
| **0728** | **This repo** — [459Crimes/BidenLaptop_0728](https://github.com/459Crimes/BidenLaptop_0728) | Extra Found Files (Hayes-attributed R-Studio export, Jul 2021) | Recovery-export tree; **94,635** hashes match none of APFS, GAI, or JPMI |
| **JPMI** | [459Crimes/BidenLaptop_JPMI](https://github.com/459Crimes/BidenLaptop_JPMI) | Mac Isaac direct-copy lineage (Crucial X6 / `HB-IMAGE-2022-04-29.E01`) | Repair-shop HFS+ home; CBS-examined “exact copy” family |
| *(indexed, not yet encyclopedia)* | — | APFS bootable (`TRIMARCO` → `TODD` → `HAYES` / MPOLO / APFS*) | Hash-join target; Marco Polo’s bootable copy |
| *(indexed, not yet encyclopedia)* | — | GAI truncated HFS+ (`hb.img`) | Hash-join target |

**You are here:** 0728. For the Wilmington repair-shop copy and post-2019 custody, open **JPMI**. For how the lineages split and rejoin: [Copy lineages](docs/COPY_LINEAGES.md). Author inventory: [Author](docs/AUTHOR.md).

Other 459Crimes publications (not laptop encyclopedias): [*Beyond the Diary*](https://BeyondTheDiary.com) · [diary release](https://ShowersWithMy.Dad).

| | |
|---|---|
| **Lineage** | Hayes-attributed MEGA recovery export (R-Studio Known File Types tree) |
| **Stamp / burst** | 28 July 2021 local / **2021-07-29 04:19:09–04:46:08 UTC** (~27 minutes) |
| **Immediate provider (to this author)** | Garrett Ziegler relayed Hayes’s MEGA link (August 2021) |
| **Alleged upstream / method** | Conan James Hayes (MEGA host per Ziegler); R-00014 unallocated-carve claim **rejected** — [carving claim](docs/HAYES_CARVING_CLAIM.md) |
| **First known download** | Marc Aaron DeGiovanni (August 2021) |
| **Tree kind** | File-category folders + synthetic names — **not** a mounted Mac volume |
| **PostgreSQL** | `rhb_forensics` source **2** (`0728 Extra Files`) |
| **Canonical paths** | **480,039** under `0728://` — [file-tree catalog](docs/catalog/file_tree.md) |
| **Extra Found Files / Root / Voice Memos** | 479,584 / 422 / 33 |
| **Distinct SHA-256 / logical bytes** | **317,319** / **336,321,196,441** (~313.2 GiB) — [hash catalog](docs/catalog/hash_manifest.md) |
| **Overlap vs APFS ∪ GAI ∪ JPMI** | **222,684** hashes (70.2%) match at least one; **94,635** (29.8%) match none |
| **This tree contains** | Articles, exhibits, derived tables — **not** the 313 GiB source files |
| **Criminal referral** | Morris notice **3 Jun 2024** → electronic tip → FBI/DOJ **28 Jul 2026** → Hunter Biden same package **30 Jul 2026** | Project identity — [Author](docs/AUTHOR.md) |
| **Author** | **459Crimes / Marc Aaron DeGiovanni**. [Author](docs/AUTHOR.md) · [*Beyond the Diary*](https://BeyondTheDiary.com) · [diary release](https://ShowersWithMy.Dad) |

## Start here

| If you want… | Open |
|---|---|
| A one-page definition | [What is 0728?](docs/01_what_is_0728.md) |
| The custody story | [Chain of custody](docs/03_chain_of_custody.md) · [MEGA delivery](docs/MEGA_DELIVERY.md) |
| What is in the tree | [What is in the corpus](docs/04_what_is_in_the_corpus.md) · [Contents census](docs/CONTENTS_CENSUS.md) |
| Conan James Hayes | [Conan Hayes](docs/CONAN_HAYES.md) · [People](docs/PEOPLE.md) |
| The recorded call (three excerpts) | [R-00014 (17 Apr 2024)](docs/R00014_CALL.md) |
| Informant / Backpage / identity cover | [Informant theory](docs/INFORMANT_THEORY.md) |
| Files with no GAI / APFS / JPMI hash | [Unmatched hashes](docs/UNMATCHED_HASHES.md) · [July 28 burst](docs/JULY_28_BURST.md) |
| Why Hayes’s unallocated-carve story fails | [Carving claim](docs/HAYES_CARVING_CLAIM.md) |
| Ziegler · Byrne · “the trick” | [Circular custody](docs/CIRCULAR_CUSTODY.md) |
| Dates and later handling | [Timeline](docs/TIMELINE.md) · [Integrity](docs/INTEGRITY.md) |
| Every article | [Article index](docs/INDEX.md) |
| The TSV / report files | **[Evidence catalog](docs/catalog/README.md)** |
| Diagrams | [Diagrams](docs/diagrams/README.md) |

## Lead finding

The 0728 reporting shows a **signature-recovery export**: R-Studio-style category folders, seven-digit placeholder names, a high-rate **July 2021** write burst, and a bag of blobs that **both matches and fails to match** the three primary laptop-lineage inventories (APFS, GAI, JPMI).

Hayes’s R-00014 claim that Extra Files were **deleted laptop bytes carved from unallocated / white space** does **not** survive: **TRIM** on the original **256 GB NVMe**; Mac Isaac’s **file-aware** copy (unallocated LBAs never left the laptop); L3 raw-surface scans of **Hayes’s own APFS image** and of **GAI** (HFS+ from **before** that APFS volume existed). R-Studio explains **stripped names**. It does not prove an unallocated source. [Hayes carving claim](docs/HAYES_CARVING_CLAIM.md).

> **0728 is not a clone of JPMI, APFS, or GAI.** Shared hashes prove shared content identity. **94,635** hashes (29.8%) match **none** of those three catalogs. Unexplained ≠ named external origin. The unmatched remainder, stripped names, and 27-minute dump are this encyclopedia’s integrity problem. [Unmatched hashes](docs/UNMATCHED_HASHES.md).

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
| **Aug 2021** | Ziegler shared **Hayes’s MEGA link** with the author; author is **first known downloader**; Ziegler attributed Hayes and (author recollection) described an iCloud/thumbnail “trick”. | Author collection · [MEGA delivery](docs/MEGA_DELIVERY.md) · [Circular custody](docs/CIRCULAR_CUSTODY.md) |
| **13 Jun 2022** | Hayes sent this author **APFS*** — the image file `RHB_Boot.imgc` — over MEGA (file datestamp). When analyzed: **APFS** / Hayes’s APFS. **Not 0728.** | Author receipt |
| **13 Sep 2022** | FBI Form **FD-597**: Hayes black iPhone “Received From”; SA **Calum Ramm** (Dallas). | Photographed FBI form — [Exhibits](docs/EXHIBITS.md) |
| **8 Apr 2022** | Byrne Locals: ~400k “deleted” files; “**the trick**”; author screenshot of Extra Found Files (473,580) and “hack **not involving the laptop**”. | Archived stream + chat · [Byrne](docs/PATRICK_BYRNE.md) |
| **17 Apr 2024** | Recorded call **R-00014** (excerpts): Trump/Mar-a-Lago; Extra Files carving; FBI/Backpage. | Audio exhibit |
| **3 Jun 2024** | Preserved call: author told **Kevin Morris** that 2021 additional files came from **unauthorized iCloud retrieval**. | Participant statement — [Author](docs/AUTHOR.md) |
| **4 Aug 2024** | Hayes signs **affidavit** (*Declaration of Conan James Hayes*: cartels, alternative identities, voting-equipment access). Photo **13 Aug**. | Photographed signed affidavit — [Informant theory](docs/INFORMANT_THEORY.md) |
| **Aug 2024** | Tina Peters trial; informant theory excluded; prosecutor said FBI confirmed Hayes was never an informant. | Court / contemporaneous journalism |
| **Before 28 Jul 2026** | Author filed an **electronic tip** to federal authorities. | Author collection record |
| **28 Jul 2026** | **Criminal referral** on 0728 submitted to **FBI and DOJ**. | Project identity — [Author](docs/AUTHOR.md) |
| **30 Jul 2026** | Author sent **Hunter Biden** the **same referral package** sent to DOJ. | Author collection record |

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

**Companions:** [Author](docs/AUTHOR.md) · [People](docs/PEOPLE.md) · [Conan Hayes](docs/CONAN_HAYES.md) · [Informant theory](docs/INFORMANT_THEORY.md) · [Patrick Byrne](docs/PATRICK_BYRNE.md) · [Todd Sanders](docs/TODD_SANDERS.md) · [Jack Maxey](docs/JACK_MAXEY.md) · [Garrett Ziegler](docs/GARRETT_ZIEGLER.md) · [Circular custody](docs/CIRCULAR_CUSTODY.md) · [Unmatched hashes](docs/UNMATCHED_HASHES.md) · [July 28 burst](docs/JULY_28_BURST.md) · [iPhone backup password](docs/IPHONE_BACKUP_PASSWORD.md) · [R-00014 call](docs/R00014_CALL.md) · [Phone seizure](docs/PHONE_SEIZURE.md) · [Tina Peters](docs/TINA_PETERS.md) · [Exhibits](docs/EXHIBITS.md) · [MEGA delivery](docs/MEGA_DELIVERY.md) · [R-Studio tree](docs/R_STUDIO.md) · [Carving claim](docs/HAYES_CARVING_CLAIM.md) · [Copy lineages](docs/COPY_LINEAGES.md) · [Diagrams](docs/diagrams/README.md) · [Timestamps](docs/TIMESTAMPS.md) · [Integrity](docs/INTEGRITY.md) · [Glossary](docs/GLOSSARY.md) · **[full index](docs/INDEX.md)**

---

**Categories:** 0728 · Extra Found Files · Conan James Hayes · MEGA recovery export · metadata/hash witness
