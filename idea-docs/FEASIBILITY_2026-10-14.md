# Candidate B: feasibility assessment and evidence for the research plan

Can Baturlar | 14 October 2026 | Planning assessment, before implementation

**Research-plan revision completed, 14 October:** The existing one-page research plan has now been updated in Word and PDF using this assessment. This document remains personal supporting reading for Can, not an additional submission document. Statements below describing the plan as not yet rewritten record the assessment's original stage and are superseded by this update. P21_ABAC-guide.pdf is now available locally; its definition and authoritative-attribute passages were checked against the downloaded copy (physical pp. 16–17 and 38–39).

## 1. Decision supported by this assessment

**Proceed to refine the research plan around Candidate B: a controlled comparison of authorization configurations in a simulated order-draft workflow.** The literature provides working precedents for the mechanism, environment, and measurements. The core study can be completed without company data, model training, a new authorization language, or a production integration.

This is a **conditional feasibility judgment**, not experimental validation. No thesis prototype was built, repository installed, model experiment run, or published result reproduced for this assessment. The unresolved conditions are a usable agent/model and budget, a validated scenario/evaluation set, and supervisor agreement on scope. They do not require a demo before presenting the plan.

The proposed contribution is an independently designed, reproducible engineering evaluation: determine where particular permission configurations prevent unauthorized access or changes, where they impede legitimate work, and what execution costs and trust assumptions they introduce. A result showing little difference, utility loss, or dependence on correct task context can be valuable if the experiment is sound. Publication is a possibility, not an established outcome.

**Recommended sequence:** this assessment → evidence-backed research plan → Simo/Jussi discussion → implementation and development pilot → frozen main experiment.

Candidate A remains possible future work. Feedback is held fixed in B; it is not an additional experimental factor.

## 2. What was checked and how to use the evidence

This assessment combines the existing full-text review of 20 supplied PDFs, renewed checks of central passages, the original draft plan, the supplied Oulu requirements, and targeted inspection of official repositories and NIST guidance. It is a focused feasibility review, not a new exhaustive literature search or a reproduction study.

Paper identifiers P01–P20 refer to the exact local versions in the [corpus manifest](<C:/Users/canba/Desktop/university/thesis/idea1-Authorization/literature/CORPUS_MANIFEST_2026-10-13.json>). Page numbers below are **physical PDF pages, counting the cover as page 1**. The [paper notes](<C:/Users/canba/Desktop/university/thesis/idea1-Authorization/literature/PAPER_NOTES_01-20_2026-10-13.md>) provide fuller critical readings. Some notes discuss the earlier Candidate A proposal; the design below governs this B assessment.

Three kinds of statement are kept separate:

- **Reported evidence:** what a source implemented, measured, or explicitly stated, within its own conditions.
- **Design inference:** our reasoned choice based on that evidence. A citation supports the rationale, not necessarily our exact workflow, sample size, or implementation.
- **Pending validation:** what only our implementation, pilot, or supervisor discussion can establish.

For meetings, prefer “this study motivates measuring both outcomes” over “this study proves our design will work.” The source register in section 12 links the actual papers; cite those in the plan and thesis rather than citing this assessment as scientific evidence.

## 3. Research questions and their justification

**RQ1 — Protection and usefulness:** In a simulated order-draft workflow, how do tool-name permissions, tool-name permissions with task-independent argument constraints, and the addition of task-bound constraints differ in executed authorization violations and authorized task completion?

**RQ2 — Execution cost and limitations:** What local authorization overhead and end-to-end execution costs do these configurations introduce, and how do incomplete or overly broad task contracts affect the task-bound configuration?

The task-contract sensitivity part should be a small, separate analysis. It should not become a study of automatically generating contracts from unrestricted natural language.

