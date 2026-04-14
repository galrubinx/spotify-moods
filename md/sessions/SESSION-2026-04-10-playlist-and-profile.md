# Session: Create Playlist + Profile Dropdown + UX Audit

**Date:** April 10, 2026
**Sprint:** Pre-sprints
**Goal:** Ship Create Playlist feature, add user profile dropdown, and audit the full UX.

---

## What Happened

Shipped two major features: Create Playlist (makes a real Spotify playlist from any mood section) and User Profile Dropdown (avatar + name + logout). Then ran a comprehensive UX audit across all ~1240 lines.

The UX audit identified 10 bugs and recommended 3 high-leverage features for virality. All findings were documented in SPEC.md.

Also discovered and later fixed the empty playlist bug for Albums mode â the Spotify `/v1/playlists/{id}/tracks` endpoint was deprecated, switched to `/v1/playlists/{id}/items`.

## Commits

| Hash | Message |
|------|---------|
| `5f6e46d` | Add Create Playlist feature for mood sections |
| `0f9e316` | Add user profile dropdown with logout button |
| `f4b29f8` | Fix playlist tracks: add error handling, logging, and album fallback |
| `2b777d4` | Fix playlist 403: create public playlist + add debug logging |
| `7b6b291` | Fix 403: use /items endpoint instead of deprecated /tracks |

## Decisions Made

- **Create Playlist uses private playlists** initially, then switched to public due to 403 errors
- **Albums mode fetches track IDs per-album** at playlist creation time (not pre-cached)

## Discovered

- 10 bugs identified (see `data/BUGS.md` for full list)
- Top 3 feature recs: OG share image, Mood Match, Vibe Check summary
- Spotify deprecated the `/tracks` endpoint â must use `/items`
