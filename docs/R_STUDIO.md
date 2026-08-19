# R-Studio / Known File Types tree

> **Hatnote.** Why Extra Found Files looks the way it does. Tutorial: [Recovery tree for non-experts](05_recovery_tree_for_non_experts.md).

**R-Studio** (R-Tools) is commercial data-recovery software. In **Known File Types** / extra-found-files mode it classifies by signature and writes a folder tree whose English bucket names match this corpus:

`Archive`, `Document`, `Graphics, Picture`, `Internet related files`, `Multimedia Video`, …

That match is **structural**. This encyclopedia does not possess the `.rsls` / project file that would prove the exact build, license, and scan target. PhotoRec and other carvers use different folder vocabularies. The 0728 names are the R-Studio dialect.

## Synthetic names

Typical Extra Found Files basenames:

- seven-digit IDs (`0442396.jpg`);
- `img_<w>x<h>x<d>_<seq>` for images without a usable name;
- `.Id_<n>` collision suffixes;
- long malformed strings for signatures without end markers.

Original Mac paths are not required for the tool to emit those names. Exact-hash matches to APFS files therefore usually **change filename**.

## Burst as export evidence

The 29 July 2021 UTC window writes categories in **non-overlapping time bands**. That is what a tool (or a scripted copy of a finished tool output) looks like when it walks buckets in order. It is **not** a user dragging folders in Finder over weeks.

It still does **not** distinguish:

- live Known File Types scan writing Extra Found Files for the first time; versus
- copying an already-finished Extra Found Files tree onto another disk.

Both can produce a 27-minute category burst.

## See also

- [What is in the corpus](04_what_is_in_the_corpus.md)
- [Carving claim](HAYES_CARVING_CLAIM.md)