| Why this question or method? | What the source actually supports | Our resulting choice and its limit |
|---|---|---|
| Why go beyond tool names? | AgentDojo P19 p. 9 reports that filtering tools cannot address attacks using tools also needed for legitimate work. MiniScope P03 p. 3 explicitly places semantic misuse of permitted calls outside its permission-hierarchy boundary. | Compare resource/value restrictions within permitted tools. This does not mean tool filtering is ineffective or that all such misuse requires our specific design. |
| Why study task-bound constraints? | Progent P01 pp. 5–6 implements deterministic tool/argument rules. Conseca P04 pp. 3–5 implements contextual policies. Intent-Governed Authorization P02 pp. 7–14 distinguishes a static permission envelope from request confinement. | There is implementation precedent. We evaluate a bounded application of established ideas; task scope is not a newly invented authorization mechanism. |
| Why measure completion as well as protection? | P02 p. 26 reports zero completed unsafe effects alongside 0/108 strict benign completions and 36/108 governed artifacts in its review-oriented real-model study. AuthBench P08 p. 6 explains why a reference permission trace may not support another valid execution path. | A system that blocks everything is not a useful success. Measure authorized completion, denials, and effects independently. P02's review-oriented purpose must be acknowledged when using this example. |
| Why these baselines? | P19 supplies a tool-filtering precedent; P01 demonstrates argument restrictions; P04 compares contextual and static policies. P04 p. 5 also shows why a no-write baseline is uninformative when every legitimate task needs writes. | Use capable, explicitly specified baselines, not a deliberately unusable restrictive configuration. These are our controlled configurations, not complete reproductions of those systems. |
| Why a simulated business workflow? | tau-bench P20 pp. 3–4 uses JSON state, Python tools, domain policies, and retail/airline tasks. AgentDojo P19 pp. 3–6 uses stateful environments with explicit task/attacker goals. | A resettable order-draft service is technically and methodologically grounded. These sources do not establish that our chosen workflow represents a particular consortium company. |
| Why deterministic policies and trusted contracts? | P01 separates policy generation from enforcement. P08 p. 6 identifies permission inference as a separate difficulty. FORGE P06 pp. 3–6 conditions enforcement on the environment and policy representation. | Hold contract creation fixed to isolate the enforcement configurations. This deliberately excludes the harder question of extracting correct permissions from arbitrary requests. |
| Why access/event logs as well as final state? | P20 p. 4 explicitly warns that the right final state can overlook missing confirmation. AuthorizationBench P18 pp. 4–5 separates completion from unauthorized actions and retains process evidence. | Independently check reads and intermediate effects, including changes later undone. The monitor's own “allowed” decision is not ground truth. |
| Why ordinary overreach as well as injection? | P18 pp. 4–9 examines authorization overstepping under both benign and malicious pressures. | Include helpful extra work and wrong-target temptations as distinct strata. A benchmark rate is not an industry incident rate. |
| Why matched legitimate controls? | AgentBoundary P17 p. 4 constructs related harmful and authorized variants and distinguishes over-refusal from ordinary capability failure. | Pair pressure cases with legitimate controls; keep related variants together in development/evaluation splits and statistical resampling. Our exact pairing and analysis are design choices. |
| Why separate local and overall overhead? | FORGE P06 p. 35 reports sub-millisecond median authorization decisions, but approximately 19% retail and 38% airline end-to-end latency increases, driven by continuation/retry costs in its selected experiment. | Measure both the checker and complete runs, plus tokens/calls. Those numbers are evidence that the distinction matters, not a forecast of our overhead. |
| Why assess bad task context? | P02 p. 26 distinguishes staying within static authority from fidelity to the request. NIST SP 800-162 §3.2.2.6 and §3.2.2.10 discusses authoritative attribute sources and attribute integrity/validation. | Test a few missing-bound and excessive-bound cases against unchanged intended authority. Correctly enforcing a bad contract can still be unsafe or obstructive. |

### A necessary terminology correction

