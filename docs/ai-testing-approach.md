# AI Testing Approach

## Testing Non-Deterministic Applications
AI applications differ from deterministic software because identical inputs do not guarantee identical outputs. This project therefore evaluates behaviour, validation, state handling, and user experience rather than the factual quality or exact wording of model-generated responses.

## What Can Be Tested Definitively
- Input validation for empty, whitespace-only, extremely long, and unsupported inputs
- UI state transitions such as streaming, stop generation, loading, and retry states
- File upload acceptance, rejection, and error messaging
- Session persistence, expiry, and multi-tab behaviour
- Error message presence and recoverability
- Cross-browser and mobile rendering consistency

## What Is Not Failed
- Exact generated response wording
- Subjective answer quality unless it affects visible UI behaviour
- Model factuality, which belongs to model evaluation rather than UI QA

## Exploratory Focus Areas
- State desynchronisation between concurrent tabs
- Streaming interruption and recovery
- Input sanitisation for HTML, script-like text, Unicode, RTL text, and emoji-only prompts
