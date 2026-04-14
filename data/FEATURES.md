# Feature Pipeline

**Last Updated:** April 14, 2026

---

## Shipped Features

| ID | Feature | Shipped | Sprint | Commit |
|----|---------|---------|--------|--------|
| FEAT-001 | Spotify OAuth (PKCE) | Apr 6 | Pre-sprints | `4400e2b` |
| FEAT-002 | Saved Albums moodboard | Apr 6 | Pre-sprints | `5cba98c` |
| FEAT-003 | Liked Songs moodboard | Apr 6 | Pre-sprints | `5cba98c` |
| FEAT-004 | Followed Artists moodboard | Apr 6 | Pre-sprints | `5cba98c` |
| FEAT-005 | 7 mood categories + genre classification | Apr 6 | Pre-sprints | `092dee3` |
| FEAT-006 | Expandable mood sections | Apr 6 | Pre-sprints | `5cba98c` |
| FEAT-007 | Shareable links (LZ-String) | Apr 6 | Pre-sprints | `9c3f0e0` |
| FEAT-008 | Share view (read-only) | Apr 6 | Pre-sprints | `9c3f0e0` |
| FEAT-009 | Dark aesthetic rebrand | Apr 6 | Pre-sprints | `9c3f0e0` |
| FEAT-010 | Create Playlist from Mood | Apr 10 | Pre-sprints | `5f6e46d` |
| FEAT-011 | User profile dropdown + logout | Apr 10 | Pre-sprints | `0f9e316` |

## Backlog â Near Term

| ID | Feature | Priority | Effort | Notes |
|----|---------|----------|--------|-------|
| FEAT-012 | OG Image / Visual Share Card | P0 | Medium | Highest-leverage virality feature. `html2canvas` or `<canvas>`, client-side. 1200x630. |
| FEAT-013 | "Vibe Check" one-liner summary | P0 | Small | Personality-style summary from top 2 moods. Screenshot hook. |
| FEAT-014 | Replace `alert()` with styled errors | P1 | Small | Inline error states matching dark aesthetic |
| FEAT-015 | Playlist cover art (auto-collage) | P1 | Medium | Generate cover from mood's album art |
| FEAT-016 | "Create All Playlists" button | P1 | Small | One click â all 7 mood playlists |
| FEAT-017 | Browser back navigation | P1 | Small | pushState/popstate handling |
| FEAT-018 | Prevent duplicate playlist creation | P1 | Small | Track created playlists, disable button |

## Backlog â Medium Term

| ID | Feature | Priority | Effort | Notes |
|----|---------|----------|--------|-------|
| FEAT-019 | "Mood Match" â compare moodboards | P2 | Large | Side-by-side comparison from shared links. Data already in URL. |
| FEAT-020 | Custom mood thumbnails / AI artwork | P2 | Large | Per-mood generated artwork |
| FEAT-021 | Mood-based color gradients on cards | P2 | Small | Warm for Party, cool for Chill, etc. |
| FEAT-022 | Playlist naming customization | P2 | Small | Name input before creating |
| FEAT-023 | "Open in Spotify" deep link | P2 | Small | After playlist creation |
| FEAT-024 | Track count badges on mood cards | P2 | Small | Show item count per mood |
| FEAT-025 | Sort moods by size | P2 | Small | Largest mood first |

## Backlog â Long Term

| ID | Feature | Priority | Effort | Notes |
|----|---------|----------|--------|-------|
| FEAT-026 | Submit Spotify extension request (go public) | P3 | N/A | Remove 5-user whitelist limit |
| FEAT-027 | Custom domain (moodsbygal.com) | P3 | Small | DNS + Vercel config |
| FEAT-028 | Playlist collaboration (merge moods) | P3 | Large | Two users merge their mood playlists |
| FEAT-029 | Weekly mood digest | P3 | Large | Email/notification with mood changes |

---

## Priority Guide

- **P0:** Do next â highest impact, unblocks growth
- **P1:** Important â ship within 1-2 sprints
- **P2:** Nice to have â when P0/P1 are clear
- **P3:** Future â requires infrastructure or external deps
