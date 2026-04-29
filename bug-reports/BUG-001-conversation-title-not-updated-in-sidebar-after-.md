## BUG-001 — Conversation title not updated in sidebar after rename without page refresh

**Title:** Conversation title not updated in sidebar after rename without page refresh
**Environment:** Chrome 124, Windows 11, ChatGPT Web (April 2026)
**Severity:** Major | **Priority:** High

**Steps to Reproduce:**
1. Open any existing conversation in sidebar
2. Click the edit (pencil) icon on the conversation
3. Type new name "My Renamed Chat"
4. Press Enter
5. Observe sidebar immediately

**Expected Result:** Sidebar shows "My Renamed Chat" instantly
**Actual Result:** Sidebar still shows old name; only updates after page refresh (F5)

---
