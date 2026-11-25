---
title: "Teaching with Memorable Communication"
date: 2026-11-25
description: "Teaching notes on using What? So What? Now What?, vocal variety, varied evidence, visuals, and analogies to help students understand and remember."
categories:
  - Teaching
  - Communication
---

**Source:** [Matt Abrahams, *6 Tips for Making Presentations Memorable*](https://med.stanford.edu/content/dam/sm/faculty-diversity/documents/Site_Content/Making%20Presentations%20Memorable_Matt%20Abrahams.pdf)

**Original source subject tags:** None listed in the handout.

Clear teaching gives students a message they can follow, a reason to care, and something to do with what they learn. These notes adapt selected ideas from Matt Abrahams's presentation advice to classroom teaching.

## Structure the message first

Abrahams reports that people retain structured information up to 40% more reliably and accurately than information presented in a freeform manner. The handout does not cite the underlying study, so I treat this as his reported finding rather than a guaranteed improvement in student learning.

His recommended **What? → So What? → Now What?** structure gives an explanation a clear direction:

| Question | Purpose | Illustrative cloud-cost example |
|---|---|---|
| **What?** | State the core message, idea, or central claim. | Our cloud infrastructure costs increased 30% last quarter because of unoptimised compute instances. |
| **So What?** | Explain why the message matters. | If left unchecked, this trend will consume $120,000 of our annual R&D budget by Q4. |
| **Now What?** | Tell the audience what to do with the information. | I recommend approving a two-week sprint to implement autoscaling, which we estimate will cut spending by 20% next month. |

These numbers are illustrative. In a real proposal, the cost forecast and expected savings would need supporting evidence.

In class, the same structure can turn a topic into a short learning sequence. For a lesson on autoscaling:

- **What?** Explain how a system adds or removes compute capacity as demand changes.
- **So What?** Ask students what happens when capacity stays fixed during a traffic spike or a quiet overnight period.
- **Now What?** Give students a workload graph and ask them to propose a scaling policy, explaining its cost and performance tradeoffs.

The final step gives students a task that uses the idea they have just heard.

## Vary voice, evidence, and visuals

Abrahams recommends variation in delivery and supporting material. For teaching, I would apply this in three ways:

- **Voice:** Vary volume and speaking rate to sustain attention. Slow down for an unfamiliar term, pause after a question, and stress the words that carry the main point. Keep speech audible throughout.
- **Evidence:** Support an idea with different kinds of evidence, such as a data point, a testimonial, and an anecdote. A cost chart can show the scale of a problem; an engineer's account can explain its practical effect; a short incident story can show how it arose. These give students different ways to connect with the same idea. Make clear what each example supports: one person's experience does not establish how common a problem is.
- **Visuals:** Use an image, diagram, or graph where it explains more clearly than a paragraph on a slide. For autoscaling, show demand and allocated capacity over time, then ask students to identify wasted capacity and periods of shortage.

## Connect new ideas to familiar ones

Abrahams also recommends analogies that connect unfamiliar material to what the audience already knows. Autoscaling, for example, resembles opening more supermarket checkout counters when queues grow and closing some when demand falls.

After introducing the analogy, ask students where it breaks down. A new compute instance may take time to start, and adding instances may not help if the database is the bottleneck. This moves the discussion from a familiar picture to the actual system.

Before teaching a topic, I can use three questions to check the explanation: What should students understand? Why should it matter to them? What will they do with it? Their answers to a small application task can then show what needs explaining again.
