# 📄 masterplan.md – Prompt Optimizer

## 🧠 App Overview and Objectives
Prompt Optimizer is a lightweight, educational web tool designed to help everyday AI users reduce the environmental impact of their prompts. By analyzing and highlighting high-energy keywords and offering more sustainable alternatives, the tool encourages climate-conscious behavior in AI usage. The app serves as both a practical utility and an awareness-building resource.

## 🎯 Target Audience
- Everyday AI users
- Climate-conscious tech enthusiasts
- Students and prompt engineers

## 🚀 Core Features and Functionality
- Single-page web app
- Paste/write prompt input field
- Analyze Prompt button triggers keyword analysis
- Inline highlighting of high- and low-energy keywords:
  - High-energy (orange)
  - Low-energy (green)
- Hoverable or tappable energy rating bars (⚡⚡⚡⚡⚪ scale)
- Click-to-apply keyword replacements
- Visual key/legend
- Modal tooltip explaining energy usage in AI
- Footer with link to supporting research

## 🛠️ High-Level Technical Stack Recommendations
- **Frontend:** Next.js 14, Tailwind CSS, shadcn/UI
- **Backend & DB:** Supabase (PostgreSQL + Functions)
- **CMS (optional):** Notion
- **Auth:** None for MVP

## 🗃️ Conceptual Data Model
**Keywords Table (Supabase)**
- `keyword` (text)
- `energy_score` (numeric or enum)
- `good_alternatives[]` (array of objects w/ energy delta)
- `medium_alternatives[]` (array of objects w/ energy delta)
- `category` (optional future metadata)

**Prompt Analysis (ephemeral)**
- Transient parsing only, no storage of user prompts in MVP
- Usage metrics (if tracked) anonymized and aggregated

## 🎨 User Interface Design Principles
- Clean, calm, and educational tone
- Mobile-first layout
- Use of cards, color-coded highlights, and clear typography
- Font: Inter
- Colors:
  - Primary: #4F46E5 (Indigo)
  - High-energy: #F97316 (Orange)
  - Low-energy: #22C55E (Green)
  - Backgrounds: #FFFFFF, #F9FAFB

## 🔐 Security Considerations
- No authentication in MVP
- Ensure prompt input is sanitized to prevent injection attacks
- Use Supabase RLS to protect keyword DB from external write access
- Analytics should remain anonymous

## 🧱 Development Phases or Milestones
**MVP (v0.1):**
- Static frontend with prompt parser and inlined keyword highlighting
- Supabase backend with keyword DB and simple parsing logic
- All-in-one landing page UI

**v1.0:**
- Add tooltip/modal education layer
- Track usage analytics anonymously
- Ability to view prompt history (if login added later)

**v2.0+ Ideas:**
- AI assistant for full prompt rewrites
- Export to Notion/GDocs/etc.
- Community-sourced keyword suggestions

## ⚠️ Potential Challenges and Solutions
- **Challenge:** Quantifying "energy usage" per keyword  
  *Solution:* Use relative scoring with visual scale to avoid overclaiming

- **Challenge:** Performance of real-time replacements in-browser  
  *Solution:* Keep DOM minimal and use lightweight rendering libraries

- **Challenge:** Educating users without overwhelming them  
  *Solution:* Keep messaging friendly, concise, and opt-in (via tooltip/modals)

## 🔮 Future Expansion Possibilities
- Full AI assistant for sustainable prompt rewriting
- Weekly sustainability reports for power users
- Open API for plugin use in other prompt editors
- Research collaborations with climate AI orgs
