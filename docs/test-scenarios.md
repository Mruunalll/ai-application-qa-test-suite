# High-Level Test Scenarios

## Scenarios

### Module: Authentication
- S01: Sign up with new email account
- S02: Sign up with existing email
- S03: Login with Google OAuth
- S04: Login with email + password
- S05: Logout and session cleared
- S06: Session auto-expiry behaviour
- S07: Concurrent sessions in two browsers

### Module: Chat Interface
- S08: Submit text prompt and receive response
- S09: Streaming response renders progressively
- S10: Stop generation mid-stream
- S11: Submit prompt immediately after stopping
- S12: Submit empty prompt (Enter with no text)
- S13: Submit whitespace-only prompt
- S14: Submit extremely long prompt (10,000+ characters)
- S15: Submit prompt with special characters and emojis
- S16: Submit code block and verify syntax highlighting in response
- S17: Copy response text to clipboard
- S18: Regenerate response

### Module: Conversation Management
- S19: Create new conversation
- S20: Rename conversation
- S21: Delete conversation
- S22: Archive conversation
- S23: Share conversation via link
- S24: Search past conversations
- S25: Sidebar conversation list scrolling (50+ chats)

### Module: Model Switching
- S26: Switch from GPT-3.5 to GPT-4o in active chat
- S27: Model persists across new conversations
- S28: GPT-4o-specific features visible only when GPT-4o selected

### Module: Custom Instructions
- S29: Set custom instructions and start new chat
- S30: Verify instructions applied in response
- S31: Disable custom instructions — verify not applied
- S32: Switch model while custom instructions active

### Module: File Upload
- S33: Upload valid PDF and ask questions about it
- S34: Upload image and request description
- S35: Upload file >25MB
- S36: Upload unsupported file type (.exe)
- S37: Upload corrupted PDF

### Module: Mobile
- S38: Chat input usable when keyboard open (iOS)
- S39: Chat input usable when keyboard open (Android)
- S40: Swipe to delete conversation (native app)
- S41: App background/foreground — chat state preserved

---
