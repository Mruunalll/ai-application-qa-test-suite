## BUG-007 — Regenerate response creates duplicate assistant message when clicked rapidly

**Title:** Regenerate response creates duplicate assistant message when clicked rapidly
**Environment:** Chrome 124, Windows 11
**Severity:** Minor | **Priority:** Low

**Steps to Reproduce:**
1. Receive response
2. Click "Regenerate" button
3. Click "Regenerate" again immediately before first regeneration starts

**Expected Result:** Only one regeneration runs; second click ignored or debounced
**Actual Result:** Two regenerated responses appended to conversation — duplicate assistant messages

---
