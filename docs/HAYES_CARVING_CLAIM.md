# Hayes carving claim — technical demolition

> **Hatnote.** Audio: [`R-00014_0728_carving.mp3`](exhibits/audio/R-00014_0728_carving.mp3) (SHA-256 `2df257a7df2df14a6793a0287e6d9a1c5fa6267d60afd7199c996a07ea36b157`). Transcript: [`R-00014_excerpts.txt`](exhibits/audio/R-00014_excerpts.txt). This page is the **measured rebuttal**, not a polite paraphrase. Hayes’s unallocated-space story is **physically incompatible** with SSD TRIM, with Mac Isaac’s **file-aware** copy, with L3 raw-surface scans of **Hayes’s own APFS image** and of **GAI** (an HFS+ copy that **predates** the APFS bootable volume), and with the 0728 hash tables. R-Studio Known File Types explains **stripped names**. It does **not** prove the input was unallocated space of any drive.

## The one sentence

> **Conan Hayes told this author he carved Extra Found Files from deleted “white space” / unallocated space of the laptop.** Every material part of that description is false as an origin story for the SHA-256-unmatched remainder, and false as a description of how circulating laptop copies even *could* contain carveable unallocated bytes. The Extra Found Files **tree looks like R-Studio output** because someone ran (or copied) a Known File Types export. That is a **packaging** fact. It is not evidence that the bytes came from unallocated space.

## What he said (R-00014, 17 April 2024)

| Offset | Claim | Technical status |
|---|---|---|
| **00:20:29** | “those I carved from … they were deleted and I brought them back to life” | **False as corpus origin.** 205,262 of 0728’s hashes are **allocated** APFS files. Those objects were not deleted. The **94,635** hashes that match **none** of APFS, GAI, or JPMI are the files this encyclopedia is about — and they are **not** sitting in unallocated space of the disks Hayes later supplied or of GAI. |
| **00:22:55** | “carved … the white space … no directory … floats in the unallocated space” | **False as physics and as copy method.** On the original **256 GB NVMe**, TRIM/deallocate leaves nothing to carve. Mac Isaac’s April 2019 recovery was a **file-aware copy to a store server**, which **does not transfer unallocated LBAs**. A later R-Studio tree with fake names is what you get when you **scan files that already exist**, not proof the input was unstructured free space. |
| **00:23:37** | still partitioned; “a lot of like compression”; bringing them back “can get extra space”; “wasn’t maxed out at 256” | **Confused and capacity-incompatible.** Compression does not mint **94,635 new SHA-256 identities**. The July 2021 burst alone is **~295.76 GB logical** in ~27 minutes — larger than the **256 GB** SSD — while Hayes agreed live usage was “about 220, 230.” Leftover free space on that device cannot be both TRIM-zeroed **and** a 300 GB unique payload. |
| **00:24:03** | “when they’re in the unallocated space, it’s a **different partition**” | **Technically illiterate.** Unallocated space is **free allocation inside a volume**, not a spare partition full of Hunter Biden JPEGs. APFS/HFS+ do not hide a second “deleted-files partition.” |
| **00:20:51 / 00:24:03** | “I’d have to look”; “refresh my memory” | Consistent with a story that does not survive contact with the disks. |

Clip: [R-00014](R00014_CALL.md).

## 1. 256 GB NVMe + TRIM — there is nothing to carve after deallocate

Hunter Biden’s MacBook Pro (A1708, serial `FVFXC2MMHV29`) used an Apple **PCIe NVMe** blade. Nominal capacity in this project’s record: **256 GB**. Apple SSDs have **TRIM enabled by default** on the High Sierra-era OS that machine ran.

What TRIM/NVMe Deallocate does:

1. The filesystem marks extents free.
2. macOS **batches** deallocate and tells the SSD those LBAs are unused.
3. The controller **drops** those NAND pages from the valid map. Subsequent reads of trimmed LBAs on Apple/DRAT-class devices return **zeros** (or another deterministic empty pattern).
4. **Carving zeros recovers zeros.** There is no JPEG header in a TRIM’d LBA.

HDD folklore — “delete only removes the directory entry; the bytes sit in white space until overwritten” — is what Hayes recited at **00:22:55**. That is **spinning-disk, non-TRIM** talk. It is **not** how an Apple NVMe in 2018–2019 behaves after TRIM has flushed.

This project **does not hold** a `dd` of the original internal SSD. That gap does **not** rescue Hayes. Every **circulating** copy this encyclopedia can test was made **after** the shop recovery, by **file-aware** methods (next section), onto **other media**. Those copies never received the original NVMe’s unallocated map.

