# Stripped names and missing metadata

> **Hatnote.** Why Extra Found Files look like they fell out of a shredder and were taped into type folders.

## What a normal laptop file remembers

A file on APFS/JPMI typically has:

- a **human path** (`Users/roberthunter/Pictures/…/IMG_1234.JPG`);
- **filesystem times** (created/modified when the user or app wrote it);
- often **EXIF** (camera, GPS, original datetime).

## What 0728 usually has instead

R-Studio Known File Types **does not need** the catalog. It sees `FF D8 FF` (JPEG) and writes a new file:

```text
0728://Extra Found Files/Graphics, Picture/JPEG Image/0442396.jpg
```

or

```text
img_600x800x24_0424111.jpg
```

The number is a **recovery ID**, not Hunter’s album name. `.Id_4295402858` means “name collision.” Dimensions in the filename are **what the carver guessed**, not proof of a camera.

**EXIF** may survive inside the JPEG (some 0728 pictures still say iPhone X / GPS). **Filesystem timestamps** on the export are mostly **28–29 July 2021** or later **2026 copy** times — not “when the photo was taken.”

That combination — **original names gone, mixed EXIF, export-time mtimes** — is exactly what raw carving produces. It is also exactly what you would use if you wanted a pile of files that is **hard to map back** to a source disk without hashing.

## Same bytes, new name

When a 0728 hash **matches** APFS, the **content** is the laptop file and the **name** is not. Parent-project count: only on the order of **116** shared hashes keep the same basename. Renaming is the default.

When a 0728 hash **does not match**, you cannot even point to “this used to be `IMG_1234.JPG` on the Mac.” You only have a recovery ID and maybe EXIF.

## Why this is the 0728 problem

Hayes said the files “float in unallocated space” with “no directory.” The tree **agrees** that directories were not preserved **in the export**. That is Known File Types **output**. It is **not** proof the input was leftover free space: **205,262** hashes are allocated APFS files; L3 does not find a substantial unmatched payload in APFS or GAI unallocated; TRIM and the shop file-aware copy make original-NVMe unallocated a dead hypothesis. [Carving claim](HAYES_CARVING_CLAIM.md).

So:

- the tool scanned **already-named files** (and/or mixed jobs) and **stripped** the labels; or
- several media were **merged** into one Extra Found Files tree; or
- something else (cloud renditions, other copies) was poured in.

The **stripped names hide which is which** until you fingerprint. That is why SHA-256 overlap is the spine of this encyclopedia. [Unmatched hashes](UNMATCHED_HASHES.md) · [July 28 burst](JULY_28_BURST.md).
