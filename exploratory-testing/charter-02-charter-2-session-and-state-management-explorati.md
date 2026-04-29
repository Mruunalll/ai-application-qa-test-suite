# Charter 2: Session and State Management Exploration
**Mission:** Find state bugs around multi-tab use, session expiry, model switching, and navigation
**Area:** Authentication boundary → Conversation state → Model state
**Duration:** 90 minutes

**Session Notes:**
- Two tabs, same account → both work independently ✅
- Delete conversation in Tab 1 → Tab 2 still shows it until refresh ⚠️
- Rename in Tab 1 → Tab 2 shows old name (BUG-001 confirmed in multi-tab) ❌
- Session expires → typing in input → submit → silent failure; no prompt to re-auth ❌
- Back button from active chat → goes to previous chat correctly ✅
- Rapid model switching (5 times in 3 seconds) → no crash; final model applied ✅
- Switch model → send message → switch back quickly → response attributed to wrong model indicator ⚠️
- Open 6 chat tabs simultaneously → performance degraded; 2 tabs show spinner indefinitely ⚠️

**Edge Cases Found:**
- Session expiry during streaming: response silently cut off; no error shown; partial response stuck with "typing" indicator permanently
- Multi-tab deletion inconsistency is a real UX problem for power users

---
