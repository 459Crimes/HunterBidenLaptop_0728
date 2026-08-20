# Glossary

> **Hatnote.** Terms of art in the 0728 encyclopedia. Tutorial: [Recovery tree for non-experts](05_recovery_tree_for_non_experts.md). Style: [Sourcing](MANUAL_OF_STYLE.md).

## 0728 / Extra Found Files

This corpus. Recovery-export tree, not a disk image. URI `0728://`.

## 459Crimes

Publisher. **Marc Aaron DeGiovanni**. See [Author](AUTHOR.md).

## Allocated / unallocated

Allocated space belongs to live filesystem objects on a **volume**. 0728 is not that volume. Hayes used “unallocated” / “white space” for deleted-file carving on R-00014. That account fails TRIM, file-aware copy, and L3 tests. APFS-matching hashes inside 0728 show many blobs also exist as **allocated** files on the indexed APFS tree. [Carving claim](HAYES_CARVING_CLAIM.md).

## TRIM / NVMe Deallocate

Host command telling an SSD that LBAs are unused. Apple SSDs TRIM by default. After deallocate, reads typically return **zeros**. Carving zeros recovers nothing. The original laptop was a **256 GB NVMe**.

## L3 (raw-surface / anchor sweep)

Parent-project full-file verification of 0728 byte ranges against raw APFS and GAI partition bytes (allocated, slack, unallocated). The APFS unallocated prototype found **158** distinct files / **~60 MiB** — not Extra Found Files. [Carving claim](HAYES_CARVING_CLAIM.md).

## APFS / APFS* / Hayes’s APFS / MPOLO / TODD

**APFS*** is the compressed image file `RHB_Boot.imgc`. Hayes sent it **directly** to this author over a **MEGA link on 13 June 2022**, the date stamped on the file (acquisition name `CJH20220613`). It is **not** a USB stick delivered to the author.

When that image is decompressed and analyzed, this encyclopedia calls it **APFS** or **Hayes’s APFS** (PostgreSQL source 1). The bytes inside are a CCC-expanded copy that once lived on a SanDisk Extreme; that describes **imaged media**, not the delivery channel.

**MPOLO** is Marco Polo’s claimed June 2021 Hayes **bootable laptop** — a different, reduced copy. **TODD** is the Sanders/Trimarco bootable hypothesis upstream of Hayes. None of these is 0728.

## Burst

~27-minute UTC window **2021-07-29 04:19:09–04:46:08** when a large fraction of 0728 paths were written in category bands.

## Exclusive hash

A SHA-256 present in 0728 and absent from a named comparison set (here: APFS ∪ GAI ∪ JPMI unless a caption says otherwise).

## GAI

Government Accountability Institute truncated HFS+ image. Hash-join target only.

## JPMI

John Paul Mac Isaac copy lineage (HFS+ `Untitled` / Crucial X6). Separate encyclopedia.

## Known File Types / Extra Found Files

R-Studio mode that dumps signature hits into type folders. The English folder names in this corpus match that dialect.

## Asset / informant / CHS

Three different labels. This encyclopedia keeps them apart.

| Term | Meaning here |
|---|---|
| **Asset** | Someone used **on and off** for help — not a badge, not payroll employment. Hayes’s R-00014 words: Homeland work; “I helped FBI on Backpage case”; “I come in and out”; “I'm not associated or affiliated.” That is **at least an asset**. Gloss of Hayes’s self-report, not a Bureau file label held here. |
| **Informant** | The word Peters’s lawyers used (Backpage / cartels / identity concealment). Also the word the prosecutor said the FBI **denied**. |
| **CHS** | Registered confidential human source. **Not** established. Hayes did not claim it. The FD-597 is not it. |

[Informant theory](INFORMANT_THEORY.md).

## MEGA

Cloud transfer used for the August 2021 0728 share (Hayes → Ziegler → author) and for **APFS*** (`RHB_Boot.imgc`, Hayes → author **13 June 2022**).

## R-00014

Recorder filename of the 17 April 2024 Hayes–DeGiovanni call.

## Synthetic name

Placeholder basename assigned by recovery software (`0442396.jpg`, `img_WxHxD_…`).

## Source bytes

The Extra Found Files objects under `source/recovered/`. Not in this GitHub tree.

## Trick / circular custody

Repeating recovery vocabulary (Ziegler iCloud/thumbnails; Byrne “the trick”; author “hack not involving the laptop”; Hayes unallocated carve). Graded lead, not a closed hash loop. [Circular custody](CIRCULAR_CUSTODY.md).

## Unmatched hash

A 0728 SHA-256 absent from indexed APFS, GAI, **and** JPMI. **94,635** such fingerprints. [Unmatched hashes](UNMATCHED_HASHES.md).
