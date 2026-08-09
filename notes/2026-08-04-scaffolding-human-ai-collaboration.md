---
title: "Reading Session - Scaffolding Human-AI Collaboration"
date: 2026-08-04
description: "Reading notes on a field experiment about behavioral and cognitive scaffolds in human-AI collaboration."
categories:
	- Research Notes
	- Human-AI Collaboration
	- AI Tools
---

# Reading session - Scaffolding Human-AI Collaboration

**Paper:** Alex Farach, Alexia Cambon, Lev Tankelevitch, Connie Hsueh, and Rebecca Janssen, *Scaffolding Human-AI Collaboration: A Field Experiment on Behavioral Protocols and Cognitive Reframing* (arXiv:2604.08678v2, 2026)

**Session date:** 2026-08-04  
**Method:** Three-pass paper-reading method  
**Progress:** Pass 1 and Pass 2 complete. Stop before Pass 3.

## Pass 1: screening

- **Paper type:** Quantitative empirical field experiment.
- **Domain:** Human-AI collaboration, organizational GenAI adoption, AI-assisted knowledge work.
- **Problem:** Organizations have widely deployed GenAI tools, but productivity gains remain uneven. The paper asks whether the bottleneck has shifted from access to AI toward how employees integrate AI into work practices.
- **Main intervention types:** Behavioral scaffolding through a structured pair-level AI collaboration protocol, and cognitive scaffolding through individual partnership-oriented AI training.
- **Study setting:** 388 employees at Gap Inc., organized into 194 pairs. Both conditions had access to Microsoft Copilot.
- **Headline findings reported by authors:** The structured pair protocol was associated with lower document quality and lower document production. Partnership training showed possible benefits for top-quality individual documents, but the pre-specified continuous Task B model was null.
- **Initial triage decision:** Proceed to Pass 2 because the paper is directly relevant to Human-GenAI collaboration and organizational AI adoption, but its claims require careful validity assessment.

## Reader reconstruction after Pass 1

> The problem in this paper is that the productivity gain when organizations adopt GenAI tools is unclear. Its main claimed contribution is that mandating structured AI collaboration in organizations could result in worse outcomes than flexible use, and individual-level partnership training may be better. The evidence is that the behavioral protocol was associated with lower pair document quality and much lower document production, while partnership training was associated with higher odds of top-quality individual documents in an exploratory binary model. This paper matters because it helps me understand the current state of human-GenAI collaboration in organizations, which could be my PhD research area or proposal.

## Tutor feedback after Pass 1

- Good reconstruction of the problem and evidence.
- Refine "partnership training is better" to a more cautious claim: partnership training showed possible benefits for reaching top-quality individual documents.
- Do not turn the paper into "behavioral scaffolding bad, cognitive scaffolding good." The authors explicitly warn against that interpretation.
- Safer takeaway: in this field experiment, a rigid synchronous AI-collaboration protocol created coordination and compliance costs, while cognitive reframing showed possible benefits for individual AI use, but both findings are constrained by design and measurement limitations.

## Pass 2: comprehension and evidence mapping

### Argument map

| Link | Mapping | Evidence location |
|---|---|---|
| Problem | GenAI access is widespread, but organizational productivity gains remain uneven. | Abstract pp. 1-2; Introduction 1.1 pp. 3-4 |
| Gap | Prior work shows heterogeneous AI productivity effects, but less is known about scaffolds that shape how employees use AI in organizations. | Introduction 1.1-1.3 pp. 3-5 |
| Research question | If access is no longer the bottleneck, what interventions help people use AI more effectively? | Introduction 1.1 p. 4 |
| Approach | Field experiment with 388 Gap Inc. employees; treatment varied use structure, not AI access. | Present Study p. 5; Method 3.1-3.3 pp. 9-11 |
| Evidence | Task A: pair-level structured protocol vs naturalistic use. Task B: individual partnership training vs basic Copilot training. | Method 3.2-3.4 pp. 10-13 |
| Findings | Task A treatment had lower document production and lower quality; Task B treatment had no significant continuous effect but higher odds of perfect-score documents in an exploratory binary model. | Results 4.1-4.3 pp. 15-20 |
| Contribution | Rigid collaborative AI protocols can create coordination costs; cognitive reframing may help some individual users reach top-quality output, but evidence is bounded. | Discussion 5.1-5.4 pp. 25-29; Conclusion p. 32 |

### Methodology map

