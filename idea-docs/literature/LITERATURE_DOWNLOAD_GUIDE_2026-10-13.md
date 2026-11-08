# Literature discovery and download guide
## Task-scoped runtime authorization for industrial AI agents

**Search date:** 13 October 2026  
**Prepared for:** Can Baturlar, University of Oulu  
**Stage:** Broad discovery, relevance screening, and selected full-text checks. This is not the completed critical literature review.

## How to use this guide

This guide contains **39 research papers/reports and 6 theses**. Five of the theses are master's theses; one is a bachelor's review. Inclusion means a work is worth considering for a stated purpose, not that its results or novelty claims have been accepted.

Start with the twelve papers below. Download the remaining groups as useful; we do not need to read all 45 equally deeply within two weeks. Each entry records what was actually inspected, why it matters, and the question to investigate in a detailed reading. No code has been run or results reproduced.

For arXiv entries, the linked version is pinned where its version was checked. P20 uses the unversioned record because its current version number was not verified. Keep the arXiv identifier/version in downloaded filenames. A PDF link is a download route, not a claim that the complete PDF was read or that it will bypass browser access restrictions. Where no direct PDF route was verified, use the repository's file/download link.

Suggested local folder: `reference/authorization-papers/`. Suggested filename: `P01_Progent_2504.11703v3.pdf`.

