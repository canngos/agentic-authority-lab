# KNOWLEDGE — Task-Scoped Runtime Authorization for Industrial AI Agents

**Handoff date:** 13 October 2026  
**Student:** Can Baturlar  
**University:** University of Oulu  
**Supervisor:** Simo Hosio  
**Selected thesis direction:** Task-Scoped Runtime Authorization for Industrial AI Agents

The user requested this file to transfer relevant information from a long thesis-topic exploration conversation into a new chat. The entire document is in English; existing academic titles, research questions, and the current research plan are retained. It is intended to provide enough context to understand the current situation without opening another file.

## Latest user-confirmed update — 13 October 2026

This section records the user's clarification in the new thesis workspace. Where older sections describe these matters as unknown, this update takes precedence. Earlier research proposals remain provisional.

### Literature discovery completed in this workspace — 13 October 2026

- At the user's request, a broad web discovery and screening pass covered research repositories, publisher/author records, ResearchGate results, and Finnish university repositories. Direct Google Scholar and Helka access was blocked; these are coverage limitations, not completed native database searches.
- Guide: [Literature discovery and download guide](idea1-Authorization/literature/LITERATURE_DOWNLOAD_GUIDE_2026-10-13.md), containing 39 research papers/reports and 6 theses, with links, relevance, inspection depth, and close-reading questions. Search log: [Search log](idea1-Authorization/literature/SEARCH_LOG_2026-10-13.md).
- This completes discovery/screening for the first batch, not the critical literature review or contribution selection. The user plans to download PDFs before detailed reading. No paper code was run.
- Important additions to the earlier handoff include MiniScope, Conseca, FORGE, ActGov, ASTRA/CASA, The Verifier Tax, AuthorizationBench, and AgentBoundary. Do not assume the denial-feedback comparison is novel before close reading.
- Version corrections: arXiv 2602.16708v3 is now *Formal Policy Enforcement for Real-World Agentic Systems* (FORGE; previously PCAS); MiniScope v2 was revised 6 October 2026; *Stateful Governance* v2 calls its system MasuGate; ToolMisuseBench has paper arXiv:2604.01508.
- Selected full-text checks found explanatory feedback in Progent, structured feedback/recovery in FORGE, and auto-acceptance after repeated rejections in The Verifier Tax's main protocol. These are methodological points to examine, not final comparative judgments.

### Supervisor feedback

- Simo saw `Research-Plan-Authorization-Agents_Can-Baturlar-DRAFT.pdf` and considered it well structured and relevant to the user's MSc in Computer Science.
- He did not review the plan in detail. He requested a deeper literature review to identify a contribution and define the research questions.
- Simo said Jonas might also be a second supervisor. This is a possibility, not a confirmed appointment.
- No specific experimental design or denial-feedback contribution has been approved.

### GPT-Lab / AI Champion correspondence

The user sent the same draft to Jussi, explaining Simo's support for the AI engineering direction, the tentative authorization topic, the proposed simulated order workflow, and the need to refine the contribution through literature review. The email requested feedback on fit and possible thesis collaboration.

Jussi replied, as quoted by the user:

> Dear Can,
>
> there is definitely interest for this in AI Champion, perhaps even with some of our consoritum companies (Granlund, Fira, Koja, Kone). Please do the literature review, formulate initial research questions, and lets have another sync-up meeting then.
>
> BR,
> Jussi

- This confirms Jussi's stated interest in the topic within AI Champion.
- Involvement of the named consortium companies is a possibility; no company use case, data access, or participation is confirmed.
- The immediate milestone is to complete a sufficiently deep literature review and formulate initial research questions, then email Jussi to arrange another sync-up meeting.
- The user remains interested in a paid research assistant role. The earlier GPT-Lab discussion covered both possible employment and MSc contributions; the latest email is not a job offer.

### Contribution selection and working approach

- The user considers denial-feedback / safe recovery potentially strong but has not examined it in detail or selected it.
- First understand the relevant papers in depth, then prepare and compare a small set of contribution suggestions before deciding.
- Do not anchor the review on validating the previous assistant's denial-feedback suggestion.

### Timeline and availability

- The user wants to finalize the plan within a maximum of two weeks and send it to Simo and Jussi. Relative to this conversation date, the target is **27 October 2026**; this is a personal planning target, not a reported institutional deadline.
- System preparation and subsequent phases are intended to follow that planning milestone.
- The user has other courses until December and expects to focus exclusively on the thesis **after 13 December 2026**.
- Target graduation remains May 2027. Weekly thesis hours before December have not been specified.

## 1. Most important current decision

The user's latest statement, translated into English:

> Simo liked the “Task-Scoped Runtime Authorization for Industrial AI Agents” idea. We will continue in this area.

**We are no longer choosing between two thesis topics. The selected area is task-scoped runtime authorization.** The previously considered version-aware multi-agent state-sharing topic remains an unselected alternative.

This decision establishes the direction of proceeding in authorization with Simo. However, the following should not yet be treated as finalized:

- The final research question and precise academic contribution.
- Whether the formal title will change.
- Whether the original comparison of three authorization methods will remain unchanged.
- Whether Simo has accepted the **denial-feedback / safe-recovery** narrowing proposed in the latest literature review.
- The model, framework, sample size, and final experimental matrix.
- Formal co-supervision or an industrial partnership with GPT-Lab.

**Important distinction:** The user said that Simo liked the main topic. There is no information about which specific contribution, baseline, or sample size Simo approved. Proposals in this file must not be presented as supervisor decisions.

## 2. User context, motivation, and constraints

### Information explicitly provided by the user

- An MSc Computer Science student at the University of Oulu, living in Tampere.
- **Target graduation: May 2027.**
- Wants to develop a career in AI engineering, AI-native engineering, agentic AI, and the application of AI to business and industrial processes.
- Works with n8n and has AI automation ideas, but does not want their interests to be understood as limited to automation.
- Learns through personal projects. **GameBuddy**, according to the user, is their first production-grade product published on Google Play and developed using Claude/AI agents.
- Has a project called **AIGateKeeper**. Does not want to present it simply as a product-development thesis; seeks an independent research question and a measurable contribution.
- Has stated that continuing to a PhD is not the primary near-term goal. Wants to learn and contribute in a research environment.
- **Does not want interviews as a research method.** Prefers developing a system/prototype, collecting data, and analyzing trade-offs through controlled experiments.
- Keeping the scope small is very important. The previous supervisor also discouraged expanding the scope. Avoid multiple broad research questions or work equivalent to several separate theses.
- Has an **RTX 5070 Ti** laptop; the exact VRAM capacity is unknown. Can allocate a budget for model APIs, but has not specified an amount.

### Transition from the previous thesis

- The previous topic concerned **Persuasive Systems Design (PSD)** and did not involve much AI.
- A professor named Harri suggested the topic. The user accepted because it was interesting at the time; the plan was prepared with and approved by the supervisor.
- Following a supervisor change, **Simo Hosio** became the new supervisor. Simo also liked the previous plan.
- The concrete progress reported by the user consists of an **interview website** and some literature reading. The user did not report collecting data, recruiting participants, or completing the main analysis.
- The motivation for moving toward AI is a clearer career and research interest arising from projects and research-group discussions, rather than a claim that the previous topic has no value.
- As of the latest message, Simo liked the authorization idea. Whether the university's formal topic-change procedures have been completed is unknown.

## 3. Connections with GPT-Lab and individual researchers

The user contacted GPT-Lab after the Alihankinta expo. Do not say that the user met Jiri Härmä face-to-face at the stand: according to a later clarification, the user learned that Jiri had left and called him by phone.

Researchers involved in the discussions:

- **Jussi Rasku:** Sent the meeting invitation. Liked the user's profile/projects and mentioned a possible part-time research assistant position in his group in Seinäjoki, but **made no definite promise**.
- **Muhammad Waseem**.
- **Jiri Härmä**.

According to the user's account of the meeting:

- The projects and ideas were received positively.
- The researchers questioned the fit between the user's AI interests and the existing PSD thesis.
- Jussi considered AIGateKeeper substantial and asked why it had not become the thesis topic.
- He suggested that the user could change topics if progress was still limited and asked to be informed if the topic changed.
- They mentioned the possibility of doing the thesis together with GPT-Lab if the user brought a suitable AI topic.

This is **the user's account**, not a job offer, confirmed co-supervision arrangement, funding commitment, or promise of data access.

Relevant links:

