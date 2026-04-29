## BUG-002 — File upload silently drops files >25MB with no error message shown to user

**Title:** File upload silently drops files >25MB with no error message shown to user
**Environment:** Chrome 124, macOS Sonoma, ChatGPT Plus
**Severity:** Critical | **Priority:** High

**Steps to Reproduce:**
1. Click the paperclip attachment icon
2. Select a 30MB PDF file
3. Observe upload behaviour

**Expected Result:** Error message: "File size exceeds the 25MB limit. Please upload a smaller file."
**Actual Result:** File appears to upload (progress spinner shows briefly), then silently disappears. No error message. User assumes upload succeeded and asks questions about it — model responds as if no file was attached.

---