| Dimension | What the paper reports |
|---|---|
| Unit of analysis | Task A: pair/document. Task B: individual/document. Surveys: individual, clustered by pair. |
| Population/sample | 388 full-time Gap Inc. employees with Microsoft Copilot access, organized into 194 pairs. Contractors, temporary employees, and research assistants excluded. |
| Design | Pair-level randomized design, stratified by functional area and balanced on AI comfort and job level. Major caveat: AM session = control, PM session = treatment. |
| Treatment | Task A: Create-Out-Loud protocol involving synchronous meeting, verbal discussion, transcript, and Copilot-as-drafter. Task B: partnership training using AI as thought partner/smart intern framing and iterative prompting. |
| Control | Task A: naturalistic AI use. Task B: standard Copilot feature and prompt training. |
| Outcomes | LLM-graded document quality, document production, self-reported experience, and belief change. |
| Analysis | ITT OLS; HC2 for Task A; CR2 clustered SEs for Task B and surveys; BH correction; Lee bounds for attrition; word-count sensitivity and mediation. |
| Validity checks | Human validation of LLM grading, cross-model reliability, word-count sensitivity, Lee bounds, and session-effect sensitivity. |
| Ethics/conflict notes | Informed consent reported. All authors are Microsoft employees, and Microsoft Copilot is a Microsoft product. |

### Claim-evidence table

| Claim | Evidence supplied | Evidence strength | Concerns |
|---|---|---|---|
| Structured collaborative AI protocol reduced Task A output quality. | Control mean 15.63 vs treatment 10.68; b = -4.96, p < .001; all rubric dimensions lower. | Moderate to strong | AM/PM confound and LLM word-count bias. |
| Structured protocol reduced document production. | Task A production: control 93/97, treatment 71/97; OR = 0.12, p < .001. | Strong | Mechanism partly inferred; could include infrastructure or session issues. |
| Task A quality result survives attrition sensitivity. | Lee bounds remain negative: lower -7.01, upper -3.34. | Moderate to strong | Lee bounds depend on monotonicity assumption. |
| Word count partly explains Task A quality gap. | Score-word count Spearman rho = .646; adding word count reduces effect by 33%. | Moderate | Word count may be proxy for effort, quality, or grader bias. |
| Partnership training improved individual Task B quality. | Continuous model: treatment 18.1 vs control 17.3, p = .223, null. Binary perfect-score model: OR = 2.07, p = .022. | Weak to moderate | Binary threshold post-hoc; Lee bounds cross zero; Task B ceiling effect. |
| Partnership training shifted beliefs. | Exploration change +0.26 treatment vs -0.02 control, BH p = .013; composite BH p = .047. | Weak to moderate | First belief measure occurred after Task A, so change may reflect recovery from treatment frustration. ANCOVA null. |
| LLM grading is usable for ranking but imperfect. | Cross-model ICC .921; LLM-human rank order Task A rho .79, Task B rho .58; LLM generous by +4.9 points. | Moderate | Human-human agreement also modest; Task B measurement weak. |

## Reader reconstruction after Pass 2

> The authors study the effect of behavioral scaffolding and cognitive scaffolding on employees' AI usage because the productivity gain is unclear. Prior work is limited by heterogeneous AI productivity effects. They address this using behavioral scaffolding and cognitive scaffolding to find the bottleneck of AI productivity gain. They evaluate it with document quality, document production, self-reported experience, and belief change. They find behavioral scaffolding reduces document production and document quality, and cognitive scaffolding improves the document quality. This supports the idea that rigid collaborative AI protocols can create coordination costs; cognitive reframing may help some individual users reach top-quality output, but remains uncertain because of differential attrition, AM/PM confound, carry-over effect, and word-count bias in LLM grading.

## Refined reconstruction

> The authors study how behavioral scaffolding and cognitive scaffolding affect employees' GenAI-assisted work because productivity gains from organizational GenAI adoption remain uneven and unclear. Prior work shows heterogeneous AI productivity effects, but is limited in explaining how organizational interventions shape actual AI-use practices. They address this through a field experiment comparing structured pair-level AI collaboration with naturalistic AI use, and partnership-oriented AI training with basic technical training. They evaluate outcomes using document production, LLM-graded document quality, self-reported experience, and belief change. They find that the behavioral scaffold reduced document production and document quality, while the cognitive scaffold showed possible benefits for reaching top-quality individual documents. This supports the idea that rigid collaborative AI protocols can create coordination costs, and that cognitive reframing may help some individual users, but the conclusions remain uncertain because of differential attrition, the AM/PM confound, carry-over effects, ceiling effects, and word-count bias in LLM grading.

## Current judgement

The Task A evidence is comparatively stronger: the structured protocol was associated with worse completion and lower quality, and the negative quality result survives Lee bounds.

