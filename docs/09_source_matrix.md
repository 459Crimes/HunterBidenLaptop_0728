# 9. Source matrix

> **Encyclopedia.** Reading list: [Bibliography](BIBLIOGRAPHY.md). Style classes: [Sourcing](MANUAL_OF_STYLE.md).

Each row is a **claim** used in the articles, the **class**, and the **source**. Inventory claims cite `build/` files.

| Claim | Class | Source |
|---|---|---|
| 0728 canonical inventory is 480,039 paths, 317,319 SHA-256, 336,321,196,441 bytes | Direct 0728 | `build/corpus_info/01_acquisition.tsv`; PG `files` source 2, `0728/%` |
| Extra Found Files / Root / Voice Memos = 479584 / 422 / 33 | Direct 0728 | `build/file_tree/01_top_level_summary.tsv` |
| Category and extension rollups as published | Direct 0728 | `build/file_tree/02_*.tsv`, `build/metadata/02_extension_distribution.tsv` |
| 205,262 hashes match APFS; 194,936 GAI; 82,186 JPMI; 222,684 any; 94,635 none | Direct 0728 + comparative | `build/hash_manifest/04_coverage.tsv` |
| Vs all other indexed sources: 234,436 match, 82,883 exclusive (26.1%) | Comparative (broader) | Parent `SOURCE_OVERLAP_0728_REPORT.md` (2026-07-10) |
| ~177,488 paths in UTC burst 2021-07-29 04:19:09–04:46:08 | Direct 0728 | Parent four-primary-sources note; mtime year 2021 in `01_time_distribution.tsv` |
| Ziegler relayed Hayes’s MEGA link to author, Aug 2021 | Author collection | [MEGA delivery](MEGA_DELIVERY.md); parent `docs/PROVENANCE.md` |
| Author is first person **known** to download from Hayes’s MEGA link | Author collection | Same |
| Hayes hosted Extra Found Files on MEGA (per Ziegler) | Participant (Ziegler) | Same |
| Ziegler attributed Extra Files to Hayes | Participant (Ziegler) | Same |
| Hayes carved Extra Files from unallocated space | Participant (Hayes) — **rejected as origin** | R-00014 00:20:29–00:24:33; rebuttal [carving claim](HAYES_CARVING_CLAIM.md) |
| Hayes self-reported Homeland / Backpage FBI help | Participant (Hayes) | R-00014 00:25:07–00:25:46 |
| Hayes described a California van, warrant, powered-off phone | Participant (Hayes) | R-00014 00:01:49–00:08:13 |
| FD-597 2022-09-13 names CONAN HAYES, black iPhone, Received From | Photographed federal form | `docs/exhibits/fbi/fd597_2022-09-13_conan_hayes_iphone.jpeg` |
| SA Calum Ramm, Dallas; `cwramm@fbi.gov` | Photographed federal form | Ramm card + handwritten email exhibits |
| Warrant excerpt authorizes biometric unlock of Hayes cellphone | Photographed excerpt | `hayes_cellphone_biometric_warrant_excerpt.jpeg` |
| Mesa County: Hayes used Wood’s badge, imaged elections server | Court-recited | *People v. Peters*, Colo. App. 24CA1951; trial journalism |
| Informant theory excluded; prosecutor recited FBI “never an informant” | Court / journalism | CPR 2024-08-01; appellate ¶89 |
| Peters bond motion: Hayes claimed federal informant / Backpage / cartels; identity concealed | Court filing (Peters counsel) | https://tinapeters.us/wp-content/uploads/2024/12/11-17-2024-Motion-for-Bond-on-Appeal.pdf |
| Byrne Locals 8 Apr 2022: ~400k files; “the trick”; portable drive on camera | Archived public stream | locals.com/patrickbyrne/feed?post=1966482; [Byrne](PATRICK_BYRNE.md) |
| Author chat: “hack not involving the laptop”; Extra Found Files Properties 473,580 | Archived Locals chat + hosted still | [Exhibits](EXHIBITS.md) |
| Ziegler said Hayes used thumbnails to trick iCloud | Participant recollection (author of Ziegler) — UAS | [Circular custody](CIRCULAR_CUSTODY.md) |
| MPOLO lacked keychain vaults; Hayes fuller copy had `login_renamed_1.keychain-db` | Comparative / author collection | [iPhone backup password](IPHONE_BACKUP_PASSWORD.md) |
| **28 Jul 2026** | Author FBI/DOJ criminal referral on 0728 | Project identity | [Author](AUTHOR.md) |
| **30 Jul 2026** | Author sent Hunter Biden same referral package as DOJ | Author collection | [Author](AUTHOR.md) |
| **3 Jun 2024** | Morris call: unauthorized iCloud retrieval claim | Participant (author) | [Author](AUTHOR.md) |
| 0728 is not a clone of JPMI/APFS/GAI | Interpretation of overlap | Coverage TSV: both matches and misses exist |
| Sep 2022 phone event more likely Mesa County than Trump-call | Inference | Date coincidence with Lindell seizure; incomplete warrant file |

Rows that are **inference** must not be restated in the lead as fact.
