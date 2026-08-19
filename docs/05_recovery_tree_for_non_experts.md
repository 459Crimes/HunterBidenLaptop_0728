# 5. Recovery tree for non-experts

> **Encyclopedia.** Companion: [R-Studio](R_STUDIO.md) · [Glossary](GLOSSARY.md) · [What is in the corpus](04_what_is_in_the_corpus.md).

A **disk image** is a byte-for-byte (or near-byte-for-byte) picture of a drive: partition table, filesystem, free space. **JPMI** and **APFS** are in that family (E01 / raw dd).

A **recovery export** is what happens when software *scans* media, recognizes file signatures (`FF D8 FF` for JPEG, and so on), and **writes new files** into folders named after those types. The new files get new names. Original folders are usually gone.

0728 is the second kind.

## What you should expect to see

| Feature | Live Mac copy | 0728 Extra Found Files |
|---|---|---|
| `Users/roberthunter/...` | Yes | No |
| Mail `.emlx` in `Library/Mail` | Yes (on the order of 128k on JPMI/APFS) | Scattered `.eml` / carves, not a Mail V6 store |
| Photos library package | Yes | JPEGs in `Graphics, Picture/` |
| CNID / APFS object ID | Yes | No |
| Category folders (`Document/Text Document`) | No | Yes |
| Names like `0442396.jpg` | Rare | Typical |

## Signature recovery in one paragraph

When a JPEG is deleted on a spinning disk, the bytes often remain until overwritten. Tools search for JPEG headers in that leftover space **and** in allocated files. They dump each hit as a new file. They do not reconstruct Finder paths. They frequently **over-match** (calling a plist a “webarchive”) and **under-match** (truncated files).

Hayes’s phrase “white space … no directory” is ordinary deleted-file talk. The **0728 tree still contains hundreds of thousands of hashes that also exist as allocated files** on APFS. Signature recovery of a *whole volume* (allocated + free) can produce that mix. A carve of *only* unallocated space on the *currently indexed* APFS image has not been shown to produce this tree. Parent-project unallocated searches are negative for many 0728-unique samples.

## Collision suffixes and malformed names

R-Studio writes `.Id_123` when two recovered objects would share a name. It writes long garbage names when a signature has no clean end marker. Both appear in Extra Found Files. They are **tool behavior**, not proof of forgery and not proof of authenticity.

## Unallocated ranges vs “deleted Hunter files”

On a live image, unallocated *ranges* are leftover capacity. They are not a count of recoverable user documents. 0728 is already an export of whatever the tool accepted as files. Treating 0728’s 313 GiB as “313 GiB of deleted Hunter files from the MacBook NVMe” skips every other hypothesis (other copies, other media, allocated-file recopy, cloud exports, mis-carves).

## See also

- [Carving claim](HAYES_CARVING_CLAIM.md)
- [Timestamps](TIMESTAMPS.md)
