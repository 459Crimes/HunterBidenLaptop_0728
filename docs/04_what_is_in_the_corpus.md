# 4. What is in the corpus

> **Encyclopedia.** Tables: [file-tree catalog](catalog/file_tree.md) · [Contents census](CONTENTS_CENSUS.md) · [Hash catalog](catalog/hash_manifest.md).

0728 is a **typed dump**, not a Mac user tree. Counts below use the canonical filter `source_id = 2` and `relative_path LIKE '0728/%'`.

## Top level

| Top-level | Paths | Distinct SHA-256 | Logical bytes |
|---|---:|---:|---:|
| Extra Found Files | 479,584 | 316,937 | 329,826,539,825 |
| Root | 422 | 381 | 6,397,917,523 |
| Voice Memos | 33 | 26 | 96,739,093 |
| **Total** | **480,039** | **317,319** | **336,321,196,441** |

`Root/` looks like macOS installer and Spotlight crumbs, not a live volume root. `Voice Memos/` is the rare bucket whose content dates look like **2018–2019 iPhone recordings** rather than recovery stamps.

## Extra Found Files categories

| Category | Paths | Distinct SHA-256 | Logical bytes |
|---|---:|---:|---:|
| Document | 281,530 | 205,136 | 7.24 GB |
| Graphics, Picture | 126,597 | 59,306 | 43.81 GB |
| Internet related files | 61,439 | 45,068 | 99.13 GB |
| Multimedia Video | 5,998 | 4,111 | 146.34 GB |
| Archive | 2,685 | 2,418 | 22.43 GB |
| Executable, Library, DLL | 460 | 266 | 1.53 GB |
| Development files | 427 | 319 | 10 MB |
| Multimedia Audio | 172 | 166 | 2.61 GB |
| Font | 121 | 78 | 5.33 GB |
| Multimedia | 81 | 19 | 110 MB |
| Document Spreadsheet | 49 | 25 | 0.9 MB |
| Other files | 13 | 13 | 50 MB |
| Disk images | 12 | 12 | 1.24 GB |

Byte mass lives in **video** and **“webarchive”** buckets. Row mass lives in **`.txt` documents**.

## Extensions (canonical tree)

| Extension | Paths | Distinct SHA-256 | Logical bytes |
|---|---:|---:|---:|
| txt | 277,390 | 202,416 | 4.88 GB |
| jpg | 91,277 | 43,675 | 33.08 GB |
| webarchive | 43,087 | 29,017 | 98.85 GB |
| png | 32,335 | 13,529 | 6.32 GB |
| xml | 17,813 | 15,556 | 0.28 GB |
| mp4 | 4,668 | 2,828 | 103.97 GB |
| pdf | 3,928 | 2,613 | 2.33 GB |
| vp6 | 1,323 | 1,276 | 42.37 GB |
| zip | 550 | 413 | 7.66 GB |
| tar | 294 | 294 | 12.14 GB |

Full table: [`02_extension_distribution.tsv`](../build/metadata/02_extension_distribution.tsv).

Many `.webarchive` objects are **mislabeled** Apple plist / CardDAV / NSKeyedArchive wrappers with trailing foreign data — a recovery-signature failure, not Safari’s on-disk format. That is interpretation grounded in parent-project unpack work; this encyclopedia does not re-unpack those bytes.

## Hash overlap with laptop-lineage primaries

| Join | Distinct SHA-256 |
|---|---:|
| 0728 total | 317,319 |
| also in APFS (source 1) | 205,262 |
| also in GAI (source 116) | 194,936 |
| also in JPMI (source 122) | 82,186 |
| any of those three | **222,684 (70.2%)** |
| none of those three | **94,635 (29.8%)** |

A 0728 hash that matches APFS is **the same bytes** as some file in Hayes’s APFS (`RHB_Boot.imgc` / APFS*). It is not proof the bytes were copied from that **13 June 2022** MEGA image (they could share an earlier common source). A 0728 hash that matches none of the three is **unexplained in those catalogs**.

Vs **all** other indexed `rhb_forensics` sources (including 0728 derivatives), an earlier report counted **82,883** exclusive hashes (26.1%). Derivative sources (webarchive copies, unpacks) shrink the exclusive set. Both numbers are useful; they answer different questions. See [Integrity](INTEGRITY.md).

## Naming

Most Extra Found Files basenames are **not** original. Of hashes shared with APFS/GAI, only a tiny set keep the same basename (parent project: on the order of **116**). Renaming is expected in Known File Types output.

## See also

- [Recovery tree for non-experts](05_recovery_tree_for_non_experts.md)
- [R-Studio](R_STUDIO.md)
- [Contents census](CONTENTS_CENSUS.md)
