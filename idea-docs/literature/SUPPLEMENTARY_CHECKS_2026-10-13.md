# Supplementary overlap and artifact checks

13 October 2026. These checks supplement the 20 local PDFs. They are deliberately narrow: recovery feedback, persistent authorization, scoring, and reusable materials. They do not constitute a new exhaustive repository or university-thesis search.

## Additional PDFs to preserve locally

### 1. Schema First Tool APIs for LLM Agents: A Controlled Study of Tool Misuse, Recovery, and Budgeted Performance

[Record](https://arxiv.org/abs/2603.13404v1) | [PDF](https://arxiv.org/pdf/2603.13404v1) | [HTML inspected](https://arxiv.org/html/2603.13404v1)

**Checked:** Sections 4-7, particularly the diagnostic arms and actual pilot results.

**Finding:** This is close prior art for generic errors, constraint information, and corrective hints. Its reported experiment uses a small Qwen2.5-0.5B pilot on eight tasks and reports zero end-task success in every condition. The broad experimental design and proposed granularity ablations must not be mistaken for demonstrated improvements. Interface validity is its focus; persistent task-specific authority is different.

**Consequence:** Our thesis needs a competent clean-task baseline and must claim an authorization-specific extension, not the invention of diagnostic-granularity comparisons. Preserve the PDF before finalizing the related-work comparison.

### 2. Debugging the Debuggers: Failure-Anchored Structured Recovery for Software Engineering Agents (PROBE)

[Record](https://arxiv.org/abs/2605.08717v1) | [PDF](https://arxiv.org/pdf/2605.08717v1) | [HTML inspected](https://arxiv.org/html/2605.08717v1)

**Checked:** Guidance generation, controlled repair protocol, main recovery table, and overhead discussion.

**Finding:** PROBE already turns failed-run evidence into bounded guidance and compares it with outcome-only and trace-summary feedback while keeping the repair agent and budget fixed. It covers software repair, enterprise workflows, and AIOps. Its 56/257 recovered cases measure improvement on initially unresolved runs, not all original tasks. Guidance generation adds a separate cost.

**Consequence:** Generic structured recovery is not a gap. The proposed distinction is continuation under persistent, resource-level authority with separately scored lawful completion and justified stopping. Compare the exact enforcement assumptions before making that distinction final.

### 3. AIR: Improving Agent Safety through Incident Response

[Record](https://arxiv.org/abs/2602.11749v1) | [PDF](https://arxiv.org/pdf/2602.11749v1) | [HTML inspected](https://arxiv.org/html/2602.11749v1)

**Checked:** Section 3's detection, remediation, and rule-generation semantics.

**Finding:** AIR detects incidents after execution, invokes containment/recovery, terminates the compromised original task, and derives guardrails for future runs. Natural-language checks involve agent interpretation.

**Consequence:** Recovery after harm and recovery after a prevented unauthorized action are different experimental settings. Cite this distinction explicitly instead of treating every use of the word “recovery” as the same problem. This source also appears in Verifier Tax's discussion.

### 4. Defeating Prompt Injections by Design (CaMeL)

[Record](https://arxiv.org/abs/2503.18813v2) | [PDF](https://arxiv.org/pdf/2503.18813v2)

Already P25 in the earlier download guide. Its full text was **not** analyzed in this 20-paper run. Add it next as architectural background and check its capability/data-flow assumptions against our proposed guard. Do not infer that it lacks recovery features from this review.

### Optional: Loud Failures, Quiet Failures: Fault Detection and Recovery in Tool-Using Language Model Agents

[Record](https://arxiv.org/abs/2610.10062v1) | [PDF](https://arxiv.org/pdf/2610.10062v1) | [HTML inspected](https://arxiv.org/html/2610.10062v1)

**Checked:** Fault activation, clean controls, scoring, and task-clustered analysis.

**Finding:** The study distinguishes noticing a fault from recovering. Recovery is agreement with a model's own clean-run state, which need not be the correct task outcome; repeated clean runs also disagree. Some faults do not activate in every assigned run.

**Consequence:** Report exposure explicitly, retain independent goal checks, and cluster uncertainty by task family. This paper helps refine measurement but is not essential to choose the initial topic.

## Non-PDF sources that affect the novelty and material checks

### Hivemind Labs: Prompt less, check more

[Research note, 14 September 2026](https://www.hivemind.au/insights/prompt-less-check-more)

The full note was inspected. It directly compares specific failure feedback with generic retry for deterministic checks, including retail tasks. The author explicitly acknowledges confounding from message role, quoted drafts, and, in one comparison, changed gates. The experiment releases the final attempt even when a check still fails; corrected gates were tested post-hoc on the same tasks. This is a company research note, not verified peer-reviewed evidence.

It is close enough to cite. It weakens any broad “nobody compared generic and specific feedback” claim and motivates fixed gates, consistent delivery, held-out evaluation, and persistent denial. A clean extension may still be worthwhile; the mere existence of confounds does not prove our exact question is globally novel.

### ToolMisuseBench versions

[Current dataset card](https://huggingface.co/datasets/sigdelakshey/ToolMisuseBench) | [Repository](https://github.com/akgitrepos/toolmisusebench) | [v2 roadmap](https://github.com/akgitrepos/toolmisusebench/tree/master/toolmisusebench/version2)

The supplied P15 PDF and newer dataset describe different releases. The v2 roadmap explicitly proposes recoverable versus unrecoverable authorization cases, safe stopping, better state checks, and stronger baselines. Those distinctions are prior art too. A roadmap is not proof that every proposed feature is implemented or evaluated.

**Next audit:** match code commit, dataset manifest, current paper, fault persistence, recovery affordances, and scorer. Inspect whether denial can disappear after retry, whether an alternate path has equal authority, and whether stopping is separately measured. Do not build on a release label alone. The code tree and documentation were inspected; the implementation was not run or fully audited.

### AgentDojo

[Author repository](https://github.com/ethz-spylab/agentdojo)

Repository availability was checked. The supplied paper supports its stateful tool/environment/evaluator design. No installation or compatibility test was performed. Reuse requires a pinned commit, license inspection, and a decision between extending its framework and using a smaller custom service.

### tau-bench

[Original author repository](https://github.com/sierra-research/tau-bench)

The README warns that the original tasks are outdated and redirects to a successor. Preserve the distinction between the supplied 2024 paper, later tau² work, and current code. Any adapted order task needs a provenance record and its own validated scoring; a new environment is not a benchmark reproduction.

## Search scope and stopping rule

Targeted queries covered authorization-denial feedback, structured recovery, and the named closest papers. Primary paper pages/HTML and author-maintained repositories were preferred. Search results unrelated to tool-using AI authorization were discarded. No absence-of-results query is treated as evidence of novelty.

Before freezing the plan, the remaining check is bounded: compare the exact interventions and authorization semantics in Schema First, PROBE, AIR, the Hivemind note, and ToolMisuseBench v2; add CaMeL for the architectural context. Expand the search only if these sources point to a directly overlapping evaluation. This prevents the two-week planning period from becoming an unbounded collection exercise.

## Evidence status

The 20 local PDFs support the main review. The additional HTML checks refine the recommendation and expose close overlaps. Downloading these additional PDFs would improve the local archive; it is not a reason to postpone the current findings or pretend that only abstracts were available. No additional article was represented as fully reviewed when only its metadata or a repository description was checked.
