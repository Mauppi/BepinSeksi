# Lethal Company mod installation

This repository snapshots the contents of the game's `BepInEx` folder:
installed mods, patchers, BepInEx core files, active configuration, and custom
LethalBots settings and soundboard clips. It records the installed files,
including locally modified mods; package manifests may describe an earlier
upstream release. It does not contain mod source projects.

The game and the loader files beside `Lethal Company.exe`, such as `winhttp.dll`
and `doorstop_config.ini`, are outside this repository. A restored installation
still needs Lethal Company and the compatible BepInEx loader in the game folder.
Locally hosted dialogue, transcription, and speech services used by the
LethalBots configuration must also be set up separately.

## Storage

Git LFS is required. `.gitattributes` sends compiled mods, Unity bundles, and
speech model binaries to LFS, including bundles with no filename extension.
Configuration, documentation, and small media files remain in ordinary Git.
File bytes and configuration line endings are preserved.

The setup audit on 2026-09-14 found approximately 1.01 GiB of installed files.
After excluding runtime data and backups, about 1.00 GiB uses LFS and 9.04 MiB
remains in ordinary Git before compression. These five files exceed 50 MiB:

| Asset | Size (MiB) |
| --- | ---: |
| `plugins/BLB_Thunderstore_Mods_LOL-Boom_Variants/boomvariants.lethalbundle` | 203.89 |
| `plugins/mrgrm7-LethalCasino/lethalcasinoassets` | 151.06 |
| `plugins/BLB_Thunderstore_Mods_LOL-Boom_Scraps/boomscraps.lethalbundle` | 88.04 |
| `plugins/Generic_GMD-Generic_Interiors/generic interiors bunker.lethalbundle` | 66.10 |
| `plugins/Generic_GMD-Generic_Interiors/generic interiors sh and br.lethalbundle` | 63.35 |

GitHub blocks ordinary Git files larger than 100 MiB and warns above 50 MiB.
See [GitHub's file limits](https://docs.github.com/en/repositories/working-with-files/managing-large-files/about-large-files-on-github).
GitHub Free and Pro currently include 10 GiB of LFS storage and 10 GiB of
monthly download bandwidth per account. Changed LFS files consume their full
size again in history, and downloads consume bandwidth; existing account use
also counts. See [Git LFS usage and allowances](https://docs.github.com/en/billing/concepts/product-billing/git-lfs).

## Clone and restore

Install Git and Git LFS before cloning. Replace the example URL with this
repository's remote URL:

```powershell
git lfs install
git clone <repository-url> BepInEx
cd BepInEx
git lfs pull
git lfs fsck
```

Clone into an empty destination, then use the resulting contents as the game's
`BepInEx` folder with the game closed. A clone without LFS downloads leaves
small pointer files where DLLs and bundles should be; those files cannot load
in the game. GitHub's source ZIP downloads may also omit LFS contents depending
on the repository settings, so use a Git LFS clone for restoration.

## Update the snapshot

With the game closed after changing mods or settings:

```powershell
git status --short
git add .
git diff --cached --stat
git commit -m "Update mods and configuration"
git push
```

The LFS pre-push hook uploads referenced large files automatically. Existing
binary patterns cover updates to the installed mods. Before adding a new large
asset with an unfamiliar extension or no extension, track its exact path:

```powershell
git lfs track --filename "plugins/ExampleMod/newasset"
git add .gitattributes "plugins/ExampleMod/newasset"
```

## Ignored runtime files

- Logs and rotated logs (`*.log`, `*.log.*`, and `logs/` or `Logs/`).
- BepInEx `cache/`.
- `config/LethalBots/Audio/GeneratedVoices/`, including future nested files.
- LethalBots `DialogueMemory/` runtime conversation history.
- Local backups, temporary files, environment files, and editor/OS metadata.

Active `.cfg` and LethalBots JSON configuration files, plus
`config/LethalBots/Soundboard/`, are included. The generated-voice directory
does not need to exist for its ignore rule to work.

## Connect a remote

The initial setup is local. After creating an empty remote repository with LFS
support, run these commands from this folder:

```powershell
git remote add origin <repository-url>
git push -u origin main
```
