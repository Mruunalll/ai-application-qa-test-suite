# Charter 1: Input Boundary and Adversarial Input Handling
**Mission:** Explore how the chat interface handles extreme, unusual, and adversarial text inputs — focusing on UI stability, not model accuracy
**Area:** Chat input field → submission → rendering
**Duration:** 75 minutes

**Session Notes:**
- Empty submit → no-op ✅
- Spaces only → submitted as message (BUG-009) ❌
- 5,000 chars → accepted; API processes ✅
- 50,000 chars (pasted) → accepted; no limit shown; very long render time ⚠️
- Right-to-left Arabic text → rendered correctly ✅
- Mixed RTL+LTR → alignment slightly off, readable ⚠️
- Null byte (`\x00`) in prompt → no crash; model receives sanitised input ✅
- Markdown in prompt (`**bold**`) → some rendered in user bubble (inconsistent) ⚠️
- HTML in user message → `<b>bold</b>` shown as plain text ✅ (XSS safe)
- Emoji-only prompt (50 emojis) → model responds correctly ✅

**Observations:**
- No character counter in input field — users don't know when they're approaching limits
- Very long prompts cause noticeable UI jank during paste operation

---
