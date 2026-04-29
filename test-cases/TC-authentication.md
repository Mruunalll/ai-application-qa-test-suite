# TC authentication

| TC ID | Module | Title | Preconditions | Test Steps | Expected Result | Priority | Severity |
|-------|--------|-------|---------------|------------|-----------------|----------|----------|
| TC-001 | Auth | Login with valid email + password | Account exists | 1. Go to chat.openai.com 2. Click Log in 3. Enter email + password 4. Submit | User authenticated; redirected to chat interface; conversation history visible | High | Critical |
| TC-002 | Auth | Login with incorrect password | Account exists | 1. Enter valid email 2. Enter wrong password 3. Submit | Error: "Wrong email or password" shown; account not locked after 1 attempt | High | Major |
| TC-003 | Auth | Session persists across browser tabs | Logged in | 1. Open new tab 2. Navigate to chat.openai.com | User still logged in; no re-auth required | Medium | Minor |
| TC-004 | Auth | Logout clears session | Logged in | 1. Click profile icon 2. Click Log out | Redirected to login page; back button does not return to authenticated state | High | Critical |
| TC-005 | Auth | Session expiry with pending typed prompt | Logged in; session nearing expiry | 1. Type long prompt in input 2. Wait for session to expire (do not submit) 3. Try to submit | User shown re-auth prompt; typed prompt preserved OR clearly warned before loss | High | Major |
