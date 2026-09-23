# Agent team

I will use a four-agent custom team to build Mona's Project Pulse dashboard, coordinated through GitHub Copilot CLI in a Codespace.

- Orchestrator — model: Claude Opus 4.7 (copilot). Responsibility: coordinates the workflow, breaks the work into phases, delegates to specialist agents, and verifies that the pieces fit together. Definition: `.github/agents/orchestrator.agent.md`.
- Planner — model: Claude Opus 4.7 (copilot). Responsibility: researches the repository, reads the relevant docs and code paths, identifies constraints and edge cases, and produces the ordered implementation plan before coding starts. Definition: `.github/agents/planner.agent.md`.
- Designer — model: Gemini 3.1 Pro (copilot). Responsibility: shapes the dashboard UX and visual design, including accessibility, layout, hierarchy, styling, and responsive treatment for the Project Pulse experience. Definition: `.github/agents/designer.agent.md`.
- Coder — model: GPT-5.5 (copilot). Responsibility: implements the actual code, fixes bugs, builds logic, and adds runnable app support when needed for the dashboard. Definition: `.github/agents/coder.agent.md`.

Together, this team gives us planning, design, implementation, and orchestration in a single workflow, with each custom agent defined under `.github/agents/` and run from the GitHub Copilot CLI environment in the Codespace.
