# Sourcing and terminology

> **Hatnote.** How this encyclopedia labels evidence. It is not a court opinion and not a filesystem measurement. See also [Source matrix](09_source_matrix.md) and [Scope](SCOPE.md).

This repository is written so a technically literate reader can audit it like a Wikipedia article: **lead, sources, infobox facts, limitations, see-also**. Contested politics are not edited into the lead. The publication covers **one corpus**, with labeled evidence classes.

## The one question

> **What does the 0728 Extra Found Files corpus itself show, and what does the Conan James Hayes record attached to it show?**

Comparative analysis of other laptop datasets belongs in a different project ([Scope](SCOPE.md)), except where SHA-256 overlap is published as a named join.

## Evidence classes

These classes are kept distinct:

| Class | Typical sources | Attribution |
|---|---|---|
| **Direct 0728 report** | [Evidence catalog](catalog/README.md) (`build/file_tree`, hashes, extensions, mtimes) | “0728 reports…” / “the inventory contains…” |
| **Court-recited** | Colorado trial / *People v. Peters*, 24CA1951 | “The court recounts…” |
| **Complaint allegation** | Pleadings in laptop-adjacent civil cases | Pleading language; not an affidavit |
| **Contemporaneous journalism** | CPR, Colorado Sun, Colorado Newsline, LA Times | Named reporter observation or attributed quote |
| **Participant account** | R-00014 call; Ziegler MEGA attribution; Hayes Signal | “Hayes said…” / “Ziegler’s account…” |
| **Photographed federal form** | FD-597, Ramm card, warrant excerpt | “The photographed form shows…” — not a certified copy |
| **Comparative inventory** | APFS/GAI/JPMI rows in `rhb_forensics` | Cite source_id; do not call the row `0728://` |
| **Independent forensic** | Parent-project unallocated scans, CBS (JPMI lineage) | Separate attribution |
| **Interpretation** | R-Studio Known File Types knowledge | “Consistent with…” rather than “proves Hayes sat at…” |
| **Inference** | Two-hop MEGA vs older “from Hayes” shorthand | Labeled as inference |
| **Project identity** | [Author](AUTHOR.md); FBI 0728 referral | Who published this repo. Distinct from SHA-256 tables |

## The three-layer sentence

**Observed fact → interpretation → limitation** appear as adjacent sentences.

Example:

> 0728 reports **94,635** distinct SHA-256 values with no exact match in APFS (source 1), GAI (116), or JPMI (122). That is unexplained relative to those three catalogs. It is not, by itself, a named source (iCloud hack, third laptop, or planted dump).

The sentence “Hayes hacked Hunter Biden’s iCloud and stuffed the results into Extra Found Files” is not supported by that row.

## Claims not established by the present record

The following are **not** findings of this encyclopedia:

- that 0728 is a sector copy of the MacBook internal SSD;
- that 0728 was carved from the June 2022 APFS image as now indexed;
- that every unmatched hash is non-laptop in origin;
- that Hayes was a registered FBI confidential informant;
- that the 13 Sep 2022 iPhone event was caused by a call with Donald Trump;
- that Ziegler’s MEGA folder is byte-identical to Hayes’s working tree;
- that Marco Polo analyzed the JPMI / Della Rocca copy (it used MPOLO + 0728);
- that the FBI referral of 28 July 2026 is an FBI finding;
- that every timestamp is a 2021 recovery event (2026 working-copy mtimes exist);
- that synthetic names imply the bytes are fake.

Integrity wording used in the articles is in [Integrity](INTEGRITY.md).

## Names and abbreviations

| Term | Meaning in this repo |
|---|---|
| **0728 / Extra Found Files** | This recovery-export corpus. Not from the laptop files *per se* as a filesystem extract |
| **JPMI** | John Paul Mac Isaac **copy lineage** (separate encyclopedia) |
| **APFS** | TRIMARCO→Hayes bootable SanDisk family (`HB Boot Drive`). Sibling, not this tree |
| **APFS*** | Jun 2022 Hayes `RHB_Boot.imgc` to this author |
| **GAI** | Government Accountability Institute truncated HFS+ image (`hb.img`) |
| **MPOLO** | Marco Polo’s claimed Jun 2021 Hayes **bootable laptop**, not 0728 |
| **R-00014** | 17 April 2024 recorded call, Hayes and DeGiovanni |
| **Source bytes** | Contents of `source/recovered/`; **not** in this GitHub tree |

Articles expand 0728 on first use.

## Source URIs

| Scheme | Copy |
|---|---|
| `0728://` | This corpus (canonical `0728/` inventory prefix) |
| `JPMI://` | Mac Isaac direct-copy lineage |
| `APFS://` | TRIMARCO→APFS bootable family |
| `GAI://` | GAI truncated HFS+ |

Example: `0728://Extra Found Files/Graphics, Picture/JPEG Image/0442396.jpg`. Do not cite a JPMI, APFS, or GAI path as if it were a 0728 inventory row.

## Counts

Path count, distinct SHA-256, and “unique human documents” are different quantities. PostgreSQL source 2 also stores a duplicate `source/` prefix. Public tables use `0728/`. See [Contents census](CONTENTS_CENSUS.md).

## Photographs and personal data

FBI-form photographs are **custody exhibits**. Captions record what the paper shows. This encyclopedia describes **structure and provenance**; it is not a gallery of Extra Found Files user content.

## See also

- [Source matrix](09_source_matrix.md)
- [Limits](07_limits_and_open_questions.md)
- [How to verify](08_reproducibility.md)
- [Evidence catalog](catalog/README.md)
