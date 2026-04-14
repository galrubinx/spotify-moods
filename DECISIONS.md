# Decision Log

Architectural and product decisions for Moods by Gal. Each entry captures what was decided, why, and what alternatives were considered.

---

## DEC-001: Single-file architecture (Apr 6)

**Decision:** Keep the entire app in one `index.html` file â HTML, CSS, and JS inline.

**Why:** Zero build step, trivial Vercel deployment, easy for a solo dev to navigate. The app is ~1240 lines which is manageable in a single file.

**Alternatives considered:** Component-based framework (React, Svelte) â rejected as overkill for current scope. Multi-file vanilla JS â rejected for deployment simplicity.

**Revisit when:** The file exceeds ~2000 lines or we need shared components across pages.

---

## DEC-002: PKCE OAuth, no backend (Apr 6)

**Decision:** Use Spotify's PKCE OAuth flow entirely client-side. No server, no token proxy.

**Why:** Eliminates hosting costs, simplifies deployment, and Vercel serves static files for free. PKCE is secure for public clients.

**Alternatives considered:** Authorization Code flow with a backend proxy â more secure token handling but requires server infrastructure.

**Revisit when:** We need refresh tokens or server-side Spotify API calls.

---

## DEC-003: Genre-based mood classification with fallback chain (Apr 6)

**Decision:** Classify by artist genres first â audio features second â name-hash third.

**Why:** Genre data is the most reliable signal. Audio features are deprecated for new apps. Name-hash ensures every item lands in a mood even with no metadata.

**Trade-off:** Name-hash is essentially random distribution â items without genre or audio data get arbitrary moods.

---

## DEC-004: LZ-String URL compression for sharing (Apr 6)

**Decision:** Compress moodboard data with LZ-String and encode it in the URL `?s=` parameter.

**Why:** No backend needed to store shared boards. Anyone with the link can view. Fully stateless.

**Trade-off:** URL length limits (~2K safe, ~8K Chrome max) constrain how much data can be shared. Large libraries may hit limits. See BUG-002.

**Revisit when:** Share links consistently fail â may need a URL shortener or server-side storage.

---

## DEC-005: Session-based sprints (Apr 14)

**Decision:** Use session-based sprints instead of fixed time periods. Each Cowork session defines its own goals and scope.

**Why:** Solo project with variable work cadence â fixed weekly sprints would create artificial pressure. Sessions are natural work units.

**Revisit when:** Multiple contributors join or we need predictable delivery cadence.

---

## DEC-006: Project management in-repo (Apr 14)

**Decision:** Track sprints, bugs, features, decisions, and session notes directly in the GitHub repo under `md/` and `data/` folders.

**Why:** Everything is versioned with the code. No external tool dependency. Readable on GitHub. Future sessions pick up full context from the repo itself.

**Alternatives considered:** Notion, Linear, GitHub Issues â all add external dependencies and context-switching for a solo project.
