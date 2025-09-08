# AI Dev Project Setup Prompts — Summary

> A concise, step‑by‑step markdown guide to bootstrap PRD, UX, and SRS docs with LLMs.

---

## 1) Why this matters
- Help your LLM grasp scope and constraints
- Force you (product owner) to clarify tradeoffs
- Surface alternative approaches and new ideas

---

## 2) Quick flow (at a glance)

| Step | Prompt & Role | Inputs you provide | Primary Outputs | Where it’s used next |
|---|---|---|---|---|
| 1 | **Product Expert → PRD** | Idea description + answers to clarifying questions | Product Requirements Document (PRD) in MD | Attach to UX prompt |
| 2 | **UX Designer → UI Doc** | PRD + persona details + preferences | User Interface Design Doc (MD) | Attach to Software Architect prompt |
| 3 | **Software Architect → SRS** | PRD + UI Doc + your dev skills/tools | Software Requirements Spec (SRS) in MD | Hand to engineering/codegen |

---

## 3) Minimal operating instructions
1. Paste the **Product Expert Prompt** into your LLM and answer its questions.
2. Paste the PRD output + **UX Prompt** into a new chat. Answer persona/brand questions. Approve one of the options; get the final **UI Design Doc**.
3. Paste **PRD + UI Doc + Software Architect Prompt** into a new chat. Answer stack/skills questions to get the **SRS**.
4. Save `01_PRD.md`, `02_UI.md`, `03_SRS.md` in `/docs` for reuse.

---

## 4) Prompts (drop‑in)

### 4.1 Product Expert Prompt → PRD
**Context**: You are an expert product manager. Co‑create a concise PRD in markdown so other LLMs understand the product.

**Instructions**:
1) Ask me to explain the project idea.
2) If details are missing (see headings), ask targeted follow‑ups.
3) Output a PRD using these headings:
   - Elevator Pitch (1 paragraph)
   - Who is this app for
   - Functional Requirements
   - User Stories
   - User Interface (high level)

**Owner prep**: Have a 3–5 sentence idea, target users, MVP scope, and constraints ready.

---

### 4.2 UX Designer Prompt → UI Design Doc
**Context**: You are an expert UX designer. Produce a concise UI Design Doc in markdown.

**Inputs**: 1) PRD 2) current chat

**Instructions**:
1) If PRD missing, ask for it or help create it.
2) Ask persona/brand/theme questions if unclear.
3) Propose **3 UI options** (natural language only).
4) Ask me to choose/amend.
5) Output the final UI doc with these headings:
   - Layout Structure
   - Core Components
   - Interaction patterns
   - Visual Design Elements & Color Scheme
   - Mobile/Web/Desktop considerations
   - Typography
   - Accessibility

---

### 4.3 Software Architect Prompt → SRS
**Context**: You are an expert software architect. Create a concise SRS in markdown.

**Inputs**: 1) PRD 2) UI Design Doc

**Also ask**: My existing skillset and preferred frameworks/languages.

**Output headings (exact)**:
- System Design
- Architecture pattern
- State management
- Data flow
- Technical Stack
- Authentication Process
- Route Design
- API Design
- Database Design ERD

---

## 5) File structure & naming
```
/docs
  01_PRD.md
  02_UI.md
  03_SRS.md
  README.md (this quick guide)
```

---

## 6) Owner checklist (copy/paste)
- [ ] I can explain the product in 5 sentences
- [ ] I know the primary user persona(s)
- [ ] I listed MVP features vs. later
- [ ] I chose 1 of the 3 UI options and documented amendments
- [ ] I confirmed my stack preferences and constraints
- [ ] I saved PRD/UI/SRS as markdown in `/docs`

---

## 7) Notes on examples
- The included **Levercast** examples show ideal PRD, UX, and SRS shapes. Use them as scaffolds; swap content for your app.
- Keep outputs concise; depth grows as questions are answered.

---

## 8) Tips for better outputs
- Answer with specifics: entities, limits, success metrics, non‑goals
- Keep the LLM focused by pinning headings
- Separate chats per role to avoid context contamination
- Save every output for reuse in the next step

---

## 9) Next
- Start at **4.1 Product Expert Prompt** and proceed.

