# TC custom instructions

| TC ID | Module | Title | Preconditions | Test Steps | Expected Result | Priority | Severity |
|-------|--------|-------|---------------|------------|-----------------|----------|----------|
| TC-024 | Custom Instructions | Set custom instructions | Settings accessible | 1. Profile → Custom Instructions 2. Set "Always respond in bullet points" 3. Save 4. Start new chat 5. Ask open question | Response formatted in bullet points as instructed | High | Major |
| TC-025 | Custom Instructions | Instructions not applied after model switch | Custom instructions set; GPT-4o active | 1. Set custom instruction 2. Start chat with GPT-4o 3. Switch to GPT-3.5 mid-conversation 4. Send new message | Custom instructions still applied in new model context | High | Major |
| TC-026 | Custom Instructions | Disable custom instructions | Instructions set | 1. Go to Custom Instructions 2. Toggle OFF 3. Save 4. New chat 5. Ask same question | Response does not follow custom instructions; default format used | Medium | Major |
