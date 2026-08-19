# Contents census

> **Hatnote.** How to read the counts. Tables: [file-tree catalog](catalog/file_tree.md).

| Quantity | Value | What it is **not** |
|---|---:|---|
| Canonical paths (`0728/`) | 480,039 | Unique human documents |
| Extra Found Files paths | 479,584 | A Mac home directory listing |
| Distinct SHA-256 | 317,319 | Path count (duplicates exist) |
| Logical bytes | 336,321,196,441 | “Deleted space on the MacBook NVMe” |
| PG `files` rows source 2 (all prefixes) | 960,533 | Canonical census — includes duplicate `source/` prefix |
| APFS-matching hashes | 205,262 | Proof 0728 was copied from the 13 June 2022 MEGA image |
| Primary-exclusive hashes | 94,635 | Named alternative source |

Path count > hash count because the same blob can appear more than once (recovery duplicates, category collisions).

Byte majority of unmatched content in parent-project notes is large webarchives and videos, not extra `.txt` rows. Row majority of the whole tree is `.txt`.

Laptop-reference **SAS twins** of Extra Found Files: **479,584** files. That number matches this catalog’s Extra Found Files path count.

## See also

- [What is in the corpus](04_what_is_in_the_corpus.md)
- [Glossary](GLOSSARY.md)
