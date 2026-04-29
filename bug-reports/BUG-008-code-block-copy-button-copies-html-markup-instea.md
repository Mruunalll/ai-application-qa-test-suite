## BUG-008 — Code block "Copy" button copies HTML markup instead of plain code on Firefox

**Title:** Code block "Copy" button copies HTML markup instead of plain code on Firefox
**Environment:** Firefox 125, Windows 11 — not reproducible on Chrome
**Severity:** Major | **Priority:** High

**Steps to Reproduce:**
1. Send prompt: "Show a JavaScript fetch example"
2. Response includes fenced code block
3. Click Copy button on code block in Firefox

**Expected Result:** Pure JavaScript code in clipboard (no HTML)
**Actual Result:** Clipboard contains `<pre><code class="language-js">...` — HTML markup copied; paste into code editor produces broken output

---