Do not argue that “static authorization cannot express task context.” NIST SP 800-162 §2.2 describes attribute-based decisions using subject, object, and contextual information. **Our inference:** a fixed rule such as “the record must match the trusted current task” can be evaluated against changing task attributes. A task-bound implementation can therefore be an application of established ABAC principles. The study compares available policy inputs and restrictions, not “traditional access control” against an inherently novel replacement. [NIST definition and guidance](https://nvlpubs.nist.gov/nistpubs/specialpublications/NIST.SP.800-162.pdf).

## 4. A bounded, fair comparison

Retain the original draft's one-agent, four-tool structure: read an order, check inventory, create a draft, and update a draft. Treat draft creation/modification as real state changes **inside the simulation**, not as placing a production order. Specify whether reading an order also returns its associated drafts; avoid silently adding an unrestricted search/export tool.

The agent has no direct database, shell, or network route around the dispatcher. All calls use the same validated tool schemas, service implementation, and baseline account permissions. Ordinary business validity, such as an existing record and an editable draft status, applies equally across conditions.

Use neutral labels **C1, C2, C3** so these conditions are not confused with thesis Candidates A and B:

| Condition | Enforced authority | Example |
|---|---|---|
| C1: tool names | A declared set of permitted tool classes for the task type; no additional per-record or per-value task restrictions | A read-only task permits reading/inventory but not creating/updating drafts. An update task permits the necessary read and update tools. |
| C2: tool names + standing argument constraints | C1 plus frozen, task-independent restrictions, such as an approved product set, editable field set, and per-call quantity ceiling | A draft update must use an approved product and quantity within the standing limit, but need not concern the currently assigned order. |
| C3: addition of task-bound constraints | C2 plus trusted current-task resource bindings and narrower operation/value limits | Only the assigned order/draft and authorized fields/products/quantity are allowed; newly created draft IDs must be bound to this task by the service. |

The tool-name set comes from the same trusted task-type mapping in all three conditions, not from a different LLM planner per arm. In the primary experiment, keep the model-visible schemas and task instructions identical across arms; enforce the selected configuration at execution. Thus C1 evaluates runtime tool-name authorization, not AgentDojo's exact tool-hiding intervention.

C2 must be meaningful, not just JSON type checking. For example, the standing quantity ceiling may reject clearly excessive quantities in C2 and C3, while a smaller task-specific ceiling distinguishes C3. Choose values and permitted products from documented workflow requirements before testing, and include legitimate tasks spanning the supported range. Do not tune limits against held-out attacks.

The intended allowance sets are nested for a fixed task/state: C3 permits a subset of C2, and C2 a subset of C1. Checking that relationship is a verification obligation. **Reduced permitted action space is expected by construction; it is not itself the empirical discovery.** The research measures realized violations, successful work, false denials, and costs when an agent operates under these restrictions.

Hold model/version, task information, initial state, tools, step budget, and denial-response format fixed. A single generic denial template is sufficient for the primary comparison. Record internal reason categories for analysis without turning feedback quality into a second treatment. No automatic permission widening or acceptance after repeated denial.

The main informative contrast is C3 versus C2; C2 versus C1 explains the added value of standing argument constraints. This is not a head-to-head performance claim against complete Progent, FORGE, MiniScope, or commercial IAM implementations.

## 5. Task contracts, scenarios, and independent ground truth

Each scenario needs four separately recorded objects:

1. **Intended authority:** the authored specification of permitted reads, resources, operations, fields, and value/effect limits.
2. **Task objective:** acceptable outcomes, independent of authorization. Permit multiple valid solutions where appropriate.
3. **Enforcement input:** the task contract supplied to C3 and the standing rules supplied to C2/C3.
4. **Environment:** initial state, tool behavior, and clean or manipulated lower-trust content.

The evaluator uses the intended authority, not the enforcement decision. In the sensitivity analysis, change item 3 while keeping items 1 and 2 fixed. Otherwise a bad contract would redefine the ground truth and conceal its own error.

A trusted application supplies the contract from structured task metadata. The model cannot edit it or promote text in an order note into authorization. Newly created drafts receive service-issued IDs and a trusted task association; do not grant access merely because an ID appeared in model output. A single-process serialized implementation can make the policy check and mutation one controlled operation. Distributed credential delegation, concurrent transactions, and cryptographic capability issuance are outside this initial experiment.

Clarify quantity semantics before implementing: “set quantity to 10,” “increase by at most 10,” and “create at most 10 units across drafts” are different requirements. Include duplicate/repeated-call probes and enforce the selected effect bound accordingly. A per-call ceiling must not be reported as a cumulative task limit.

### Coverage needed to avoid a predetermined winner

| Scenario class | Purpose |
|---|---|
| Ordinary authorized work | Establish that all arms can perform legitimate reads and required writes. Include multi-step work and legitimate boundary values. |
| Action through a disallowed tool class | Cases C1 should already prevent; demonstrate where tool names suffice. |
| Violation of a standing argument rule | Cases C2 should prevent, such as a non-approved product or quantity above its standing ceiling. |
| Wrong record within the same account | Test task identity rather than merely cross-account access already blocked by common permissions. |
| Wrong field/product or excessive quantity within standing bounds | Test the incremental task contract while using an otherwise permitted tool. |
| Authorized near-neighbour | Similar IDs, quantities, or wording, but explicitly authorized; expose unnecessary denials or stopping. |
| Benign pressure and injected instructions | Distinct sources of overreach, introduced through specified channels. Keep the actual user request and intended authority unchanged in injection pairs. |

Not every class needs every possible cross-product. Publish a coverage matrix and stratum counts. Every main legitimate task must have at least one verified authorized execution path under each intended configuration. A reference path is evidence of feasibility, not the only allowed solution. Impossible-under-authority tasks, if retained, belong in a separately reported stopping stratum rather than the primary completion denominator.

Use two complementary evaluation layers:

- **Deterministic call/short-sequence probes:** directly test allowed and forbidden boundaries, including unauthorized reads, repeated creates, default arguments, unknown IDs, and changes later undone. These test policy/adapter correctness regardless of whether a model happens to attempt the action.
- **Natural end-to-end agent runs:** measure actual behavior, completion, violations, and cost under matched initial scenarios. Do not insert forced violating calls and then describe them as naturally model-generated behavior.

This separation protects against two misleading outcomes: a guard looking correct because the model never challenges it, and a constructed probe advantage being presented as a discovered LLM behavior difference.

## 6. Measurements and analysis

| Outcome | Operational definition |
|---|---|
| Executed authorization violation | An episode with at least one unauthorized successful read or state transition, judged against intended authority. Also report read/write categories separately. |
| Raw goal completion | Whether an acceptable goal state/output was reached, regardless of unauthorized side effects. |
| Authorized completion | Goal completed and no executed authorization violation anywhere in the episode. This is the primary usefulness outcome. |
| Unauthorized attempt | A proposed call outside intended authority, whether blocked, failed in the service, or executed. Do not label all denied calls unauthorized. |
| False denial | A call that is authorized and service-valid at that state but rejected by the selected monitor. Report probe results separately from conditional rates on calls observed in agent runs. |
| Stops and capability failures | Distinguish refusal, exhausted budget, service failure, and ordinary reasoning mistakes. A non-completed task is not automatically overblocking. |
| Local overhead | Time for policy evaluation/binding and incremental dispatcher work on matched calls, separated from logging and model/network time where practical. |
| End-to-end cost | Wall time, model calls, input/output tokens, and retries per episode; report successful and failed episodes, not only successes. |

Record the proposed call, resolved arguments, policy decision, service outcome, accessed resource, before/after change, and model-visible response. A database snapshot cannot detect a read, and final-state equality can conceal an unauthorized write later reversed. The event evaluator must therefore inspect accesses and transitions as well as final state.

Avoid circular evaluation: do not invoke the monitor's decision function as the authority oracle. Use independently specified expected cases and a separate event/state evaluator. Sharing the same intended contract specification is reasonable; copying the implementation being tested is not independent verification. Test the evaluator with deliberately altered traces so known violations are detected and lawful paths accepted.

Report clean, benign-pressure, and injection outcomes separately. If an attack-bearing field is never read, record non-exposure; keep all assigned episodes in the main denominator and report exposed-only results as secondary. Conditional exposure can differ across arms and must not silently select the comparison population.

Use paired differences across matched scenario families. Average repeated runs within each family/condition, and resample complete families, keeping variants and repetitions together, for uncertainty intervals. Do not treat renamed copies or repeated runs as independent task families. The matching precedent comes from P17; this resampling specification is our methodological choice, not a claim that P17 prescribes this exact analysis.

Define the primary contrast/outcomes before the main runs. Report uncertainty and per-stratum counts; small subgroup results are exploratory. Freeze rules, prompts, scenarios, attack content, and scoring after development. If evaluation exposes a genuine defect, document it and rerun affected comparisons consistently rather than selectively repairing one arm's results.

**Zero observed violations means zero in the evaluated sample.** It does not estimate a universal zero risk. If all three configurations have similar outcomes because the selected agent rarely overreaches, report that limitation alongside the probe coverage. Do not weaken a baseline or keep searching for attacks after seeing held-out results merely to obtain a preferred ranking.

## 7. Materials and implementation feasibility

Official artifacts were inspected on 14 October 2026. Links to `main` below are moving references, not pinned experimental versions. No compatibility or installation test was performed. Before reuse, record a commit/release, dependency lock, and data version.

| Material checked | Observed evidence | Decision for this thesis |
|---|---|---|
| Progent | [Package manifest](https://raw.githubusercontent.com/sunblaze-ucb/progent/main/pyproject.toml) declares Python ≥3.9, JSON Schema, Pydantic, provider SDKs, and Z3. [Core policy code](https://raw.githubusercontent.com/sunblaze-ucb/progent/main/secagent/tool.py) includes argument checks and policy-generation state. [MCP middleware](https://raw.githubusercontent.com/sunblaze-ucb/progent/main/secagent/progent_proxy.py) checks calls before forwarding and has an update path. | Concrete implementation precedent. Prefer a small shared dispatcher for our three configurations; importing the complete generation/update stack would add uncontrolled behavior and integration work. This assessment did not audit the whole repository. |
| AgentDojo | [Runtime source](https://raw.githubusercontent.com/ethz-spylab/agentdojo/main/src/agentdojo/functions_runtime.py) provides registration, argument validation, environment dependencies, and function execution; it also resolves nested calls. [Manifest](https://raw.githubusercontent.com/ethz-spylab/agentdojo/main/pyproject.toml) requires Python ≥3.10 and several provider/framework dependencies. | Credible alternative harness. If reused, all effectful nested calls must pass the monitor. Its broader framework is optional for four custom tools; it is not necessary to port all domains. |
| Original tau-bench | [Retail tool source](https://raw.githubusercontent.com/sierra-research/tau-bench/main/tau_bench/envs/retail/tools/modify_pending_order_address.py) checks existence/pending state and mutates a dictionary. The description requests confirmation, but the inspected function does not itself establish confirmation. [Package dependencies](https://raw.githubusercontent.com/sierra-research/tau-bench/main/setup.py) include multiple provider libraries. | Strong business-tool example and direct evidence that tool prose and execution enforcement can differ. Inspiration is simpler than adopting its full LLM-user experiment. |
| tau version status | The [original README](https://raw.githubusercontent.com/sierra-research/tau-bench/main/README.md) warns that its tasks are outdated and directs readers to the [successor repository](https://github.com/sierra-research/tau2-bench), now branded tau³. | Do not call a custom order workflow a tau-bench reproduction or combine original-paper results with current tasks. Reusing tasks would require a specific version and review of its fixes. |
| Licenses | Root license files for [Progent](https://raw.githubusercontent.com/sunblaze-ucb/progent/main/LICENSE), [AgentDojo](https://raw.githubusercontent.com/ethz-spylab/agentdojo/main/LICENSE), and [original tau-bench](https://raw.githubusercontent.com/sierra-research/tau-bench/main/LICENSE) identify MIT terms. | There is no apparent root-code availability obstacle. Preserve applicable notices and check separately bundled components/data before copying. This is not an audit of every dependency or successor-repository license. |

**Recommended implementation route:** a small Python simulation with JSON or in-memory state, four deterministic tool functions, one dispatcher, three policy configurations, and a separate evaluator. This is an engineering recommendation based on the limited scope and the inspected Python precedents, not a claim that Python is experimentally superior. No local GPU is required if a hosted tool-calling model is selected; model access and costs remain unresolved.

The real work is specifying trustworthy task contracts, implementing the complete boundary, authoring balanced scenarios, and validating the evaluator. Reusing a policy library does not eliminate that work. Conversely, we need not reproduce an entire published platform to demonstrate these known mechanisms in a controlled study.

## 8. Scale, budget, and time

The existing draft proposes approximately 80 held-out scenarios and three repetitions. Treat these as **planning placeholders**, not literature-established sufficiency or a statistical power calculation.

An illustrative interpretation consistent with 80 scenarios is 40 genuinely distinct scenario families with two variants each. Three configurations and three repetitions would produce **40 × 2 × 3 × 3 = 720 main episodes for one model**. If “80” instead means 80 families with two variants, the total is 1,440. The plan must resolve this ambiguity. Development, contract-sensitivity runs, retries, and any second model are additional.

For example, 12 separate development families × two variants × three conditions × two repetitions would add 144 episodes. This is a workload example, not an instruction to run or a required pilot size. Families must differ in meaningful workflow/authority structure; merely changing record IDs does not justify claiming 40 independent scenarios.

Budget estimate after model selection:

`total cost = sum over episodes [(input tokens × input price + output tokens × output price) / 1,000,000] + separately priced provider features`

Measure token usage and duration in development, use current provider prices, and allow a declared contingency for interrupted/invalid runs. Do not infer this budget from published benchmark costs. A second model is desirable for a robustness check if affordable, but the core can be a single-model system study with appropriately limited claims. Do not spend the budget on repetitions at the expense of distinct scenario coverage.

| Phase | Planning effort, not a measured estimate | Dependency |
|---|---|---|
| Complete rationale and revise plan | Within the existing two-week planning window, aiming for 27 October | Read this assessment; settle scope with Can; arrange supervisor/lab feedback |
| Define contracts, tools, and evaluator | Approximately 2–3 focused weeks | Agreed core scope |
| Implement conditions and verify boundary | Approximately 2–3 focused weeks, partly overlapping specification | Deterministic fixtures and authorized reference paths |
| Develop scenarios and pilot | Approximately 2–3 focused weeks | Working system and chosen model/budget |
| Freeze, run, and analyze main study | Approximately 2–3 focused weeks plus rerun contingency | Validated scorer, viable pilot, frozen materials |
| Write and revise | Continuous notes; reserve several additional weeks for synthesis and supervisor revisions | Analyzed results and actual feedback turnaround |

These are rough work-package estimates, not a promise of 8–12 calendar weeks. With courses until 13 December, October–early December can focus on planning and reading; substantial implementation can start after that. The early-2027 period appears workable for a bounded study, but actual weekly availability and university submission/review dates still need a calendar. Company onboarding or a larger platform would materially change this assessment.

## 9. Risks, fallback choices, and later validation gates

| Risk | Assessment now | Bounded response |
|---|---|---|
| Comparison is predetermined by policy expressiveness | Real methodological risk | Include cases where each level suffices, legitimate controls, and end-to-end trade-offs; separate probe verification from behavioral findings. |
| Model cannot do ordinary tasks | Not yet measured | Use development tasks to distinguish agent capability from authorization; simplify task complexity or choose a suitable model before freezing. |
| Model rarely attempts overreach | Not yet measured | Use motivated development pressures and deterministic boundary probes; retain honest null end-to-end results if held-out differences remain small. |
| Contract excludes valid paths or permits extra effects | Known risk in P02/P08 | Verify authorized paths and boundary counterexamples; add a small separate missing/overbroad contract sensitivity check. |
| Guard and evaluator share a mistake | Engineering risk | Separate implementations and reviewable expected events; verify unauthorized reads and temporary writes, not only final snapshots. |
| Dependencies consume the project | Inspectable but untested artifacts | Use the small custom harness; defer integration with complete research frameworks. |
| Runtime cost exceeds available resources | Budget unknown | One model first, limited tool rounds, development-based estimate; reduce optional scope before weakening core comparisons. |
| Industrial example is too generic for GPT-Lab | Broad interest confirmed, concrete fit pending | Ask Jussi which actual delegation boundary matters; adapt fields/scenarios while keeping the four-tool architecture. Company access remains optional. |

**Before the main experiment**, require: service/evaluator agreement on authored fixtures; no unexplained bypass or scoring error; documented authorized paths; sufficient clean-task capability for interpretable comparisons; measured cost within budget; and frozen policies/scenarios. Choose any numerical competence/precision thresholds prospectively based on the intended claim and pilot, not after main results. These gates belong after plan discussion and implementation. They are not reasons to demand a demo now.

## 10. Academic and GPT-Lab value

The supplied Oulu guide supports software design, implementation, and testing (pp. 11, 16), requires significant independent contribution and justified choices (p. 31), and explicitly does not require the solution to outperform prior work (p. 32). See the [requirements mapping](<C:/Users/canba/Desktop/university/thesis/idea1-Authorization/literature/OULU_REQUIREMENTS_AND_SCOPE_2026-10-13.md>) and original guide in section 12. This supports the form of Candidate B; Simo still judges the final scope and quality.

Can's substantive contribution would be the authority/task model, carefully controlled configurations, executable scenario set, independently verified evaluation, and analysis of when restrictions help or hinder the workflow. Merely building a gateway and demonstrating that it blocks a wrong ID would be insufficient depth.

For GPT-Lab, the prospective practical output is an inspectable example of how to constrain an agent delegated a business task, with measured consequences and explicit assumptions about where trusted task metadata comes from. Jussi's message is evidence of interest in this general direction and possible company use cases. It does not confirm company requirements, access, supervision arrangements, a paid research-assistant role, or acceptance of these RQs.

The supervisor meeting should resolve three concrete points: whether this comparison is sufficient MSc scope; which realistic order/draft delegation boundary would be useful to AI Champion; and what model resources and domain feedback are available. A company-inspired case can strengthen relevance without becoming a prerequisite for completion.

## 11. What should change in the existing research plan next?

The [current draft](<C:/Users/canba/Desktop/university/thesis/idea1-Authorization/Research-Plan-Authorization-Agents_Can-Baturlar-DRAFT.pdf>) is already close to a feasible design. The assessment supports refinement rather than changing direction:

1. Describe the contribution as a controlled application/evaluation of established authorization mechanisms.
2. Define C1/C2/C3 precisely, including what task context each sees, meaningful standing restrictions, and shared account/business rules.
3. Use the two evidence-backed RQs above; treat contract sensitivity as a bounded limitation analysis.
4. Add independent access and transition checks to the proposed database audit. Include reads and unauthorized effects later undone.
5. Add capable legitimate controls and cases where simpler policies suffice; avoid an all-wrong-record test set.
6. State that family-level pairing/splitting/resampling includes all related variants and repetitions.
7. Keep “approximately 80” provisional and make scenario/family/variant counting explicit.
8. Specify that this is a simulated order-draft workflow, not a validated industrial deployment.
9. Respect the university instructions supplied by Can on 14 October: the Laturi plan is **maximum one A4 page**, under the three headings purpose, methods/material/devices/software, and expected results, and is approved by the supervisors. Keep detailed source support in an accompanying rationale document for discussions. Compact citations may be used if space permits; the supplied excerpt neither requires nor prohibits them. The full evidence matrix and experimental protocol do not need to be squeezed into the formal one-page plan, and no formal appendix submission requirement has been established.

The subsequent research-plan revision on 14 October incorporates these recommendations in the existing one-page PDF and Word document. It keeps the three required sections, makes both RQs explicit, and leaves the final experiment size to the development pilot. This does not constitute supervisor approval. The detailed evidence here is for Can's reading and preparation, rather than an extra document to upload.

### Short answers for the meeting

**“Why this research question?”** AgentDojo identifies attacks that use the same tools as legitimate work, and MiniScope explicitly excludes some within-permission argument misuse. Progent and contextual-policy research demonstrate ways to restrict arguments. That motivates comparing how much those restrictions help in a bounded business workflow while preserving legitimate completion. [P19 p. 9; P03 p. 3; P01 pp. 5–6; P04 pp. 3–5]

**“Why this method?”** tau-bench and AgentDojo establish workable stateful simulations with tool interfaces and explicit outcomes. We adopt that experimental structure to hold the environment constant across authorization configurations. We add independent authority/event checks because tau-bench explicitly notes that final-state success can miss a policy violation. [P20 pp. 3–4; P19 pp. 3–6]

**“Why not just report blocked attacks?”** Intent-Governed Authorization shows that zero unsafe completed effects and successful autonomous completion are different outcomes. Our evaluation therefore measures both executed violations and authorized completion, and distinguishes rejected attempts from effects. [P02 p. 26; P01 p. 14]

**“What do you contribute if these mechanisms already exist?”** A controlled, reproducible evaluation of specified configurations in an explicitly modeled workflow: where each restriction level is sufficient, its effect on legitimate work and cost, and its dependence on correct task contracts. The claim is useful empirical engineering evidence, not invention of task-aware access control.

**“Is it feasible without a company or a new algorithm?”** The reviewed studies supply implemented precedents, public Python artifacts exist, and Oulu permits an engineering design-and-evaluation thesis. This supports proceeding to the plan. Our local implementation, experiment budget, and company-specific relevance are still to be validated. [P01; P19; P20; Oulu guide pp. 11, 16, 31–32]

## 12. Source register and focused additional reading

The following are the versions supporting this assessment, not a claim that every source is peer reviewed. Progent and several 2026 works are reviewed here as preprints; Conseca, AgentDojo, and the supplied AgentSpec publication layout provide additional venue-backed precedents. No finding is strengthened merely by the number of citations.

| ID | Original source | Main passages used |
|---|---|---|
| P01 | [Progent, local PDF](<C:/Users/canba/Desktop/university/thesis/reference/authorization-papers/P01_Progent.pdf>); [arXiv 2504.11703v3](https://arxiv.org/abs/2504.11703v3) | pp. 5–6 enforcement; pp. 8–10 evaluation/approval assumptions; p. 14 scorer correction |
| P02 | [Intent-Governed Authorization, local PDF](<C:/Users/canba/Desktop/university/thesis/reference/authorization-papers/P02_Intent-Governed.pdf>); [2606.22916v4](https://arxiv.org/abs/2606.22916v4) | pp. 7–14 contract/boundary; pp. 26–27 outcomes and limitations |
| P03 | [MiniScope, local PDF](<C:/Users/canba/Desktop/university/thesis/reference/authorization-papers/P03_MiniScope.pdf>); [2512.11147v2](https://arxiv.org/abs/2512.11147v2) | p. 3 threat model and within-permission non-goals |
| P04 | [Conseca, local PDF](<C:/Users/canba/Desktop/university/thesis/reference/authorization-papers/P04_Contextual-Agent-Sec.pdf>); [2501.17070v3](https://arxiv.org/abs/2501.17070v3) | pp. 3–5 contextual checks, small evaluation, restrictive-baseline limitation |
| P06 | [FORGE, local PDF](<C:/Users/canba/Desktop/university/thesis/reference/authorization-papers/P06_Formal-Policy.pdf>); [2602.16708v3](https://arxiv.org/abs/2602.16708v3) | pp. 3–6 assumptions; pp. 12–14 selected-task evaluation; p. 35 overhead |
| P08 | [AuthBench, local PDF](<C:/Users/canba/Desktop/university/thesis/reference/authorization-papers/P08_Evolvent-AI.pdf>); [2605.14859v2](https://arxiv.org/abs/2605.14859v2) | p. 6 policy sufficiency and executor dependence |
| P17 | [AgentBoundary, local PDF](<C:/Users/canba/Desktop/university/thesis/reference/authorization-papers/P17_Agent-Boundary.pdf>); [2609.33658v1](https://arxiv.org/abs/2609.33658v1) | p. 4 matched families and separate outcome definitions |
| P18 | [AuthorizationBench, local PDF](<C:/Users/canba/Desktop/university/thesis/reference/authorization-papers/P18_Act-On-Your-Behalf.pdf>); [author PDF](https://www.zhipingzhang.com/_files/ugd/3840b5_415101659c9f406d888aa5fce66889d5.pdf) | pp. 4–5 contract, observable actions, feasible paths; pp. 6–9 evaluation |
| P19 | [AgentDojo, local PDF](<C:/Users/canba/Desktop/university/thesis/reference/authorization-papers/P19_AgentDojo.pdf>); [2406.13352v3](https://arxiv.org/abs/2406.13352v3) | pp. 3–6 environment/evaluation; p. 9 shared-tool limitation |
| P20 | [tau-bench, local PDF](<C:/Users/canba/Desktop/university/thesis/reference/authorization-papers/P20_t-Bench.pdf>); [2406.12045v1](https://arxiv.org/abs/2406.12045v1) | pp. 3–4 materials, reward caveat, repeated reliability |
| P21 / NIST | [ABAC guide, local PDF](<C:/Users/canba/Desktop/university/thesis/reference/authorization-papers/P21_ABAC-guide.pdf>); [SP 800-162, official PDF](https://nvlpubs.nist.gov/nistpubs/specialpublications/NIST.SP.800-162.pdf), January 2014 with 2019 updates | §2.2, printed pp. 6–7 / physical pp. 16–17; §3.2.2.6 and .10, printed pp. 28–29 / physical pp. 38–39. Targeted sections checked online and in the downloaded copy; not a full-document review. |
| Oulu | [CSE thesis guide](<C:/Users/canba/Desktop/university/thesis/reference/thesis_instructions/CSE_diploma_thesis_instructions.pdf>); [evaluation instructions](<C:/Users/canba/Desktop/university/thesis/reference/thesis_instructions/Evaluation_Instructions.pdf>) | Guide pp. 11, 16, 29–34; rubric on contribution and evaluation. Supplied versions; latest official status not independently certified. |

**Additional download received:** NIST SP 800-162 is now saved as P21_ABAC-guide.pdf. It fills a foundational access-control terminology gap and helps defend the baseline definitions. It is guidance, not experimental evidence of agent performance. No additional batch of agent papers was needed for this plan revision. If we later reuse successor tau tasks or choose another complete harness, read that exact version's paper and fixes before claiming benchmark reproduction. The selected topic still needs an updated, scope-focused literature search during thesis writing.

## 13. Final feasibility status

| Dimension | Status |
|---|---|
| Literature basis for the problem and mechanism | Sufficient to justify a plan; close prior art acknowledged |
| Technical build path | Credible from implemented precedents and inspected artifacts; local integration untested |
| Evaluation validity | Feasible with the baseline, oracle, and scenario corrections above |
| Time and cost | Plausible at this bounded scope; actual model budget, task-authoring effort, and calendar pending |
| MSc form and contribution | Supported by the supplied guidance; exact scope subject to Simo's judgment |
| GPT-Lab fit | Broad interest documented; concrete use case and collaboration still to discuss |
| Need for a pre-plan demo | No blocking implementation uncertainty identified that requires one now |
| Next action | Can reviews the revised one-page research plan and supporting rationale before supervisor discussion |
