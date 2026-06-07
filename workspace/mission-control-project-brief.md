# Mission Control – Project Brief

**Project name**
- **Enoch’s Command Center**

**What we’re building**
- A dark‑mode web dashboard that gives you an instant, calm, “mission‑control” view of your personal OpenClaw ecosystem. It shows a high‑level board with **Tasks, Calendar, Projects, Memory, Docs, Team/status,** and a 2‑D office view. You can drill down from the overview into detailed lists, code notes or GitHub status, while the UI stays minimal with deep navy background, amber accents and muted teal highlights.

**Why it matters**
- You’re juggling coding, research, career planning, and spiritual growth. A single screen that reflects the live state of all your agents, tasks and documents removes friction and keeps you focused on what matters.

**Screens to build first**
1. **Tasks** – Kanban board (backlog → in‑progress → done) pulling real OpenClaw tasks from the workspace.
2. **Calendar** – Calendar view of all cron jobs / scheduled agent actions, with status badges per agent.
3. **Projects** – Summary of each personal project with progress bar, linked docs, and associated tasks or docs.

**Agent crew + mission statement**
- **Enoch** – chief‑of‑staff, orchestrator, sees all data.
- **Solomon** – research & information gathering.
- **Bezalel** – code conversion & generation.
- **Nehemiah** – strategic planner & schedule optimizer.

> *“Enoch’s Command Center is a personal AI‑powered command hub that tracks goals, streamlines study and coding, keeps all documents up‑to‑date, and offers career coaching—calibrating my direction as new research or industry insights emerge.”*

**Visual direction**
- Dark navy background, warm amber accents, muted teal highlights.
- Clean sans‑serif typography.
- Modern, minimal UI: cards, status LEDs, subtle geometric accents.
- Subtle Christian undertone: a small tasteful biblical motif in the header if desired.

**Integrations (day one)**
- **Discord webhook** – push task updates, alerts.
- **GitHub** – pull repo status, PR info, and simple commit logs.

**Use real OpenClaw data from day one**
- The dashboard must query data from `~/.openclaw/workspace/`, `memory/YYYY‑MM‑DD.md`, `MEMORY.md`, `USER.md`, `AGENTS.md`, and `openclaw.json`.
- No mock data; the app must reflect the actual live state.

**Tech stack**
- **Framework**: Next.js (App Router) with **TypeScript**.
- **Styling**: Tailwind & shadcn/ui.
- **Runtime**: `localhost:3000` (or chosen port).
- **Data layer**: File‑based persistence (or lightweight SQLite, agent decides).

**Next step for Enoch**
1. Scaffold the project (create‑next‑app).
2. Install Tailwind, shadcn/ui.
3. Create the three core screen components and data hooks that read the workspace.
4. Hook up Discord webhook and GitHub API.
5. Commit the repo and push.
6. Run `npm run dev` locally, verify live sync, and review the dashboard.

---

*Give the brief to the agent, and they’ll start building the first phase. The first reply should be a description of what data they’ve discovered, any clarifying questions or a phased plan, not finished code.*