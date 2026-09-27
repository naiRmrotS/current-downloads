# Current — downloads

Release artifacts for **Current**, the social simulation game. This repository is
not source: it exists so the download links on the game's page have a public home,
because release assets on the game's own repository are not fetchable by anyone
without access to it.

## Get it

Open **[Releases](../../releases)** and pick your platform:

| Platform | File | Size | Notes |
| --- | --- | --- | --- |
| Windows | `Current-Setup-…-x64.exe` | ~122 MiB | installer, per-user, desktop shortcut |
| Windows | `Current-…-portable.exe` | ~122 MiB | one file, installs nothing |
| Android | `Current-…-debug.apk` | ~17 MiB | copy to the phone and tap it |

## Before you run it

**Neither build is code-signed.** Windows will show *"Windows protected your PC"*
— *More info*, then *Run anyway*. The Android apk is signed with the debug key, so
it sideloads fine and the Play Store refuses it; Play Protect will warn about an
unknown developer. That is expected, not a sign of tampering — but check the
SHA-256 in the release notes anyway, because that is what it is there for:

```bash
sha256sum Current-Setup-0.1.0-x64.exe
# Windows: Get-FileHash .Current-Setup-0.1.0-x64.exe -Algorithm SHA256
```

## What the game is

Runs in a browser, on Windows, and on Android — one renderer, three shells. The
simulation, the cast, the save and the on-device AI all run locally; the only
things that use a network are the optional account service and whichever model
provider you configure. Signing in on a second device gives you the same account
and its own town, because the save lives on the device that plays it.

## Where the source is

Private, and it stays that way: this repository carries builds, not code.
