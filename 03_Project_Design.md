# FitBuddy — Project Design Phase

## Page 7 — Input-to-Output Mapping

| User Input | Used For | Output |
|---|---|---|
| Age, gender | Fitness profile and basic safety context | Suitable exercise intensity |
| Height, weight | BMI and calorie estimation | Daily calorie target |
| Goal | Plan direction | Workout type and diet focus |
| Fitness level | Difficulty selection | Beginner/intermediate/advanced approach |
| Days per week | Weekly structure | Number of training days |
| Equipment | Exercise selection | Home/gym-compatible exercises |
| Diet preference | Meal selection | Matching meal plan |
| Notes/injuries | Personal constraints | Prompt instructions to respect notes |

---

## Page 8 — Data Flow Design

### High-Level Flow

**User → FitBuddy Web App → Gemini API → FitBuddy Web App → User**

1. The user enters profile information.
2. FitBuddy validates the values.
3. The application calculates BMI and an estimated daily calorie target.
4. A structured prompt is prepared.
5. Gemini generates the workout and meal plan.
6. FitBuddy parses the JSON response.
7. The result is displayed as a weekly workout, daily meals, and tips.

### Main Data Elements
- User profile
- Generated prompt
- Gemini response
- Weekly workout plan
- Meal plan
- Fitness tips

---

## Page 9 — Requirement and System Design

### Functional Requirements
- Collect user details.
- Validate age, height, and weight.
- Build a structured Gemini prompt.
- Generate a workout and diet plan.
- Display the plan in a readable format.
- Allow demo-plan generation without an API key.
- Allow printing/saving the displayed plan as PDF through the browser.

### Non-Functional Requirements
- Fast response when the AI service responds normally.
- Simple, mobile-friendly UI.
- Safe handling of the API key in the current browser-based implementation.
- Readable and maintainable code.
- Clear error messages when generation fails.

### Design Principle
The interface should minimise the number of steps between entering a profile and viewing the generated plan.
