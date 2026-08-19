# Timestamps

> **Hatnote.** `files.mtime` on the working inventory is a **mixed clock**. Table: [`01_time_distribution.tsv`](../build/metadata/01_time_distribution.tsv).

## Families

| Family | Typical years | Meaning |
|---|---|---|
| Recovery / export | **2021** (177,488 paths) | July burst; tool write time |
| Working copy / index | **2026** (266,664 paths) | Later copy onto this project’s disks |
| Preserved content | 2015–2019 scatter; Voice Memos 2018–2019 | Possible original mtimes kept by the carver |
| Garbage / overflow | 2038–2105; a few 2002–2010 | Carve artifacts, FAT epoch mistakes, or parser noise |

Do not line up a 2026 mtime with a 2021 MEGA download and call it “Hayes recarved in 2026.” The 2026 cluster is handling of **this working tree**.

Do not line up a 2017 JPEG EXIF with “the MacBook did not exist yet” as a 0728 argument. EXIF is content metadata; recovery mtime is export metadata.

UTC burst analysis in the parent project used destination write stamps in a 27-minute window. That window is the **best 0728-internal clock** for materialization.

## See also

- [Timeline](06_timeline_and_handling.md)
- [Metadata catalog](catalog/metadata.md)
