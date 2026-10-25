# RapTech GameHub Releases

Downloads and update manifests for **RapTech GameHub**, the new version of
RapTech for internet cafés. It holds **no source code**: one small file per
product, plus a GitHub release per build with the programs attached.

GameHub is two separate programs, and they update independently:

| Product | What it is | Manifest | Release tags |
| --- | --- | --- | --- |
| `server` | RapTech GameHub Server — the counter, the staff dashboard behind the desk | [`server/latest.json`](server/latest.json) | `server-vX.Y.Z` |
| `client` | RapTech GameHub Client — the terminal on each shop PC | [`client/latest.json`](client/latest.json) | `client-vX.Y.Z` |

## Status

Nothing has been released yet. Both manifests say `"version": "0.0.0"` with an
empty `url`, which means "nothing published" — a GameHub program reads that as
"you are up to date", never as an error.

## Why this repository is public

A shop PC has to be able to ask "is there a newer version?" without
credentials. The GameHub source is private; this is not, and it contains
nothing that needs to be. Programs read the raw manifest —
`raw.githubusercontent.com/Ralph313-creator/RapTech-GameHub-Releases/main/<product>/latest.json`
— rather than the GitHub API: no token, no rate limit.

## What a manifest says

```json
{
  "product": "server",
  "version": "1.0.0",
  "released": "2026-11-01",
  "notes": "What changed, in one line.",
  "url": "https://github.com/Ralph313-creator/RapTech-GameHub-Releases/releases/download/server-v1.0.0/RapTech-GameHub-Server.exe",
  "size": 14680064,
  "sha256": "…"
}
```

A download is trusted only when it is HTTPS from a GitHub host and its size and
SHA-256 match the manifest.

## Licences

Every GameHub program needs a licence key from RapTech (`GH1C-…` for the floor,
`GH1S-…` for the counter) after its free month. Keys from the older RapTech
(`RT1…`) are not accepted.