The Task B evidence is weaker: the continuous pre-specified model is null, while the positive binary model is exploratory and vulnerable to attrition and ceiling effects.

## Resume point

Continue with Pass 3: reconstruction and critical evaluation.

Key Pass 3 question:

> Can this experiment really separate the effect of scaffold type from the effects of task type, timing, attrition, and measurement design?

Suggested Pass 3 structure:

1. Independent reconstruction of the study design.
2. Assumption audit.
3. Validity assessment.
4. Alternative explanations for Task A and Task B.
5. Replication or extension blueprint for a PhD research direction.

## Pass 3: reconstruction and critical evaluation

### Reader defence

> The strong contribution of this paper is that it studies the effects of behavioral scaffolding and cognitive scaffolding on employee productivity using AI tools. The most consequential assumption is that document quality and document production can measure employee productivity with AI aid. The best supported conclusion is that behavioral scaffolding harms employee productivity when using AI aid. The least secure conclusion is that cognitive scaffolding helps improve employee productivity. AM/PM timing has a big influence on the result.

### Tutor refinement

- Strong contribution: yes, but phrase more precisely as a field experiment on organizational GenAI-use scaffolds under real employee training conditions. The contribution is not just studying productivity; it is separating access to AI from structures that shape AI use.
- Most consequential assumption: good. Add that productivity is being operationalized narrowly through short-document production and LLM-graded quality, not broader workplace productivity.
- Best-supported conclusion: narrow the wording. The strongest supported conclusion is that, in this study, the mandated Create-Out-Loud pair protocol was associated with lower completion and lower LLM-graded quality than naturalistic use. This is stronger than the general claim that behavioral scaffolding harms productivity.
- Least secure conclusion: correct. The cognitive-scaffolding result rests on an exploratory binary model, while the pre-specified continuous model is null and Lee bounds cross zero.
- AM/PM timing: correct as a major threat, but not the only one. Differential attrition, protocol non-compliance, carry-over effects, ceiling effects, and word-count bias also matter.

### Final Pass 3 judgement

The study provides comparatively credible evidence that the specific synchronous behavioral protocol, implemented in this one-day organizational setting, created coordination and completion costs. The strongest evidence is Task A document production and quality: treatment pairs produced fewer documents and lower-scoring documents, and the Task A quality gap survives Lee bounds.

The study provides weaker evidence that cognitive reframing improves individual AI-assisted work. Task B's pre-specified continuous quality analysis is null; the positive perfect-score model is post-hoc and vulnerable to attrition and ceiling effects. Belief-change evidence is also ambiguous because the first belief measure occurred after Task A, making recovery from Task A frustration a plausible explanation.

The paper's broad theoretical contrast between behavioral and cognitive scaffolding should therefore be treated as hypothesis-generating. Its best-supported practical lesson is narrower: organizations should be cautious about mandating rigid synchronous AI-collaboration protocols without piloting the coordination burden, infrastructure reliability, and measurement strategy.

### Alternative explanation exercise

Reader interpretation:

> Timing may matter because PM participants may be more fatigued. The treatment group could get lower Task A scores not only because of the behavioral scaffold itself, but because the PM session made it harder to sustain the energy and discipline needed to follow the Create-Out-Loud protocol.

Tutor refinement:

This is a strong alternative explanation. It is more precise than a simple "PM fatigue" account because it proposes an interaction: the afternoon session may have been especially damaging for a cognitively and socially demanding protocol. In other words, timing may not depress all performance equally; it may amplify the coordination costs of the treatment.

### Stress tests

| Stress test | What it asks | Assessment |
|---|---|---|
| Would the Task A result survive balanced session timing? | If control and treatment were both run in AM and PM, would the treatment still underperform? | Cannot determine from this paper. The AM/PM confound remains a central internal-validity threat. |
| Would behavioral scaffolding work with better infrastructure? | If all pairs could meet synchronously and use Copilot smoothly, would the protocol still harm output? | Cannot determine. Compliance data show many treatment pairs were stranded, so the result partly reflects implementation friction. |
| Would the protocol work for tasks requiring true knowledge integration? | Task A may reward domain-specific depth more than pair synthesis. | Cannot determine. The authors' own framework predicts behavioral scaffolds may help when cross-perspective integration benefits exceed coordination costs. |
| Would Task B show an effect with a better measurement scale? | The 20-point LLM rubric had a severe ceiling effect. | Possibly. The pre-specified continuous model was null, but the ceiling makes it hard to detect distributional shifts. |
| Would human grading change the conclusion? | LLM grading rewarded word count and was generous, especially for Task B. | It might weaken or alter the Task B result. Task A rank-order agreement was stronger than Task B, so Task A is less vulnerable but still not immune. |
| Would the belief-change result survive a true pre-treatment baseline? | Beliefs were first measured after Task A, not before randomization. | Cannot determine. The authors argue belief change likely reflects recovery from Task A frustration rather than durable training-induced change. |

