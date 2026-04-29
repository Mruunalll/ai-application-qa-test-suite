# TC model switching

| TC ID | Module | Title | Preconditions | Test Steps | Expected Result | Priority | Severity |
|-------|--------|-------|---------------|------------|-----------------|----------|----------|
| TC-022 | Model Switching | Switch GPT-3.5 → GPT-4o | Plus account; active conversation | 1. In active chat, click model selector 2. Switch to GPT-4o | Model switches; next response uses GPT-4o; model indicator updates in UI | High | Major |
| TC-023 | Model Switching | Model selection persists to new chat | GPT-4o selected | 1. Select GPT-4o 2. Start new conversation | New chat opens with GPT-4o pre-selected | Medium | Minor |
