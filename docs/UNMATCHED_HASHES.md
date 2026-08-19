# Unmatched hashes — files that are *not* on APFS, GAI, or JPMI

> **Hatnote.** Non-technical explanation of the 0728 remainder. Method: exact SHA-256. Tables: [hash catalog](catalog/hash_manifest.md). Images: [23-image exhibit](TWENTY_THREE_IMAGES.md). Burst: [July 28](JULY_28_BURST.md).

## The kitchen-table version

Imagine three photocopiers made copies of “the laptop”:

| Copier | Project name | What it is |
|---|---|---|
| Repair-shop lineage | **JPMI** | File list + hashes from Mac Isaac’s copy |
| Hayes’s APFS / APFS* | **APFS** | MEGA image `RHB_Boot.imgc`, sent **13 June 2022** |
| GAI’s drive | **GAI** | Truncated HFS+ image |

**SHA-256** is a fingerprint of the **exact bytes**. If two files have the same fingerprint, they are the same object (not “looks similar”).

0728 is a **fourth pile** of files with fake recovery names. We fingerprint every 0728 file and ask: does this fingerprint appear in JPMI, APFS, or GAI?

| Result | Distinct fingerprints | Share of 0728 |
|---|---:|---:|
| Yes — at least one of the three | **222,684** | 70.2% |
| **No — none of the three** | **94,635** | **29.8%** |

The **94,635** are the unmatched set. They are the reason this encyclopedia exists.

SQL (canonical):

```sql
-- 0728 hashes with no hash_sources row for APFS(1), GAI(116), or JPMI(122)
```

Published: [`04_coverage.tsv`](../build/hash_manifest/04_coverage.tsv).

## What “no match” does **not** mean

It does **not** automatically mean “from another person’s computer” or “from a live iCloud hack.” It means: **this exact byte object is not in the catalogs we have**.

A photo can fail SHA-256 and still be “the same picnic”:

- recompressed JPEG;
- cropped or resized;
- preview vs full resolution;
- carver glued two fragments;
- iCloud served a different rendition.

The **23-image exhibit** was built to show that mix: all 23 are SHA-256 negatives; **12** still have a visual/perceptual relationship to laptop-lineage pictures; **11** do not under the review rules. [23-image exhibit](TWENTY_THREE_IMAGES.md).

## How we got the three catalogs

| Source | What was compared | Gap |
|---|---|---|
| APFS / Hayes’s APFS | Live files in the decompressed `RHB_Boot.imgc` (source 1) | Not the MacBook’s internal NVMe; CCC-expanded external imaged as a **file**, delivered MEGA **2022-06-13** |
| GAI | Files on the truncated HFS+ image (source 116) | Missing ~300 GiB tail |
| JPMI | Reported hashes from the Mac Isaac metadata package (source 122) | Metadata/hash witness; not every E01 byte re-read here |

Parent-project work also unpacked APFS **archives**, iPhone **backups**, and Mail. Those joins **barely move** the unmatched pile (iPhone backups accounted for **16** tiny unmatched hashes). So “it’s just the phone backup” is false for the remainder.

## What the unmatched pile looks like

Not a mystery second iPhone model. Unmatched **images** mostly use cameras **already on the laptop** (iPhone 6s/7/X, etc.) — the **bytes** differ. The bulky unmatched types in earlier APFS-only notes were **webarchive**, **txt**, **jpg** with stripped names, **vp6**, large **mp4**.

**Stripped names** are the recovery-tool’s fingerprint: `0442396.jpg`, `img_600x800x24_0424111.jpg`. Original Finder paths are gone. That is expected for Known File Types output. Combined with the July 28 **burst**, it means: someone poured a huge mixed bag into new folders in about **27 minutes**, throwing away the filing cabinet labels. [Stripped names](STRIPPED_NAMES.md).

## Why “carved from unallocated” does not explain this pile

Hayes’s R-00014 account is the **named competing story** for these 94,635 hashes. It fails on four independent technical grounds:

1. **TRIM** on the original **256 GB NVMe** — deallocate returns zeros; carving zeros recovers nothing.
2. **File-aware shop copy** — Mac Isaac copied allocated files to a store server; unallocated LBAs never entered the circulating copies.
3. **L3 on Hayes’s APFS (APFS*)** — the **image file** he MEGA-sent this author on **13 June 2022** does not hold a substantial unmatched payload in unallocated space (~60 MiB class residue in the unallocated prototype vs ~313 GiB of 0728).
4. **L3 on GAI** — HFS+ lineage from **before** the 12 Dec 2020 APFS bootable volume existed; same absence of a substantial unallocated source.

R-Studio **did** strip filenames. That is how Known File Types **writes**. It is not evidence the **input** was white space. [Carving claim](HAYES_CARVING_CLAIM.md).

## Author’s investigative reading (labeled)

The FBI referral (28 Jul 2026) treated the unmatched + stripped + burst mix as a **substantial basis to investigate** unauthorized acquisition — not as a completed proof. This encyclopedia keeps that as **project identity**. [Integrity](INTEGRITY.md) · [Informant theory](INFORMANT_THEORY.md).

## See also

- [Contents census](CONTENTS_CENSUS.md)
- [Copy lineages](COPY_LINEAGES.md)
- [How to verify](08_reproducibility.md)
