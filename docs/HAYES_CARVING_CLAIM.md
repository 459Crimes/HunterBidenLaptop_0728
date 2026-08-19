# Hayes carving claim

> **Hatnote.** The method statement versus the inventory. Quotes: [R-00014](R00014_CALL.md). Tree: [R-Studio](R_STUDIO.md). Integrity: [Integrity](INTEGRITY.md).

## The statement

On 17 April 2024 Hayes said Extra Files were **deleted**, **carved**, **brought back to life**, floating in **unallocated / white space**, possibly on a **different partition**, and that he would have to **refresh his memory** on the exact structure.

No tool output was produced on the call. Parent-project follow-ups did not yield an R-Studio project or offset map.

## What would corroborate it

| Evidence | Status in this repo |
|---|---|
| R-Studio log naming the source disk | Missing |
| Hash of the source image *before* the scan | Missing |
| Offset list mapping 0728 files → unallocated ranges | Missing |
| Negative result: 0728-unique samples absent from APFS allocated **and** unallocated | Parent project: many unique samples **not** found in indexed APFS unallocated — which **cuts against** “carved from this APFS image’s free space,” not against carving some *other* medium |
| Mix of allocated-file hashes in the export | **Present** (205,262 APFS joins) — expected if the tool scanned a whole volume, not only free space |

## Fair reading

Hayes may have run a Known File Types scan against **some** laptop-lineage copy (or more than one medium) in July 2021. “Unallocated only” is **narrower** than what 0728 contains. “The June 2022 APFS image we now index” is **later** than July 2021 and **fails** as a sole source for the exclusive hashes and for JPMI∩0728 proxy populations that APFS/GAI catalogs lack.

Parent-project burst synthesis: **8,946** hashes in the July 2021 burst sit in JPMI∩0728 but not APFS/GAI, mapping overwhelmingly to Photos Library **proxy derivatives**. That is a custody constraint on “Hayes only had the APFS image later sent to the author.”

Kitchen-table rewrite of the unmatched remainder and the 27-minute dump: [Unmatched hashes](UNMATCHED_HASHES.md) · [July 28 burst](JULY_28_BURST.md) · [Stripped names](STRIPPED_NAMES.md).

## See also

- [Limits](07_limits_and_open_questions.md)
- [Copy lineages](COPY_LINEAGES.md)
- [Informant theory](INFORMANT_THEORY.md)
