# Test Plan

## Project Overview

### Application Description
ChatGPT is an AI-powered conversational application by OpenAI. It allows users to interact with large language models (GPT-4o, GPT-4, GPT-3.5-turbo) through a chat interface. Features include multi-turn conversations, file uploads (PDF, images), web browsing, code interpreter, custom instructions, GPT model switching, and conversation management (rename, delete, share, archive). The application is available via web browser and native iOS/Android apps.

### Scope

#### ✅ In-Scope
- User authentication: sign-up, login, logout, session management
- Chat interface: text input, submission, streaming response, stop generation
- Conversation management: new chat, rename, delete, archive, share
- Model switching: GPT-4o vs GPT-3.5
- Custom Instructions: setup, apply, disable
- File upload: PDF analysis, image interpretation
- Prompt edge cases: empty, whitespace-only, very long, special characters, code blocks
- Mobile web and native app behaviour (iOS + Android)
- Usability: response formatting, markdown rendering, code block copy
- Accessibility: keyboard navigation, screen reader (basic check)

#### ❌ Out-of-Scope
- OpenAI API internals and model accuracy/hallucination measurement
- ChatGPT Plus/Team/Enterprise paid-tier exclusive features
- Plugin marketplace (deprecated)
- GPT Store / custom GPTs (separate QA scope)
- Penetration testing or jailbreak attempts
- DALL-E image generation

### Test Environment

| Category | Details |
|----------|---------|
| Browser (Web) | Chrome 124, Firefox 125, Safari 17, Edge 124 |
| OS | Windows 11, macOS Sonoma |
| Mobile — iOS | iPhone 14 (iOS 17.4), Safari + ChatGPT app |
| Mobile — Android | Samsung Galaxy S23 (Android 14), Chrome + ChatGPT app |
| Network | WiFi (100Mbps), 4G (throttled via DevTools) |
| Accounts | Free tier (GPT-3.5 default) + ChatGPT Plus test account |
| Screen Sizes | 1920×1080, 1440×900, 768px (tablet), 390×844 (iPhone 14) |

---

## Test Strategy

### Testing Types

| Type | Description |
|------|-------------|
| **Functional** | Verify all features (chat, upload, manage conversations) work correctly |
| **Regression** | Core flows re-verified after OpenAI deploys UI updates |
| **Exploratory** | Unscripted sessions: edge-case inputs, state management, session boundary |
| **Usability** | Nielsen heuristics: learnability, efficiency, error prevention, recovery |
| **Compatibility** | Cross-browser + iOS/Android native vs web |
| **Boundary Value** | Input length limits, file size limits, conversation turn limits |
| **Negative Testing** | Empty inputs, invalid file types, extremely long prompts, special/Unicode characters |
| **Session/State** | Behaviour after session timeout, multi-tab usage, back-button navigation |

### Approach
1. Map application features to test modules
2. Execute structured test cases across all modules
3. Run exploratory charters for high-risk areas (input handling, session, mobile)
4. Document all defects with screen recordings (Loom) and annotated screenshots
5. Usability evaluation using 10 Nielsen heuristics as a post-test pass
6. Mobile testing on real devices; not only DevTools emulation

### Risk Areas & Mitigation

| Risk | Likelihood | Mitigation |
|------|-----------|------------|
| UI state desync after streaming | High | Test stop/resume, rapid navigation during stream |
| Session expiry UX — user loses draft | High | Test timeout behaviour with pending prompt typed |
| File upload silent failures | High | Test max size, wrong formats, corrupted files |
| Mobile keyboard obscuring input | High | Test on real iOS + Android hardware |
| Custom instructions not applied correctly | Medium | Verify instructions in new chat vs existing chat |
| Model switch mid-conversation losing context | Medium | Test explicit model switches during long chats |
| Markdown/code rendering inconsistencies | Medium | Test across browsers for render parity |

---
