# How It Works — The Agent Framework

This document explains how the agent team works together, how ideas flow through the system, and how to get the most out of working with this team.

---

## The Big Picture

This is a shared agent library — a team of specialists, each with a defined role, personality, and set of outputs. Every project you work on can reference this same team. When you update an agent's instructions here, the update applies everywhere.

Think of it like a real software studio, except the whole team is always available, always in context, and always focused on your project.

---

## How an Idea Becomes a Product

```
You → Atlas → Pedro → Beatrice / Uma / Archie → Stephanie → Ferdinand / Brandi → Quincy / Knox → William
```

### 1. You have an idea
Bring it to **Atlas** (`@atlas`). He's your chief of staff. He'll do a quick gut check, align on goals, and hand you off to the right person.

### 2. Pedro shapes it into a PRD
**Pedro** (`@pedro`) interviews you — one or two questions at a time — and turns your idea into a Product Requirements Document. He phases large ideas into manageable chunks and keeps the PRD updated as the project evolves.

### 3. The specialists weigh in
Once the PRD is ready, Pedro and Atlas trigger:
- **Beatrice** (`@b`) — validates the idea with market research and competitive analysis
- **Uma** (`@uma`) — defines the UX, user flows, and design system
- **Archie** (`@archie`) — designs the technical architecture and system design

### 4. Stephanie builds the backlog
**Stephanie** (`@stephanie`) takes everything from the PRD, architecture, and design and turns it into a clear, prioritized backlog of issues and tasks. She also brings in **Knox** (`@knox`) before major features begin to catch security concerns early.

### 5. The engineers build
- **Ferdinand** (`@ferdinand`) builds the frontend UI
- **Brandi** (`@brandi`) builds the backend APIs and data layer
- They collaborate on connectivity before handing off to QA

### 6. Quincy, Knox, and Uma review
- **Quincy** (`@quincy`) runs comprehensive tests and documents everything in the test log
- **Knox** (`@knox`) conducts a security review after each major feature
- **Uma** (`@uma`) conducts a design review of any frontend work, checking for consistency with the design guide
- All three surface findings as clearly documented issues in the backlog for the engineers to resolve

### 7. William documents
**William** (`@william`) can be triggered at any point to polish documentation, add plain-language callouts, and make sure everything is readable by the whole team.

### 8. Atlas keeps track of everything
**Atlas** maintains `project-hq.md` and `next-steps.md` throughout. At the end of every session, he updates `next-steps.md` so you can always pick right back up where you left off.

---

## Operating Modes

### 🚀 Autopilot Mode
Set a goal and let Atlas run the team. Use `/goal [description]` or tell Atlas directly. He'll orchestrate the workflow end to end and check in at key decision points.

Best for: when you want to make fast progress and trust the team to move.

### 🧭 Co-pilot Mode
Work alongside the team, invoking agents directly as you need them. Atlas advises and routes but you're in the driver's seat.

Best for: when you want to stay close to the work and make decisions as you go.

---

## Pre-Flight Check

At the start of any autopilot session, Atlas will run a quick pre-flight:
1. What's the goal for this session?
2. Any cost constraints or new context?
3. Quick sync with Pedro to confirm alignment with the PRD

---

## Project File Structure

Every project that uses this agent team should maintain the following structure:

```
/product
  prd.md                        ← Pedro maintains
  /specs
    feature-name.md             ← Pedro maintains, one per feature
  /strategy
    market-research.md          ← Beatrice maintains
    competitive-analysis.md     ← Beatrice maintains
    product-strategy.md         ← Beatrice maintains
  /design
    design-guide.md             ← Uma maintains
    user-flows.md               ← Uma maintains

/technical
  architecture.md               ← Archie maintains
  backlog.md                    ← Stephanie maintains
  test-log.md                   ← Quincy maintains
  security-log.md               ← Knox maintains
  devops.md                     ← Pippa maintains
  data-notes.md                 ← Dex maintains (when needed)

project-hq.md                   ← Atlas maintains (master status)
next-steps.md                   ← Atlas maintains (session handoff)
```

---

## Cost Rules

The team defaults to free and open source tools at all times. No agent will approve or implement a paid service without your explicit sign-off. Atlas enforces this during the pre-flight check and throughout the build. When a paid option comes up, the team will flag it and propose a free alternative while waiting for your decision.

---

## Updating the Team

To update an agent, edit their markdown file in this repo. The change applies to every project that references this library. Use git history to track what changed and roll back if needed.

---

## Adding a New Agent

1. Create a new file in `/agents/core/` following the same structure as existing agents
2. Add an alias file in `/agents/aliases/` for their role name
3. Update this document and the README roster
4. Tag Atlas so he knows a new team member has joined
