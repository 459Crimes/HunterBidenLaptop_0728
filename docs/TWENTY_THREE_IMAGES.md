# The 23-image exhibit (Lead Exhibit A)

> **Hatnote.** Wikipedia-style rewrite of the FBI-report image analysis. **Not a copy of the referral PDF.** No source-image bytes are hosted here. The exhibit itself lives in the parent project’s `output/pdf/fbi_image_exhibit_23/` package.

## Why 23 pictures?

There are **94,635** unmatched hashes. Nobody can start an investigation by staring at all of them. Investigators picked **23 JPEGs** from unmatched **graphics** using a category-balanced score (not a random poll, not a probability).

All 23 fail **exact SHA-256** against indexed **APFS, GAI, and JPMI**. Then each was asked a friendlier question: *is there still a related picture on the laptop copies?*

| Finding | Count |
|---|---:|
| Exact-byte negative vs APFS/GAI/JPMI | **23 / 23** |
| Some image-level relationship to a primary (looks like the same photo/session) | **12** |
| No similar primary image under the review rules | **11** |
| Camera-roll / scene / burst continuity | 9 |
| Same session, different frame | 3 |
| Only 0728-internal context | 9 |
| Content-era timestamps (not July 2021 export time) | 21 |
| Filesystem times inside the July burst | 2 |

**Do not** scale 12/23 to all 94,635 hashes. The 23 are a **teaching set**.

## Four different “sames”

Keep these apart (this is the whole exhibit):

1. **Same bytes** — SHA-256. Failed for all 23.
2. **Same decoded picture** — perceptual hashes (pHash/dHash/wHash/aHash) at distance zero. “Looks identical after you open it.”
3. **Same outing** — GPS, burst, camera roll, time neighbors.
4. **0728 sibling** — another Extra Found Files file that *does* hash-match a laptop copy, sitting next to the questioned one.

So: a questioned file can be a **different JPEG** of a picnic that **is** on the laptop (larger preview, different compression). That is **not** “proved hacked.” It **is** “this 0728 object is not the cataloged laptop file.”

## Categories (C1–C6)

| Code | Plain language | Selected |
|---|---|---:|
| C1 | Nothing similar on the laptop copies | 4 |
| C2 | 0728 picture is **larger** than the look-alike on the laptop | 4 |
| C3 | Same size/content, different JPEG plumbing (ICC, quantization) | 4 |
| C4 | Computer said “match”; a human said “no, different photo” | 4 |
| C5 | Non-Apple camera (Nikon, Sony, Canon) | 3 |
| C6 | Other processing pipeline | 4 |

**C2** is the one to sit with: if Extra Files were only carved leftovers of the **same** allocated JPEGs, you would not expect a **bigger** rendition than the laptop copy. That pattern is consistent with **another store** of the photo (cloud original, phone, different export) — which is exactly the [thumbnail / iCloud “trick”](CIRCULAR_CUSTODY.md) allegation, still unverified as a mechanism.

## What the exhibit is for

It supports the author’s conclusion that there is a **testable** source problem. It does **not** name a hacker or prove Apple was breached.

Master SHA-256 (parent package): `5fb327bebf44c7eb6a5c027342f9de36cbdfac363433bc4f80416e409d64608b`.

## See also

- [Unmatched hashes](UNMATCHED_HASHES.md)
- [Integrity](INTEGRITY.md)
