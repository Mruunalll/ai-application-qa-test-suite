# TC conversation management

| TC ID | Module | Title | Preconditions | Test Steps | Expected Result | Priority | Severity |
|-------|--------|-------|---------------|------------|-----------------|----------|----------|
| TC-018 | Conversations | Rename conversation | Conversation exists in sidebar | 1. Hover over conversation in sidebar 2. Click pencil/edit icon 3. Type new name "Test QA Chat" 4. Press Enter | Conversation renamed immediately in sidebar; name persists after page refresh | High | Major |
| TC-019 | Conversations | Delete conversation | Conversation exists | 1. Hover over conversation 2. Click delete icon 3. Confirm deletion | Conversation removed from list; if it was open, new chat starts | High | Major |
| TC-020 | Conversations | Share conversation via link | Conversation with messages | 1. Open conversation 2. Click Share button 3. Generate link 4. Open link in incognito | Shared link opens conversation in read-only view; no login required to view | Medium | Major |
| TC-021 | Conversations | Rename — verify immediate UI update | Conversation exists | 1. Rename conversation 2. Observe sidebar before page refresh | Name updates instantly in sidebar without page reload | High | Major |