| Read first | Paper | Download |
|---|---|---|
| P01 | [Progent: Securing AI Agents with Privilege Control](https://arxiv.org/abs/2504.11703v3) | [PDF](https://arxiv.org/pdf/2504.11703v3) |
| P02 | [Intent-Governed Tool Authorization for AI Agents](https://arxiv.org/abs/2606.22916v4) | [PDF](https://arxiv.org/pdf/2606.22916v4) |
| P03 | [MiniScope: Authorizing Agents with Least-Privilege Permissions](https://arxiv.org/abs/2512.11147v2) | [PDF](https://arxiv.org/pdf/2512.11147v2) |
| P04 | [Contextual Agent Security: A Policy for Every Purpose](https://arxiv.org/abs/2501.17070v3) | [PDF](https://arxiv.org/pdf/2501.17070v3) |
| P05 | [AgentSpec: Customizable Runtime Enforcement for Safe and Reliable LLM Agents](https://arxiv.org/abs/2503.18666v3) | [PDF](https://arxiv.org/pdf/2503.18666v3) |
| P06 | [Formal Policy Enforcement for Real-World Agentic Systems](https://arxiv.org/abs/2602.16708v3) | [PDF](https://arxiv.org/pdf/2602.16708v3) |
| P07 | [ActGov: Governing LLM Agent Actions via Policy-Constrained Validation](https://arxiv.org/abs/2609.24446v2) | [PDF](https://arxiv.org/pdf/2609.24446v2) |
| P08 | [Do Coding Agents Understand Least-Privilege Authorization?](https://arxiv.org/abs/2605.14859v2) | [PDF](https://arxiv.org/pdf/2605.14859v2) |
| P11 | [The Verifier Tax: Horizon Dependent Safety Success Tradeoffs in Tool Using LLM Agents](https://arxiv.org/abs/2603.19328v1) | [PDF](https://arxiv.org/pdf/2603.19328v1) |
| P12 | [CRITICTOOL: Evaluating Self-Critique Capabilities of Large Language Models in Tool-Calling Error Scenarios](https://arxiv.org/abs/2506.13977v1) | [PDF](https://arxiv.org/pdf/2506.13977v1) |
| P14 | [Causality Laundering: Denial-Feedback Leakage in Tool-Calling LLM Agents](https://arxiv.org/abs/2604.04035v1) | [PDF](https://arxiv.org/pdf/2604.04035v1) |
| P19 | [AgentDojo: A Dynamic Environment to Evaluate Prompt Injection Attacks and Defenses for LLM Agents](https://arxiv.org/abs/2406.13352v3) | [PDF](https://arxiv.org/pdf/2406.13352v3) |

## What this search changes

1. **The mechanism overlap is broader than the handoff described.** Progent, IGAC, MiniScope, Conseca, FORGE, ActGov, and the ASTRA/CASA line all deserve attention before proposing a new task-authorization mechanism. Their boundaries and evaluations differ, so they should not be treated as equivalent systems.
2. **Denial feedback is already part of several systems.** Progent supplies reasons; FORGE returns structured corrective feedback; IGAC specifies reason codes. A controlled comparison might still be useful, but discovery does not establish that such a comparison is absent.
3. **Post-intervention recovery and its costs have been measured.** The Verifier Tax is particularly close to the proposed empirical direction. Its rejection/auto-acceptance protocol is a material methodological distinction, not a minor implementation detail.
4. **Benchmarks offer ways to separate completion from authority.** AuthBench, AuthorizationBench, AgentBoundary, AgentDojo, and APort evaluate different units and properties. Their reported rates cannot be compared directly.
5. **Task-based authorization has a long history.** Thomas and Sandhu's TBAC work belongs in the background, alongside modern agent papers.
6. **Finnish theses help with framing and scope.** None of the selected theses has been verified as an exact match for task-scoped agent authorization. That is a search outcome, not evidence that no such thesis exists.

These are preliminary screening conclusions supported by the linked entries below, not a final contribution decision.

## Version and identity corrections

- **MiniScope:** current checked title is *Authorizing Agents with Least-Privilege Permissions*, v2, 6 October 2026. Earlier search results show *A Least Privilege Framework for Authorizing Tool Calling Agents*.
- **FORGE:** arXiv 2602.16708v3 is *Formal Policy Enforcement for Real-World Agentic Systems*. Older versions/search results use *Policy Compiler for Secure Agentic Systems* and PCAS terminology.
- **Stateful Governance:** the checked v2 calls its system **MasuGate**. The earlier handoff used Provenact.
- **ToolMisuseBench:** an arXiv paper was located, 2604.01508, in addition to the dataset/repository noted in the handoff.
- **AuthBench** (P08), **AuthorizationBench** (P18), and **AgentBoundary** (P17) are distinct.
- **AgentBound** (P26, MCP server confinement) is different from **AgentBoundary** (P17, counterfactual safety evaluation), even though P17's abstract calls its framework AgentBound.
- **AgentSpec:** use the runtime-enforcement paper by Wang, Poskitt, and Sun. Search also returns an unrelated embodied-scaffold paper with the same short name.
- Publication-year labels can differ between the original preprint and a later proceedings paper. A listed conference venue does not imply that the linked arXiv version is identical to the final proceedings version.

## Evidence labels

- **Record and abstract:** bibliographic/abstract screening only.
- **Selected full-text sections:** relevant methods, evaluation, or limitations passages were inspected online. This still does not mean a complete close reading.
- **Indexed excerpt:** search exposed a passage or title page; inspect the downloaded document to verify its context.
- **Preprint; venue not confirmed:** no peer-reviewed venue was established in this search. This is not a claim that the work has never been accepted.
- The relevance statements and questions below are our screening judgments; reported methods are attributed to the authors.

## A. Closest authorization and enforcement work

### P01. Progent: Securing AI Agents with Privilege Control

**Authors:** Shi et al.  
**Date/version:** 2025; v3 May 2026  
**Status:** Preprint; venue not confirmed  
**Inspected:** Selected full-text sections

[Paper / repository record](https://arxiv.org/abs/2504.11703v3) · [Download PDF](https://arxiv.org/pdf/2504.11703v3)

**Why relevant:** Symbolic policies over tool names and arguments, task-based policy construction, and controlled policy updates make this a direct comparator.

**For our close reading:** Read policy semantics, approval assumptions, fallback feedback, and ablations. It already returns an explanatory denial; do not claim that explanatory feedback itself is new.

### P02. Intent-Governed Tool Authorization for AI Agents

**Authors:** Zhu and Wang  
**Date/version:** 2026; v4 September 18  
**Status:** Preprint  
**Inspected:** Selected full-text sections

[Paper / repository record](https://arxiv.org/abs/2606.22916v4) · [Download PDF](https://arxiv.org/pdf/2606.22916v4)

**Why relevant:** Narrows static authority using a trusted request and intent certificate, then checks tool and payload effects.

**For our close reading:** Separate certificate fidelity, enforcement correctness, accepted draft authority, and completed effects. Inspect which reason codes are implemented versus proposed.

### P03. MiniScope: Authorizing Agents with Least-Privilege Permissions

**Authors:** Zhu et al.  
**Date/version:** 2025; v2 October 6, 2026  
**Status:** Preprint; venue not confirmed  
**Inspected:** Selected full-text sections

[Paper / repository record](https://arxiv.org/abs/2512.11147v2) · [Download PDF](https://arxiv.org/pdf/2512.11147v2)

**Why relevant:** Task-centric hierarchical permissions and contextual runtime enforcement directly overlap the broad topic.

**For our close reading:** Read permission granularity and hierarchy construction. Separate simulated permission-confirmation behavior from evidence about actual people. Earlier v1 has a different title.

### P04. Contextual Agent Security: A Policy for Every Purpose

**Authors:** Tsai and Bagdasarian  
**Date/version:** 2025  
**Status:** HotOS 2025 workshop paper  
**Inspected:** Record, abstract, and indexed method excerpt

[Paper / repository record](https://arxiv.org/abs/2501.17070v3) · [Download PDF](https://arxiv.org/pdf/2501.17070v3)

**Why relevant:** Conseca proposes context- and purpose-specific policies generated from trusted context and enforced deterministically.

**For our close reading:** Establish how this earlier formulation differs from the proposed task-scoped gateway. Distinguish its conceptual contribution from the scale of its evaluation.

### P05. AgentSpec: Customizable Runtime Enforcement for Safe and Reliable LLM Agents

**Authors:** Wang, Poskitt, and Sun  
**Date/version:** 2025; ICSE 2026  
**Status:** ICSE 2026; DOI 10.1145/3744916.3764546  
**Inspected:** Record and indexed full-text excerpts

[Paper / repository record](https://arxiv.org/abs/2503.18666v3) · [Download PDF](https://arxiv.org/pdf/2503.18666v3)

**Why relevant:** A runtime rule language with triggers, predicates, and enforcement mechanisms; essential prior work on enforcing agent constraints.

**For our close reading:** Compare policy expressiveness, rule-development/test separation, intervention behavior, and domain-specific measures.

### P06. Formal Policy Enforcement for Real-World Agentic Systems

**Authors:** Palumbo et al.  
**Date/version:** 2026; v3 May 8  
**Status:** Preprint; earlier versions titled Policy Compiler for Secure Agentic Systems  
**Inspected:** Selected full-text sections

[Paper / repository record](https://arxiv.org/abs/2602.16708v3) · [Download PDF](https://arxiv.org/pdf/2602.16708v3)

**Why relevant:** FORGE separates policies from agent reasoning using Datalog and a reference monitor; includes approval and customer-service cases.

**For our close reading:** Read structured denial feedback and recovery overhead. Its compared configurations also differ in prompt policy content, so they do not isolate feedback alone.

### P07. ActGov: Governing LLM Agent Actions via Policy-Constrained Validation

**Authors:** Zhang et al.  
**Date/version:** 2026; v2 September 22  
**Status:** Preprint  
**Inspected:** Record and abstract

[Paper / repository record](https://arxiv.org/abs/2609.24446v2) · [Download PDF](https://arxiv.org/pdf/2609.24446v2)

**Why relevant:** Validates proposed actions against task-scoped authority and policies, with SMT-based checks during policy construction.

**For our close reading:** Inspect the abstraction from concrete API calls to policy records, policy-development data, and independent utility/security evaluation.

### P08. Do Coding Agents Understand Least-Privilege Authorization?

**Authors:** Yan et al.  
**Date/version:** 2026; v2 May 15  
**Status:** Preprint; introduces AuthBench  
**Inspected:** Record and abstract

[Paper / repository record](https://arxiv.org/abs/2605.14859v2) · [Download PDF](https://arxiv.org/pdf/2605.14859v2)

**Why relevant:** Studies inference of file-level permission boundaries and simultaneous under- and over-authorization.

**For our close reading:** Compare policy sufficiency and tightness. An API-domain extension needs a substantive distinction beyond replacing files with orders.

### P09. Hybrid Inspection and Task-Based Access Control in Zero-Trust Agentic AI

**Authors:** El Helou et al.  
**Date/version:** 2026  
**Status:** Preprint; CASA  
**Inspected:** Record and abstract

[Paper / repository record](https://arxiv.org/abs/2605.02682v1) · [Download PDF](https://arxiv.org/pdf/2605.02682v1)

**Why relevant:** Combines deterministic flow controls with semantic task-to-tool matching across multi-turn conversations.

**For our close reading:** Separate deterministic integrity checks from model-based authorization judgments; examine task extraction errors and matched baselines.

### P10. Delegated Authorization for Agents Constrained to Semantic Task-to-Scope Matching

**Authors:** El Helou et al.  
**Date/version:** 2025  
**Status:** Preprint; ASTRA  
**Inspected:** Record and abstract

[Paper / repository record](https://arxiv.org/abs/2510.26702v1) · [Download PDF](https://arxiv.org/pdf/2510.26702v1)

**Why relevant:** Connects delegated authorization scopes to the agent's assigned task and provides a task/scope matching dataset.

**For our close reading:** Read scope granularity and whether evaluation covers complete executed workflows or semantic matching decisions.

## B. Denial feedback, recovery, and tool failure

### P11. The Verifier Tax: Horizon Dependent Safety Success Tradeoffs in Tool Using LLM Agents

**Authors:** Sah et al.  
**Date/version:** 2026  
**Status:** Preprint  
**Inspected:** Selected full-text sections

[Paper / repository record](https://arxiv.org/abs/2603.19328v1) · [Download PDF](https://arxiv.org/pdf/2603.19328v1)

**Why relevant:** Explicitly measures intervention, recovery, safety, task completion, and cost in airline/retail workflows.

**For our close reading:** Crucial caveat: the main protocol describes auto-acceptance after three rejections and a separate hard-abort analysis. Its results must not be generalized to an always-enforcing gateway.

### P12. CRITICTOOL: Evaluating Self-Critique Capabilities of Large Language Models in Tool-Calling Error Scenarios

**Authors:** Huang et al.  
**Date/version:** 2025  
**Status:** Preprint; venue not confirmed  
**Inspected:** Selected full-text sections

[Paper / repository record](https://arxiv.org/abs/2506.13977v1) · [Download PDF](https://arxiv.org/pdf/2506.13977v1)

**Why relevant:** Benchmark for diagnosing and correcting tool-use errors; close methodological background for post-denial behavior.

**For our close reading:** Inspect error construction and recovery scoring. Tool responses can come from caches, actual APIs, or a model simulator; distinguish these evidence sources.

### P13. When Tools Fail: Benchmarking Dynamic Replanning and Anomaly Recovery in LLM Agents

**Authors:** Zhu et al.  
**Date/version:** 2026  
**Status:** Preprint; ToolMaze  
**Inspected:** Record and abstract

[Paper / repository record](https://arxiv.org/abs/2606.05806v1) · [Download PDF](https://arxiv.org/pdf/2606.05806v1)

**Why relevant:** Separates workflow complexity from explicit/implicit and transient/permanent tool failures.

**For our close reading:** Determine which recovery metrics transfer to authorization denials and which assume faults that can eventually disappear.

### P14. Causality Laundering: Denial-Feedback Leakage in Tool-Calling LLM Agents

**Authors:** Chinaei  
**Date/version:** 2026  
**Status:** Preprint  
**Inspected:** Selected full-text sections

[Paper / repository record](https://arxiv.org/abs/2604.04035v1) · [Download PDF](https://arxiv.org/pdf/2604.04035v1)

**Why relevant:** Examines information learned from denials and its influence on later actions.

**For our close reading:** The evaluation uses three constructed differential scenarios, not benchmark-scale live LLM runs. Relevant to disclosure boundaries, not evidence that all detailed feedback is harmful.

### P15. ToolMisuseBench: An Offline Deterministic Benchmark for Tool Misuse and Recovery in Agentic Systems

**Authors:** Sigdel and Baral  
**Date/version:** 2026  
**Status:** Preprint; repository and dataset available  
**Inspected:** Record, abstract, repository/dataset descriptions

[Paper / repository record](https://arxiv.org/abs/2604.01508v1) · [Download PDF](https://arxiv.org/pdf/2604.01508v1)

**Why relevant:** Fault injection for CRUD, retrieval, files, and scheduling under step/call/retry budgets includes authorization failures.

**For our close reading:** Audit whether reported baselines are live language agents or deterministic strategies, and pin dataset/repository versions. The handoff had not identified this paper's arXiv record.

### P16. When Tool Outputs Become Commands: Separating Action Induction from Runtime Authorization in Tool-Augmented LLM Agents

**Authors:** Guo et al.  
**Date/version:** 2026  
**Status:** Preprint; SARA  
**Inspected:** Record and abstract

[Paper / repository record](https://arxiv.org/abs/2608.27146v1) · [Download PDF](https://arxiv.org/pdf/2608.27146v1)

**Why relevant:** Separates action provenance from authority and checks tool actions against the user objective and authorized evidence.

**For our close reading:** Inspect authorization judgment reliability, recovery after denials, and the cost of additional model calls.

### P36. Tools Fail: Detecting Silent Errors in Faulty Tools

**Authors:** Sun, Min, Chang, and Bisk  
**Date/version:** 2024  
**Status:** EMNLP 2024  
**Inspected:** Publisher record and abstract

[Paper / repository record](https://aclanthology.org/2024.emnlp-main.790/) · [Download PDF](https://aclanthology.org/2024.emnlp-main.790.pdf)

**Why relevant:** Provides a taxonomy and study of silent tool failures and recovery.

**For our close reading:** Background for distinguishing explicit authorization denials from plausible-looking but incorrect outputs.

## C. Evaluation methods and adjacent defenses

### P17. AgentBoundary: Counterfactual Evaluation of Safety in Tool-Using LLM Agents

**Authors:** Yang et al.  
**Date/version:** 2026  
**Status:** Preprint  
**Inspected:** Record and abstract

[Paper / repository record](https://arxiv.org/abs/2609.33658v1) · [Download PDF](https://arxiv.org/pdf/2609.33658v1)

**Why relevant:** Varying apparent risk independently of permission helps separate authorized-task refusal from unsafe compliance.

**For our close reading:** Assess the counterfactual task construction and post-state checks. Do not confuse this paper with AgentBound (P26); its abstract itself uses AgentBound for the framework.

### P18. Act on Your Behalf, Beyond Your Authorization: Benchmarking LLM Agent Authorization Alignment

**Authors:** Zhang, Li, Huang, and Li  
**Date/version:** 2026  
**Status:** Author-hosted preprint; author lab reports COLM HAIPS workshop recognition  
**Inspected:** Author-lab summary and PDF availability

[Paper / repository record](https://peach.codes/publication/) · [Download PDF](https://www.zhipingzhang.com/_files/ugd/3840b5_415101659c9f406d888aa5fce66889d5.pdf)

**Why relevant:** AuthorizationBench distinguishes task completion from the principal's authorized scope, including ordinary pressures rather than only attacks.

**For our close reading:** Read contract construction, executable out-of-scope paths, and labels. AuthBench (P08) and AuthorizationBench are different works.

### P19. AgentDojo: A Dynamic Environment to Evaluate Prompt Injection Attacks and Defenses for LLM Agents

**Authors:** Debenedetti et al.  
**Date/version:** 2024  
**Status:** NeurIPS 2024 Datasets and Benchmarks  
**Inspected:** Record and abstract; proceedings record checked

[Paper / repository record](https://arxiv.org/abs/2406.13352v3) · [Download PDF](https://arxiv.org/pdf/2406.13352v3)

**Why relevant:** Executable tasks with untrusted tool data provide a common evaluation setting for several candidate baselines.

**For our close reading:** Read legitimate task validators, attacker goals, task dependence, and clean-task competence before deciding whether to adapt its framework.

### P20. τ-bench: A Benchmark for Tool-Agent-User Interaction in Real-World Domains

**Authors:** Yao, Shinn, Razavi, and Narasimhan  
**Date/version:** 2024  
**Status:** Research paper; venue not checked  
**Inspected:** Abstract and author-repository description

[Paper / repository record](https://arxiv.org/abs/2406.12045) · [Download PDF](https://arxiv.org/pdf/2406.12045)

**Why relevant:** Business API workflows and database-state validation are useful models for an order-management testbed.

**For our close reading:** Read success checks, repeated-run reliability, policy compliance, and simulated-user assumptions. The author repository flags old task versions as outdated; pin any reused release.

### P21. InjecAgent: Benchmarking Indirect Prompt Injections in Tool-Integrated Large Language Model Agents

**Authors:** Zhan, Liang, Ying, and Kang  
**Date/version:** 2024  
**Status:** Findings of ACL 2024  
**Inspected:** Publisher record and abstract

[Paper / repository record](https://aclanthology.org/2024.findings-acl.624/) · [Download PDF](https://aclanthology.org/2024.findings-acl.624.pdf)

**Why relevant:** Useful source of controlled indirect-injection scenarios and attack objectives.

**For our close reading:** Check whether the evaluated continuation corresponds to a full business workflow; attack success and legitimate completion require distinct denominators.

### P22. The Task Shield: Enforcing Task Alignment to Defend Against Indirect Prompt Injection in LLM Agents

**Authors:** See publisher record  
**Date/version:** 2025  
**Status:** ACL 2025 long paper  
**Inspected:** Publisher record and abstract

[Paper / repository record](https://aclanthology.org/2025.acl-long.1435/) · [Download PDF](https://aclanthology.org/2025.acl-long.1435.pdf)

**Why relevant:** Checks whether instructions and tool calls contribute to user objectives; a relevant semantic alternative to permission predicates.

**For our close reading:** Distinguish goal alignment from explicit authority: an action can help a task while still requiring permission.

### P23. GuardAgent: Safeguard LLM Agents via Knowledge-Enabled Reasoning

**Authors:** Xiang et al.  
**Date/version:** 2025  
**Status:** ICML 2025; PMLR 267  
**Inspected:** Publisher metadata and abstract

[Paper / repository record](https://proceedings.mlr.press/v267/xiang25a.html) · [Download PDF](https://raw.githubusercontent.com/mlresearch/v267/main/assets/xiang25a/xiang25a.pdf)

**Why relevant:** Guardrail reasoning and executable checks offer another approach to policy enforcement.

**For our close reading:** Read guard generation, trust assumptions, and failure handling before considering it as a baseline.

### P24. Securing AI Agents with Information-Flow Control

**Authors:** Costa et al.  
**Date/version:** 2025  
**Status:** Preprint in checked arXiv/Microsoft records  
**Inspected:** Record and abstract

[Paper / repository record](https://arxiv.org/abs/2505.23643v2) · [Download PDF](https://arxiv.org/pdf/2505.23643v2)

**Why relevant:** Fides tracks confidentiality and integrity labels and enforces information-flow policies.

**For our close reading:** Map the difference between protecting data flows and restricting record/operation authority. Avoid treating their guarantees as interchangeable.

### P25. Defeating Prompt Injections by Design

**Authors:** Debenedetti et al.  
**Date/version:** 2025; SaTML 2026  
**Status:** IEEE SaTML 2026; downloadable arXiv version may differ from proceedings  
**Inspected:** Record and abstract; publisher/program checked

[Paper / repository record](https://arxiv.org/abs/2503.18813v2) · [Download PDF](https://arxiv.org/pdf/2503.18813v2)

**Why relevant:** CaMeL separates trusted control flow from untrusted data and uses capabilities for tool calls.

**For our close reading:** Read the policy assumptions and utility limits; this is architectural security context, not simply another denial message.

### P35. APort Vault: Benchmarking AI Agent Payment Authorization with the Open Agent Passport

**Authors:** Uchibeke  
**Date/version:** 2026  
**Status:** Preprint; project-associated benchmark  
**Inspected:** Record and abstract

[Paper / repository record](https://arxiv.org/abs/2609.22076v1) · [Download PDF](https://arxiv.org/pdf/2609.22076v1)

**Why relevant:** Separately records payment requests, decisions, recipient permissions, and actual transfers.

**For our close reading:** Audit replay realism, legitimate-utility coverage, matched comparisons, and attack-cohort/policy confounding rather than relying on large evaluation counts.

## D. Execution boundaries and authority over time

### P26. AgentBound: Securing Execution Boundaries of AI Agents

**Authors:** Bühler et al.  
**Date/version:** 2025; v3 April 2026  
**Status:** FSE 2026 listed in arXiv journal reference  
**Inspected:** Record and abstract

[Paper / repository record](https://arxiv.org/abs/2510.21236v3) · [Download PDF](https://arxiv.org/pdf/2510.21236v3)

**Why relevant:** Restricts MCP servers' host-resource access using declarative permissions.

**For our close reading:** Separate host/server confinement from semantic misuse of an otherwise permitted business operation.

### P27. Temporary Authority, Permanent Effects: Commit-Time Authorization for LLM Agents

**Authors:** Santos-Grueiro  
**Date/version:** 2026  
**Status:** Preprint  
**Inspected:** Record and abstract

[Paper / repository record](https://arxiv.org/abs/2607.10487v1) · [Download PDF](https://arxiv.org/pdf/2607.10487v1)

**Why relevant:** CommitGuard studies authority that becomes stale between an earlier check and a durable effect.

**For our close reading:** Read controlled invalidation, clean controls, and commit witnesses if temporal authority becomes a candidate contribution.

### P28. Stateful Governance for Concurrent Agentic Systems

**Authors:** Peng and Wu  
**Date/version:** 2026; v2 August 10  
**Status:** Preprint; system now called MasuGate  
**Inspected:** Record and abstract

[Paper / repository record](https://arxiv.org/abs/2608.02764v2) · [Download PDF](https://arxiv.org/pdf/2608.02764v2)

**Why relevant:** Authorization depends on changing shared budgets, inventory, and approval state.

**For our close reading:** Its abstract explicitly includes a scripted LLM-free procurement evaluation. Distinguish concurrency/enforcement evidence from agent behavioral evidence. The handoff's Provenact terminology is superseded.

### P29. When Consent Outlives Context: Residual Authority Replay in Long-Lived Agents

**Authors:** Zhang et al.  
**Date/version:** 2026  
**Status:** Preprint  
**Inspected:** Record and abstract

[Paper / repository record](https://arxiv.org/abs/2609.33910v1) · [Download PDF](https://arxiv.org/pdf/2609.33910v1)

**Why relevant:** Examines authority persisting beyond the task/context that originally justified it.

**For our close reading:** Relevant if comparing persistent versus task-expiring permissions; inspect lifecycle assumptions and production-derived semantics.

### P30. Context-to-Execution Integrity for LLM Agents

**Authors:** Santos-Grueiro  
**Date/version:** 2026  
**Status:** Preprint  
**Inspected:** Record and abstract

[Paper / repository record](https://arxiv.org/abs/2607.06000v1) · [Download PDF](https://arxiv.org/pdf/2607.06000v1)

**Why relevant:** Binds field, effect, and invocation authority at the execution boundary.

**For our close reading:** Inspect concrete authority bindings and the distinction among proposed calls, admitted calls, and observed effects.

### P31. Capability Gates Are Not Authorization: Confused-Deputy Failures in LLM Agent Frameworks

**Authors:** Mellafe Zuvic  
**Date/version:** 2026  
**Status:** Preprint  
**Inspected:** Record and abstract

[Paper / repository record](https://arxiv.org/abs/2606.28679v1) · [Download PDF](https://arxiv.org/pdf/2606.28679v1)

**Why relevant:** ScopeGate evaluates per-call value authorization and contrasts it with tool availability.

**For our close reading:** Audit pinned framework versions, small trial counts, benign controls, and which checks are genuinely task-specific.

## E. Conceptual and historical foundations

### P32. A Framework for Formalizing LLM Agent Security

**Authors:** Siu et al.  
**Date/version:** 2026  
**Status:** Preprint; OpenReview copy also discovered  
**Inspected:** Record and abstract

[Paper / repository record](https://arxiv.org/abs/2603.19469v1) · [Download PDF](https://arxiv.org/pdf/2603.19469v1)

**Why relevant:** Organizes contextual security into task alignment, action alignment, source authorization, and data isolation.

**For our close reading:** Use it to define the thesis threat model precisely; theoretical oracle definitions are not automatically deployable validators.

### P33. SoK: Trust-Authorization Mismatch in LLM Agent Interactions

**Authors:** Shi et al.  
**Date/version:** 2025; v2 February 2026  
**Status:** Preprint / systematization  
**Inspected:** Record and abstract

[Paper / repository record](https://arxiv.org/abs/2512.06914v2) · [Download PDF](https://arxiv.org/pdf/2512.06914v2)

**Why relevant:** A broad map of agent security through belief, intention, and permission.

**For our close reading:** Useful for citation chasing and terminology; verify any claimed gap against the primary papers, especially newer work.

### P34. Authenticated Delegation and Authorized AI Agents

**Authors:** South et al.  
**Date/version:** 2025  
**Status:** Preprint  
**Inspected:** Record and abstract

[Paper / repository record](https://arxiv.org/abs/2501.09674v1) · [Download PDF](https://arxiv.org/pdf/2501.09674v1)

**Why relevant:** Explains delegated authority, identity, restricted scopes, and auditable responsibility.

**For our close reading:** Background for boundaries between authentication, delegation, and authorization. No need to implement its entire identity architecture.

### P37. Task-based Authorization Controls (TBAC): A Family of Models for Active and Enterprise-oriented Authorization Management

**Authors:** Thomas and Sandhu  
**Date/version:** 1997 workshop  
**Status:** IFIP WG11.3 Database Security; author-hosted copy  
**Inspected:** Indexed author PDF opening/abstract

[Paper / repository record](https://profsandhu.com/confrnc/ifip/i97tbac.pdf) · [Download PDF](https://profsandhu.com/confrnc/ifip/i97tbac.pdf)

**Why relevant:** Task-oriented authorization predates LLM agents and gives the thesis a security foundation.

**For our close reading:** Read authorization activation, progression, and workflow context; make the agent-specific contribution explicit.

### P38. Enforceable Security Policies

**Authors:** Schneider  
**Date/version:** 1998 repository report  
**Status:** Cornell technical-report version; later journal version not audited here  
**Inspected:** Repository record and abstract

[Paper / repository record](https://ecommons.cornell.edu/entities/publication/5a936aa1-8a4f-41df-bc17-f2db479cf33e) — download through the file link on this record.

**Why relevant:** Foundational account of which policies execution monitors can enforce.

**For our close reading:** Use to reason about runtime enforcement boundaries; do not cite a technical report as the journal version without checking metadata.

## F. Finnish theses and regional research

### T01. Vulnerability Testing Sandbox Environment For Artificial Intelligence Systems

**Authors:** Joni Kemppainen  
**Date/version:** 2026  
**Status:** University of Oulu, MSc in Computer Science and Engineering  
**Inspected:** Indexed PDF title page and method excerpt

[Paper / repository record](https://oulurepo.oulu.fi/handle/10024/62452) · [Download PDF](https://oulurepo.oulu.fi/bitstream/handle/10024/62452/nbnfioulu-202605133306.pdf?isAllowed=y&sequence=1)

**Why relevant:** Local MSc example of building a controlled AI-security testing environment.

**For our close reading:** Read artifact evaluation and scope limitations; it is not direct evidence of a task-authorization research gap.

### T02. Digital twin data processing through AI: RAG based prototype and future perspectives

**Authors:** Ville Rytkönen  
**Date/version:** 2026  
**Status:** University of Oulu, MSc, Information Processing Science  
**Inspected:** Repository abstract and indexed PDF title page

[Paper / repository record](https://oulurepo.oulu.fi/handle/10024/63254) · [Download PDF](https://oulurepo.oulu.fi/bitstream/handle/10024/63254/nbnfioulu-202606114105.pdf?isAllowed=y&sequence=1)

**Why relevant:** Industrial prototype in Nokia's laboratory; useful example of framing an applied artifact through design science.

**For our close reading:** Read how the industrial problem, contribution, and evaluation connect. Low relevance to authorization mechanisms.

### T03. The Model Context Protocol in LLM Agent Architectures: The Clean Agent Architecture Pattern

**Authors:** Kalle Kulonen  
**Date/version:** 2026  
**Status:** Tampere University, MSc, Information Technology  
**Inspected:** Indexed PDF abstract; landing-page access denied

[Paper / repository record](https://trepo.tuni.fi/handle/10024/234490) · [Download PDF](https://trepo.tuni.fi/bitstream/handle/10024/234490/KulonenKalle.pdf?isAllowed=y&sequence=2)

**Why relevant:** MCP and separation of workflow logic from integration concerns provide architectural context.

**For our close reading:** The abstract explicitly describes an early proposal without full implementation, evaluated by qualitative criteria/scripted walkthrough. Do not use it as an experimental sample-size template.

### T04. VAPU: Verifying Multi-Agent System for Source Code Modernisation

**Authors:** Valtteri Ala-Salmi  
**Date/version:** 2025  
**Status:** Tampere University, MSc, Information Technology  
**Inspected:** Repository metadata/abstract and indexed PDF abstract

[Paper / repository record](https://trepo.tuni.fi/handle/10024/230444) · [Download PDF](https://trepo.tuni.fi/bitstream/10024/230444/2/Ala-SalmiValtteri.pdf)

**Why relevant:** A prototype-and-comparison thesis examining model, temperature, and task variation.

**For our close reading:** Useful for experimental reporting and MSc scope, despite a different research problem. Do not import its multi-agent scope into this thesis.

### T05. Analysing security incidents using multi-agent AI systems

**Authors:** Oskari Palojärvi  
**Date/version:** 2025  
**Status:** Aalto University, MSc, Computer Science  
**Inspected:** Repository metadata and abstract

[Paper / repository record](https://aaltodoc.aalto.fi/items/8ef9433a-9fa2-44e8-8bbf-7dbae5121766) — download through the file link on this record.

**Why relevant:** Applied language-agent architecture evaluated using security incidents.

**For our close reading:** Read the evaluation chapter as an MSc example; it concerns agents doing security work, rather than securing agents' authority.

### T06. Large Language Model (LLM) agents: Applications and security

**Authors:** Aleksi Kalliomäki  
**Date/version:** 2025  
**Status:** Aalto University, bachelor's thesis  
**Inspected:** Repository metadata and abstract

[Paper / repository record](https://aaltodoc.aalto.fi/items/e94bb73f-3a39-448d-9fea-6fabdb1394fa) — download through the file link on this record.

**Why relevant:** Optional introductory literature review of agent applications and security.

**For our close reading:** Background only. Not an MSc experimental precedent or proof of novelty.

### P39. Evil-AI Benchmark: An Evaluation Framework for Adversarial Security Assessment of LLM Agents in Smart Environments

**Authors:** Varol et al.  
**Date/version:** 2026  
**Status:** IEEE Access 14; University of Helsinki research record; not a thesis  
**Inspected:** University publication record and abstract

[Paper / repository record](https://researchportal.helsinki.fi/en/publications/evil-ai-benchmark-an-evaluation-framework-for-adversarial-securit/) — download through the file link on this record.

**Why relevant:** Combines tool/actuation checks, adversarial scenarios, capability tests, and benign over-refusal tests in smart environments.

**For our close reading:** Relevant to industrial evaluation framing. Read actuation verification and judge/human evaluation; Helsinki affiliation does not make this a Helsinki thesis.

## Additional source routes and artifacts

These are supplementary to the paper links, not additional papers counted above.

- [Progent author artifact](https://github.com/sunblaze-ucb/progent) — URL given in the paper; search also returned [lindsey98/progent](https://github.com/lindsey98/progent). Verify which repository/commit matches the downloaded version.
- [CriticTool code](https://github.com/Shellorley0513/CriticTool).
- [ToolMisuseBench code](https://github.com/akgitrepos/toolmisusebench) and [dataset](https://huggingface.co/datasets/sigdelakshey/ToolMisuseBench). Pin the release/commit and reconcile versions before reuse.
- [AgentDojo code](https://github.com/ethz-spylab/agentdojo).
- [Original τ-bench repository](https://github.com/sierra-research/tau-bench) — its current README directs users to a newer benchmark repository and flags outdated tasks.
- [ASTRA project](https://outshift-open.github.io/ASTRA).
- [AgentSpec published author PDF](https://cposkitt.github.io/files/publications/agentspec_llm_enforcement_icse26.pdf).
- [Conseca HotOS proceedings PDF](https://sigops.org/s/conferences/hotos/2025/papers/hotos25-100.pdf).
- [AgentDojo NeurIPS proceedings record](https://proceedings.nips.cc/paper_files/paper/2024/hash/97091a5177d8dc64b1da8bf3e1f6fb54-Abstract-Datasets_and_Benchmarks_Track.html).
- [CaMeL IEEE proceedings record](https://ieeexplore.ieee.org/abstract/document/11691650).
- [AgentSpec ResearchGate preprint](https://www.researchgate.net/publication/390142942_AgentSpec_Customizable_Runtime_Enforcement_for_Safe_and_Reliable_LLM_Agents) and [ResearchGate conference record](https://www.researchgate.net/publication/414231445_AgentSpec_Customizable_Runtime_Enforcement_for_Safe_and_Reliable_LLM_Agents). ResearchGate availability varies; prefer the author/repository PDF.
- [ToolMisuseBench ResearchGate record](https://www.researchgate.net/publication/403468014_ToolMisuseBench_An_Offline_Deterministic_Benchmark_for_Tool_Misuse_and_Recovery_in_Agentic_Systems).

## Search coverage and limits

The search combined general and domain-restricted web queries, direct repository/publisher record checks, version checks, and limited reference following from full-text papers. Relevant papers were retained regardless of whether they support the original gateway idea or the denial-feedback suggestion. Generic vendor marketing, duplicate mirrors, unrelated uses of “agent authorization,” and peripheral application papers were not treated as research evidence.

| Source | What was possible | Limit |
|---|---|---|
| arXiv | Direct records, version histories, abstracts, and selected full-text HTML | Complete methodological assessment remains pending |
| ACL Anthology | Publisher records, abstracts, PDF routes | Most papers screened rather than fully read |
| PMLR / ICML | GuardAgent publisher record and PDF route | No artifact execution |
| ACM / HotOS / FSE / ICSE | Publisher-oriented searches, official program/author records, DOI metadata | Not a complete search of ACM's subscription index |
| IEEE / SaTML | Publisher/program verification and regional journal record | Not a complete search of IEEE Xplore |
| NeurIPS | AgentDojo official proceedings verification | Targeted rather than exhaustive venue search |
| ResearchGate | Indexed records, uploaded excerpts, alternate versions | Some records offer only a full-text request; not a substitute for publication verification |
| Google Scholar | Direct search attempted; domain-restricted discovery attempted | Direct query inaccessible through the tool; no completed native Scholar search or citation-count analysis |
| OuluREPO | Site searches, repository abstracts, indexed PDF passages | Some item requests failed; exact-topic thesis coverage incomplete |
| Trepo | Site searches, one accessible thesis record, indexed PDF abstracts | Some pages timed out or returned an Anubis access-denied screen |
| Aaltodoc | Indexed individual item metadata and abstracts | Home-page fetch returned 403; individual results were still discoverable |
| Helsinki Helka | Direct access attempted | Returned 403; no native catalog search completed |
| Helsinki Helda / research portal | English/Finnish targeted searches; journal article record | No sufficiently close Helsinki thesis verified; a download-statistics-only title was not treated as a verified thesis |
| Author/lab sites and Cornell repository | Open author PDFs, AuthorizationBench record, historical enforcement report | Secondary discovery leads were checked against primary sources where retained |

The University of Helsinki result included in the guide is a **journal article**, not a thesis. There is no claim that this search exhausted Finnish repositories or identified every relevant paper.

Search phrases and follow-up records are saved separately in `SEARCH_LOG_2026-10-13.md`.

## Close-reading extraction sheet

For each high-priority PDF, record:

1. Exact citation, version, venue, and artifact commit.
2. Problem and claimed contribution.
3. Trust boundary: who supplies authority, who can change it, and what is assumed trustworthy.
4. Policy granularity: tool, argument, record, operation, time, cumulative budget, or execution history.
5. Intervention: deny, modify, ask, retry, stop, or expand authority.
6. Feedback: content, format, disclosure boundary, and whether it reveals a solution.
7. Evaluation: tasks, distinct templates, models, repetitions, attacks, clean controls, and train/development/test separation.
8. Ground truth: attempted versus executed violations; completion versus appropriate stopping; independence of the evaluator.
9. Baseline fairness and confounding changes between conditions.
10. Cost: policy-check overhead versus total extra reasoning/retry cost.
11. Limitations supported by the methods, including reproducibility.
12. What remains unanswered, and whether an MSc-sized experiment can answer it.

Only after that comparison should we choose a contribution and formulate initial research questions for Simo and Jussi.

