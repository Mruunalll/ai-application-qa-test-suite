## BUG-009 — Whitespace-only message submitted and creates empty chat bubble

**Title:** Whitespace-only message submitted and creates empty chat bubble
**Environment:** Chrome 124, Safari 17
**Severity:** Major | **Priority:** High

**Steps to Reproduce:**
1. Click chat input
2. Press spacebar 5 times
3. Press Enter

**Expected Result:** Message not sent; input cleared or stays
**Actual Result:** Empty/whitespace message appears as user bubble in chat; API call made; model responds to empty input

---
