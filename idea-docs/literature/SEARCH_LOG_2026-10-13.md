# Literature discovery search log — 13 October 2026

## Scope and protocol

Purpose: identify and prioritize primary literature for an MSc on task-scoped runtime authorization for industrial AI agents, without presupposing that denial-feedback recovery is the final contribution.

This is a narrative discovery log, not a PRISMA review. Search ranking, retrieval truncation, indexing gaps, and access restrictions mean that exact total hit counts would not be meaningful. The accompanying guide contains the 45 selected records; it does not claim to contain every relevant publication.

Inclusion: task/intent/argument-level authorization; runtime enforcement; related information-flow controls; post-intervention recovery; benchmark designs separating authority and utility; limited foundations; Finnish MSc examples useful for artifact evaluation and scope.

Exclusion/deprioritization: unrelated application-domain uses of authorization, generic commercial claims, unverified mirrors, duplicate versions, broad multi-agent architectures with little connection to the question, and source-code repositories presented as academic theses without an institutional record.

## Query families

Representative exact queries issued in this session (quotes indicate search strings, not quotations from papers):

### Authorization and enforcement

- `"LLM agents" "task" "authorization" privilege control`
- `"Progent" "Securing AI Agents"`
- `"Intent-Governed Tool Authorization"`
- `site:arxiv.org "agents" "least-privilege"`
- `"LLM agents" "runtime enforcement" policy`
- `"LLM agents" "information flow" Fides`
- `"AI agents" "authorization" "benchmark"`
- `"LLM" "authorization" "TaskShield"`
- `"AuthorizationBench" agents arxiv`
- `"AgentBoundary" arxiv`
- `"ASTRA" "delegated authorization" arxiv`
- `"Contextual Agent Security: A Policy for Every Purpose"`
- `"LLM" "authorization" site:usenix.org`
- `"agent" "authorization" site:dl.acm.org task`
- `"agent" "authorization" site:ieeexplore.ieee.org`

### Recovery and feedback

- `"AI agents" "denial" "recovery" authorization`
- `site:arxiv.org "agent" "denial-feedback"`
- `"LLM" "tool" "error recovery" benchmark`
- `"agent" "denial feedback" "recovery" paper -site:reddit.com`
- `"tool" "error messages" "LLM" recovery benchmark paper` — restricted to arXiv, ACL Anthology, OpenReview.
- `"authorization" "feedback" "agents" "ablation"` — arXiv.
- `"tool" "error feedback" "structured" "agents"` — arXiv and ACL Anthology.
- `"ToolMisuseBench"`

### Finnish repositories

- `site:oulurepo.oulu.fi "agent" "security" "language"`
- `site:oulurepo.oulu.fi "prompt injection" thesis`
- `site:trepo.tuni.fi "agent" "authorization"`
- `site:trepo.tuni.fi "large language" "agent" security thesis`
- `site:aaltodoc.aalto.fi "agents" "security"`
- `site:aaltodoc.aalto.fi "agent" "access control"`
- `site:helka.helsinki.fi "language model" "agent"`
- `site:helda.helsinki.fi "agent" "prompt injection"`
- `site:helda.helsinki.fi "prompt injection" "thesis"`
- `site:helda.helsinki.fi "LLM" "agents" security`
- `site:helda.helsinki.fi "kielimalli" "tietoturva"`
- `site:helda.helsinki.fi "tool-using" "agents"`
- `site:etheses.helsinki.fi "language models" security`
- `site:ethesis.helsinki.fi "agent" "security"`
- Exact-title follow-ups for Kemppainen, Kulonen, Rytkönen, and Evil-AI Benchmark.

### Discovery portals and foundations

- `site:scholar.google.com "Progent"`
- `site:scholar.google.com "tool" "authorization" "agents"`
- `site:researchgate.net "AgentSpec" runtime`
- `"Task-based authorization controls" Thomas Sandhu 1997`
- `"Enforceable security policies" Schneider pdf`
- `"GuardAgent" knowledge enabled reasoning ICML 2025`
- `"tau-bench" benchmark tool agent user interaction`

## Direct access and selected follow-ups

- Google Scholar query attempted at https://scholar.google.com/scholar?q=LLM+agent+authorization+least+privilege — inaccessible through the tool. Native Scholar results were not reviewed.
- Helka supplied by the user — returned HTTP 403.
- OuluREPO home accessible; some item fetches failed.
- Trepo home timed out; Kulonen landing page returned access denied; VAPU record was accessible.
- Aaltodoc home returned HTTP 403; indexed individual item records exposed thesis metadata and abstracts.
- Helda returned several peripheral results and a download-statistics-only title, “Error Propagation and Memory Contamination in Tool-Using LLM Agents.” Its item, author, date, and degree were not verified, so it was excluded from the download guide.
- Author publication page for AuthorizationBench linked directly to the PDF; no arXiv identifier was inferred.
- arXiv version histories checked for the core works; stale indexed abstracts were superseded by directly opened version records.
- Full-text method/evaluation passages inspected for Progent, MiniScope, FORGE, The Verifier Tax, IGAC, CriticTool, and Causality Laundering.
- Reference following from MiniScope identified Conseca and authenticated delegation.
- Publication checks used ICSE metadata for AgentSpec, ACL for Task Shield/InjecAgent/Tools Fail, PMLR for GuardAgent, NeurIPS proceedings for AgentDojo, and IEEE/SaTML for CaMeL.
- No PDFs were saved automatically, consistent with the user's intention to download them. No author was contacted, login attempted, payment made, code run, or experimental result reproduced.

## Next review stage

Inspect the user's downloaded PDFs using the extraction questions at the end of the guide. Record page/section references for contribution claims and limitations. Follow additional references when they affect a candidate contribution, then compare a small number of feasible options.

