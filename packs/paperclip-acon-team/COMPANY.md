---
name: ACON Agent Organization
slug: acon-agent-organization
---

# ACON Agent Organization

Project-agnostic ACON agent organization. Task assignments must provide the exact project, repository, task scope, acceptance criteria, and verification; this package creates no project/workspace configuration.

## Roster and reporting chart

All roles are intended to be registered in this organization. The orchestrator is the sole root; every other role reports directly to it. The roster is descriptive package data, not a Paperclip ACL. Verify actual registered identity, membership, and ownership from authoritative Paperclip records before delegation.

| ID | Role | Reports to | Canonical ACON source mapping |
|---|---|---|---|
| `orchestrator` | ACON Orchestrator | — | `AGENTS.md` |
| `scout` | ACON Scout | orchestrator | `.agents/reference/crew/scout.md` |
| `researcher` | ACON Researcher | orchestrator | `.agents/reference/crew/researcher.md` |
| `oracle` | ACON Oracle | orchestrator | `.agents/reference/crew/oracle.md` |
| `worker` | ACON Worker | orchestrator | `.agents/reference/crew/worker.md` |
| `ship` | ACON Ship | orchestrator | `.agents/reference/crew/ship.md` |
| `code-reviewer` | ACON Code Reviewer | orchestrator | `.agents/reference/crew/code-reviewer.md` |
| `reviewer` | ACON Reviewer | orchestrator | `.agents/reference/crew/reviewer.md` |
| `security-reviewer` | ACON Security Reviewer | orchestrator | `.agents/reference/crew/security-reviewer.md` |
| `gitops` | ACON GitOps | orchestrator | `.agents/reference/crew/gitops.md` |
| `frontend-engineer` | ACON Frontend Engineer | orchestrator | `.agents/skills/engineering/frontend-conventions/SKILL.md`, `.agents/skills/design/interface-design/SKILL.md` |
| `backend-engineer` | ACON Backend Engineer | orchestrator | `.agents/skills/engineering/api-design/SKILL.md`, `.agents/skills/engineering/domain-modeling/SKILL.md` |
| `database-engineer` | ACON Database Engineer | orchestrator | `.agents/skills/engineering/zero-downtime-migrations/SKILL.md`, `.agents/skills/engineering/domain-modeling/SKILL.md` |
| `ui-ux-designer` | ACON UI/UX Designer | orchestrator | `.agents/skills/design/interface-design/SKILL.md`, `.agents/skills/design/craft/anti-ai-slop.md`, `.agents/skills/design/craft/state-coverage.md` |
| `qa-engineer` | ACON QA Engineer | orchestrator | `.agents/skills/engineering/tdd/SKILL.md`, `.agents/skills/engineering/diagnosing-bugs/SKILL.md` |
| `performance-engineer` | ACON Performance Engineer | orchestrator | `.agents/skills/engineering/diagnosing-bugs/SKILL.md`, `.agents/skills/engineering/codebase-design/SKILL.md` |
| `devops-engineer` | ACON DevOps Engineer | orchestrator | `.agents/skills/security-devops/shell-scripting/SKILL.md`, `.agents/skills/security-devops/security-audit/SKILL.md` |

## Operating and safety boundary

No auto-hire, cross-team task/agent modification, cross-team assignment, or nested orchestration is authorized by this package. Non-orchestrator agents are not coordinators. Prompt text and reportsTo links do not enforce permissions, team ownership, workspace isolation, or conversation isolation. Captain approval remains required for gated operations. The package contains no projects, tasks, routines, skills, environment inputs, secrets, workspace commands, or repository paths.

Agent heartbeat is configured disabled in the portable extension. This does not prove that all wakeups are disabled or that an imported agent has paused status. Import must be submitted through a supported UI/API request with `pauseAutomations: true`, then the owner must verify resulting status and automation state. The ZIP itself cannot set import status.

An empty declared permission map/grant list does not prove zero effective permissions: Paperclip may apply importer/company defaults. Inspect effective permissions after import in a separately authorized disposable company before activation.

## Source provenance and license

Role adaptations map to the ACON crew personas and skill references listed above. ACON authority and safety wording remains ACON policy; no upstream runtime, tools, fixed provider catalog, terminal recipe, or permissions are adopted. Capability/verification reconciliation is informed by Fleet revision `0af843fa2c92413ea16c50e50bd8a9e24f1d1995` as ideas only. This attribution is not an authorship claim for the full ACON content. The following MIT notice applies to adapted source portions, not the entire ACON repository:

```text
MIT License

Copyright (c) 2025 Addy Osmani

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
