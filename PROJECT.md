# Moods by Gal â Project Hub

> Everything you need to pick up where the last session left off.

---

## Quick Links

| What | Where |
|------|-------|
| Live app | [spotify-moods.vercel.app](https://spotify-moods.vercel.app) |
| GitHub | [galrubinx/spotify-moods](https://github.com/galrubinx/spotify-moods) |
| Slack | #spotify-mood |

## Project Structure

```
spotify-moods/
âââ index.html              â The entire app (~1240 lines)
âââ PROJECT.md              â You are here
âââ ROADMAP.md              â High-level phases and goals
âââ DECISIONS.md            â Architectural and product decisions
âââ SPEC.md                 â Full product spec (features, architecture, competitive landscape)
âââ CHANGELOG.md            â Legacy session log (pre-sprint system)
âââ md/
â   âââ sprints/
â   â   âââ SPRINT-001.md   â Current sprint: Stability
â   âââ sessions/
â   â   âââ SESSION-2026-04-06-initial-build.md
â   â   âââ SESSION-2026-04-07-oauth-fix.md
â   â   âââ SESSION-2026-04-10-playlist-and-profile.md
â   âââ templates/
â       âââ SPRINT-TEMPLATE.md
â       âââ SESSION-TEMPLATE.md
âââ data/
    âââ BUGS.md               â All known bugs with severity and status
    âââ FEATURES.md          â Feature pipeline: shipped, backlog, and long-term
```

## Current State (April 14, 2026)

**Active Sprint:** [Sprint 001 â Stability](md/sprints/SPRINT-001.md)
**Phase:** 1 of 4 (Stability â Virality â Social â Growth)
**Total Commits:** 19 on main
**Open Bugs:** 10 (1 critical, 3 high, 3 medium, 3 low)
**Shipped Features:** 11

## How to Start a New Session

1. Read this file to get oriented
2. Check the active sprint in `md/sprints/` for current goals
3. Review `data/BUGS.md` and `data/FEATURES.md` for what to work on
4. Create a new session file from `md/templates/SESSION-TEMPLATE.md`
5. When done, update the sprint log and mark tasks complete

## How to Start a New Sprint

1. Copy `md/templates/SPRINT-TEMPLATE.md` to `md/sprints/SPRINT-NNN.md`
2. Pull objectives from `data/FEATURES.md` (P0 first) and `data/BUGS.md` (critical/high first)
3. Fill in the retro on the previous sprint before starting
4. Update the "Active Sprint" link in this file
