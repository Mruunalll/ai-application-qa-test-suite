## BUG-004 — Custom instructions not applied to messages sent immediately after model switch in active session

**Title:** Custom instructions not applied to messages sent immediately after model switch in active session
**Environment:** Chrome 124, ChatGPT Plus (GPT-4o), Custom Instructions enabled
**Severity:** Major | **Priority:** High

**Steps to Reproduce:**
1. Set custom instruction: "Always start responses with 'As instructed:'"
2. Start new chat with GPT-4o
3. Confirm instruction is applied (first message includes "As instructed:")
4. Switch model to GPT-3.5 using model selector
5. Send new message in same conversation

**Expected Result:** "As instructed:" prefix still present — custom instructions apply regardless of model
**Actual Result:** First message after model switch does NOT include the prefix; custom instructions appear reset for that turn

---