### Cleaner replication design

The cleanest follow-up study would separate scaffold type, time, task type, and unit of analysis.

| Design feature | Recommendation | Reason |
|---|---|---|
| Session timing | Randomize control and treatment within both AM and PM sessions | Separates treatment effects from fatigue, logistics, and infrastructure timing |
| Scaffold type | Test behavioral and cognitive scaffolds independently and jointly | Avoids bundling behavioral scaffold with Task A and cognitive scaffold with Task B |
| Unit of analysis | Include both pair and individual versions of each task | Separates scaffold effects from pair-vs-individual work |
| Task type | Use at least one open-ended task and one constrained task in each condition | Separates scaffold effects from task structure |
| Measurement | Use blinded human grading plus LLM grading, with rubrics designed to avoid ceiling effects | Reduces dependence on LLM scoring and word-count bias |
| Attrition handling | Make submission part of the outcome and reduce avoidable non-submission | Avoids conditioning only on surviving documents |
| Process data | Log meeting success, Copilot usage, prompt counts, time-on-task, document versions, and interruptions | Tests mechanism rather than only final output |
| Pre-registration | Pre-register primary outcomes, thresholds, exclusion rules, and missing-data strategy | Reduces ambiguity between confirmatory and exploratory results |

### Contribution judgement

| Dimension | Judgement |
|---|---|
| Claimed novelty | A field experiment testing behavioral and cognitive scaffolds for organizational GenAI use. |
| Demonstrated novelty | Stronger for the empirical setting than for the scaffold taxonomy; the taxonomy remains confounded by task and unit differences. |
| Theoretical significance | Useful for thinking about coordination costs and mental models in AI adoption, but not definitive evidence that behavioral scaffolds are worse than cognitive scaffolds. |
| Empirical significance | Task A negative result is meaningful and comparatively robust; Task B positive result is suggestive but weak. |
| Practical significance | Organizations should pilot rigid AI-collaboration protocols carefully before mandating them. |
| Boundary conditions | Single organization, Microsoft Copilot, one-day training event, AM/PM confound, LLM grading, short document tasks, high attrition. |

### PhD research extensions

| Extension | Motivating limitation | Possible research question |
|---|---|---|
| Session-balanced replication | AM/PM confound | Do behavioral AI-collaboration protocols still reduce output when time-of-day is randomized? |
| Mechanism study of coordination cost | Protocol non-compliance and stranded pairs | Which specific frictions make structured human-AI collaboration fail: meeting logistics, cognitive load, role ambiguity, or AI mediation limits? |
| Task-contingency study | Behavioral scaffold may help only for some tasks | When does AI-supported collaboration benefit from structure, and when does structure impose unnecessary overhead? |
| Measurement study | LLM grading and word-count bias | How should researchers validly measure quality in AI-assisted knowledge work? |
| Cognitive-scaffold replication | Task B evidence is weak | Does partnership-oriented AI training improve work quality when measured with non-ceiling outcomes and lower attrition? |
| Longitudinal workplace study | One-day task limits external validity | Do AI-use scaffolds change actual work routines and productivity over weeks or months? |

## Final synthesis

### One-sentence thesis

Farach et al. attempt to show that, once employees already have access to GenAI tools, the way organizations scaffold AI use can shape work outcomes, but the effects depend heavily on coordination costs, task design, measurement, and implementation conditions.

### Structured abstract

| Element | Synthesis |
|---|---|
| Problem | Organizational GenAI access is widespread, but productivity gains remain uneven. |
| Gap | Prior research shows heterogeneous AI effects, but less is known about organizational interventions that shape how employees use AI in practice. |
| Method | Field experiment with 388 Gap Inc. employees, organized into 194 pairs, comparing naturalistic vs structured pair-level AI use in Task A and basic vs partnership-oriented AI training in Task B. |
| Evidence | Document production, LLM-graded document quality, self-reported experience, belief change, Lee bounds, word-count sensitivity, human validation of LLM grading, and session-effect sensitivity analyses. |
| Findings | The structured pair protocol was associated with lower document completion and lower LLM-graded quality. Partnership training did not significantly improve continuous Task B quality, but was associated with higher odds of perfect-score documents in an exploratory binary model. |
| Contribution | The paper provides field evidence that rigid synchronous AI-collaboration protocols can create coordination costs, and suggestive evidence that cognitive reframing may help some individual users reach top-quality outputs. |
| Main limitation | Treatment is confounded with AM/PM timing and bundled with task type, unit of analysis, attrition, and measurement differences. |

