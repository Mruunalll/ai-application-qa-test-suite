## BUG-010 — Conversation search returns no results for recently renamed conversations

**Title:** Conversation search returns no results for recently renamed conversations
**Environment:** Chrome 124, ChatGPT Web
**Severity:** Minor | **Priority:** Medium

**Steps to Reproduce:**
1. Rename a conversation to "Project Alpha Research"
2. Immediately use conversation search bar
3. Search for "Project Alpha"

**Expected Result:** Renamed conversation appears in results
**Actual Result:** No results found; conversation only appears after waiting ~30 seconds (indexing delay with no indication)

---
