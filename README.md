# The Studio — Agent Library

A shared team of AI agents for software development projects. Each agent has a defined role, personality, and set of outputs. Every project you work on references this same library — update an agent here and the change applies everywhere.

---

## Meet the Team

| Name | Role | Invoke As |
|---|---|---|
| **Atlas** | Orchestrator | `@atlas` or `@orchestrator` |
| **Pedro** | Product Manager | `@pedro` or `@pm` |
| **Beatrice (B)** | Business Analyst | `@beatrice`, `@b`, or `@ba` |
| **Uma** | UX / Design | `@uma`, `@ux`, or `@design` |
| **Archie** | Principal Architect | `@archie` or `@architect` |
| **Stephanie** | Staff Engineer | `@stephanie` or `@staff` |
| **Ferdinand** | Frontend Engineer | `@ferdinand` or `@frontend` |
| **Brandi** | Backend Engineer | `@brandi` or `@backend` |
| **Knox** | Security | `@knox` or `@security` |
| **Pippa** | DevOps / Platform | `@pippa` or `@devops` |
| **Quincy** | QA Engineer | `@quincy` or `@qa` |
| **William** | Technical Writer | `@william` or `@writer` |
| **Dex** | Data Agent (v2) | `@dex` or `@data` |

---

## Quick Start

**Not sure who to talk to?** Always start with Atlas.

```
@atlas I have a new idea I want to build
```

**Have an idea to shape?** Go to Pedro.

```
@pedro I want to add a feature that lets users...
```

**Want to check project status?**

```
@atlas where do we stand on the project?
```

**Want the team to run autonomously toward a goal?**

```
/goal [describe what you want to accomplish this session]
```

---

## Repo Structure

```
/agents
  /core
    atlas.md
    pedro.md
    beatrice.md
    uma.md
    archie.md
    stephanie.md
    ferdinand.md
    brandi.md
    knox.md
    pippa.md
    quincy.md
    william.md
    dex.md
  /aliases
    orchestrator.md
    pm.md
    ba.md
    ux.md
    design.md
    architect.md
    staff.md
    frontend.md
    backend.md
    security.md
    devops.md
    qa.md
    writer.md
    data.md

/framework
  how-it-works.md

README.md
```

---

## How Ideas Flow Through the Team

```
You → Atlas → Pedro → Beatrice / Uma / Archie → Stephanie → Ferdinand / Brandi → Quincy / Knox → William
```

See `/framework/how-it-works.md` for the full workflow, operating modes, project file structure, and cost rules.

---

## Project Files

Each project maintains its own set of documents that the team keeps updated:

```
/product
  prd.md
  /specs
  /strategy
  /design

/technical
  architecture.md
  backlog.md
  test-log.md
  security-log.md
  devops.md

project-hq.md       ← master project status (Atlas)
next-steps.md       ← session handoff (Atlas)
```

---

## Ground Rules

- **Free by default** — the team never commits to paid services without your explicit approval
- **Atlas always updates `next-steps.md`** at the end of every session so you can always pick right back up
- **Every agent has a role alias** — you never need to remember a name to find the right person
- **All documents have changelogs** — nothing is edited silently
- **This repo is version controlled** — update any agent and roll back if needed

---

## Adding a New Agent

See `/framework/how-it-works.md` for instructions on adding new agents to the library.
