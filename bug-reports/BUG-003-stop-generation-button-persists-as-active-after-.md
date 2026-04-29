## BUG-003 — Stop generation button persists as active after response fully completes

**Title:** Stop generation button persists as active after response fully completes
**Environment:** Chrome 124, Firefox 125 — both confirmed
**Severity:** Major | **Priority:** Medium

**Steps to Reproduce:**
1. Send any prompt
2. Wait for response to complete fully
3. Observe the Stop (■) button

**Expected Result:** Stop button disabled or hidden after response completion
**Actual Result:** Stop button remains visually active for 3–8 seconds after completion; clicking it at this point shows a brief blank flash in the chat area

---
