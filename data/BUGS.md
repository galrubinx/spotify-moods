# Bug Tracker

**Last Updated:** April 14, 2026

---

## Active Bugs

| ID | Severity | Bug | Status | Found | Sprint |
|----|----------|-----|--------|-------|--------|
| BUG-001 | Critical | Token expiry mid-session â no 401 handling, API calls silently fail after ~1hr | Open | Apr 10 | â |
| BUG-002 | High | Share links can exceed URL length limits (~2K safe, ~8K max) with 200 items | Open | Apr 10 | â |
| BUG-003 | High | No error UI on OAuth failure â denying permissions shows nothing to user | Open | Apr 10 | â |
| BUG-004 | Medium | Native `alert()` for empty libraries/errors â breaks dark aesthetic | Open | Apr 10 | â |
| BUG-005 | Medium | Duplicate playlists on repeated clicks â no deduplication, button re-enables after 8s | Open | Apr 10 | â |
| BUG-006 | High | Shared moodboard items have no Spotify URLs â clicking reloads page, destroys moodboard | Open | Apr 10 | â |
| BUG-007 | Low | Audio features API deprecation risk â loading text says "Analyzing audio features..." even on failure | Open | Apr 10 | â |
| BUG-008 | Low | Clipboard fallback broken â catch handler retries same failing API | Open | Apr 10 | â |
| BUG-009 | Low | Prefetch count badges stuck on "Loading..." when count-fetch fails | Open | Apr 10 | â |
| BUG-010 | Medium | No browser back navigation â no pushState/popstate, back leaves app entirely | Open | Apr 10 | â |

## Resolved Bugs

| ID | Bug | Resolution | Fixed | Commit |
|----|-----|------------|-------|--------|
| BUG-000 | Empty playlist bug for Albums mode â 0 tracks added | Switched to `/v1/playlists/{id}/items` endpoint (deprecated `/tracks`) | Apr 14 | `7b6b291` |

---

## Severity Guide

- **Critical:** App is broken or unusable for core flows
- **High:** Major feature degraded, bad UX, or data loss risk
- **Medium:** Noticeable UX issue but workaround exists
- **Low:** Minor polish, edge case, or cosmetic
