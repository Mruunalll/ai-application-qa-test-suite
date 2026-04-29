## BUG-011 — Android app loses typed draft when app sent to background and returned after 2+ minutes

**Title:** Android app loses typed draft when app sent to background and returned after 2+ minutes
**Environment:** Samsung Galaxy S23, Android 14, ChatGPT native app v1.2024.x
**Severity:** Major | **Priority:** High

**Steps to Reproduce:**
1. Open ChatGPT Android app
2. Type long prompt (200+ words) without sending
3. Press Home button (app goes to background)
4. Wait 2+ minutes
5. Return to ChatGPT app

**Expected Result:** Typed draft preserved in input field
**Actual Result:** Input field cleared; entire typed prompt lost

---
