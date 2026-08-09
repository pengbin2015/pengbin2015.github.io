---
title: "Code with Me or for Me? How Increasing AI Automation Transforms Developer Workflows"
date: 2026-08-06
description: "A summary of a controlled study comparing GitHub Copilot and OpenHands across realistic software-development tasks."
categories:
  - Research Notes
  - Human-AI Collaboration
  - AI Tools
---

**Paper URL:** [arXiv:2507.08149](https://arxiv.org/abs/2507.08149)

**arXiv subjects:** `cs.SE` (Software Engineering)

Coding agents promise more than code completion. They can inspect a repository, edit files, run commands, and attempt fixes on their own. The important question is not only whether they finish more work, but how they change the developer’s role.

Chen and colleagues compare GitHub Copilot with OpenHands in a controlled study of 20 developers. Each participant used both tools on realistic tasks involving research and analysis, feature work, and bug fixing. The study measured task correctness, active user effort, survey responses, and interaction traces.

Agents performed better on task correctness and reduced the time users spent actively working. They also helped participants complete some tasks that they could not complete with Copilot. The advantage is easy to understand: an agent can explore files, run tests, and carry out a sequence of changes without waiting for the user to request each step.

But less active effort is not the same as a better developer experience. Participants reported weaker understanding and control when working with the agent. Total elapsed time was not clearly better once the agent’s own work time was included. Satisfaction and flow also did not improve in step with correctness. A system can solve more of the task while leaving its user less certain about what happened and why.

The paper’s most useful contribution is its account of a workflow shift. With Copilot, the developer remains close to implementation: writing, selecting, adapting, and debugging code in small steps. With an agent, the developer spends more time specifying the task, monitoring progress, inspecting changes, giving feedback, and deciding when to intervene. The work moves from direct execution toward supervision.

That shift should not be mistaken for a complete account of expertise. The study lasts only a short time, uses one copilot and one agent, and includes a small, mostly student sample. It measures task completion more directly than code quality, maintainability, security, long-term learning, or professional judgement. The results therefore show a change in workflow, not whether developers become more skilled, less skilled, or differently skilled over time.

For teams adopting coding agents, the implication is clear: improving task success is necessary but insufficient. Developers need ways to inspect the agent’s reasoning, verify its changes, and retain control over important decisions. The most useful agent is not simply one that can act. It is one that makes its actions reviewable and supports the developer in supervising them well.

Future research should compare more tools with comparable underlying models, follow developers over longer projects, and measure verification behaviour directly. It should also examine outcomes that matter in production software: maintainability, security, integration, and the developer’s ability to explain and repair the result without the agent.
