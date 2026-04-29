# Charter 3: Mobile UX — iOS and Android Friction Points
**Mission:** Identify mobile-specific interaction bugs, keyboard behaviour, and native app vs web parity
**Area:** Mobile web (Safari) + Native app (iOS + Android)
**Duration:** 90 minutes, real devices

**Session Notes (iOS Safari):**
- Keyboard hides input + send button (BUG-005) ❌
- Double-tap to zoom on chat bubbles triggers zoom → hard to reverse ⚠️
- Copy of long response on iOS: selected text correctly ✅
- Share conversation link — iOS Safari share sheet works ✅
- Pinch to zoom disabled on chat — intentional but can frustrate users with small text ⚠️

**Session Notes (Android Chrome):**
- Input visible above keyboard ✅ (no BUG-005 equivalent)
- Autocorrect changes technical terms (e.g., "API" → "Api") — OS level, not app bug ⚠️
- Back hardware button in mid-chat → exits to conversation list (correct) ✅

**Session Notes (Native iOS App):**
- Haptic feedback on send ✅ (nice touch)
- Swipe left to delete conversation ✅
- Background → foreground (< 2 min): state preserved ✅
- Background → foreground (> 5 min): streaming response lost; blank bubble shown ⚠️

**Session Notes (Native Android App):**
- Background 2+ min → draft lost (BUG-011) ❌
- Notification taps open correct conversation ✅
- App does not use biometric auth option (Face ID/fingerprint for re-auth) — usability gap ⚠️

---
