# Requirements Traceability Matrix

## RTM

| Requirement ID | Requirement Description | Test Case IDs | Status |
|----------------|------------------------|---------------|--------|
| REQ-001 | User can log in with email/password and OAuth | TC-001, TC-002 | ✅ Pass |
| REQ-002 | Logout clears session completely | TC-004 | ✅ Pass |
| REQ-003 | Session expiry handled gracefully | TC-005 | ❌ Fail (silent failure) |
| REQ-004 | Chat interface accepts and processes text prompts | TC-006 | ✅ Pass |
| REQ-005 | Streaming response renders progressively | TC-007 | ✅ Pass |
| REQ-006 | Stop generation works mid-stream | TC-008 | ✅ Pass |
| REQ-007 | Stop button disabled after completion | TC-009 | ❌ Fail (BUG-003) |
| REQ-008 | Empty prompt not submitted | TC-010, TC-011 | ❌ Fail (BUG-009) |
| REQ-009 | Long prompts handled without crash | TC-012 | ✅ Pass |
| REQ-010 | HTML/script input sanitised | TC-014 | ✅ Pass |
| REQ-011 | Code blocks render with syntax highlight + copy | TC-015, TC-016 | ❌ Fail (BUG-008 - Firefox) |
| REQ-012 | Conversations can be renamed | TC-018, TC-021 | ❌ Fail (BUG-001) |
| REQ-013 | Conversations can be deleted | TC-019 | ✅ Pass |
| REQ-014 | Conversations shareable via link | TC-020 | ❌ Fail (BUG-006 - 404 after delete) |
| REQ-015 | Model switching works correctly | TC-022, TC-023 | ✅ Pass |
| REQ-016 | Custom instructions applied consistently | TC-024, TC-025, TC-026 | ❌ Fail (BUG-004) |
| REQ-017 | PDF file upload and analysis works | TC-027 | ✅ Pass |
| REQ-018 | File size limit enforced with clear error | TC-029 | ❌ Fail (BUG-002) |
| REQ-019 | Unsupported file types rejected | TC-030 | ✅ Pass |
| REQ-020 | Mobile input not obscured by keyboard | TC-032 | ❌ Fail (BUG-005 - iOS Safari) |

---
