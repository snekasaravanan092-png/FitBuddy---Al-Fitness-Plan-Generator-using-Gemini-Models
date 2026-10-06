# FitBuddy — Project Testing

## Page 15 — Testing Strategy

### Input Validation Tests
Test that:
- Age accepts values from 14 to 90 in the current implementation.
- Height accepts values from 120 to 230 cm.
- Weight accepts values from 30 to 250 kg.
- Invalid values produce a visible error instead of generating a plan.

### API Tests
Verify:
- Missing API key is handled.
- A valid Gemini response is parsed.
- Empty AI responses are handled.
- Failed HTTP requests display an error message.
- The UI returns to an usable state after an error.

### UI Tests
Check:
- Input labels are readable.
- Buttons are usable.
- Loading state appears during generation.
- Generated plan is visible and structured.
- Mobile layout changes to a single-column layout.

---

## Page 16 — Functional Test Cases and Expected Results

| Test Case | Action | Expected Result |
|---|---|---|
| Valid demo input | Click Generate demo plan | Demo plan appears |
| Missing Gemini key | Click Generate with Gemini | Key-required error appears |
| Invalid age | Enter age outside allowed range | Validation error appears |
| Invalid height | Enter height outside allowed range | Validation error appears |
| Invalid weight | Enter weight outside allowed range | Validation error appears |
| API failure | Use an invalid/unavailable request | Error message appears |
| Valid Gemini request | Submit valid profile with key | AI plan appears |
| Mobile screen | Open on narrow viewport | Layout becomes single column |
| Print | Click Print or save as PDF | Browser print dialog is opened |

### Testing Goal
The application should fail clearly and safely rather than displaying incomplete or misleading output.
