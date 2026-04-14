# Sprint 001 â Stability

**Started:** April 14, 2026
**Status:** Active
**Phase:** 1 (Stability)
**Goal:** Fix the critical bugs that block real users from having a smooth experience.

---

## Objectives

1. [ ] **Token resilience** â Users can leave the tab open without the app silently breaking
2. [ ] **Share view works end-to-end** â Shared links are clickable and don't destroy the moodboard
3. [ ] **Clean error states** â No more native `alert()` or silent failures
4. [ ] **Spotify dashboard setup** â At least 2-3 testers whitelisted so others can try the app

## Scope

### Must Do (committed)

- [ ] BUG-001: Token expiry handling â fetch wrapper that catches 401s, prompts re-login
- [ ] BUG-006: Fix shared moodboard click-through â disable links when `item.url` is empty
- [ ] BUG-003: Add error UI for OAuth failures â styled inline, not console-only
- [ ] BUG-004: Replace `alert()` calls with styled inline error states (ties into FEAT-014)
- [ ] Whitelist 2-3 testers on Spotify Developer Dashboard

### Stretch (if time allows)

- [ ] BUG-005: Prevent duplicate playlist creation
- [ ] BUG-010: Browser back navigation (pushState/popstate)
- [ ] FEAT-013: "Vibe Check" one-liner summary (small effort, big impact)

## Results

| Metric | Target | Actual |
|--------|--------|--------|
| Critical bugs fixed | 1 (BUG-001) | â |
| High bugs fixed | 2 (BUG-003, BUG-006) | â |
| Medium bugs fixed | 1 (BUG-004) | â |
| Testers whitelisted | 2-3 | â |
| Commits pushed | â | â |

## Session Log

| Session | Date | What happened |
|---------|------|---------------|
| â | â | â |

## Retro Notes

**What went well:**
- 

**What to improve:**
- 

**Carry over to next sprint:**
- 
