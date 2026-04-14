# Session: Sprint 1 Kickoff â Stability Fixes

**Date:** April 14, 2026
**Sprint:** 001 (Stability)
**Goal:** Fix the critical and high-priority bugs that block real users. Set up project management system.

---

## What Happened

Set up a full project management system (data/, md/, core files) and then fixed 7 bugs in one session.

### Bug Fixes

1. **BUG-001 (Critical): Token expiry handling** â Created a `spotifyFetch` wrapper that intercepts all Spotify API calls. Catches 401 responses and proactively checks `tokenExpiresAt` before making requests. Shows a styled "Session Expired" toast with a "Reconnect to Spotify" button. Token expiry time is persisted in localStorage and restored on page load.

2. **BUG-003 (High): OAuth error UI** â When token exchange fails (denied permissions, timeout), a styled error toast now appears with a "Try Again" button instead of silently hiding the loading overlay.

3. **BUG-004 (Medium): Replace all alert() calls** â Built a reusable toast notification system with error/success/info variants, auto-dismiss, and action buttons. Replaced every `alert()` call in the app (4 total). Toast UI matches the dark aesthetic with animations.

4. **BUG-005 (Medium): Duplicate playlist prevention** â Added a `createdPlaylists` tracker. After a playlist is created, the button permanently shows "Playlist Created (N tracks) â Open" and clicking it opens the playlist in Spotify. Resets when switching moodboard types.

5. **BUG-006 (High): Share view broken links** â Items in shared moodboards now render as `<div>` instead of `<a>` when `item.url` is empty. No more accidental page reloads destroying the moodboard.

6. **BUG-008 (Low): Clipboard fallback** â Replaced the broken fallback (which retried the same failing clipboard API) with a hidden textarea + `execCommand('copy')` approach. Final fallback shows a toast with the URL to copy manually.

7. **BUG-009 (Low): Prefetch badges stuck** â When count-fetching fails, badges now show descriptive text ("Saved albums", etc.) instead of staying on "Loading..."

### Project Management Setup

Created the full tracking system: `data/BUGS.md`, `data/FEATURES.md`, `md/sprints/`, `md/sessions/`, templates, `DECISIONS.md`, `ROADMAP.md`, `PROJECT.md`.

## Decisions Made

- **Toast system over modals:** Toasts are less intrusive, stack naturally, and auto-dismiss (DEC: chose toasts for errors instead of modal dialogs)
- **Permanent playlist success state:** Better than the 8-second reset â prevents accidental duplicates and gives permanent access to the playlist link

## Discovered

- The `exchangeCodeForToken` returns `expires_in` (usually 3600s) â we now track this
- `document.execCommand('copy')` is deprecated but works as a fallback where clipboard API doesn't
