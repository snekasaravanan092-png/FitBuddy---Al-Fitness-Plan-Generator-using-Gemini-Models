# FitBuddy — Project Development Phase

## Page 12 — User-Side Requirements and Interface

### Input Screen
The application collects:
- Name
- Age
- Gender
- Height
- Weight
- Goal
- Fitness level
- Training days per week
- Equipment
- Diet preference
- Optional injuries/notes

### Actions
- **Generate with Gemini**
- **Generate demo plan**

The result panel displays the generated plan without requiring the user to navigate to another page.

---

## Page 13 — Technology Stack

### Frontend
- HTML
- CSS
- JavaScript

### AI / API
- Google Gemini
- Gemini `generateContent` REST API
- JSON request/response format

### Development Tools
- VS Code
- Node.js / Python as project development tools
- Git and GitHub

### Services
- Google AI Studio
- Gemini API key
- Hosting such as Netlify or Vercel

### Hardware
- Laptop/PC
- At least 4 GB RAM
- Internet connection
- Modern web browser

---

## Page 14 — Architecture and Request Flow

### Three-Layer Concept

**Presentation Layer**
- Web form
- Loading state
- Generated-plan display

**Application Layer**
- Validate inputs
- Calculate basic profile values
- Build the prompt
- Manage the Gemini request
- Format the result

**AI Layer**
- Gemini model receives the structured profile and instructions.
- Gemini returns the requested JSON fitness plan.

### Request Flow
1. Browser collects user details.
2. Application validates the details.
3. Application creates the prompt.
4. Gemini receives the request.
5. Gemini returns structured JSON.
6. Application renders workouts, meals, statistics, and tips.
