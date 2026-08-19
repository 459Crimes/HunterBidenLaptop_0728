# Integrity (unknown-origin hashes, carving, referral)

> **Hatnote.** What 0728 reporting shows about **source mix**. Laptop-derived media (JPMI/APFS/GAI as filesystems) are **not** accused of hacking in the sibling JPMI encyclopedia. Unknown-origin **files** relative to those catalogs live **here**.

## Bounded finding

> **0728 is a mixed bag.** Exact SHA-256 matches tie **70.2%** of its hashes to at least one of APFS, GAI, or JPMI. **29.8%** (**94,635** hashes) match none of those three. Hayes’s R-00014 story — that Extra Files were **deleted laptop bytes carved from unallocated / white space** — is **physically and forensically false** as the origin of that remainder (TRIM on the 256 GB NVMe; file-aware shop copy; L3 negatives on Hayes APFS and on pre-APFS GAI). Unexplained hashes are still **not** a named intrusion. Takedown: [Carving claim](HAYES_CARVING_CLAIM.md).

“No named origin” ≠ “proved hacked.” “Matched APFS” ≠ “copied from the June 2022 SanDisk.”

## Where this sits next to JPMI

The JPMI encyclopedia attributes **no hacking** to JPMI or other **laptop-derived media**, and points at 0728 as the separate corpus that contains unknown-origin blobs. This encyclopedia **is** that corpus. It does not reverse the JPMI finding. It **localizes** the open attribution problem.

## Three layers

### 1. This repository’s overlap tables

`build/hash_manifest/04_coverage.tsv` — APFS 205,262; GAI 194,936; JPMI 82,186; union 222,684; complement 94,635.

### 2. Hayes’s method claim (rejected as origin)

R-00014 carving language is on tape. It does **not** survive TRIM physics, the file-aware copy chain, capacity arithmetic, or L3 scans of the APFS image Hayes later sent and of GAI. Missing R-Studio project logs are consistent with that: there is no offset map from unmatched 0728 files into unallocated ranges of those disks. [Carving claim](HAYES_CARVING_CLAIM.md).

### 3. Author FBI referral (28 July 2026)

DeGiovanni referred 0728 as **potentially hacked**. That is **project identity / advocacy**, citing stripped names and unmatched bytes. It is not an FBI conclusion and not a row in `04_coverage.tsv`.

## Frequent confusions

**“Most files hash-match the laptop, so 0728 is just the laptop.”**  
Most *hashes* match. A large *byte* remainder and 94,635 hashes do not. Synthetic names hide which is which until you join.

**“Unmatched hashes are iCloud hacks.”**  
Not established. Hypotheses include other copies not indexed, carver false positives, transcodes, truncated objects, and true external origin.

**“CBS said the laptop was clean, so 0728 is clean.”**  
CBS examined a Mac Isaac/FBI **exact-copy** lineage (JPMI family), not Extra Found Files.

## How the remainder was measured

Compare every distinct 0728 SHA-256 to indexed **APFS (source 1)**, **GAI (116)**, and **JPMI (122)**. A hit is **exact bytes**. A miss is the unmatched set. Unpacking APFS archives, iPhone backups, and Mail barely moves the miss pile. Non-technical write-up: [Unmatched hashes](UNMATCHED_HASHES.md). Teaching set: [23-image exhibit](TWENTY_THREE_IMAGES.md). Clocks: [July 28 burst](JULY_28_BURST.md). Names: [Stripped names](STRIPPED_NAMES.md).

The FBI-referral **analysis** (not the PDF) is rewritten into those articles. Human-side hypotheses that belong with the remainder: [Informant theory](INFORMANT_THEORY.md) · [Circular custody](CIRCULAR_CUSTODY.md).

## See also

- [Scope](SCOPE.md)
- [Limits](07_limits_and_open_questions.md)
- [Author](AUTHOR.md)
