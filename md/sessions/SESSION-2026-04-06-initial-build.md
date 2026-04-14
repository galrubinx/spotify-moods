# Session: Initial Build â Concept to Deployed MVP

**Date:** April 6, 2026
**Sprint:** Pre-sprints
**Goal:** Build the entire Moods by Gal app from concept to deployed MVP in one session.

---

## What Happened

Built the full app in a single day â 11 commits from first landing page to fully branded, shareable moodboard with three content types (albums, tracks, artists).

Started with a static mood layout, then layered in Spotify OAuth (PKCE), real data fetching, genre-based mood classification, and LZ-String compressed sharing. Major rebrand at the end: violet + Cooper Black fonts, #0a0a0a dark background, mobile responsive.

## Commits

| Hash | Message |
|------|---------|
| `74f5bcb` | Add Spotify mood albums landing page |
| `aa54127` | Remove emojis, add image fallback handlers |
| `4bced7f` | Fix: replace file with clean version (no emojis, image fallbacks) |
| `ec1433a` | Remove gradient icons, add Spotify OAuth user profile |
| `f90826d` | Add Spotify Client ID for OAuth login |
| `4400e2b` | Fix OAuth: switch to PKCE flow |
| `5cba98c` | MVP: real Spotify data + thumbnail fix |
| `7bb7553` | Fix: use individual artist fetches for dev-mode Spotify apps |
| `092dee3` | Fix mood categorization + remove corrupted emojis |
| `d9b35f2` | UI: bigger share CTA, hide discover banner for owners, mobile responsive |
| `9c3f0e0` | Rebrand to violet + Cooper Black fonts + shareable links + mobile |

## Decisions Made

- **Single-file architecture:** One index.html, no build step (DEC-001)
- **PKCE OAuth:** No backend needed (DEC-002)
- **7 moods:** Morning, Chill, Workout, Late Night, Melancholy, Party, Romantic
- **Genre â audio features â name-hash fallback chain** (DEC-003)
- **LZ-String URL sharing** (DEC-004)

## Discovered

- Spotify app is in dev mode with 0/5 users whitelisted â nobody else can authenticate
