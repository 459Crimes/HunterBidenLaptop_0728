# 2. 0728 Provenance — The 5 Ws and How

> **Encyclopedia.** [People](PEOPLE.md) · [Conan Hayes](CONAN_HAYES.md) · [Exhibits](EXHIBITS.md) · [Copy lineages](COPY_LINEAGES.md) · [Source matrix](09_source_matrix.md) · [Index](INDEX.md).

Provenance means the history and identity of evidence: **who handled it, what it is, when relevant events occurred, where those events occurred, why the copy exists, and how the copy was made or preserved.**

For 0728, some of those answers are established directly by the inventories. Others are known only at a broader historical level. A few remain unresolved.

## Who?

### Original content context

Many 0728 blobs **hash-match** files whose paths on APFS/JPMI/GAI sit under a `roberthunter` Mac home, Mail, Photos, or iPhone backup. That is **content identity**. It is not a statement that 0728 *is* that home directory.

### Alleged recovery operator

**Conan James Hayes** is the person Ziegler named as the **MEGA host** for Extra Found Files and the person who, in April 2024, described carving them from unallocated space.

### Immediate MEGA custodian to this project

**Garrett Ziegler** shared **Hayes’s download URL** in **August 2021**. He relayed the link; he did not originate the share. Older shorthand “received from Conan Hayes” or “Ziegler provided the MEGA share” **without** naming Hayes as upstream collapses the **two-hop** chain. This encyclopedia keeps the hops separate. [MEGA delivery](MEGA_DELIVERY.md).

### First known download

**Marc Aaron DeGiovanni** is the **first person known to download** from Hayes’s MEGA link. Whether anyone else downloaded earlier is **not** established here.

### Later forensic custody

This author / 459Crimes retained the tree under `source/recovered/` and indexed it as PostgreSQL source **2**. Known-good SAS twins of the 479,584-file Extra Found Files folder exist on staging/production volumes in the parent project; those are **byte-custody copies of the export**, not independent recoveries.

## What?

0728 is not a partitioned Mac storage environment.

It is a **directory tree** with:

- R-Studio-style type buckets;
- synthetic filenames;
- a small `Root/` of macOS installer/Spotlight crumbs;
- a small `Voice Memos/` set with 2018–2019 content dates;
- SHA-256 coverage for the canonical 480,039 paths.

The inventory presently contains **480,039** canonical paths and **317,319** distinct hashes.

## When?

There is no single “0728 date.” Different dates describe different events.

| Date / period | What the record reports | Evidentiary meaning |
|---|---|---|
| Years before 2019 | EXIF, voice-memo, and some preserved mtimes | Historical content can predate the export |
| April 2019 | Mac Shop recovery | Laptop-universe context; **not** the 0728 export date |
| May 2021 | Mesa County trusted build (Hayes) | Hayes forensic-imaging act on a **different** system |
| **2021-07-28 / 07-29** | Local stamp + UTC write burst (~177k paths in ~27 min) | **Materialization** of this tree |
| August 2021 | Ziegler shares Hayes’s MEGA link; author download (**first known**) | Project acquisition |
| **13 June 2022** | Hayes MEGA-sends APFS* (`RHB_Boot.imgc` image file) | Different object |
| 2022-09-13 | FBI FD-597 iPhone | Hayes/FBI contact; not 0728 hashing |
| 2024-04-17 | R-00014 carving statement | Participant method account |
| 2026 mtimes on ~267k paths | Working-copy / index stamps on this project’s disks | Handling, not 2021 recovery |

### The 2021/2026 mtime split

`files.mtime` for `0728/` is **not** a single clock. About **177,488** paths carry **2021** (the burst). About **266,664** carry **2026** (later copy or inventory on the working disks). A scatter of pre-2015, 2015–2020, and impossible future years are preserved or garbage timestamps from carves. See [Timestamps](TIMESTAMPS.md).

## Where?

The recovery **host** is unidentified. No Windows ADS / `desktop.ini` fingerprint is claimed. R-Studio is cross-platform. MEGA is a cloud drop. This author’s working copies live on `laptop.459.network` and known-good SAS mirrors. The **source volume Hayes scanned** is not in this GitHub tree.

## Why?

Hayes’s stated reason (R-00014) is that deleted material was **brought back to life** from white space. Ziegler’s reason for sharing was Marco Polo laptop research. This encyclopedia does not need a political motive to describe the tree.

## How?

**Observed:** signature-recovery folder layout; synthetic names; ordered category burst; dual hash behavior (allocated-file matches **and** unmatched hashes).

**Claimed (Hayes):** unallocated carve, possibly “a different partition,” with memory not refreshed on the exact structure.

**Not shown:** the `.rts` / R-Studio project, the input image hash, carve settings, or a map from 0728 path → disk offset.

Evaluation: [How the tree was written](R_STUDIO.md) · [Carving claim](HAYES_CARVING_CLAIM.md).
