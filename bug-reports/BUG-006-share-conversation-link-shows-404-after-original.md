## BUG-006 — "Share conversation" link shows 404 after original conversation is deleted

**Title:** "Share conversation" link shows 404 after original conversation is deleted
**Environment:** Chrome 124, tested with incognito verification
**Severity:** Major | **Priority:** Medium

**Steps to Reproduce:**
1. Open conversation → click Share → copy link
2. Test link in incognito (works ✅)
3. Delete original conversation
4. Re-open shared link in incognito

**Expected Result:** Either: link still works (read-only snapshot) OR shows "This conversation is no longer available"
**Actual Result:** Generic 404 page — no helpful message; user has no context for why link broke

---
