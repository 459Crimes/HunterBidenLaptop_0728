# July 28, 2021 — the 27-minute dump

> **Hatnote.** What the clocks on Extra Found Files actually show. Numbers from the parent-project burst audit (rewritten, not copied). Non-technical first.

## Kitchen-table version

On the evening of **28 July 2021** (UTC−6) / morning of **29 July 2021 UTC**, a computer wrote **177,488** files in about **27 minutes**. That is not a person dragging folders in Finder for a month. It is a **machine burst**: recovery software (or a copy of its output) stamping a finished pile.

Think of a high-speed scanner that:

1. does **not** keep original folder names;
2. dumps JPEGs into `Graphics, Picture/`, videos into `Multimedia Video/`, and so on;
3. pauses a few times (eight “batches” if you split on 15-second gaps);
4. finishes so fast that, **if** you naively treated every byte as unique payload off one disk, the implied rate (**~248 MB/s**) is faster than a typical gigabit Ethernet pipe and larger than a **256 GB** laptop SSD.

Those last comparisons are **warnings**, not a measured network speed. Duplicate paths, overlapping carves, and one-second timestamp buckets inflate “logical bytes.”

## Controlling measurements

| Measure | Value |
|---|---|
| UTC window | **2021-07-29 04:19:09 – 04:46:08** |
| UTC−6 rendering | 28 Jul 2021 **22:19:09 – 22:46:08** |
| Paths in window | **177,488** |
| Distinct SHA-256 | **105,654** |
| Logical bytes | **295,759,259,827** (~295.76 GB) |
| Batches (≥15 s idle split) | **8** |
| Batch-span seconds | **1,193** (427 s idle between batches) |
| Logical rate (batch span) | **~247.91 MB/s** |

The burst is **inside** 0728; it is not the whole 480,039-path tree. Other files have 2026 working-copy mtimes or preserved content dates. [Timestamps](TIMESTAMPS.md).

## Eight batches (for the curious)

| Batch | UTC | Paths | Logical bytes |
|---:|---|---:|---:|
| 1 | 04:19:09–04:20:42 | 7,015 | 26.0 GB |
| 2 | 04:25:02–04:33:36 | 124,525 | 61.5 GB |
| 3 | 04:33:57–04:35:57 | 20,123 | 36.5 GB |
| 4 | 04:36:19–04:36:29 | 123 | 9.9 GB |
| 5 | 04:36:57–04:39:08 | 22,083 | 38.8 GB |
| 6 | 04:39:40–04:42:25 | 2,028 | 57.5 GB |
| 7 | 04:43:13 | 1 | 14.2 GB |
| 8 | 04:43:36–04:46:08 | 1,590 | 51.4 GB |

Categories were written in **bands** (archives, then documents, then pictures, then video). That is R-Studio walking type buckets — or a copy of such a tree.

## Why this matters for unmatched files

The **same 27 minutes** contain:

- blobs whose SHA-256 **already exist** on APFS/GAI/JPMI (laptop-related content, new fake names);
- blobs whose SHA-256 exist on **none** of those three.

If Extra Files were “only deleted Hunter files from one laptop SSD,” you would not expect a **mixed** bag at scanner speed with **labels stripped**. You would also not expect logical volume **above** the nominal 256 GB internal drive. Those are **investigative constraints**, not a completed reconstruction of Hayes’s desk. [Unmatched hashes](UNMATCHED_HASHES.md) · [Stripped names](STRIPPED_NAMES.md) · [Carving claim](HAYES_CARVING_CLAIM.md).

## What we do not conclude from the rate

- that a gigabit download happened;
- that eight R-Studio jobs were clicked;
- that 28 July is the date of an intrusion (it is the date of **this output**).

## See also

- [R-Studio](R_STUDIO.md)
- [Integrity](INTEGRITY.md)
