# Bug Tracker

**Last Updated:** April 14, 2026

---

## Active Bugs

| ID | Severity | Bug | Status | Found | Sprint |
|----|----------|-----|--------|-------|--------|
| BUG-002 | High | Share links can exceed URL length limits (~2K safe, ~8K max) with 200 items | Open | Apr 10 | Ã¢ÂÂ |
| BUG-007 | Low | Audio features API deprecation risk Ã¢ÂÂ loading text says "Analyzing audio features..." even on failure | Open | Apr 10 | Ã¢ÂÂ |
| BUG-010 | Medium | No browser back navigation Ã¢ÂÂ no pushState/popstate, back leaves app entirely | Open | Apr 10 | Ã¢ÂÂ |
| BUG-011 | High | Mood classification inaccurate Ã¢ÂÂ kids/upbeat songs (e.g. ÃÂÃÂÃÂÃÂ ÃÂÃÂÃÂÃÂÃÂÃÂÃÂ) sorted into Melancholy. Genre-to-mood mapping needs validation and improvement | Resolved | Apr 14 | Sprint 001 |

## Resolved Bugs

| ID | Bug | Resolution | Fixed | Commit |
|----|-----|------------|-------|--------|
| BUG-000 | Empty playlist bug for Albums mode Ã¢ÂÂ 0 tracks added | Switched to `/v1/playlists/{id}/items` endpoint (deprecated `/tracks`) | Apr 14 | `7b6b291` |
| BUG-001 | Token expiry mid-session Ã¢ÂÂ API calls silently fail after ~1hr | Added `spotifyFetch` wrapper with 401 handling + token expiry tracking + reconnect toast | Apr 14 | Sprint 001 |
| BUG-003 | No error UI on OAuth failure | Added toast notification on connection failure with retry button | Apr 14 | Sprint 001 |
| BUG-004 | Native `alert()` breaks dark aesthetic | Replaced all `alert()` calls with styled toast notification system | Apr 14 | Sprint 001 |
| BUG-005 | Duplicate playlists on repeated clicks | Added `createdPlaylists` tracking object, button stays as "Open" link after creation | Apr 14 | Sprint 001 |
| BUG-006 | Shared moodboard items have no Spotify URLs Ã¢ÂÂ clicking reloads page | Share view now uses `<div>` instead of `<a>` when URL is empty | Apr 14 | Sprint 001 |
| BUG-008 | Clipboard fallback broken Ã¢ÂÂ catch handler retries same failing API | Replaced with hidden textarea + `execCommand('copy')` fallback | Apr 14 | Sprint 001 |
| BUG-009 | Prefetch count badges stuck on "Loading..." | Added catch handler that resets badges to descriptive text on failure | Apr 14 | Sprint 001 |

---

## Severity Guide

- **Critical:** App is broken or unusable for core flows
- **High:** Major feature degraded, bad UX, or data loss risk
- **Medium:** Noticeable UX issue but workaround exists
- **Low:** Minor polish, edge case, or cosmetic
