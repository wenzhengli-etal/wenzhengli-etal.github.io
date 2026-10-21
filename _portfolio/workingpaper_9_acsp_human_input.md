---
title: "When does human input matter? Evaluating LLM-assisted analysis of public participation in the housing approval process"
collection: portfolio
order: 2
status: "In progress"
authors: "Wenzheng Li, Julia Harten, Andrew Yan, Christos Thrampoulidis"
presented: "Presented at ACSP 2026"
image: "/images/ACSP2026_human_input.jpg"
slides: "/files/ACSP2026_human_input_LLM.pdf"
summary: "Large language models can read public comments at scale, but how much human work does a trustworthy result actually require? Using 350 Vancouver rezoning projects, we measure the accuracy bought by each additional hour of human effort &mdash; and find that writing definitions is the best buy, while prompt refinement is the worst."
---

Planners increasingly use language models to read public input at a scale no team could handle by hand. What stays hidden is the human work behind the output: how much of it a credible result needs, where it pays off, and when more of it stops helping. To the planner, the process is still a black box.

This project opens it. We assemble the public record of 350 housing rezoning projects in Vancouver from 2018 to 2025 — online public comments, diarized public hearing transcripts, and staff referral reports — and run three tasks against a human-coded gold standard:

- **Topic classification** — which of 14 topics (affordability, traffic, and so on) a comment raises;
- **Sentiment** — a speaker's overall stance toward the application;
- **Named entity recognition** — who is speaking, by role and by name.

Each task is built up in four cumulative stages, from bare category names (D0) through definitions (D1), annotated examples (D2), and refinement on a development set (D3). Because every stage is costed in human hours, each one can be priced: not just whether accuracy improves, but what the improvement costs.

<figure class="wl-figure">
  <img src="/images/ACSP2026_human_input.jpg" alt="Left: macro-F1 against cumulative human hours for three tasks. Right: F1 points gained per hour at each stage.">
  <figcaption>Accuracy against cumulative human hours (left) and the return of each stage in F1 points per hour (right). One point = 0.01 F1.</figcaption>
</figure>

Three results stand out. Human input raises accuracy in every task, but by very different amounts: from D0 to D3, topic classification gains 0.40 F1, sentiment 0.11, and named entity recognition only 0.06. Within each task, the categories that require judgement start lower and move most, while those settled by an explicit cue in the text begin high and improve little. And the stages are not equally worth the time — writing definitions is the best buy in every task, examples pay for the classification tasks but not for extraction, and refinement costs the most while returning the least.

The practical implication is that effort should be planned by category rather than spread evenly: always write the definitions, add examples where the task is classification, and reserve refinement for the categories that genuinely turn on judgement. A ceiling remains in every task, which is the subject of the error analysis.