## 2. Mac Isaac file-aware copy — unallocated bytes were never in the pipeline

The repair-shop operation was **not** a sector clone of the NVMe.

JPMI encyclopedia (`BidenLaptop_JPMI`, [How the files left the laptop](https://github.com/459Crimes/BidenLaptop_JPMI/blob/main/docs/COPY_METHOD.md)):

- April 2019: data recovered onto Mac Isaac’s **store server**, then a customer drive.
- 26 September 2019: new HFS+ volume `Untitled`; **file-aware, timestamp-preserving copy** of the `roberthunter` home.
- Later: volume clone onto a Crucial X6 that **did not exist in 2019**.

A file-aware copy (`ditto` / Finder / similar) copies **named allocated files**. It does **not** copy:

- NVMe unallocated LBAs;
- file slack;
- TRIM-pending or TRIM-completed deallocate regions;
- APFS snapshot remnants unless those snapshots are themselves copied as files.

**Consequence.** Even if — contrary to TRIM physics — the original SSD still held deleted-file remnants in April 2019, **those remnants never left the laptop** via Mac Isaac’s method. Downstream copies (JPMI, GAI HFS+, TRIMARCO/Hayes APFS bootables) are **allocated-tree descendants**. You cannot “carve white space” of a copy that never received white space.

Hayes’s Extra Files story requires a **sector image of the original NVMe taken before TRIM emptied free LBAs**. No such image is in this project. The copies Hayes had are the **wrong class of object**.

## 3. R-Studio stripped the names. That is not “carved from unallocated.”

Extra Found Files **is** an R-Studio Known File Types **export tree**: type buckets, seven-digit IDs, `img_WxHxD_…`, `.Id_` collisions, ~27-minute category burst. [R-Studio](R_STUDIO.md) · [Stripped names](STRIPPED_NAMES.md) · [July 28 burst](JULY_28_BURST.md).

Known File Types does **not** require unallocated input. It will happily scan:

- a mounted volume of **live files**;
- a folder drop;
- a disk image’s **entire** byte range (allocated **and** free);
- several jobs merged into one Extra Found Files tree.

When the input is **already named files**, the tool still **throws away Finder paths** and writes recovery IDs. That is why 0728 hashes that **match APFS** almost never keep the original basename (parent-project: on the order of **116** shared hashes keep the same name).

**Stripped metadata is therefore evidence of the export mode, not of the source region.** Using R-Studio as a **laundry** — dump a mixed bag so nothing has a real path — is the opposite of Hayes’s “I resurrected deleted fragments from no-man’s-land.”

The mix inside the **same 27 minutes** is decisive:

- blobs whose SHA-256 **already exist as allocated files** on APFS/GAI/JPMI;
- blobs whose SHA-256 exist on **none** of those three.

Unallocated-only carving of one laptop SSD cannot emit **both** populations at scanner speed with labels stripped. That is a **merged, renamed dump**.

## 4. L3 raw-surface tests — Hayes’s APFS, and GAI before that APFS volume existed

SHA-256 catalogs test **indexed files**. L3 tests **raw partition bytes**: allocated files, slack, snapshots, free space, concatenated unallocated exports.

### APFS (the SanDisk Hayes later sent this author)

This is the disk Hayes’s story needs. If Extra Files were carved from “the laptop” he worked, **this is the candidate he actually delivered** (`RHB_Boot.imgc`, June 2022; CCC-family volume **12 Dec 2020**, snapshots **5 Jan 2021**).

Parent-project L3 / unallocated prototype on the APFS unallocated-byte concatenation (~154 GiB of exported free space; then-unmatched universe ~112k hashes):

| Stage | Result |
|---|---|
| L3 full-file occurrences | **185** hits |
| Distinct 0728 files | **158** |
| Verified bytes | **62,608,009** (~59.7 MiB) |

That is a **positive control** that the scanner works: a **tiny** subset of then-unmatched objects really did sit contiguously in APFS free space. It is **not** Extra Found Files. **59.7 MiB** is not **313 GiB**. **158** files are not **94,635** unmatched hashes.

Later full-surface work located additional byte-exact hits of formerly “unmatched” objects on APFS/GAI surfaces (including some unallocated). Those recoveries **shrink** the mystery pile. They do **not** convert Hayes’s dump into an unallocated carve of one 256 GB SSD. The **controlling remainder** of this encyclopedia — hashes still absent from APFS, GAI, **and** JPMI catalogs — is **94,635**. Those objects are **not** a substantial unallocated population on Hayes’s APFS image.

**Hayes’s own disk falsifies Hayes’s source claim.** If he carved Extra Files from that stick’s white space, L3 would have found the unmatched payload there. It did not, except a rounding-error residue.

### GAI (HFS+ copy that predates the APFS bootable)

**GAI** is a truncated **HFS+** image (`Biden Lap 2` / `hb.img`), not APFS. The TRIMARCO → Hayes **APFS** volume was created **12 December 2020**. GAI is an **earlier HFS+ lineage**. It cannot contain the later APFS container’s unallocated map because **that APFS filesystem did not exist yet**.

L3 / full-surface work on acquired GAI bytes likewise does **not** place a substantial unmatched-0728 payload in GAI unallocated (GAI is also truncated by ~300 GiB at the tail — a coverage gap, not a hidden 300 GiB of Extra Files). If Extra Files were “deleted laptop bytes floating in white space,” they would have had to survive:

1. TRIM on the NVMe;
2. file-aware shop copy (they wouldn’t);
3. an HFS+ copy made **before** the APFS bootable existed;
4. **and** Hayes’s later APFS image.

They survive **none** of those tests in bulk.

## 5. Capacity arithmetic Hayes walked into on the call

At **00:23:25–00:23:59** the author put the **256 GB SSD** on the table. Hayes agreed it “wasn’t maxed out”; the author said live fill was “about 220, 230.”

| Quantity | Value |
|---|---|
| Nominal internal SSD | **256 GB** |
| Hayes-agreed live fill | ~220–230 GB |
| Implied free on that device (if the numbers were about one disk) | ~26–36 GB |
| 0728 canonical logical | **336,321,196,441 bytes (~313.2 GiB)** |
| July 2021 burst logical | **295,759,259,827 bytes (~275.6 GiB)** |
| Distinct 0728 SHA-256 | **317,319** |
| Unmatched vs APFS ∪ GAI ∪ JPMI | **94,635** |

You cannot “bring back” ~276–313 GiB of unique logical output from ~30 GB of free space on a TRIM’d 256 GB NVMe. Hayes’s “compression … extra space … grow in size” (**00:23:37**) is not a recovery model. Inflating a carved file by decompressing it still requires the **compressed bytes** to have been on the medium. They were not, in bulk, on APFS unallocated, GAI unallocated, or any file-aware copy of the laptop.

## 6. Claim-by-claim map

| Hayes word | What it would require | What the measurements show |
|---|---|---|
| Deleted | Files absent from the live tree but present as remnants | 205,262 hashes are **live APFS files**; unmatched remainder is **not** in unallocated of APFS/GAI in any substantial amount |
| Brought back to life | Carve of residual user bytes | TRIM zeros; file-aware copies never had those bytes |
| White space / no directory | Source region with no catalog | R-Studio **output** has no catalog because Known File Types **discards** it |
| Unallocated space | Free extents on a volume that still hold old files | L3: ~60 MiB class residue on APFS unallocated prototype, not 0728 |
| Different partition | A second partition of deleted data | No such partition on APFS/GAI/JPMI maps |
| Compression / grow | Logical size > physical because of inflate | Does not create new SHA-256s absent from three catalogs; burst already exceeds the SSD |

## What this page does **not** claim

- that **zero** 0728 objects ever existed as a raw remnant anywhere (L3 found a **small** APFS-unallocated residue);
- that the original NVMe was `dd`’d and hashed here (it was not);
- that R-Studio was not used (the tree **is** that dialect);
- a named alternative source for every one of the 94,635 hashes.

It **does** claim: Hayes’s **process description** — Extra Files as deleted laptop bytes floating in unallocated / another partition, resurrected by carving — is **not** how the unmatched 0728 corpus was obtained, **not** how a 256 GB TRIM’d SSD works, **not** what a file-aware shop copy can contain, and **not** what L3 sees on the APFS disk he later sent or on GAI.

## See also

- [Unmatched hashes](UNMATCHED_HASHES.md)
- [Integrity](INTEGRITY.md)
- [July 28 burst](JULY_28_BURST.md)
- [Limits](07_limits_and_open_questions.md)
- [Copy lineages](COPY_LINEAGES.md)
- JPMI: [How the files left the laptop](https://github.com/459Crimes/BidenLaptop_JPMI/blob/main/docs/COPY_METHOD.md)