- [GPT-Lab projects](https://gpt-lab.eu/projects/)
- [AI Champion project description](https://projects.tuni.fi/aichampion-en/about/)

The user is particularly interested in applying AI to industry. The proposed simulation was considered potentially relevant to GPT-Lab/AI Champion, but the project team has not confirmed the fit of this specific experiment.

### Simo / Jonas context

In the earlier review, the [Oulu Crowd Computing](https://ubicomp.oulu.fi/research/cc) page listed Simo Hosio and **Jonas Oppenlaender** in the same group. The user considers Jonas's interests a good match for their own.

- [Jonas's Oulu profile](https://www.oulu.fi/en/researchers/jonas-oppenlaender): The previous check found information about AI agents, generative AI, prompt engineering, and AI Engineering teaching.
- [Simo's Oulu profile](https://www.oulu.fi/en/researchers/simo-hosio).
- [Adapting Socio-Technical Congruence to Human-Agent Collectives](https://oulu.cris.fi/en/publications/e26719f7-34cd-40e2-a098-5aa132fddbad): A joint work by Jonas Oppenlaender, Aku Visuri, and Simo Hosio. It provides a general connection to technical agent reliability, but does not establish authorization expertise or a supervision commitment.

There is no information indicating that Jonas has a role in this thesis. A new chat should not assume that Simo specializes in security/authorization.

## 4. What does the topic investigate, in simple terms?

Permission to use an `update_order` tool does not mean that an agent may update every order in any way. Permissions can be tied to the records and operational limits of the current task.

Example:

- Task: Create/update a draft for 20 units for order 123.
- Tool-level permission: `update_draft` may be used.
- Static business rule: The quantity must remain within certain general limits.
- Task-specific rule: Only the order/draft belonging to this task may be modified, and only through operations permitted for this task.
- If the agent tries to write to record 456, the call is blocked **before reaching the service**.

The aim is to check whether a proposed tool call exceeds the authority established by the trusted application. This does not require the agent to reason correctly every time.

### Concepts that must remain distinct

| Concept | Meaning in this thesis |
|---|---|
| Authentication | Establishing the caller's identity. This has not been selected as the main research topic. |
| Authorization | Determining whether a particular tool, record, and operation are permitted. |
| Task-scoped authorization | Narrowing authority according to the current task's identity, target records, and limits. |
| Runtime enforcement | Checking a call before actual tool execution and allowing or blocking it. |
| Policy correctness | Whether the authorization rule accurately represents the user's actual intent/business rule. |
| Enforcement correctness | Whether the software correctly implements the supplied rule. |
| Agent recovery | Returning to a permitted course of action, or stopping appropriately, after a call is denied. |
| Task success | An independently verified task outcome, rather than the agent's claim of success. |

Correctly enforcing a rule and producing the correct rule are separate problems. The initial plan excludes automatic policy generation.

### Trust boundary

Proposed small architecture:

`Trusted task/context -> Agent -> Proposed tool call -> Authorization adapter -> Local business service`

Denial feedback/tool results return to the agent. A separate evaluator inspects the service state and event records.

- A trusted application supplies task permissions; the agent cannot expand its own authority.
- A `task_id` supplied by the agent, or its statement that “I am authorized to do this,” is not sufficient evidence of authorization.
- Every actual execution path available to the agent must pass through the enforcement layer (**complete mediation**).
- Monitoring model API traffic is not equivalent to controlling tool execution.
- Within the proposed scope, the integrity of the business service, enforcement layer, and trusted task inputs is assumed. Research into compromising the operating system/container or taking over the enforcement layer was not planned.
- A correctly functioning gateway does not establish the safety of all agent systems.

## 5. Initial research plan developed in the conversation

**Status:** The current starting plan prepared for the user. Simo liking the main area does not imply acceptance of every detail in this plan. The latest literature review indicated a need to narrow the contribution claim further.

### Original research question

> How does task-scoped authorization affect executed policy violations and legitimate task completion compared with static tool permissions?

### Experimental conditions

1. **Tool-name allowlist:** Checks only which tools may be called.
2. **Tool-name + static argument restrictions:** Tool restrictions plus fixed argument constraints independent of the current task.
3. **Task-scoped restrictions:** Adds task-specific record identifiers and operation limits to the second condition.

These conditions are a proposed thesis design, not a standardized three-way benchmark established in the literature. The static baseline must be defined fairly and realistically; it must not be weakened merely to produce poor results.

### Small application

- One AI agent.
- A resettable local order service.
- Four tools: read an order, check inventory, create a draft, and update a draft.
- An authorization adapter that checks tool names/arguments.
- Logs of authorization decisions and actual service effects.
- Independent correctness checks.

### Initial numerical outline

- Approximately **80 held-out scenarios**, with **3 repetitions** per condition.
- With three conditions, approximately 720 workflow runs; this is not the number of model calls.
- These numbers are **initial estimates**, not the result of a power analysis, budget calculation, or supervisor decision.
- Both clean and manipulated tool-response conditions were considered.
- Development and evaluation scenarios are separate; prompts/policies will be frozen before testing.
- Conditions will use the same model, tools, initial service state, and step budget.
- Incorrect/incomplete trusted task contexts were a candidate for a separate sensitivity analysis.

### Initial exclusions from scope

Multi-agent delegation, automatic policy generation, approval interfaces, interviews, and production ERP integration. These were scope boundaries proposed by the assistant; the user explicitly ruled out interviews in particular.

## 6. Main literature-review finding: the mechanism alone is not new

**Evidence status:** The following summaries are based on web searches and primary sources opened during the earlier conversation. No new internet search was performed when writing this handoff. Newer source versions/publication status should be checked before using the sources in the thesis. This work was not described as a systematic literature review.

### 6.1 AgentSpec — basic runtime enforcement

- Title: **AgentSpec: Customizable Runtime Enforcement for Safe and Reliable LLM Agents**.
- Authors: Haoyu Wang, Christopher M. Poskitt, Jun Sun.
- [arXiv](https://arxiv.org/abs/2503.18666), [full text](https://arxiv.org/html/2503.18666).
- The previous verification listed **ICSE 2026 acceptance**, proceedings pages 2938–2950, DOI **10.1145/3744916.3764546**.
- Runtime rules using triggers, predicates, and enforcement mechanisms; applications to code, embodied agents, and driving.
- Implication for the thesis: “Applying runtime rules to an agent” cannot serve as the novelty claim.

### 6.2 Progent — very close to the original idea

- Latest examined title: **Progent: Securing AI Agents with Privilege Control**. Earlier versions may use “Programmable Privilege Control.”
- Tianneng Shi, Jingxuan He, Zhun Wang, Hongwei Li, Linyu Wu, Wenbo Guo, Dawn Song.
- [arXiv](https://arxiv.org/abs/2504.11703), [v3 full text](https://arxiv.org/html/2504.11703v3).
- Initial version: April 2025; examined v3: May 2026.
- Symbolic permission rules over tool names and arguments; initial policy generation from the task and updates during execution.
- Distinguishes narrowing from expanding authority, with approval logic for expansion.
- Options following a prohibited call include stopping, asking the user, or returning an explanatory error to the agent. The default explanation includes the reason for denial and guidance to continue the task.
- The examined ablations concern approval options and models; they were not presented as the matched feedback comparison proposed here.
- **Primary comparison source to prioritize.** Reproducing/adapting a relevant component could be considered instead of inventing another framework; its code, license, and runnability have not yet been tested.

### 6.3 Intent-Governed Tool Authorization — task narrowing already exists

- Title: **Intent-Governed Tool Authorization for AI Agents**.
- Genliang Zhu, Chu Wang.
- [arXiv](https://arxiv.org/abs/2606.22916), [examined v4](https://arxiv.org/html/2606.22916v4), 18 September 2026.
- A short-lived certificate derives task/request boundaries from the user's trusted request, narrows tool visibility, and checks payload compliance.
- Follows the principle of not exceeding static integration authority; an OpenPort-based prototype.
- Includes stable reason codes, denials, runtime tests, and small end-to-end LLM evaluations.
- Implication for the thesis: Blocking an operation that is permitted by static credentials but inappropriate for the current task is already directly addressed.
- Producing simple reason codes is also not a novelty claim by itself.

### 6.4 AuthBench — effects of under- and over-permissive policies

- Title: **Do Coding Agents Understand Least-Privilege Authorization?**
- [arXiv](https://arxiv.org/abs/2605.14859), [full text](https://arxiv.org/html/2605.14859).
- Infers file-level read/write/execute permissions from tasks; 120 terminal tasks and executable evaluation.
- Omitting necessary permissions and granting unnecessary authority can occur simultaneously.
- Its scope is the filesystem; extension to networks, APIs, and other resources is identified as future work.
- Implication for the thesis: The broad claim that incorrect/incomplete policies harm security or completion is not new. An API-level extension is possible, but changing the domain alone should not be considered sufficient justification.

### 6.5 SARA — distinguishing authorization decisions from agent recovery

- Title: **When Tool Outputs Become Commands: Separating Action Induction from Runtime Authorization in Tool-Augmented LLM Agents**.
- [arXiv](https://arxiv.org/abs/2608.27146), [full text](https://arxiv.org/html/2608.27146).
- Distinguishes a tool output inducing an action from that action being authorized; uses execution-time authorization and provenance.
- Evaluated on AgentDojo/AgentDyn; examines additional guard and agent-inference costs.
- The limitations section states that recovery after a denial depends on the host agent's replanning ability.
- Relevance to the thesis: Measuring enforcement separately from post-denial behavior is meaningful, but the observation that recovery matters cannot be presented as new.

### 6.6 CriticTool — recovery from tool errors is already studied

- Title: **CriticTool: Evaluating Self-Critique Capabilities of Large Language Models in Tool-Calling Error Scenarios**.
- [arXiv](https://arxiv.org/abs/2506.13977), [full text](https://arxiv.org/html/2506.13977), [code](https://github.com/Shellorley0513/CriticTool).
- Tool-selection, argument, and environmental errors; permission errors are included among environmental errors.
- Evaluates correction, retry, skip, and finish behavior.
- Implication for the thesis: The general idea of an agent tool-error recovery benchmark is not new. A specific feedback effect under a fixed authorization policy would need to be isolated.

### 6.7 ToolMisuseBench — a related artifact that might be useful

- [Dataset/readme](https://huggingface.co/datasets/sigdelakshey/ToolMisuseBench/blob/main/README.md).
- [Code](https://github.com/akgitrepos/toolmisusebench).
- The dataset citation lists Akshey Sigdel and Rista Baral as authors.
- CRUD, retrieval, files, and scheduling; controlled errors such as authorization failures, timeouts, and schema drift, plus budget limits.
- The dataset and repository readmes appeared to differ in versions/counts; a specific commit/release must be pinned before use.
- Not verified as a peer-reviewed publication; the artifact was not run. The availability of a benchmark does not automatically establish a research contribution.

### 6.8 Causality Laundering — information leakage through denial messages

- Title: **Causality Laundering: Denial-Feedback Leakage in Tool-Calling LLM Agents**.
- Mohammad Hossein Chinaei.
- [arXiv](https://arxiv.org/abs/2604.04035), [full text](https://arxiv.org/html/2604.04035).
- An ARM prototype addresses the use of information learned from denied calls in subsequent calls.
- The small evaluation uses three manually constructed attack scenarios; it must not be described as a broad, live, end-to-end LLM evaluation.
- Implication for the thesis: Detailed denial explanations are not automatically safer. Feedback should not disclose information beyond what the agent is already authorized to receive.
- Building a new information-flow security system within the main thesis could unnecessarily expand its scope.

### 6.9 AgentBound — limits of the enforcement layer

- Latest examined title: **AgentBound: Securing Execution Boundaries of AI Agents**.
- [arXiv](https://arxiv.org/abs/2510.21236), [full text](https://arxiv.org/html/2510.21236).
- Restricts MCP servers' access to system resources through manifests/sandboxing.
- Explicitly acknowledges the inability to prevent semantic misuse within permitted resources.
- System-level confinement and this thesis's task/record/argument-level checks are different and potentially complementary.

### 6.10 Other relevant sources and items requiring deeper reading

- [AgentDojo](https://arxiv.org/abs/2406.13352), [code](https://github.com/ethz-spylab/agentdojo): An important benchmark for evaluating attacks alongside legitimate task success. Verified as NeurIPS 2024 in the previous conversation. Not run locally.
- [InjecAgent — Findings of ACL 2024](https://aclanthology.org/2024.findings-acl.624/): Examples of indirect prompt injection originating in tool outputs.
- [Temporary Authority, Permanent Effects: Commit-Time Authorization for LLM Agents](https://arxiv.org/abs/2607.10487): Authority that was valid earlier may no longer be valid when the effect occurs; CommitGuard. Encountered at the abstract level and through PlanFence's citations in the earlier review; no decision was made to reproduce the entire system here.
- [Stateful Governance for Concurrent Agentic Systems](https://arxiv.org/abs/2608.02764): Provenact; stale authorization under changing state such as budgets/inventory. The authors' abstract was examined in the earlier review; the experiments were not audited in detail.
- [When Consent Outlives Context](https://arxiv.org/abs/2609.33910): Approval/authorization context persisting across tasks. The abstract was seen in the previous review; deeper verification remains pending.
- [NIST SP 800-207](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-207.pdf): Zero Trust is not a model aimed only at human users; non-person entities are also in scope.

### Limits concerning source quality

Conference acceptance was verified for AgentSpec. Many other recent sources listed here are arXiv manuscripts; this does not establish peer-reviewed acceptance. Large numerical performance claims were deliberately omitted from this file; if needed, they should be verified in the original source alongside the experimental conditions. A search-result summary must not be confused with a full methods review.

## 7. Latest proposed narrow contribution: authorization-denial feedback and safe recovery

**Status: An assistant proposal; neither the user nor Simo has explicitly accepted this specific subtopic yet.**

### Candidate research question

> Under fixed task-scoped permissions, how does authorization-denial feedback affect legitimate task recovery, appropriate stopping, and execution cost in an order-management workflow?

### Candidate contribution statement

> This thesis isolates the effect of authorization-denial feedback on recovery and appropriate stopping under a fixed task-scoped policy, using a reproducible order-management testbed with independently checked outcomes.

### Candidate title

**Authorization-Denial Feedback and Safe Recovery in Industrial AI Agents**

Do not automatically replace the user's selected main title with this title. It is one option for narrowing the same research area.

### Why was this contribution proposed?

Claiming a new task-authorization mechanism substantially overlaps with Progent and Intent-Governed Authorization. Isolating the behavioral effect of denial messages while holding the policy and enforcement constant could provide a smaller, measurable experiment.

The exact proposed matched comparison was not verified in the closely related works examined. **This is not evidence that nobody has done it.** Post-denial recovery and feedback are already part of the literature; the contribution could be to measure this component separately under specific conditions.

### Proposed comparisons

| Condition | Information returned to the agent |
|---|---|
| Generic denial | “Action denied.” |
| Reasoned denial | The permission boundary that was violated, with a short natural-language explanation. |
| Structured denial | The same reason and disclosable scope information, for example as JSON error codes/fields. |

**Two distinct research questions must not be conflated:**

- What is the effect of providing more information?
- What is the effect of presenting the same information in natural language versus a structured format?

If the last condition changes both information content and format, the two effects cannot be separated. One narrow primary comparison can be selected; a three-way or full factorial study is not mandatory. Reasoned denial should be considered a strong baseline close to Progent.

Feedback should not directly supply the correct next tool call/solution; otherwise, the experiment measures general assistance and an oracle advantage. Only information authorized for disclosure within the task should be used.

### Scenario classes

1. **Recoverable wrong target:** A write to record 456 is denied when the task concerns 123; the correct operation on 123 remains possible.
2. **Permitted alternative path:** A predefined alternative permitted route genuinely satisfies the original goal.
3. **Task impossible under current authority:** Completion requires missing permissions. Appropriate behavior is to stop or report the missing authority.
4. **Clean control:** A task that does not require a policy violation; measures unnecessary abandonment and basic competence.

If an order requires 40 units but authority permits only 20, producing a 20-unit draft cannot count as success unless the task's success criteria explicitly allow it. Silently changing the goal must be distinguished from legitimate recovery.

### What would the main research result be?

If the same correct enforcement blocks the same prohibited writes in every condition, the security rate may remain unchanged. This is expected. The denial message should not be credited with “improving security” on that basis.

The main outcomes are legitimate completion, appropriate stopping, repeated prohibited attempts, false success claims, and additional execution cost. Richer feedback could help, have no effect, or be harmful.

### Alternative narrowing

Analyze the completion–protection trade-off under under- and over-permissive task permissions at the API level. This is feasible, but its distinction from AuthBench and intent-governed authorization requires further justification. This alternative should not be packaged as a second thesis added to the feedback experiment.

## 8. The user's critical question: how will we get the agent to make an incorrect call?

The user reasonably asked: “If the prompt says 123, how will I get the agent to update 456?”

Three experimental levels must be clearly separated:

### A. Enforcement-layer correctness tests

- The test harness supplies valid/invalid tool-call examples directly to the authorization adapter.
- Tests boundaries such as wrong records, quantity limits, and unlisted operations.
- These tests establish whether enforcement works correctly.
- **They do not measure the probability of natural agent errors.** Basic unit-test results alone are not a thesis contribution.

### B. Controlled continuation experiments starting at the same denial point

- The task, conversation history, and denied call are prepared as a fixed starting state.
- Only the denial feedback returned to the agent changes; subsequent behavior is measured.
- Requires realistic histories and consistent service state.
- These conditions measure recovery after a denial has occurred; they do not establish how often the agent would spontaneously make that error.

### C. End-to-end agent experiments

- The agent selects tools and generates arguments through actual model calls.
- Clean, ambiguous, or manipulated tool-response conditions may be used.
- Manipulation does not guarantee an incorrect call.
- Runs with no errors/denials must also be reported; do not select only failed runs.
- The initial error rate and post-denial recovery are calculated separately.

Data from these three levels must not be mixed into a single success percentage. Controlled fault injection must be explicitly labeled.

## 9. Measurements and experimental quality

### Possible outcomes to measure

| Metric | Correct interpretation |
|---|---|
| Executed policy violations | Unauthorized service effects that actually occurred, rather than agent attempts or gateway blocks. |
| Legitimate task completion | Completion of authorized, solvable tasks, verified against independent business rules. |
| Appropriate stopping | Stopping without unauthorized effects/false success claims when the task cannot be solved under current authority. A different category from completion. |
| Repeated denied calls | Unnecessarily repeating the same/similar prohibited call; a behavioral and cost indicator. |
| False success claims | The agent reports completion, but the service state does not satisfy the goal. |
| Rejected authorized calls | Incorrectly blocking a call permitted by an independent definition of authority. |
| False task abandonment | Giving up when an authorized solution exists; different from an enforcement false positive. |
| Latency / inference cost | Measure enforcement-layer time separately from total workflow time; include tokens and model calls. |

Define the denominator of every rate in advance: tasks, attempted calls, and completed episodes are different units. A checker faithfully enforcing an incorrect policy input should not be classified as having an enforcement bug.

### Independent evaluation

- The agent's own account of success cannot be the main source of truth.
- Use service database snapshots and actual tool-execution logs.
- The evaluator should not duplicate the policy checker and share the same bug; independent business rules/manually reviewed fixtures are needed.
- Separate development and test scenarios; copies of the same template with only IDs changed must not be presented as different independent tasks.
- Control the model, prompts, tools, policy, and overall execution budgets across conditions.
- Repetitions of the same task must not be counted as independent new tasks. Paired differences and task-clustered bootstrap confidence intervals were considered.
- Define and report timeouts, parsing failures, API errors, and retries in advance.
- A null result can be valid; improved success must not be assumed.

### Model selection

The user asked whether a simple local model would be preferable because OpenAI models might be “too smart.” The methodological direction discussed was:

- A local model may be suitable for development and cost control.
- Do not deliberately select a weak model to make the hypothesis succeed.
- Check tool-use competence on clean tasks through a pilot.
- One main model can be fixed; if resources permit, use a second stronger model on a limited, preselected robustness subset.
- Report different models' results under the same conditions separately.
- No specific model, provider, or framework has been selected. VRAM capacity and the exact API budget are unknown.

## 10. AIGateKeeper: what was learned about the existing application

Source path: `C:/Users/canba/Desktop/workspace/AIGatekeeper`

The user explicitly authorized code inspection, and a read-only inspection was performed earlier in the conversation. During preparation of this handoff, only the continued existence of the directory was checked; the code was not audited again. The following findings come from the earlier inspection.

- A Go-based, self-hosted TLS interception proxy with a React web console.
- Extracts prompts/text from GenAI request bodies, scans for secrets/PII through DLP, makes allow/block/monitor decisions, and records audit events.
- OpenAI, Anthropic, Gemini, Copilot, Ollama, and generic parser paths were examined.
- Scanning tool arguments as text within conversation history is not actual tool-execution authorization.
- The examined policy inputs concerned service/passthrough/IP/bypass/oversize/parse errors/extraction and DLP findings.
- **The examined version did not implement actual task-scoped tool-execution authorization tied to task IDs, order records, and quantity limits.**
- It forwarded clean requests and streamed responses; the authorization gateway described here would require an additional adapter to be developed.
- The repository was not modified for this thesis, and tests were not run. Its full security properties should not be treated as verified.

The earlier inspection read the README and files associated with the names `policy/evaluate.go`, `policy.go`, `proxy/enforce.go`, `proxy/stages.go`, `parser/extractor.go`, and `audit/event.go`. Their exact subdirectories should be rediscovered; do not invent absolute paths from these names.

**User's document preference:** The initial research plan must **not mention AIGateKeeper by name**. Instead, describe the small authorization gateway application to be developed and its purpose. Inspiration or partial code reuse is possible; the thesis does not need to inherit all features of the existing product.

## 11. Expected personal and academic value

The user has repeatedly asked what the thesis would contribute to them and others, and what problem it solves. Explanations should use concrete examples.

Possible outputs:

- A small, understandable enforcement prototype operating between an agent and a business system.
- Reproducible tasks, policy fixtures, and experimental conditions.
- Evidence showing how particular designs behave in particular situations in terms of completion, cost, and appropriate stopping.
- AI engineering experience in tool integration, authorization boundaries, evaluation, failure analysis, and reproducibility.

Producing working software alone is not a research contribution. The contribution lies in answering an open question with controlled, comparable evidence. Do not promise salary increases, employment, a “top 1%” profile, or publication acceptance.

## 12. Claims corrected in earlier evaluations

The user shared a long strategic thesis report that strongly recommended authorization. The following overstatements were corrected:

- There was insufficient evidence for a “definitively winning topic” or career/salary guarantees.
- Cryptographic warrants, OBO identity chains, a general DSL/compiler, and multi-agent delegation should not all be added to one MSc thesis.
- Micro-/sub-millisecond latency must not be promised before measurement.
- Finite experiments are not a general mathematical security proof.
- NIST Zero Trust is not limited to human users.
- The number of blocked calls is not the number of actual unauthorized operations.
- Literature must not be distorted to validate earlier recommendations; contribution claims should be updated when closely related work is found.

Shared report path: `C:/Users/canba/.codex/attachments/c7b9d943-306f-4ca0-9357-572d3089e7a5/Pasted text.txt`. This report was not used as an authoritative research source.

## 13. Full English text of the current research plan

This is the content of the references-free PDF that was created. **It is an initial draft predating the latest literature review and should not be read as approval of the final contribution.** Although references appear elsewhere in this knowledge file, they are omitted from the plan at the user's request.

### Task-Scoped Runtime Authorization for Industrial AI Agents

#### 1. The Purpose of the Work

An agent permitted to call a business tool may still act on the wrong record or exceed the authority of its current task. Tool-level allowlists cannot express all such restrictions. This thesis proposes an authorization gateway prototype to examine whether binding permissions to a trusted task context improves safety without excessively blocking legitimate work.

Research question: How does task-scoped authorization affect executed policy violations and legitimate task completion compared with static tool permissions?

#### 2. Methods and Materials

The prototype will mediate between one AI agent and a simulated industrial order service. It will inspect proposed tool calls, evaluate their names and arguments against trusted permissions, allow or reject execution, and log decisions for evaluation. The resettable service will expose four tools: read an order, check inventory, create a draft, and update a draft. Three conditions will be compared: tool-name allowlists; tool-name and static argument restrictions; and the same restrictions augmented with task-specific record identifiers and operation limits. A trusted application will supply task permissions independently of model output. Every tool execution will pass through the gateway before reaching the service.

An initial target of approximately 80 held-out scenarios will pair authorized requests with controlled attempts to access unrelated records or exceed quantity limits. Both clean and manipulated tool responses will be included. Policies and prompts will be frozen after a separate development set. Conditions will use the same agent model, tools, initial database states, and step budget, with three repetitions per scenario. A separate database audit will determine actual effects rather than rely on agent claims. Measurements will include executed violations, legitimate task completion, rejected authorized calls, and added latency. Paired comparisons and scenario-level bootstrap confidence intervals will assess differences. Incorrect or incomplete trusted task contexts will be tested separately as a sensitivity analysis. The scope excludes multiple agents, automatic policy generation, approval interfaces, interviews, and production ERP integration.

#### 3. Expected Results

Expected outputs are an enforcement adapter, a bounded policy representation, and evidence on the protection-overblocking trade-off of task-bound permissions. Results will identify where contextual restrictions add value beyond static argument checks. Conclusions will depend on complete mediation and correct policy inputs; the study will not claim that a gateway alone makes arbitrary agents safe.

## 14. Files and formatting preferences

### Main files

| File | Description |
|---|---|
| `C:/Users/canba/Documents/Codex/2026-10-01/s/KNOWLEDGE.md` | This handoff. |
| `C:/Users/canba/Documents/Codex/2026-10-01/s/output/pdf/Task_Scoped_Runtime_Authorization_Research_Plan_No_References.pdf` | Latest standalone authorization plan; one page, no references/links, no mention of AIGateKeeper. |
| `C:/Users/canba/Documents/Codex/2026-10-01/s/output/Thesis_Contribution_Literature_Review_2026-10-13.md` | Latest detailed review comparing the two candidate topics. Its “topic not yet selected” context is superseded by the user's latest decision. |
| `C:/Users/canba/Documents/Codex/2026-10-01/s/work/build_authorization_no_references.py` | Existing helper script that generates the standalone plan. |
| `C:/Users/canba/Documents/Codex/2026-10-01/s/work/build_aigatekeeper_plans.py` | The earlier five gateway plans; the standalone script uses definitions from this file. |
| `C:/Users/canba/Documents/Codex/2026-10-01/s/work/build_research_plans.py` | Shared PDF renderer and the earlier five general thesis ideas. |
| `C:/Users/canba/Desktop/university/thesis/Research-Plan-v2_Can-Baturlar.pdf` | Previous PSD plan and formatting reference. |
| `C:/Users/canba/Desktop/workspace/AIGatekeeper` | Code for the existing personal application. |

Other historical files, with relative paths rooted in `C:/Users/canba/Documents/Codex/2026-10-01/s`:

- `output/pdf/AIGK_02_Task_Scoped_Authorization_Research_Plan.pdf`: Older version containing the AIGateKeeper name and references; do not confuse it with the newer standalone version.
- `output/pdf/Can_Baturlar_AIGateKeeper_Five_Research_Plans.pdf`: Earlier combined document containing five alternatives.
- `output/pdf/Version_Aware_State_Sharing_Research_Plan_No_References.pdf`: Draft of the other topic, which was not selected.
- CV: `C:/Users/canba/Desktop/cv/v3/with-photo/Can Baturlar – CV.pdf`. No unverified list of skills, courses, or grades was derived from the CV for this knowledge file.

### Research-plan preferences

- English, **one page**.
- The same structure as the existing PSD research plan:
  1. The Purpose of the Work
  2. Methods and Materials
  3. Expected Results
- The user's current standalone-plan request specifies **no links/references**.
- Do not use the AIGateKeeper name; describe the application to be developed by its general function.
- This preference does not mean that citations should be omitted from the actual thesis or literature research.
- The previous renderer uses an approximately A4-sized page, roughly 72 pt margins, Times New Roman 12 pt body text, and a centered title. Reuse the existing source scripts if appropriate.
- The user previously asked “where is the file?” because the file was not apparent. Always provide a normal clickable Markdown file link when delivering a file.

### Previous technical environment

Windows / PowerShell. The absolute paths in this document belong to the current machine; accessibility in another chat or environment is not guaranteed.

Previous Python path: `C:/Users/canba/.cache/codex-runtimes/codex-primary-runtime/dependencies/python/python.exe`. PDFs were generated using ReportLab, verified through pypdf/pypdfium2, and visually inspected. Environment/skill paths may change and should be rediscovered when needed.

## 15. Limits of findings from Finnish thesis repositories

The user previously requested Finnish university thesis repositories as sources for the deeper literature research. The latest review included:

- [Oskari Palojärvi — Analysing security incidents using multi-agent AI systems, Aalto 2025](https://aaltodoc.aalto.fi/items/8ef9433a-9fa2-44e8-8bbf-7dbae5121766): Listed as an MSc thesis in the repository; a related example of implementation and multi-agent evaluation. The search/repository summary was seen, but the full thesis methodology was not analyzed.
- [Aleksi Kalliomäki — Large Language Model (LLM) agents: Applications and security, Aalto 2025](https://aaltodoc.aalto.fi/items/e94bb73f-3a39-448d-9fea-6fabdb1394fa): A bachelor's literature review. It is not evidence for an MSc experiment's scale or the novelty of the selected contribution.

This review does not imply an exhaustive search of Finnish repositories for the selected narrow topic. Further research may examine the Oulu, Tampere, and Aalto repositories for examples of methods and scale; theses should not be treated as guarantees of novelty.

## 16. Outstanding work and a sensible continuation in the new chat

### Not yet done

- No experimental testbed, agent loop, or authorization adapter has been developed for this thesis.
- Paper code has not been run, and results have not been reproduced.
- No model/API/framework has been selected.
- No dataset has been collected, and no evaluation tasks have been written.
- No pilot has been conducted, and no statistical results have been obtained.
- No detailed meeting notes from Simo have been obtained concerning the new sub-question/contribution.
- Thesis collaboration with GPT-Lab has not been finalized.

### Suggested order of continuation

1. If Simo's feedback includes a specific sub-question, expectation, or methodological detail, obtain it from the user; proceed without reopening the main authorization decision.
2. Examine specific versions, experiments, and artifacts of the closest works in depth, particularly Progent and Intent-Governed Authorization.
3. Select one bounded contribution statement and research question: the original policy comparison, the feedback/recovery narrowing, or another properly justified extension.
4. Define the baseline, controls, intervention, and independent success criteria on one page.
5. Consider approximately 12–20 scenarios for a small development pilot; this number is a suggestion. First check clean-task competence and correct enforcement, then measurable behavioral differences.
6. Determine the main evaluation size based on pilot variance and cost; do not automatically treat 80×3 as the final design.
7. Update the research plan to reflect the narrowed contribution. Update this handoff as implementation and experimental results progress.

This sequence is not an instruction to start building the entire application. It is context to help the new chat continue according to the user's next request.

## 17. Distinctions the next assistant must preserve

- **Decided:** Proceeding in authorization with Simo.
- **Not decided:** The denial-feedback subtopic, exact research question, and final experimental matrix.
- **Current knowledge:** Closely related runtime/task-authorization work exists; the initial mechanism claim is not new.
- **Candidate contribution:** A controlled empirical comparison or bounded replication/extension.
- **Not established:** An entirely original method, industry-wide prevalence, a positive result, or guaranteed academic value.
- **Existing application:** The personal AIGateKeeper project.
- **Not implemented:** The task-scoped experimental enforcement and benchmark proposed here.
- **Successful permission enforcement:** A prohibited effect was prevented.
- **Successful task:** The user's actual goal was achieved within the permitted authority. These two forms of success are different.
- **Appropriate stopping:** A meaningful outcome when the goal is impossible under current authority; it does not count as a completed task.
- **User preference:** Small scope, no interviews, prototype + data + comparison, with concrete and understandable explanations.

Starting point for the new chat: **The main area has been selected. The next goal is to finalize the academic contribution and a feasible, narrow experimental design within that area.**

## 18. First 20-paper critical review completed, 13 October 2026

Can supplied 20 PDFs in `reference/authorization-papers` and requested careful reading to produce solid findings, initial research questions, and a methods/materials path. Browser use, including Chrome if needed, is authorized. This run used local full-text extraction, targeted visual checks of PDF tables/figures, and primary-source web checks. It did not need Chrome UI automation.

### Saved review package

- [Findings and recommendation](<C:/Users/canba/Desktop/university/thesis/idea1-Authorization/literature/REVIEW_FINDINGS_2026-10-13.md>)
- [Individual critical notes for all 20 papers](<C:/Users/canba/Desktop/university/thesis/idea1-Authorization/literature/PAPER_NOTES_01-20_2026-10-13.md>)
- [Proposed study protocol](<C:/Users/canba/Desktop/university/thesis/idea1-Authorization/literature/PROPOSED_STUDY_2026-10-13.md>)
- [Supplementary checks and focused download list](<C:/Users/canba/Desktop/university/thesis/idea1-Authorization/literature/SUPPLEMENTARY_CHECKS_2026-10-13.md>)
- [Corpus manifest with exact versions/page counts/SHA-256](<C:/Users/canba/Desktop/university/thesis/idea1-Authorization/literature/CORPUS_MANIFEST_2026-10-13.json>)

The corpus totals **496 PDF pages**, including references/appendices. Review focused on full-text methods, assumptions, evaluation, results, limitations, and relevant appendix details. Do not claim that every appendix prompt/proof was independently verified or that any experiments were reproduced. Eight key pages were visually checked. Intermediate extraction/rendering material is under `tmp/pdfs/`.

### Main findings that supersede abstract-only impressions

1. Task-scoped tool/argument enforcement is substantial prior art: Progent, Conseca, Intent-Governed Authorization, FORGE, and related systems. The original broad mechanism comparison needs replication/extension framing.
2. Explanatory denial and corrective guidance are already present: Progent p. 5; Conseca pp. 3-4; FORGE pp. 35-36; SARA p. 8. Do not claim a new mechanism merely for returning reasons, JSON, or alternatives.
3. Intent-Governed Authorization's reviewed v4 real-model study reports 40/198 unsafe accepted drafts, zero unsafe executed effects, **0/108 strict benign completions**, and 36/108 governed artifacts. This distinction is central, not an accusation that its review-oriented design fails its own stated purpose.
4. FORGE's 58%-to-98% comparison is six selected tau² tasks, three models, five trials (52/90 to 88/90), not the full benchmark. Enforcement, feedback, and policy presentation are changed together; it does not isolate feedback.
5. Verifier Tax's main protocol automatically accepts the last proposal after three rejections. Its retrospective fail-closed analysis is not a separate end-to-end rerun. Some recovery subsets are tiny.
6. ToolMaze may count appropriate termination as success. tau-bench's final-state reward explicitly can overlook a confirmation-policy violation. Separate lawful goal completion, appropriate stopping, prohibited attempts, and actual effects.
7. ToolMisuseBench P15 reports three deterministic heuristic baselines, not LLM results. Its newer v0.2 dataset/roadmap includes typed recoverability, stronger baselines, and recoverable/unrecoverable authorization ideas. Reconcile code/data/paper versions before reuse or novelty claims.
8. P08 is AuthBench, P18 is AuthorizationBench, and P17 is AgentBoundary. P06's supplied version uses FORGE rather than the older PCAS name. Exact PDF versions are in the manifest.

### Recommended candidate, still NOT selected or approved

Working title: **Recovering Within Authority: Evaluating Denial Feedback for Tool-Using AI Agents in Order-Management Workflows.**

Recommended contribution: controlled empirical extension with fixed deterministic task-scoped enforcement; compare generic denial, reason, and reason plus bounded task-visible guidance. This is an information-content comparison, not a pure JSON-format experiment.

- RQ1: How does feedback affect authorized completion when a valid authorized solution remains?
- RQ2: How does it affect appropriate stopping, repeated prohibited attempts, and false completion claims when no authorized solution exists?
- Cost/calls/tokens/latency are secondary outcomes.

Primary design: identical pre-denial checkpoint across treatments, explicit repairable/alternative/no-authorized-solution strata, clean competence controls, independent state/trajectory/authority oracles, fixed fail-closed policy, no automatic widening. The imposed initial call is not a model-generated continuation attempt. A smaller natural end-to-end check measures exposure separately. Under correct fixed enforcement, zero forbidden effects is an invariant, not proof that one feedback arm improves security.

Keep one agent, one simulated order workflow, approximately four tools, trusted application-supplied contracts, and frozen feedback templates. Do not start implementing a full platform or rewrite the standalone plan as an accepted direction without Can's selection. Pilot/main counts in the protocol are illustrative and require variance/cost checks; no paid-run budget or model has been chosen.

### Closest new work checked and remaining reading

Primary HTML method/result checks found close prior art in **Schema First Tool APIs** (2603.13404v1), **PROBE / Debugging the Debuggers** (2605.08717v1), and **AIR** (2602.11749v1). Local PDFs are requested for the archive. **CaMeL / Defeating Prompt Injections by Design**, already P25 (2503.18813v2), remains a priority full-text architectural check. **Loud Failures, Quiet Failures** (2610.10062v1) is useful optional measurement reading.

The Hivemind Labs research note *Prompt less, check more* directly compares specific feedback and generic retry but acknowledges message/prompt/gate confounds and experimental final-attempt release. Cite it as a company research note. ToolMisuseBench v2's roadmap already discusses recoverability and safe stopping. These narrow the potential contribution; a global absence/first-ever claim is unjustified.

No testbed, dataset, model comparison, empirical results, company agreement, or research-assistant appointment resulted from this review. The next step is to discuss the saved recommendation with Can, complete the bounded closest-work checks, choose the contribution with supervisor input, and finalize the plan within the two-week window. The proposed schedule aims for 27 October 2026 and leaves system development/main experiments for later phases.

## 19. Scope-selection priority clarified by Can, 13 October 2026

**This clarification supersedes novelty-driven ranking in section 18.** Can explicitly said the aim is not the most unique scope or inventing a new mechanism. The research must be doable, academically sound for the MSc thesis, and a good area for GPT-Lab. He will read the documents and has not selected the denial-feedback direction.

Do not push the topic into a narrower or more complex gap merely because related work exists. Applied implementation, adaptation, replication, and comparative evaluation of established methods are acceptable candidate contributions under his stated expectations. They still require clear questions, sound baselines, useful measurements, and honest conclusions; supervisor/lab suitability must not be guaranteed by the assistant.

Reassess the original authorization-method comparison as a main candidate, not merely infrastructure validation. It is the direct continuation of the draft Simo and Jussi saw. Denial feedback remains an optional alternative whose extra requirements (matched checkpoints, feasibility labels, termination scoring) need justification through practical value and workload. Do not combine both into a large factorial study by default.

The findings document and optional feedback protocol were updated to reflect this. Prioritize one agent, one simulated workflow, a few tools, hand-written trusted policies, and independent state/effect checks. Company access and a research-assistant role remain unconfirmed and must not be prerequisites for finishing the thesis. No new research direction was selected by this clarification.

## 20. Oulu thesis requirements checked against the supplied PDFs

Reviewed `reference/thesis_instructions/CSE_diploma_thesis_instructions.pdf` (41 pages, cover June 2026) and `Evaluation_Instructions.pdf` (two pages, no visible issue date). Detailed findings and requirement-to-study mapping: [Oulu requirements and scope](<C:/Users/canba/Desktop/university/thesis/idea1-Authorization/literature/OULU_REQUIREMENTS_AND_SCOPE_2026-10-13.md>). This was a review of supplied files, not independent verification of the latest official release or current administrative deadlines.

Key evidence supports the scope clarification in section 19:

- Guide p. 32 explicitly says the solution does not have to be better than prior work, but analysis against objectives and comparison with the state of the art are essential.
- Guide p. 31 requires a significant personal contribution through independent analytical problem-solving, comparing alternatives, and justifying choices. Mere execution of instructions is insufficient.
- Guide pp. 11, 16, 31-32 expressly accommodate software design, implementation, and testing. Applied evaluation of established methods is a credible thesis form; no blanket requirement for a new algorithm was identified.
- Guide p. 30 warns against overly ambitious objectives and says a separate theory section is unnecessary if it does not fit naturally.
- Rubric aspects 5 and 7 mention major new results/publication/patents at the upper end of particular descriptors, not as universal thesis requirements. Scope and challenge also matter; do not make the study trivial or promise a grade from the rubric.
- Results must be measured, evaluated against goals, and critically discussed; estimates must not be mixed with actual findings (guide p. 32; rubric aspect 6).
- A university research unit may act as commissioner (p. 11); company involvement is not the only route. Interviews appear as an example for eliciting requirements, not a universal requirement (p. 31).
- Literature coverage should be thorough for the selected scope; use original sources and accurate IEEE referencing (pp. 33-34). Twenty papers are not an automatic completeness threshold.

AI-use requirements are relevant to this collaboration: guide pp. 13 and 20-21 require prior discussion/approval with the supervisor and a subsection titled **Author's Contributions and the Role of Artificial Intelligence**, specifying tools, purposes, and affected parts. Can remains responsible for accuracy/originality; AI is not a scientific source. The guide cautions against generating thesis parts and presenting them as one's own. Treat our documents as planning aids and accurately disclose actual assistance. Simo's approval of any particular AI-use arrangement has not been established; this is a supervisor requirement in the supplied document, not a reason to halt authorized planning assistance here.

The original authorization-method comparison remains a live candidate. The requirements check does not choose the topic or establish GPT-Lab's acceptance of a specific scope. Exact scope should be assessed for manageable workload, nontrivial independent work, and useful evidence, then discussed with Simo and Jussi.

## 21. Decision: Candidate B for the thesis, Candidate A as possible future research

**14 October 2026: Can explicitly selected Candidate B**, the authorization-method comparison, for the master's thesis and possible research publication. He considers it the safer option given the available literature. This supersedes earlier statements that the candidate choice is open. The exact comparison, research questions, implementation, model budget, and supervisor/lab approval remain outstanding.

Can also likes Candidate A's goal and intends to mention it in meetings as possible research after the master's thesis. Preserve its protocol as a future option, not an additional required thesis experiment. Do not expand B into a combined authorization-by-feedback factorial design by default.

The two studies can build on one another: B varies authorization approaches and measures protection/utility/cost; A fixes an authorization approach and varies denial feedback to measure lawful recovery and appropriate stopping. B can supply a validated environment, task contracts, independent effect/goal checks, and traces showing useful recovery cases. A would still need dedicated feasibility labels, matched denial checkpoints, its own held-out evaluation, and an updated literature check.

Low-cost preparation within B can include a separate feedback-rendering function and logs of attempted calls, denial categories, executed effects, and final task outcomes. These are proposed design considerations, not already implemented features or permission to begin A now. B must be a complete standalone thesis. Valid findings can be positive, negative, or null; progression to A does not require one authorization method to outperform all others.

Do not describe A as proven more unique or more publishable. It is a narrower question that may yield a distinctive empirical contribution, but the review found related work on explanatory denials, structured recovery, and feedback comparisons. Publication potential for either direction depends on the eventual contribution, rigor, findings, and venue; no publication is guaranteed.

## 22. Candidate B feasibility assessment, 14 October 2026

Can requested a feasibility assessment before refining the plan, with traceable source support for questions such as “why this research question?” and “why this method?”. He prefers literature/artifact checks before planning, not a pre-plan demo. The agreed sequence is assessment → refined plan → Simo/Jussi discussion → implementation/pilot → main experiment.

Delivered [Candidate B feasibility assessment and evidence for the research plan](<C:/Users/canba/Desktop/university/thesis/idea1-Authorization/literature/CANDIDATE_B_FEASIBILITY_2026-10-14.md>). It supports proceeding conditionally, based on the existing full-text review, renewed checks of key passages, the original draft, Oulu guidance, official repository manifests/licenses and selected source code, and targeted NIST ABAC guidance. No thesis system was implemented, dependency installed, paid model run performed, or source result reproduced. The original plan PDF/Word remains unchanged.

Important recommendations for the next plan revision (not yet approved):

- One simulated order-draft workflow, four tools, one agent; independent task/effect evaluation. Draft changes are simulation effects, not production orders.
- C1 task-type tool-name permissions; C2 adds meaningful standing task-independent argument restrictions; C3 adds trusted current-task record/field/value/effect bounds. Same visible tool schemas, task information, model, dispatcher, and feedback format. This is a configuration comparison, not a reproduction or ranking of whole published systems.
- RQ1 compares executed violations and authorized completion. RQ2 measures local/end-to-end costs and a small separate task-contract sensitivity analysis. Exact wording is in the assessment.
- Static rules can evaluate changing task attributes. NIST SP 800-162 supports established ABAC foundations; do not frame task scope as something conventional ABAC inherently cannot express.
- Policy expressiveness makes some probe differences predictable. Include cases where C1/C2 suffice and legitimate near-neighbours. Separate deterministic boundary probes from natural end-to-end agent evidence.
- Independent access/event and state-transition checks must supplement final-state audits: reads and temporary unauthorized writes can otherwise be missed. Keep intended authority distinct from enforcement inputs, especially for contract sensitivity.
- Approximately 80 scenarios remains a placeholder. Forty distinct families × two variants × three conditions × three repetitions = 720 main episodes for one model, excluding development/sensitivity. Eighty families would double this. Final scale and budget require development evidence; no power claim made.
- Recommended small Python harness is a design inference. Progent, AgentDojo, and original tau-bench provide inspectable MIT-licensed root code and implementation precedents, not verified local compatibility. Root licenses do not audit bundled components. Pin versions if reusing; old tau tasks are marked outdated, successor repository now describes tau³.
- Additional focused download: NIST SP 800-162 (official PDF linked in assessment), for definitions and trustworthy attributes. No bulk new paper collection is necessary before revising the plan; a focused literature update remains part of later thesis work.
- Main unresolved matters: model/access/budget, validated scenarios/scorer, actual workload/calendar, Simo's exact scope approval, and Jussi's concrete use-case fit. Broad GPT-Lab interest remains distinct from company access or employment.

The assessment includes a rationale matrix, source/page register, implementation materials check, workload example, risks/fallbacks, and short meeting answers. Treat it as a planning aid; the user should verify and cite the underlying original sources in the formal plan/thesis. Candidate A remains future work, not an added factor in B.

## 23. Research-plan requirement supplied by Can, 14 October 2026

Can supplied university instructions stating that the research plan entered in Laturi is **maximum one A4 page** and must contain: (1) The purpose of the work; (2) Methods/material/devices/software to be used; (3) Expected results. Supervisors approve the plan in Laturi. This is a formal length/structure constraint according to the supplied excerpt, not merely a personal formatting preference. The original webpage URL was not supplied or independently verified in this update.

The excerpt places the main thesis work, including software design/building/testing, in the subsequent stage. It does not state that a completed demo is needed for plan approval. Preserve the agreed sequence of feasibility assessment, concise plan, supervisor discussion/approval, then implementation and pilot. The plan needs a justified direction and credible method; it need not contain the full experimental protocol.

Keep the existing research plan within one A4 and the three required headings. **Can subsequently clarified that this is the actual research plan we already have, not a separate document to call a “Laturi plan.”** He supplied the university excerpt as extra context. The supporting rationale is personal reading for him; he will not upload it. Maintain its detailed source/page evidence without treating it as an additional required submission. The excerpt neither requires nor prohibits references; do not invent a mandatory bibliography or formal appendix submission. Evidence-backed choices remain essential even when the full evidence matrix is outside the one-page plan.

The supplied instructions also describe later supervisor review and student revision, graduation-related applications/tasks, supervisor evaluation, degree programme committee grade acceptance, and faculty degree granting. These are process context, not a verified current administrative checklist or deadlines. No plan or Laturi submission was created by this informational update.

## 24. Existing research plan revised, 14 October 2026

Can explicitly authorized updating the initial research plan after clarifying that it is the existing actual one-page plan. He downloaded `reference/authorization-papers/P21_ABAC-guide.pdf`. Checked its 47-page identity/version (NIST SP 800-162, January 2014 with 2019 updates) and targeted physical pp. 16–17, 38–39 on ABAC and authoritative attributes. Do not claim a full P21 review or include it retrospectively in the original 20-paper manifest.

Updated the existing files in place:

- [Research plan PDF](<C:/Users/canba/Desktop/university/thesis/idea1-Authorization/Research-Plan-Authorization-Agents_Can-Baturlar-DRAFT.pdf>)
- [Editable research plan](<C:/Users/canba/Desktop/university/thesis/idea1-Authorization/Research-Plan-Authorization-Agents_Can-Baturlar.docx>)

Previous copies are preserved under `idea1-Authorization/archive/2026-10-14-before-feasibility-revision/`. The revised document retains the original title, student identification, Times New Roman presentation, and three required headings. It contains 411 words and is one A4 page, verified through Microsoft Word PDF export, PDF page-size/count checks, and visual inspection. The packaged LibreOffice renderer was unavailable; Word rendering succeeded after the required execution escalation. No Laturi upload, external message, or supervisor approval occurred.

Revision content: two explicit RQs covering violations/authorized completion and costs/task-context sensitivity; one Python agent/service simulation with four tools; tool-name, standing-argument, and added task-bound configurations; direct checks plus held-out agent runs; capable legitimate controls; independent access/intermediate-state/final-outcome evaluation; matched settings; family-aware uncertainty; final sample size and cost set by development pilot instead of committing to 80 scenarios and three repetitions. Expected results are comparative evidence, without promising superiority. Candidate A remains future work. The supporting feasibility rationale has local P21 links and remains for Can's personal reading, not an extra upload.

## 25. Mock supervisor questions answered, 14 October 2026

Can supplied 20 mock questions about the updated plan and asked whether we can answer them. Saved complete personal preparation notes in [Supervisor mock Q&A](<C:/Users/canba/Desktop/university/thesis/idea1-Authorization/literature/SUPERVISOR_MOCK_QA_2026-10-14.md>), with page-level evidence and a source register. This did not revise the Word/PDF plan or implement any system.

Key qualifications: tighter action sets predict some direct-check differences by construction; the empirical study must address completion, realized behavior, and costs, with explicit scenario strata. Identical denial wording does not eliminate feedback-policy interactions. Correct exact policies should not produce false denials; treat these as diagnostics, distinguish configuration limitations from implementation bugs and contract corruption, and avoid promising an overblocking trade-off. A reference path does not cover every valid solution. No final family count is justified yet; renamed IDs/repetitions must not inflate independence. One model supports conditional system findings, not model-independent behavioral claims.

The document proposes concrete implementation rules for trusted task provenance, new-draft binding, generic denial content, resource-existence disclosure tests, retry accounting, independent read/transition scoring, final-claim evaluation, and one-at-a-time contract perturbations. These are recommendations requiring protocol decisions, not already agreed or implemented features. A second-model robustness subset is optional, selected prospectively if affordable.

It also proposes an 80% family-weighted clean C1 raw-goal competence screening target (alongside authorized-completion inspection and no consistently unusable workflow class), a 31 January 2027 scope checkpoint, and a 15 February 2027 pilot freeze target. **These numbers/dates are explicitly illustrative recommendations, not literature requirements, empirically validated thresholds, user commitments, or supervisor-approved dates.** Actual sample size, model/budget, calendar, and statistical precision remain unresolved. The core research plan remains a credible bounded direction; mock-question answers do not establish successful experiments or company validation.

## 26. Methods clarification and tool-count removal, 17 October 2026

The current PDF had been renamed to `idea1-Authorization/Research-Plan-Authorization-Agents_Can-Baturlar.pdf` (without `-DRAFT`) before this edit. Retained that filename when saving; older links to the former DRAFT path may be stale. The editable Word filename is unchanged.

Can asked to remove the fixed count of four tools from the research plan. Updated the existing Word/PDF files to say “synthetic data and tools for order lookup, inventory checks, and draft management.” Preserved other current text and formatting, including user-added spacing. Word export and visual inspection confirmed one A4 page. Previous versions are under `idea1-Authorization/archive/2026-10-17-before-tool-count-removal/`. Earlier four-tool descriptions remain proposed examples, not a fixed scope commitment.

Can also asked for explanations of deterministic versus non-deterministic authorization, scenario/control terminology in Turkish, infeasible-under-authority scenarios, freezing policies/prompts, independent evaluation, and using a small set of LLMs of different capabilities. He is interested in possibly evaluating lower/middle/higher capability models; no particular models, exact count, costs, or protocol changes have been approved.

Guidance for these questions: prefer deterministic rule-based enforcement of structured authority for Candidate B; the same complete policy/call/trusted-state inputs give the same decision, but changing state/context may legitimately change it. LLM-based semantic authorization is possible but adds decision-quality, variability, and cost factors and is not part of the current core. An independent evaluator means a separately implemented automated scoring module designed by Can, not necessarily another person or LLM; it must not use the monitor's own allow/deny result as ground truth. Freezing means fixing/versioning prompts and rule logic for the main comparison, not forcing every task to have identical permission values.

Recommended potential additions, still under discussion: a small separately scored set with demonstrably no authorized completion path, rather than merely an unverified solution; and a small selection of capable LLMs evaluated under all three policy configurations. Within-model policy comparisons stay primary; model comparisons are secondary robustness evidence. No-authorized-path cases must not enter the feasible-task completion denominator. Capability tiers need operational criteria and clean-task competence, not assumed universal model rankings. The only document edit in this turn is removal of the fixed tool count.

## 27. Small model selection approved and infeasible cases discussed, 17 October 2026

Can approved adding “a small selection of tool-using LLMs” to the research plan. Updated the current Word and PDF in place, matching model settings and the other experimental conditions across authorization configurations for each model, and changing the limitation to “evaluated models.” The architecture remains one agent per run. No exact model count, names, capability tiers, or budget is committed. Word export, page-size/count checks, and visual inspection confirmed one A4 page (415 words). Previous copies are preserved under `idea1-Authorization/archive/2026-10-17-before-multi-model-revision/`.

No-authorized-path scenarios remain a discussion, not an approved plan addition. Recommendation: a small secondary evaluation, with the same infrastructure and three policy conditions; no new recovery method, feedback comparison, or human-approval subsystem. Keep feasible-task completion separate from safe handling of infeasible requests. Evaluate prohibited attempts/executions, stopping versus budget exhaustion, false completion claims, and wasted calls. Honest stopping needs an explicit rubric; safety alone does not establish successful handling.

Rechecked P13 (ToolMaze), physical pp. 4–6, especially Section 3.5: permanent faults in single-path C1 tasks have no alternative, and graceful termination is treated as an appropriate outcome. This is methodological precedent for evaluating stopping, not an authorization-specific replication. Source: https://arxiv.org/html/2606.05806v1 . Rechecked P18, physical p. 5, Section 3.3: AuthorizationBench deliberately preserves a safe completion path as well as executable out-of-authorization actions. It supports the feasible core, not a claim that it evaluates no-authorized-path tasks. Author PDF: https://www.zhipingzhang.com/_files/ugd/3840b5_415101659c9f406d888aa5fce66889d5.pdf . These sources justify design options, not guaranteed results or thesis/company acceptance.

Distinguish genuine insufficiency of intended authority from an incorrectly narrow supplied permission contract (already part of RQ2 sensitivity), technical failure, and an agent merely failing to find a valid path. A bounded example is a request for quantity 20 when the actual delegated authority permits at most 10, with no available authorized approval or alternative path. Validate impossibility against all implemented tools and transitions. A user request must not implicitly override the authoritative organizational constraint. The expected gateway block is by construction; the empirical interest is agent behavior and costs, not demonstrating the obvious block as a discovery. Candidate A remains future work.

## 28. Subsequent scope and supervisor feedback, recorded 2 November 2026

Can explicitly deferred no-authorized-solution scenarios: do not add them to the current core. They can be reconsidered during development through an explicit scope decision. He retained the central purpose sentence about additional protection while preserving legitimate work. The current research plan PDF is now `idea1-Authorization/Research-Plan_Can-Baturlar.pdf`; the editable Word filename is unchanged. This turn read the actual one-page PDF and confirmed the two RQs, no fixed tool count, a small selection of LLMs, deterministic enforcement, independent evaluation, and separate permission sensitivity. No research-plan edit was made.

Can quoted Simo as saying the plan suffices for Laturi, while its terminology needs clearer explanation for thesis readers. Simo specifically asked what “evaluator” means. For this study it is separate automated scoring implemented by Can, not an assumed extra researcher or LLM. Simo advised skimming a couple of same-programme MSc theses to calibrate depth and suggested approximately 60–70 pages without unnecessary length. This does not establish a formal page limit or completed Laturi approval. Formal second-supervisor appointment, company involvement, and employment remain unconfirmed. Can is currently waiting for Jussi's response.

## 29. Phased roadmap and pending Miro upload, 2 November 2026

Can requested a full Markdown roadmap followed by an actual Miro mind-map board, covering personal reading, development, evaluation, and thesis writing. Created [THESIS_ROADMAP_2026-11-02.md](<C:/Users/canba/Desktop/university/thesis/idea1-Authorization/THESIS_ROADMAP_2026-11-02.md>). It includes eight phases, ordered local-source reading, independent-evaluator design, fair controls, pilot/freeze gates, family-aware analysis, writing guidance, a provisional calendar, and a first-week checklist. All local links were checked. The November–May dates assume limited availability through 13 December and full focus from 14 December; these are planning assumptions, not agreed graduation deadlines. Exact tools/models/sample sizes remain open. Publication and company integration are not completion dependencies.

Inspected opening pages and contents of `example-thesis/regime-aware-ml_Fatih-Sakiz.pdf`: Oulu CSE MSc, June 2026, 76 PDF pages, title “Regime-Aware Machine Learning for Dynamic Risk Management in Algorithmic Trading.” Its structure is a suitable local reading example, not a full methodological quality endorsement. Suutari (2024), repository handle 10024/53313, remains a suggested second example; Zeeshan (2024), handle 10024/51077, optional. Some Oulu web requests failed during this update; the roadmap does not claim freshly verified administrative dates.

**Miro work is incomplete because the connection changed mid-task.** An empty board was successfully created at `https://miro.com/app/board/uXjVETfz_tM=/` with the initial connection. Before any content upload Can reported changing Miro accounts and subsequently confirmed reconnection in Codex. All subsequent identity/search/composer calls returned `Unknown tool`; plugin discovery returned no Miro result. Do not upload to the earlier board without checking the current connection/account and appropriate destination. Do not report the empty board as complete.

The complete native-editable Canvas Composer payload is saved as [THESIS_ROADMAP_MIRO_2026-11-02.svg](<C:/Users/canba/Desktop/university/thesis/idea1-Authorization/THESIS_ROADMAP_MIRO_2026-11-02.svg>): three frames, 42 labeled nodes, 32 attached connectors; XML, unique IDs, and connector references validated. It is authoring data, not a standard rendered SVG preview. Once Miro works, check the account/destination, create the board if needed, upload the saved SVG using canvas_create_from_svg, inspect result/read-back dimensions and content, fix any overlap, add the final canonical board URL to the roadmap, and call board_show once. No user sharing/invites are authorized or required.

Miro authoring guidance was loaded. `canvas_load_format_skill` rejected `renderer: native` but succeeded with `{format_name: diagramming, notation: free_form}`; its guidance supports native mind-map shapes/connectors. The saved layout follows that schema. The account switch is an integration failure, not an approval rejection.


## 30. Miro roadmap completed, 2 November 2026

On Can's request to retry Miro, the connector worked again. Identity lookup succeeded and a search for the earlier roadmap in the current connection returned no results. Created and populated the new board at https://miro.com/app/board/uXjVETf6PPw=/ through the current authenticated connection. The prior board remains an empty artifact from before the account switch; it was not deleted or modified.

Uploaded the saved Canvas Composer layout: 89 items, including three frames, 42 labeled nodes, and 32 attached connectors. Adjusted heading widths and subtitle spacing after inspecting rendered dimensions. Final read-back confirmed all 89 items with no skipped items; an XML geometry check found no content-box overlaps or frame overflow. Saved the final read-back with live widget IDs to `idea1-Authorization/THESIS_ROADMAP_MIRO_LIVE_2026-11-02.svg` and updated section 15 of the Markdown roadmap with the completed board link. No sharing invitations or messages were sent.

The connection block described in section 29 is resolved. Use the new board URL and live snapshot for future edits; do not recreate the board or use the initial empty board.
