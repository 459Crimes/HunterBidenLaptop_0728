# iPhone backup password — why Hayes’s copy mattered

> **Hatnote.** Marco Polo / Ziegler **did not** recover this password from the bootable Hayes prepared for them. The vault lived on a **fuller** Hayes copy. This page is about **that gap**, not about publishing a trophy password.

## The one sentence

> The iPhone backup on the laptop is encrypted. The **password is stored in a macOS keychain**. The **MPOLO** bootable that Hayes gave Marco Polo in June 2021 was a **reduced system** — it **lacked essential system files, including password vaults**. Ziegler therefore could not open the backup from that stick. Hayes’s later working copy still contained the older keychain file `login_renamed_1.keychain-db`. That file is what made the backup decryptable. **Conan Hayes was essential**; Marco Polo’s published laptop work did not include this step.

## Why a bootable “laptop” can still miss the vault

A Carbon Copy Cloner / desktop-drop copy can look like macOS and still omit:

- `/Users/roberthunter/Library/Keychains/`
- other System/Library credential stores
- full Apple Mail / Messages containers

If you only have Photos and Documents, you do not have the **login keychain**. Without the keychain, you do not have the **iOS Backup** password entry. You can stare at `00008020-0014716A2282002E` forever.

That is the MPOLO limitation as used in this encyclopedia. [Garrett Ziegler](GARRETT_ZIEGLER.md) · [Marco Polo](MARCO_POLO.md) · [Todd Sanders](TODD_SANDERS.md) (Desktop-drop description of the Trimarco copy).

## What the fuller Hayes copy contained

On the Hayes-family APFS image later sent to this author (`RHB_Boot.imgc`, June 2022) — and in forensic extracts from that family — there is a **renamed historical keychain**:

| Property | Value |
|---|---|
| Path | `Users/roberthunter/Library/Keychains/login_renamed_1.keychain-db` |
| Size | 935,016 bytes |
| SHA-256 | `72f8c76003d500e2ede875cb4b068cbb835cbb62a062fdaa5356a01d3867752b` |
| mtime | 2019-03-17 21:16:02 |
| Role | Pre-rename copy of the user login keychain; contains an **iOS Backup** item |

The **live** `login.keychain-db` on later copies is a different, smaller file (mtime 2021-09-09 on one index). The old password **does not** open it. The renamed March 2019 file is the one that still held the era of the November 2018 iPhone backup.

Parent chain note (operator, not hosted as a how-to here): `forensics/manifests/KONA_TO_JULIAIS_CHAIN.md`.

## What was recovered (labeled, not instructed)

Project verification (2026-07-08) reconstructed:

1. export the keychain hash from `login_renamed_1.keychain-db`;
2. recover the **macOS keychain password** for that file (`koda`);
3. unlock Keychain Access and read the stored **iOS Backup** password;
4. decrypt the iPhone backup (160 domains, 6,774 files, ~28 GB in that run).

**This encyclopedia does not publish a cracking recipe.** The existence of the chain is a **custody and completeness** fact: Hayes had the vault; the Marco Polo stick did not.

The recovered iOS Backup password itself is an **operator secret** in parent notes. It is not a 0728 filename and is not required to read Extra Found Files.

## What this does **not** prove

- that Extra Found Files came from the iPhone backup (iPhone-backup joins explained **16** unmatched 0728 hashes — noise);
- that Ziegler never possessed a keychain on some other medium;
- that Apple was breached.

It **does** prove why “Marco Polo already had the laptop” is not the same sentence as “Marco Polo had the credential store.” Hayes’s **selection of what to put on the stick** is itself a handling event.

## See also

- [Copy lineages](COPY_LINEAGES.md)
- [Conan Hayes](CONAN_HAYES.md)
- [Author](AUTHOR.md)
