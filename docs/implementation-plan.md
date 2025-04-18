# 📄 implementation-plan.md – Prompt Optimizer

## 🧱 Step-by-Step Action Plan

### Phase 1 – MVP Foundation
**Goal:** Launch a single-page, interactive prompt analysis tool with inline keyword suggestions.

1. **Project Setup**
   - Create Next.js 14 app with Tailwind CSS and shadcn/UI
   - Set up GitHub repo and deployment via Vercel

2. **UI Layout & Styling**
   - Build input section with header, input box, and Analyze button
   - Add legend for visual cues and footer link to research

3. **Keyword Highlighting Engine**
   - Design frontend parsing function to identify keywords from Supabase
   - Apply inline highlighting (green/orange) and attach tooltips/modals

4. **Supabase Backend**
   - Set up database table with keywords, scores, and alternatives
   - Use Supabase Edge Functions to handle keyword matching logic

5. **Click-to-Replace Functionality**
   - Enable users to apply alternative words via click
   - Re-render prompt preview with updated keywords

6. **Analytics Layer (Optional in MVP)**
   - Add anonymous usage tracking (prompt length, keyword frequency)

7. **Deploy & Test**
   - Cross-browser testing (desktop & mobile)
   - Internal QA + early feedback from test users

---

### Phase 2 – Educational Enhancements
**Goal:** Deepen the tool’s impact with supporting context and smarter UX.

1. Add modal or tooltip explaining AI energy consumption  
2. Consider optional onboarding hover for new users  
3. Improve keyword replacement logic with minor NLP boosts (e.g. word stems)  

---

### Phase 3 – Foundation for AI Assistant
**Goal:** Structure code to allow future addition of a full prompt rewrite assistant.

1. Modularize parsing and replacement logic  
2. Add API endpoint placeholder for rewrite suggestions (OpenAI or fine-tuned model)  
3. Begin logging replacement behavior for training insights  

---

## ⏳ Timeline (Rough Estimates)
- **Week 1:** Setup + UI Layout  
- **Week 2:** Supabase integration + highlighting engine  
- **Week 3:** Keyword suggestions + click-to-replace logic  
- **Week 4:** Polish, test, and deploy  

---

## 👥 Team Recommendations (if any)
- 1 Frontend Dev (Next.js + Tailwind)  
- 1 Backend Dev (Supabase, edge functions)  
- Optional: 1 Product Designer (for future polish and educational UX)  

---

## 🧩 Optional/Deferred Tasks
- CMS integration (Notion or markdown-based)  
- Export/share optimized prompts  
- Account system or saved prompt history  
