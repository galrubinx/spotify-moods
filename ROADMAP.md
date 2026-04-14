# Roadmap

**Last Updated:** April 14, 2026

A high-level view of where Moods by Gal is headed. For detailed task tracking, see `data/FEATURES.md` and `data/BUGS.md`. For current work, see the active sprint in `md/sprints/`.

---

## Phase 1: Stability (Current)

Get the core app reliable and bug-free. Fix critical issues that block real users.

- ~~Fix token expiry handling (BUG-001)~~ Done
- ~~Fix share view broken links (BUG-006)~~ Done
- ~~Replace `alert()` with styled errors (BUG-004, FEAT-014)~~ Done
- ~~Prevent duplicate playlists (BUG-005, FEAT-018)~~ Done
- Audit & fix mood classification accuracy (BUG-011, FEAT-030)
- Add users to Spotify dev dashboard
- Browser back navigation (BUG-010)

**Exit criteria:** A new user can log in, browse moods, create a playlist, and share a link without hitting a broken state. Songs are in the right mood categories.

---

## Phase 2: Virality

Make the app shareable and screenshot-worthy. These are the highest-leverage features.

- OG Image / Visual Share Card (FEAT-012)
- "Vibe Check" one-liner summary (FEAT-013)
- Playlist cover art collage (FEAT-015)
- "Create All Playlists" button (FEAT-016)

**Exit criteria:** A user can screenshot or share their moodboard and it looks great on social media.

---

## Phase 3: Social

Turn solo exploration into a social experience.

- "Mood Match" â compare moodboards (FEAT-019)
- Mood-based color gradients (FEAT-021)
- Track count badges (FEAT-024)
- Sort moods by size (FEAT-025)

**Exit criteria:** Two friends can compare their music taste through the app.

---

## Phase 4: Growth

Scale beyond dev mode and establish the brand.

- Submit Spotify extension request â go public (FEAT-026)
- Custom domain moodsbygal.com (FEAT-027)
- Influencer campaign launch (see `Influencer_Campaign_Strategy.md`)

**Exit criteria:** Anyone with a Spotify account can use the app without being whitelisted.