### Critical appraisal

The strongest aspect of the paper is its real organizational field setting. The study does not merely ask whether AI access helps; it asks how workers are instructed to use AI once access is already available. This is directly relevant to organizational GenAI adoption.

The weakest aspect is causal separation. The paper cannot cleanly isolate behavioral scaffolding from PM timing, pair work, Task A design, compliance failure, and document-production attrition. It also cannot cleanly isolate cognitive scaffolding from Task B's ceiling effect, exploratory binary threshold, and carry-over from Task A.

Confidence in findings:

| Finding | Confidence |
|---|---|
| The Create-Out-Loud protocol was associated with lower Task A completion and quality in this setting | Moderate to high |
| Behavioral scaffolding generally harms AI-aided productivity | Low |
| Partnership training improved average Task B document quality | Low; pre-specified continuous model is null |
| Partnership training may increase the chance of top-score individual documents | Low to moderate; exploratory and attrition-sensitive |
| Belief change reflects durable cognitive reframing | Low |

### Knowledge status

| Status | Items |
|---|---|
| Understood confidently | Study design, two interventions, Task A negative result, Task B continuous null, main validity threats |
| Understood provisionally | Coordination-cost mechanism, cognitive-reframing interpretation, practical organizational implications |
| Unresolved | Whether the Task A effect would survive balanced AM/PM randomization; whether behavioral scaffolding helps on more interdependent tasks; whether cognitive training works with better measurement |
| Requires external reading | Scaffolding theory, jagged technological frontier, Lee bounds, Oster bounds, LLM-as-grader validation literature |

### Literature matrix entry

| Field | Entry |
|---|---|
| Citation | Alex Farach, Alexia Cambon, Lev Tankelevitch, Connie Hsueh, and Rebecca Janssen, "Scaffolding Human-AI Collaboration: A Field Experiment on Behavioral Protocols and Cognitive Reframing," arXiv:2604.08678v2, 2026. |
| Research question | If access to GenAI is no longer the main bottleneck, what interventions help employees use AI more effectively? |
| Theory/framework | Scaffolding theory; distinction between behavioral scaffolds that structure interaction and cognitive scaffolds that shape mental models. |
| Method | Field experiment with 388 Gap Inc. employees; pair-level Task A and individual Task B; treatment varied AI-use structure/training while all participants had Copilot access. |
| Data/sample | 388 full-time Gap Inc. employees, organized into 194 pairs. |
| Key findings | Task A behavioral protocol reduced document production and LLM-graded quality; Task B partnership training had null continuous effect but positive exploratory perfect-score result. |
| Contribution | Shows that organizational AI-use structures can matter after access is provided, and that rigid synchronous collaboration protocols may impose coordination costs. |
| Limitations | AM/PM confound, differential attrition, protocol non-compliance, carry-over effects, Task B ceiling effect, LLM grading bias, single organization, one-day tasks. |
| Relevance to my research | Highly relevant to Human-GenAI collaboration and organizational AI adoption; especially useful for designing studies on when AI-use scaffolds help or hinder knowledge work. |
| Follow-up references | Brynjolfsson et al. 2025; Dell'Acqua et al. 2026; Noy and Zhang 2023; Vygotsky 1978; Wood et al. 1976; Edmondson et al. 2001; Leonardi 2011; Lebovitz et al. 2022; Lee 2009; Oster 2019. |

### Open-questions log

| Question | Why it matters |
|---|---|
| Would the behavioral protocol still harm outcomes if AM/PM timing were balanced? | Central internal-validity issue. |
| Was the problem the idea of behavioral scaffolding, or the specific Create-Out-Loud implementation? | Determines whether the theory or implementation should be revised. |
| Which coordination costs were most damaging: scheduling, synchronous meeting friction, role ambiguity, Copilot use, or cognitive load? | Needed for mechanism-based theory building. |
| Would behavioral scaffolding help on tasks requiring stronger cross-functional integration? | Tests boundary conditions. |
| Can cognitive scaffolding improve quality under a non-ceiling measurement scale? | Needed to evaluate the weaker Task B claim. |
| How should AI-assisted knowledge-work quality be measured without rewarding length or generic completeness? | Important methodological issue for future Human-GenAI research. |
| Do short-session training effects persist in real work over time? | Needed for practical organizational claims. |
