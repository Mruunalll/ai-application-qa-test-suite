# TC chat interface

| TC ID | Module | Title | Preconditions | Test Steps | Expected Result | Priority | Severity |
|-------|--------|-------|---------------|------------|-----------------|----------|----------|
| TC-006 | Chat | Submit standard text prompt | Logged in | 1. Type "What is photosynthesis?" 2. Press Enter or click Send | Response streams progressively; formatting clean; no raw markdown symbols in output | High | Critical |
| TC-007 | Chat | Streaming response renders progressively | Logged in | 1. Send prompt expecting long response 2. Observe rendering | Text appears word-by-word or chunk-by-chunk; no full freeze until complete response | High | Major |
| TC-008 | Chat | Stop generation mid-stream | Response streaming | 1. Click Stop button during streaming | Generation halts immediately; partial response kept; input re-enabled | High | Critical |
| TC-009 | Chat | Stop button persists after completion | Response fully completed | 1. Send prompt 2. Wait for full response 3. Observe Stop button | Stop button disappears or becomes disabled after response completes | High | Major |
| TC-010 | Chat | Submit empty prompt (Enter key) | Input field empty | 1. Click chat input 2. Press Enter without typing | Nothing sent; no empty message created; input remains active | High | Major |
| TC-011 | Chat | Submit whitespace-only prompt | Input field active | 1. Type 5 spaces in input 2. Press Enter | No message sent; or spaces trimmed and treated as empty — no API call made | High | Major |
| TC-012 | Chat | Submit prompt with 10,000+ characters | Logged in | 1. Paste 10,000-character text into input 2. Submit | Either: message accepted and response generated; OR clear error with character limit shown | Medium | Major |
| TC-013 | Chat | Submit emoji-heavy prompt | Logged in | 1. Type "Tell me about 🐉🌍🎯🔥💡" 2. Send | Response generated correctly; emojis passed through without encoding errors | Medium | Minor |
| TC-014 | Chat | Submit prompt with HTML/script tags | Logged in | 1. Type `<b>Bold</b> and <script>alert(1)</script>` 2. Send | Tags treated as plain text in prompt; response not rendered as HTML; no XSS execution | High | Critical |
| TC-015 | Chat | Code block syntax highlighting | Logged in | 1. Ask "Show me a Python hello world" | Response contains fenced code block; syntax highlighted; Copy button present on code block | Medium | Minor |
| TC-016 | Chat | Copy button on code block | Response with code block visible | 1. Click Copy on code block | Correct code copied to clipboard; toast "Copied!" shown | Medium | Minor |
| TC-017 | Chat | Regenerate response | Response received | 1. Click "Regenerate" button below response | New response generated for same prompt; previous response replaced or appended | Medium | Minor |
