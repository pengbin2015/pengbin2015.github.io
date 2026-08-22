---
title: "From Overload to Convergence: Supporting Multi-Issue Human-AI Negotiation"
date: 2026-08-19
description: "A summary of a CHI study of cognitive overload in multi-issue human-AI negotiation and a Bayesian visualization designed to reduce it."
categories:
  - Research Notes
  - Human-AI Collaboration
  - Decision Support
---

**Paper URL:** [arXiv:2603.22766](https://arxiv.org/abs/2603.22766)

**arXiv subjects:** `cs.HC` (Human-Computer Interaction), `cs.AI` (Artificial Intelligence)

Negotiating with an AI agent can be difficult for a simple reason: the agent can track many trade-offs at once, while people have to hold those trade-offs in working memory. Parmar and Silpasuwanchai ask when that difference begins to matter and whether an interface can reduce the burden without taking over strategic decisions.

The study uses a property-rental negotiation in which participants played tenants against a GPT-4 landlord agent. Negotiations involved one, three, five, or seven issues. In a 2 × 4 within-subjects experiment with 32 participants, the authors compared a standard chat interface with a Decision Support interface. The support tool showed a Negotiation Horizon Grid: a heat map of the AI's likely acceptable options for each issue. It also showed a Global Convergence Panel to indicate how close the negotiation was to a mutually acceptable agreement. Both views were based on Bayesian estimates updated from the agent's offers.

The paper's central finding is a possible "plateau-cliff" pattern. Without support, participant payoffs were stable through three issues but fell at five and seven. With Decision Support, payoffs remained more stable as the number of issues increased. The tool also reduced several forms of friction: participants made fewer turns and revisions, took less time to begin responding, and reported lower mental demand, temporal demand, effort, and frustration. They also reported greater confidence and satisfaction with their negotiation strategy.

The proposed explanation is cognitive offloading. The visualization turns an internal tracking problem into a perceptual one. Rather than remembering every offer and inferring which trade-offs might work, a negotiator can inspect likely agreement zones and the overall direction of the conversation. Importantly, the system does not recommend a specific offer. It visualizes uncertainty about the agent's preferences, leaving the final strategic choice to the person. The authors describe this design goal as *Cognitive Harmony*: extending human capacity without eroding agency or redistributing value between the parties.

The paper is strongest as evidence for a within-study benefit of this particular support tool. Its measures span outcomes, process, and subjective experience, and the convergence of those measures makes the main pattern persuasive. But the broader claims need care. The Decision Support condition always followed the baseline condition, so learning or practice may explain part of its advantage. The study tests only four issue counts, meaning that the apparent three-issue threshold could fall somewhere between three and five rather than precisely at three. It also uses equal-weighted issues, one rental scenario, and one AI configuration. Those choices make the task controlled, but limit how far the result can generalize.

Agency is another open question. The authors infer that agency is preserved because the interface displays uncertainty instead of prescribing actions and because it does not shift the payoff distribution. Those are useful indicators, but they do not fully show whether people felt autonomous, understood the visualization, or followed its visual cues uncritically. Lower sequence entropy and faster replies may reflect a more focused strategy, but they could also reflect a more constrained search.

For human-AI collaboration research, the practical lesson is not that people can negotiate only three issues. It is that complex AI-mediated decisions need support that makes hidden structure visible while keeping judgment with the user. A stronger follow-up study would counterbalance interface order, test finer-grained issue counts, vary issue weights and negotiation domains, and compare multiple AI agents. It should also measure strategic understanding, overreliance, and perceived agency directly. That would clarify whether Bayesian visualization improves decision quality, not merely speed and confidence, and whether its apparent cognitive cliff is a robust human limit or a feature of this task.
