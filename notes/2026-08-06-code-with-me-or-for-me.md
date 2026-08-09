---
title: "Reading Session - Code with Me or for Me?"
date: 2026-08-06
description: "Reading notes on how increasing AI automation changes developer workflows, effort, and control."
categories:
  - Research Notes
  - Human-AI Collaboration
  - AI Tools
---

# Reading session - Code with Me or for Me?

**Paper:** Valerie Chen, Ameet Talwalkar, Robert Brennan, and Graham Neubig, *Code with Me or for Me? How Increasing AI Automation Transforms Developer Workflows* (CHI '26, 2026)

**Session date:** 2026-08-06  
**Method:** Three-pass paper-reading method  
**Progress:** Pass 1 and Pass 2 complete. Paused before Pass 3.

## Pass 1: screening

- **Paper type:** Controlled empirical user study comparing developer workflows with AI copilots and coding agents.
- **Domain:** Human-computer interaction, software engineering, AI-assisted programming, Human-GenAI collaboration.
- **Problem:** How increasingly autonomous AI coding tools change developer productivity, user experience, and interaction patterns compared with copilots.
- **Motivation:** Developers are moving from copilot-style tools toward coding agents, but human-in-the-loop evidence remains limited.
- **Gap:** Coding agents are often evaluated through static benchmarks without real developer interaction; prior HCI work focuses more on copilots.
- **Research questions:** RQ1 productivity, RQ2 user experience, RQ3 interaction patterns.
- **Approach:** Controlled within-participant study comparing GitHub Copilot and OpenHands.
- **Evaluation strategy:** 20 participants complete realistic coding tasks; outcomes include task correctness, user effort/time, Likert survey responses, qualitative feedback, and interaction trajectories.
- **Headline findings reported by authors:** Agents improved task correctness by about 35 percentage points and reduced measured user effort, but user satisfaction, understanding, and control remained concerns.
- **Initial triage decision:** Proceed to Pass 2 because the paper is directly relevant to Human-GenAI collaboration and AI in work/expertise, but its productivity and role-shift claims require methodological scrutiny.

## Reader reconstruction after Pass 1

> The problem which the paper addresses is how coding agents change developer productivity, user experience, and interaction patterns compared with copilots. Its main contribution is coding agents can shift work from hands-on coding toward supervision/management, plus design desiderata: transparency, balanced proactivity, and effective use of human effort. The evidence to support the contribution is agents improved task correctness by about 35 percentage points and reduced measured user effort. This paper matters for my research purpose is that my research area is human-genai collaboration and AI in Work and Expertise.

## Tutor feedback after Pass 1

- The reconstruction captures the core story accurately.
- Main correction: the productivity result is not simply "agents are faster." The authors report reduced **user effort**, but total elapsed time including agent actions was comparable: agent total averaged 27.9 minutes.
- The work-shift claim is partly evidence reported and partly interpretation from interaction trajectories. The strongest direct evidence is task correctness, time/user-effort data, and workflow traces.

## Pass 2: comprehension and evidence mapping

### Argument map

| Link | Mapping | Evidence location |
|---|---|---|
| Problem | Developers now use increasingly autonomous AI coding tools, but we do not know how agents change real developer workflows compared with copilots. | Abstract; Sec. 1, pp. 1-2 |
| Gap | Coding agents are often evaluated through static benchmarks without real human interaction; prior HCI work focuses more on copilots. | Sec. 1-2, pp. 2-4 |
| Research questions | RQ1 productivity, RQ2 user experience, RQ3 interaction patterns. | Sec. 3, p. 4 |
| Approach | Controlled within-participant study comparing GitHub Copilot and OpenHands. | Sec. 3; Fig. 3, pp. 4-6 |
| Evidence | 20 participants; realistic coding tasks; final code correctness; user effort/time; Likert surveys; qualitative responses; copilot videos and agent event streams. | Sec. 3.1-3.6, pp. 4-7 |
| Findings | Agents improved task correctness, reduced measured user effort, lowered cognitive load, but reduced understanding/control for some users. | Sec. 4; Figs. 4-5; Tables 2-3, pp. 7-9 |
| Contribution | Agents shift effort from implementation/setup/debugging toward instruction, supervision, and correction; future agents need transparency, calibrated proactivity, and better use of human effort. | Sec. 5-6, pp. 9-11 |

### Methodology map

| Dimension | What the paper reports |
|---|---|
| Unit of analysis | Developer-task interaction using either Copilot or OpenHands. |
| Participants | 20 students recruited via university mailing lists; all regular GitHub Copilot users; Python experience required. |
| Design | Within-participant comparison of Copilot and OpenHands; task type randomized between subjects; each participant used both tools. |
| Tools | GitHub Copilot as copilot; OpenHands powered by Claude Sonnet 3.7 as agent. |
| Tasks | Deep research/analysis, feature addition, bug fixing, sourced/adapted from GAIA and SWE-Bench. |
| Measures | Task correctness, user effort, Likert responses, qualitative responses, interaction trajectories. |
| Analysis | Linear model for task correctness; Wilcoxon signed-rank tests for Likert comparisons; qualitative trajectory analysis for interaction patterns. |
| Reproducibility | Analysis scripts reportedly in supplementary material; full task instructions in appendices. |
| Ethics | Compensation reported; formal IRB/ethics approval is not visible in the extracted text inspected today. |

### Claim-evidence table

| Claim | Evidence supplied | Evidence strength | Concerns |
|---|---|---|---|
| Agents improve task correctness over copilots. | Correctness: Copilot mean 25%, agent mean 60%; p = 0.02. Fig. 4/Sec. 4.1, p. 7. | Moderate | N=20, limited tasks, one agent/tool pairing. |
| Agents reduce user effort. | Correct solutions: Copilot 25.1 min user time vs agent 12.5 min; p = 0.01. Sec. 4.1, p. 7. | Moderate | "User effort" is operationalized differently across conditions; total elapsed agent time comparable. |
| Agents reduce cognitive load. | Likert comparison C1: 75% agree/strongly agree; p = 0.0006. Table 2/Sec. 4.2, pp. 7-8. | Moderate | Subjective measure; novelty effects possible. |
| Agents help users accomplish new tasks. | C2: 70% agree/strongly agree; p = 0.0013. Table 2/Sec. 4.2. | Moderate | Self-report plus task outcomes; mostly novice agent users. |
| Copilots may support better understanding of outputs. | C6: 55% disagreed that they understood OpenHands outputs better; qualitative comments say OpenHands was hidden/hard to control. Sec. 4.2, p. 8. | Moderate | p = 0.07, so not conventionally significant. |
| Agents shift workflows toward supervision/management. | Figure 5 trajectory abstraction; qualitative examples of users asking agents to run, explain, revise, debug. Sec. 4.3, pp. 8-9. | Moderate/indirect | The role-shift framing is interpretive; exact behavioral coding reliability is not clear from Pass 2. |
| Existing agents should be more transparent, less over-proactive, and better at leveraging human effort. | Participant feedback about hidden changes, too many files/lines, waiting during generation. Sec. 5.1, pp. 9-10. | Moderate | Design desiderata are grounded but not experimentally tested. |

### Figures and tables

**Figure 4** is central. It shows higher task correctness and lower measured user time for agents. It does not show that agents always complete work faster end-to-end; the prose notes that total time including agent actions is comparable.

**Figure 5** is conceptually important for Human-GenAI collaboration. It visualizes workflow redistribution: the human role moves from direct execution toward prompting, feedback, verification, and oversight.

**Table 2** shows the user-experience tradeoff: OpenHands was favored for lower cognitive load and new-task accomplishment, but not clearly favored for flow, satisfaction, speed, or output understanding.

**Table 3** is important for adoption: participants perceived OpenHands as competent, but many still preferred continuing with GitHub Copilot.

### Blocking concepts

| Concept | Quick explanation |
|---|---|
| User effort vs elapsed time | Agents may reduce time that humans actively spend, while total task completion time may remain similar because the agent works asynchronously. |
| Automation vs collaboration | Agents are more autonomous, but still require supervision, steering, and verification. |
| Understanding/control tradeoff | Productivity gains may come with reduced transparency and weaker user understanding of outputs. |
| Mixed-initiative interaction | Future systems may need better handoff and steering mechanisms between human and agent. |
| Expertise transformation | The paper hints that developers may shift from implementers to supervisors/managers, but it does not deeply study expertise formation. |

### Critical reading point

The paper is highly relevant to AI in work and expertise because it shows a change in the **division of labor**:

- AI takes over setup, file editing, code generation, and debugging loops.
- Humans increasingly specify goals, monitor progress, interpret outputs, and intervene when the agent overreaches.

The main gap for your research area is that the paper measures productivity and experience, but only lightly theorizes expertise. It does not deeply examine whether developers learn less, learn differently, become better supervisors, lose debugging skill, or develop new forms of agent-management expertise.

## Current judgement

The evidence that agents improve task correctness and reduce measured user effort is useful but bounded by sample size, task selection, and tool choice.

The stronger theoretical contribution for your research is not merely "agents are better than copilots." It is that increasing AI autonomy redistributes cognitive and practical labor in software work, creating new human responsibilities around specification, monitoring, verification, and intervention.

## Reader reconstruction after Pass 2

> The authors study how developers completed different tasks using copilot and agent because the prio work focued on the copilot and agents on static benchmarks. Prior work is limited by Coding agents are often evaluated through static benchmarks without real human interaction; prior HCI work focuses more on copilots. They address this using real world developmet tasks, including Deep research/analysis, feature addition, bug fixing, sourced/adapted from GAIA and SWE-Bench. They evaluate it with . They find Task correctness, user effort, Likert responses, qualitative responses, interaction trajectories. This supports Agents improved task correctness, reduced measured user effort, lowered cognitive load, but reduced understanding/control for some users, but remains uncertain because only investigate one copilt and one agent, didn't control the type of LLM, the study is still not fully representative of real-world software development workflow.

## Refined reconstruction

> The authors study how developers work with copilots and coding agents across realistic software-development tasks because prior HCI research has focused mainly on copilot-style tools, while coding agents have often been evaluated through static benchmarks without real human interaction. Prior work is limited by the lack of controlled human-in-the-loop comparisons between copilots and agents. They address this through a controlled within-participant study in which 20 regular GitHub Copilot users complete realistic tasks with both GitHub Copilot and OpenHands, including deep research/analysis, feature addition, and bug fixing tasks sourced or adapted from GAIA and SWE-Bench. They evaluate the comparison using task correctness, measured user effort, Likert survey responses, qualitative responses, final code snapshots, copilot screen recordings, and OpenHands event streams. They find that agents improved task correctness, reduced measured user effort, lowered cognitive load, and enabled users to accomplish some tasks they could not complete with copilots, but also produced weaker user understanding/control and did not clearly improve satisfaction, flow, or total elapsed time. This supports the claim that increasing AI autonomy redistributes software work from direct hands-on implementation toward instruction, monitoring, feedback, and supervision, but remains uncertain because the study uses one copilot and one agent, includes only 20 mostly student participants, does not control the Copilot LLM choice in the same way as the agent condition, uses short pre-defined tasks, and may not fully represent real-world software development workflows.

## Pass 2 judgement

Pass 2 is complete. The paper provides credible early evidence that coding agents can change the division of labor in software work, especially by automating setup, implementation, and debugging loops. However, the strongest defensible claim is narrower than "agents are better": in this study, OpenHands improved task correctness and reduced measured active user effort relative to GitHub Copilot under short controlled task conditions.

For your Human-GenAI collaboration and AI in Work/Expertise interests, the most important unresolved issue is expertise transformation: the paper shows a shift toward supervision and agent management, but it does not directly test whether developers learn differently, lose skill, gain new supervisory expertise, or change their professional judgement over time.

## Resume point

Continue with Pass 3: reconstruction and critical evaluation.

Before Pass 3, complete this reader reconstruction:

> The authors study ___ because ___. Prior work is limited by ___. They address this using ___. They evaluate it with ___. They find ___. This supports ___, but remains uncertain because ___.

Suggested Pass 3 structure:

1. Independent reconstruction of the study design.
2. Assumption audit.
3. Validity assessment, especially construct validity and external validity.
4. Alternative explanations for the productivity and workflow-shift findings.
5. Research extensions for Human-GenAI collaboration and AI in Work and Expertise.

## Pass 3: reconstruction and critical evaluation

### Independent reconstruction

| Stage | What happens | Purpose |
|---|---|---|
| Recruit participants | Recruit 20 students who regularly use GitHub Copilot and have Python experience. | Study developers who are familiar with copilots but new to agents. |
| Assign task type | Participants work on realistic tasks: deep research/analysis, feature addition, or bug fixing. | Test tools on more realistic tasks than toy programming problems. |
| Compare tools | Each participant uses both GitHub Copilot and OpenHands, with order randomized. | Enable within-participant comparison while controlling partly for individual differences. |
| Collect artifacts | Participants submit final code snapshots; Copilot work is screen-recorded; OpenHands event streams are logged. | Measure correctness and reconstruct interaction trajectories. |
| Measure productivity | Correctness is judged against task specifications; user effort is measured as active user time. | Compare task success and human labor investment. |
| Measure experience | Participants answer Likert and qualitative survey questions. | Capture cognitive load, satisfaction, flow, understanding, and future-use preferences. |
| Interpret workflow shift | Authors compare implementation, environment setup, and debugging trajectories. | Argue that agents shift work from hands-on execution to supervision and feedback. |

Core causal story implied by the paper:

> Increased tool autonomy -> agent can inspect files, edit code, run commands, and debug -> user spends less active effort and completes more tasks -> human role shifts toward specifying, monitoring, explaining, correcting, and stopping the agent -> productivity improves in some ways, but understanding/control and satisfaction remain unresolved.

### Assumption audit

| Assumption | Explicit/implicit | Why required | Evidence | Consequence if false |
|---|---|---|---|---|
| GitHub Copilot represents copilots. | Explicit | The comparison depends on Copilot as a reasonable baseline. | Authors argue Copilot is widely used and feature-representative. | If not representative, results may not generalize to Cursor, Windsurf, or other tools. |
| OpenHands represents coding agents. | Explicit | The agent-side conclusions rely on one agent. | Authors choose OpenHands as a leading open-source agent. | If OpenHands is unusually strong/weak, agent conclusions are tool-specific. |
| Participants are representative of likely new agent adopters. | Explicit/implicit | External validity depends on user population. | Participants are regular Copilot users and novice agent users. | Student-heavy sample may not represent professional developers or power users. |
| Task correctness captures productivity. | Explicit | Main productivity claim rests on correctness. | Final code snapshots evaluated against test cases/specs. | If correctness misses maintainability, security, integration, or code quality, productivity is incomplete. |
| User effort can be compared across tools. | Explicit | Time-saving claim depends on effort measurement. | Copilot effort = active end-to-end time; agent effort = time spent inspecting/responding around user messages. | If effort is operationalized asymmetrically, effort reduction may be overstated. |
| Short, pre-defined tasks approximate real software work. | Implicit | Generalization to work/expertise depends on task realism. | Tasks adapted from GAIA/SWE-Bench and real repositories. | Real work includes planning, coordination, long-term maintenance, review, and deployment. |
| More autonomous tool use can be interpreted as workflow transformation. | Implicit | Central collaboration/expertise claim depends on this. | Figure 5 and prompt annotations show shifted activity patterns. | If trajectories reflect study setup or novelty, role-shift claim may not hold longitudinally. |
| Self-reported experience reflects real user experience. | Implicit | RQ2 depends on Likert and qualitative responses. | Survey questions after task completion. | Responses may reflect novelty, frustration, expectations, or tool familiarity. |

### Validity assessment

| Dimension | Rating | Reason |
|---|---|---|
| Construct validity | Partially addressed | Task correctness and user effort are reasonable but incomplete productivity measures; "workflow shift" is plausible but partly interpretive. |
| Internal validity | Partially addressed | Within-participant design and randomized order help, but LLM choice differs across conditions and task/order learning effects remain possible. |
| External validity | Limited to moderate | Tasks are more realistic than toy tasks, but sample is small, student-heavy, short-duration, and focused on Python/popular repositories. |
| Statistical conclusion validity | Partial | Main effects report p-values, but N=20 limits subgroup and model-choice analyses. |
| Ecological validity | Moderate | Use of real tools and repositories helps; asynchronous 40-minute study tasks do not fully reflect professional software work. |
| Reproducibility | Partial | Tasks and analysis scripts are reportedly in supplementary materials, but complete recordings/event streams are not necessarily public. |
| Robustness | Partial | Appendix checks task version, experience, copilot usage, order, and model choice; many checks are underpowered. |
| Ethical validity | Cannot determine fully | Compensation is reported, but formal IRB/ethics details were not visible in inspected text. |

### Alternative explanations

| Finding | Alternative explanation | Did the paper rule it out? |
|---|---|---|
| Agents improved task correctness. | Tasks may favor agent affordances such as file editing, web browsing, and command execution. | Partly acknowledged; not fully ruled out. |
| Agents reduced measured user effort. | Effort is measured differently for agent and copilot workflows; hidden monitoring effort may be missed. | Not fully. |
| Agents lowered cognitive load. | Participants may offload responsibility without fully understanding outputs. | Partly supported by weaker understanding/control results, but not deeply tested. |
| Users accomplished new tasks with agents. | Agent may help most on unfamiliar repositories because it can browse context, not because autonomy itself is always better. | Not fully separated. |
| Copilot outputs were easier to understand. | Copilot may seem understandable because users execute more steps themselves, not because outputs are intrinsically clearer. | Not directly tested. |
| Workflow shifts toward supervision. | The study's task instructions may encourage copying a full task description into the agent and waiting. | Appendix D.3 acknowledges direct copying as a limitation. |
| Participants still prefer Copilot. | Familiarity and IDE integration may dominate over capability in short studies. | Plausible, not fully ruled out. |

### Stress tests and extensions

| Extension | Motivating limitation | What it would reveal |
|---|---|---|
| Longitudinal workplace deployment | Study tasks are short and pre-defined. | Whether agent use changes expertise, review habits, debugging skill, and professional judgement over weeks/months. |
| Compare multiple agents and copilots | One copilot and one agent. | Whether findings generalize across tool ecosystems. |
| Equalize LLM backbones | Copilot LLM choice varied, OpenHands fixed to Claude Sonnet 3.7. | Whether effects come from autonomy/interface or model capability. |
| Add code-quality/security/maintainability outcomes | Correctness is narrow. | Whether agent-produced solutions are sustainable and safe. |
| Measure verification behavior directly | Overreliance and understanding are under-measured. | How much users inspect, test, modify, or rubber-stamp agent work. |
| Expert vs novice developer comparison | Student-heavy, novice-agent sample. | Whether expertise changes how people supervise agents. |
| Planning/specification tasks | Pre-defined task descriptions omit early software lifecycle work. | How agents affect problem framing, requirement clarification, and design decisions. |
| Multi-agent/multitasking workflow study | Authors speculate developers may multitask while agents work. | Whether parallel agent management increases productivity or cognitive fragmentation. |

### Contribution judgement

| Dimension | Judgement |
|---|---|
| Claimed novelty | First controlled study of developer interactions with coding agents and direct copilot-agent comparison. |
| Demonstrated novelty | Strong as an early controlled comparison, though bounded by one agent and one copilot. |
| Empirical significance | Moderate: clear positive signal for correctness and active user effort, but small sample and short tasks. |
| Theoretical significance | Suggestive: points toward human work shifting from execution to supervision, but expertise transformation is not directly theorized or measured. The study focuses on short-term human-AI interaction during task execution, not longitudinal changes in developer knowledge, skill formation, professional judgement, or role identity. |
| Practical significance | Useful caution: agents may help users complete harder tasks, but transparency, control, and satisfaction remain adoption barriers. |
| Boundary conditions | Novice agent users, Python-centric tasks, short controlled sessions, specific tool versions, April-May 2025 AI tooling context. |

### Reader reflection on expertise transformation

> The reason that this paper does not show a full theory of expertise transformation is the paper focuses on the human-AI interaction at work.

Refined:

> This paper does not provide a full theory of expertise transformation because its study design focuses on short-term human-AI interaction during software tasks, rather than longitudinal changes in developer knowledge, skill formation, professional judgement, or role identity. It shows a shift in the division of labor, but not whether that shift produces new expertise, deskilling, reskilling, or changed standards of competent work.

Key distinction for future research:

> Workflow transformation is observed; expertise transformation is inferred but not directly studied.

### Reader defence prompt

Before final synthesis, answer:

1. What is the strongest contribution of this paper?
2. What is the most consequential assumption?
3. Which conclusion is best supported?
4. Which conclusion is least secure?
5. What evidence would change your judgement?
6. How does this paper affect your thinking about Human-GenAI collaboration and expertise?
