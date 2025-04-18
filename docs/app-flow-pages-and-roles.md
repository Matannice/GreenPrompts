# 📄 app-flow-pages-and-roles.md – Prompt Optimizer

## 🧭 Core Page: Single Landing Page
All interactions and content occur within a single-page layout.

### Page Structure & Flow
1. **Header**
   - Value proposition: “Reduce the energy impact of your AI prompts — one word at a time.”
   - Lightweight logo/branding

2. **Prompt Input Section**
   - Textarea for prompt input
   - Analyze button

3. **Results Display**
   - Parsed prompt with inline highlighting
   - Clickable keyword replacements
   - Tooltip with alternative suggestions
   - Energy bar for each keyword (⚡ scale)

4. **Visual Key / Legend**
   - Color explanation (orange = high, green = low)
   - Explanation of energy rating bars

5. **Footer**
   - Link to supporting research (e.g., arXiv paper)
   - Tiny credits / built-by blurb

6. **Modal or Tooltip (Optional)**
   - Education-focused, explaining energy impact of language models

---

## 👤 User Roles & Access

### General User (Anonymous)
- Can input prompt and run analysis
- Can see keyword scores and replacements
- Can replace keywords inline (ephemeral)
- No login required

### Admin / Developer (Internal Use Only)
- Can update keyword list and energy metadata in Supabase
- Access to internal analytics (if implemented)

---

## 🔄 User Flow

1. User lands on homepage  
2. Pastes or types prompt into input box  
3. Clicks \"Analyze Prompt\"  
4. Prompt is parsed and returned with inline feedback  
5. User clicks replacements as desired  
6. User copies optimized prompt (optional)  
7. User may explore legend or tooltip for deeper learning  

---

## 📌 Notes on Future Roles

If login is added later, roles might expand to include:
- Registered user with prompt history
- Researchers with access to anonymized analytics
- Moderators for keyword submission review
