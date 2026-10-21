---
title: "When does human input matter? Evaluating LLM-assisted analysis of public participation in the housing approval process"
collection: portfolio
order: 2
status: "In progress"
authors: "Wenzheng Li, Julia Harten, Andrew Yan, Christos Thrampoulidis"
presented: "Presented at ACSP 2026"
image: "/images/ACSP2026_accuracy_ladder.jpg"
slides: "/files/ACSP2026_human_input_LLM.pdf"
summary: "When we use large language models to read public input, where does human input actually matter &mdash; and what is left after we have done our best? We grow one prompt in four cumulative stages across 350 Vancouver rezoning projects, and at each stage measure what an hour of human work bought in accuracy."
---

Large language models changed the economics of reading public input. Conventional NLP needs task-specific training and struggles with nuanced meaning; an LLM takes instructions in plain language, needs few labelled examples, and can tell you why it gave a label. But its output is highly sensitive to the prompt, and human participation helps most on complex, planning-specific tasks. The problem is that, to the planner, the process is still a black box: we cannot tell when a result is credible or how much human input it needed.

Three things are missing. First, the marginal return of human input: at which stage, and in what form, does an hour of human work change the result? Second, whether that return depends on the task and on the kind of category. And third, the residual: what is still wrong after the last stage, and is it explainable?

The data come from 350 housing rezoning projects in Vancouver, 2018 to 2025, read through three public records: online public comments, public hearing transcripts, and staff referral reports. We take three tasks — topic classification on online comments, sentiment analysis on hearing speakers, and named entity recognition on hearing transcripts. They cover both things an LLM does with text, classifying and extracting, and inside each task we separate categories that need inference and judgement, which we call **reasoning-based**, from categories that an explicit cue in the text identifies, which we call **mention-based**.

Human input enters in four cumulative stages, each keeping everything from the one before. At D0 the researcher only names the categories; at D1 writes a definition and a scope rule for each; at D2 selects and annotates positive and negative examples; at D3 labels a development set, reviews the model's errors, rewrites rules and boundary cases, and repeats. At every stage the model labels every unit and is scored against held-out human gold, so each stage can be priced in hours as well as in accuracy.

<figure class="wl-figure">
  <img src="/images/ACSP2026_accuracy_ladder.jpg" alt="Accuracy along the four-stage ladder for three tasks, with per-category trajectories split into mention-based and reasoning-based.">
  <figcaption>Top: gold macro-F1 at each stage of the ladder (bars = 95% bootstrap intervals). Bottom: gold F1 per category, with reasoning-based categories in blue and mention-based in red.</figcaption>
</figure>

Human input raises accuracy in every task, but by very different amounts. From D0 to D3, macro-F1 rises by 0.40 on topic classification, from 0.43 to 0.83; by 0.11 on sentiment; and by only 0.06 on named entity recognition, which was nearly as good at the first stage as at the last. Within each task, the reasoning-based categories start lower and move the most, while the mention-based ones are high from the start — on sentiment, support and oppose barely move, and neutral and mixed are where the action is.

Priced in hours, the stages rank clearly. Definitions are the best buy in every task. Examples pay for classification but not for extraction, where they return nothing. Refinement costs the most and returns the least: on topics it took 63 hours for 8 points, and in every task it sits below break-even. Splitting the same hours by category group shows that the reasoning-based groups absorb more of the hours and still end lower — so the practical unit for planning human hours is the category, not the task.

What survives at D3 is not random. A blinded audit of every remaining error finds that most are deterministic: on sentiment and named entity recognition the convention decides the case and the model simply did not apply it, while on topics 44% are gaps in the prompt's own wording, so it is the codebook that has to change. Genuinely ambiguous cases are few. The residual can be explained, and most of it can be fixed.
