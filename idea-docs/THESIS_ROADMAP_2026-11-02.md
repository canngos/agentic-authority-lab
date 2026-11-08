# Thesis roadmap: from the research plan to a completed MSc thesis

**Can Baturlar · 2 November 2026 · Working roadmap, version 1**

**Thesis:** Task-Scoped Runtime Authorization for Industrial AI Agents  
**Direction:** Candidate B, a controlled engineering evaluation of authorization configurations.  
**Starting point:** [Current one-page research plan](<C:/Users/canba/Desktop/university/thesis/idea1-Authorization/Research-Plan_Can-Baturlar.pdf>).

This is your personal execution plan, not a replacement for the one-page research plan. Dates are provisional. Work can continue while Jussi responds; company involvement is an opportunity, not a prerequisite. The proposed calendar assumes limited availability until 13 December 2026 and full focus from 14 December. It leaves April and May for review and completion, subject to your actual graduation target, supervisor availability, and university deadlines.

## 1. The route in one minute

1. Learn what an Oulu MSc thesis looks like and understand the central papers yourself.
2. Turn the research plan into an exact, testable study specification.
3. Build the simulated service, authorization configurations, and independent evaluator.
4. Develop balanced scenarios and run a small pilot to establish capability, cost, and scale.
5. Freeze the experiment, run the comparisons, and preserve all evidence.
6. Analyze the findings, answer the research questions, and revise the thesis with your supervisors.

**Write throughout this process.** Background can be drafted during reading; methods during specification; implementation during development. Results must wait for measured evidence. You do not need to finish reading every paper before writing or coding.

| Phase | Provisional window | Main output | Ready to move on when… |
|---|---|---|---|
| 1. Orient and read | 2–15 November | Thesis outline, core reading notes, glossary | You can explain the problem and comparison without relying on this document |
| 2. Specify the study | 16 November–13 December | Study protocol v0.1 and example scenarios | Authority, conditions, outcomes, and scope are explicit |
| 3. Build the core | 14 December–10 January | Resettable service and complete vertical slice | A legitimate task and a blocked violation produce independently checked traces |
| 4. Complete the test environment | 11–31 January | Three configurations, evaluator, scenario inventory | Direct checks pass and baseline tasks are feasible |
| 5. Pilot and freeze | 1–21 February | Costed, versioned main-experiment protocol | Models, scenario coverage, scoring, budget, and analysis are ready |
| 6. Run the study | 22 February–14 March | Main results and separate sensitivity results | Planned runs are accounted for and data checks pass |
| 7. Analyze and finish a full draft | 15 March–4 April | Reproducible analysis and complete thesis draft | Every RQ has an evidence-based answer with limitations |
| 8. Review and submit | April–May | Revised thesis and reproducibility package | Supervisor revisions and current submission requirements are satisfied |

These are planning windows, not commitments or claims that a phase takes exactly this long. December includes holiday buffer. If progress slips, reduce optional additions before compromising the main comparison or review time.

## 2. What we are committing to

The central question remains whether task-bound permissions add protection while preserving legitimate work in a simulated order-management workflow.

- **RQ1:** How do tool-name permissions, standing argument restrictions, and additional task-bound constraints differ in executed authorization violations and authorized task completion?
- **RQ2:** What execution costs do these configurations introduce, and how do incomplete or overly broad task permissions affect task-bound enforcement?

Use three neutral condition labels throughout the code, figures, and thesis:

| Condition | What it checks | Example distinction |
|---|---|---|
| C1 | Permitted tool names for the task type | A lookup task cannot invoke a draft-update tool |
| C2 | C1 plus standing argument restrictions | Only approved products and quantities within standing limits |
| C3 | C2 plus trusted current-task restrictions | Only the assigned record, permitted fields, and task-specific effects |

The core includes one synthetic workflow, one agent per run, a small selection of tool-using LLMs, direct authorization checks, repeated agent runs, and a bounded permission-sensitivity analysis. The exact tool count, model names, scenario count, and repetition count remain open until the design and pilot justify them.

**Keep outside the core:** automatic permission generation by an LLM; a learned or non-deterministic gateway; production integration; multiple business domains; multi-agent delegation; a new authorization language; and Candidate A's denial-feedback/recovery comparison. Do not add scenarios with no possible authorized solution at this stage. These can be reconsidered later through an explicit scope decision, before the affected experiment is frozen.

The contribution is your independently justified design, implementation, evaluation, and interpretation. Smaller allowed action sets are predictable by construction. The empirical contribution concerns what agents actually attempt and execute, whether useful work still succeeds, the execution cost, and dependence on the correctness of supplied permissions. A carefully explained null result is still informative.

## 3. Phase 1: understand the thesis form and the foundations

### Start with the university guidance and two thesis examples

Read the [CSE thesis guide](<C:/Users/canba/Desktop/university/thesis/reference/thesis_instructions/CSE_diploma_thesis_instructions.pdf>) selectively: physical PDF pages 9–13 for responsibility and planning, 20–21 for AI assistance and writing, and 29–34 for chapter content, methods, discussion, and references. Read both pages of the [evaluation instructions](<C:/Users/canba/Desktop/university/thesis/reference/thesis_instructions/Evaluation_Instructions.pdf>). The [existing requirements note](<C:/Users/canba/Desktop/university/thesis/idea1-Authorization/literature/OULU_REQUIREMENTS_AND_SCOPE_2026-10-13.md>) is a navigation aid, not a substitute for those originals.

**First example, already downloaded:** [Fatih Sakiz, Regime-Aware Machine Learning for Dynamic Risk Management in Algorithmic Trading](<C:/Users/canba/Desktop/university/thesis/example-thesis/regime-aware-ml_Fatih-Sakiz.pdf>), Oulu CSE, June 2026. Its table of contents places introduction at printed p. 11, background and related work at p. 15, system design and methodology at p. 31, experimental setup at p. 38, results at p. 43, discussion at p. 57, and conclusions at p. 64. References and appendices follow. We checked its opening material and contents for structure; this is not a quality audit of the whole thesis or an endorsement of its statistical methods for our study.

**Second example to obtain:** [Lauri Suutari, Virtualized learning environment for network security using infrastructure as code practices](https://oulurepo.oulu.fi/handle/10024/53313), 2024. Use it to see how a software artifact, implementation choices, and evaluation can be explained. An optional AI-related example is [Talha Zeeshan, Large language model based multi-agent system augmented complex event processing pipeline](https://oulurepo.oulu.fi/handle/10024/51077), 2024. These are previously identified repository records; repository access was intermittent during this roadmap update. Neither implies that our thesis needs its domain or architecture.

Spend approximately an hour on the first skim of each thesis. Read the abstract, introduction, contents, beginning of methods, one results section, and discussion. Produce a one-page comparison answering:

- Where are the problem, RQs, contribution, and scope stated?
- How are unfamiliar concepts introduced before they are used?
- How are design decisions connected to sources or requirements?
- What is explained in prose, figures, tables, or appendices?
- How do results differ from discussion, and how are limitations acknowledged?

Borrow structural lessons, not sentences or research claims. Simo's 60–70-page suggestion is a writing target, not a reason to copy another thesis's length.

### Read the core literature in a useful order

The existing review covers 20 supplied papers plus targeted NIST reading. It is a foundation, not proof that you personally understand every paper or that coverage is exhaustive. Read originals in the sequence below. Physical PDF page pointers come from the existing feasibility review and apply to the downloaded versions.

| Order and resource | Focus | What you should be able to explain afterward |
|---|---|---|
| 1. [P21: NIST ABAC guide](<C:/Users/canba/Desktop/university/thesis/reference/authorization-papers/P21_ABAC-guide.pdf>) | Definition, pp. 16–17; trustworthy attributes, pp. 38–39 | Authorization can depend on subject, object, action, and context; task scope can use established ABAC principles |
| 2. [P01: Progent](<C:/Users/canba/Desktop/university/thesis/reference/authorization-papers/P01_Progent.pdf>) | Rules/enforcement, pp. 5–6; evaluation, pp. 8–11 | Why tool/argument checks are technically plausible and what assumptions they require |
| 3. [P03: MiniScope](<C:/Users/canba/Desktop/university/thesis/reference/authorization-papers/P03_MiniScope.pdf>) and [P04: Conseca](<C:/Users/canba/Desktop/university/thesis/reference/authorization-papers/P04_Contextual-Agent-Sec.pdf>) | Granularity and scope boundary; contextual versus standing policy comparison | Why our configurations differ, and why a baseline that prevents legitimate work is unhelpful |
| 4. [P18: AuthorizationBench](<C:/Users/canba/Desktop/university/thesis/reference/authorization-papers/P18_Act-On-Your-Behalf.pdf>) | Task construction and outcomes, pp. 3–9 | Why goal achievement and authorized behavior are different, including ordinary overreach |
| 5. [P19: AgentDojo](<C:/Users/canba/Desktop/university/thesis/reference/authorization-papers/P19_AgentDojo.pdf>) and [P20: tau-bench](<C:/Users/canba/Desktop/university/thesis/reference/authorization-papers/P20_t-Bench.pdf>) | Stateful tasks, tools, attacks, utility, and evaluation, approximately pp. 3–9 | How a resettable business simulation can support controlled evaluation; why final state alone is insufficient |
| 6. [P06: FORGE](<C:/Users/canba/Desktop/university/thesis/reference/authorization-papers/P06_Formal-Policy.pdf>) | Enforcement assumptions and cost reporting, especially pp. 34–36 | Why local checking time and total agent runtime must be measured separately |
| 7. [P17: AgentBoundary](<C:/Users/canba/Desktop/university/thesis/reference/authorization-papers/P17_Agent-Boundary.pdf>), [P08: AuthBench](<C:/Users/canba/Desktop/university/thesis/reference/authorization-papers/P08_Evolvent-AI.pdf>), [P02: Intent-Governed Authorization](<C:/Users/canba/Desktop/university/thesis/reference/authorization-papers/P02_Intent-Governed.pdf>) | Matched controls; valid alternative paths; permission-context limitations | How to avoid rewarding refusal, using one trace as the only valid answer, or treating a bad supplied policy as ground truth |

Read the final row during scenario design and pilot preparation; those papers need not all delay the first implementation.

For each core paper, keep a short note: **problem → mechanism → experimental setup → actual finding → limitation → implication for our study**, with exact page/section and version. Mark whether a statement is a source finding, your design inference, or something still requiring validation. Read enough of the methods and results to understand any claim you cite. Do not cite an AI summary as scientific evidence.

Use the [paper notes](<C:/Users/canba/Desktop/university/thesis/idea1-Authorization/literature/PAPER_NOTES_01-20_2026-10-13.md>) for navigation. Consult the [feasibility rationale](<C:/Users/canba/Desktop/university/thesis/idea1-Authorization/literature/CANDIDATE_B_FEASIBILITY_2026-10-14.md>) only for the decision you are currently making; you do not need to reread it linearly. Some older notes retain superseded tool counts, model suggestions, or Candidate A material. The current research plan and decisions in this roadmap take precedence.

**Writing now:** create the thesis outline, reference library, glossary, a rough problem statement, and a literature comparison table. Draft explanations of authorization, task scope, tool use, prompt injection, and the difference between attempting and executing an action.

**Exit check:** explain the three configurations, the two RQs, and the role of the independent evaluator in your own words, with source support for the main design choices.

## 4. Phase 2: turn the plan into an experimental specification

Prepare a separate working protocol. It should answer these questions before implementation becomes extensive:

1. **Workflow:** What is an order, draft, product, and inventory record? What operations are valid? What counts as completion?
2. **Trust boundary:** Which task information comes from the trusted application? Which order notes or tool responses can contain misleading instructions? The model cannot change its own authority.
3. **Permission semantics:** Which records, reads, fields, and effects are permitted? Does a quantity bound mean a final value, an increment, or a cumulative limit across multiple calls?
4. **Comparison:** What exactly changes between C1, C2, and C3? What stays identical? C2 must enforce meaningful standing restrictions, not only argument types.
5. **Ground truth:** How will intended authority and acceptable outcomes be recorded independently of the gateway's decisions?
6. **Evaluation:** Which scenario families, metrics, failure categories, controls, and comparisons answer each RQ?

Each scenario should contain an initial state, task objective, intended authority, supplied enforcement permissions, any lower-trust content, acceptable outcomes, and a verified authorized example path. The example path demonstrates feasibility; other valid solutions must remain acceptable.

Prepare a few worked examples: a normal draft update; a wrong-order update within the same account; a standing quantity violation; and a closely related authorized case. Explain which condition should block which call and why. Keep intended authority separate from the permissions supplied to C3 so RQ2 sensitivity can change one without redefining the other.

**Discuss with Simo/Jussi:** whether this boundary and workflow are useful; whether a company can suggest plausible constraints without creating a data dependency; supervision roles; model access/budget; and the intended scope of any publication. A targeted review by someone with access-control expertise can strengthen the design without making a new formal supervisor a prerequisite.

**Writing now:** a first methods draft, a trust-boundary diagram, the baseline table, and a source-to-decision table. Record alternatives considered and why you selected the bounded design.

**Exit check:** a third-party reader can work through the examples and understand what is authorized, what is being compared, and what would count as success. Seek methodological feedback before expensive experiments; do not make routine preparation depend on Jussi replying.

## 5. Phase 3: build one complete path through the system

Use a small Python implementation. Select exact libraries and provider interfaces when implementation starts, checking their current official documentation and licenses. Do not install several research frameworks merely because their papers are related.

Build in this order:

1. **Synthetic order service:** explicit data model, business-validity checks, deterministic state reset, and the necessary lookup/inventory/draft operations.
2. **Controlled tool dispatcher:** every agent-visible operation passes through the gateway; the agent has no direct database or alternative tool route around it.
3. **Authorization configurations:** shared service and schemas, with C1/C2/C3 enforced at execution. Handle newly created draft IDs using trusted service bindings.
4. **Event recording:** proposed call, decision, actual service execution, reads, before/after effects, timing, and final response. Record configuration and scenario identifiers.
5. **Independent evaluator:** separate student-written scoring code checks the trace and outcome against the scenario specification.
6. **Agent adapter:** connect one model initially and complete a legitimate task end to end.

Start with scripted calls before involving an LLM. Demonstrate one allowed action, one denied action, and one independently detected unauthorized execution under a coarser condition. A final-state check must not overlook an unauthorized read or a write later reversed.

“Independent evaluator” does not mean hiring another researcher or using another agent. You implement it; independence means its verdict does not simply repeat the gateway's allow/deny result. Validate it with deliberately constructed good and bad traces. Prefer a separate checking implementation over sharing the gateway's policy predicate as the scoring truth.

**Writing now:** the architecture, interfaces, trusted inputs, logging design, and an annotated example execution. Explain important design choices, not every function or installation command.

**Exit check:** reset → task → model/tool call → gateway → service → log → evaluator works, and the example outcomes are correct. No final research claim follows from this demonstration.

## 6. Phase 4: make the experiment fair and testable

Complete all conditions and scenario families. Include legitimate work, benign overreach, and injected instructions in specified tool-response content. Include cases where C1 or C2 already suffices and authorized near-neighbours of prohibited actions. Avoid building only examples selected to make C3 look useful.

Use direct call/sequence tests for permission boundaries, unknown IDs, omitted/default arguments, new-draft ownership, repeated effects, reset correctness, and reads/intermediate writes. Verify the intended nesting of permissions for fixed task/state inputs. Unknown or malformed authorization input must have a documented safe behavior. Keep policy checking and service mutation within a controlled execution path.

Separate development and held-out scenario families before tuning prompts and policies. Renaming an order ID does not create an independent family. Define families by meaningful task structure, authority boundary, and pressure mechanism; keep related variants together in the split.

Keep model settings, visible tools, task instructions, initial states, denial format, and step budget matched across conditions for each model. Do not give C3 a better prompt or privileged task explanation. Keep direct probes separate from natural model runs in both data and reporting.

**Writing now:** experimental setup, scenario taxonomy, outcome definitions, and threats to validity. Keep an inventory showing which family tests which requirement and RQ.

**Exit check:** boundary tests and evaluator checks pass; every legitimate main-study task has a verified authorized solution under the intended configurations; the family inventory has meaningful breadth; and the proposed comparison does not depend on an unusable baseline.

## 7. Phase 5: pilot, cost, and freeze

The pilot tests the experiment itself. It is not the final result set.

- Select a small set of accessible tool-using models that can perform the clean workflow. Do not assume marketing tiers establish capability. Compare each selected model under all three authorization conditions.
- Inspect complete traces. Distinguish model misunderstanding, tool failure, malformed arguments, policy denial, scoring errors, and ordinary task failure.
- Estimate episode cost, runtime, failure rate, and variation. Choose family coverage, repetitions, and sensitivity cases that fit the available budget and desired precision.
- Choose the analysis and failure-handling rules before the main results are visible. Specify the primary contrasts, denominators, uncertainty method, and handling of interrupted/provider-failed runs.
- Refresh the literature around the closest comparisons and evaluation methods. Record queries, dates, inclusion reasons, and any design implications. This is a targeted update, not an unlimited restart of the review.

Use a simple workload budget:

**Main episodes = models × 3 conditions × repetitions × total held-out scenario instances.**

Cost and time estimates must add the pilot, sensitivity subset, and a predeclared allowance for technical failures. Repetitions do not replace diversity of scenario families. Do not reuse an old illustrative scenario count or competence threshold as a requirement.

Freeze and version the prompts, policy logic, schemas, scenario set, evaluator, model settings, analysis plan, and failure/retry rules. Task-specific permission values can still differ between scenarios. If a material bug is discovered afterward, document the change and rerun the affected comparison consistently; do not quietly patch one condition.

**Writing now:** finalize the methods and experimental setup descriptions, including model/version details and exact sample structure. Record pilot-based choices as such.

**Exit check:** a pilot report explains capability, coverage, budget, remaining limitations, and why the main run is ready. Obtain supervisor input on the settled design where feasible before committing the main budget.

## 8. Phase 6: run and preserve the evidence

Run matched scenarios across configurations, with order randomized or interleaved in blocks to reduce time/provider drift. Record model identifiers, dates, versions/settings, prompt hashes or archived prompts, code revision, scenario versions, and seeds where supported. Seeds do not guarantee identical hosted-model behavior.

Retain successful, failed, denied, and exhausted episodes. Use the predefined retry policy; never rerun only inconvenient outcomes. Check missing records, resets, condition labels, timing units, and token accounting before analysis.

Run the **separate sensitivity analysis** on a bounded subset: remove a necessary permission or broaden a permission while leaving intended authority and the task objective fixed. This measures the consequences of incorrect supplied permissions. It does not evaluate an LLM that generates those permissions. Report its results separately from the correctly specified primary comparison.

**Writing now:** maintain a run log and a factual results skeleton. Record deviations immediately. Preserve raw evidence separately from derived tables.

**Exit check:** all planned episodes are accounted for, exclusions have documented reasons, configuration integrity is checked, and the analysis can be reproduced from saved logs.

## 9. Phase 7: analyze and answer the questions

| Measure | Meaning and reporting rule |
|---|---|
| Executed violation | At least one unauthorized successful read or state change in an episode; also distinguish reads and writes |
| Unauthorized attempt | A proposed action outside intended authority, regardless of whether it executed |
| Raw goal completion | The requested goal was achieved, even if unauthorized side effects occurred |
| Authorized completion | Goal achieved with no executed authorization violation during the episode |
| False denial | An authorized, service-valid proposed action was blocked by authorization; report the denominator explicitly |
| Local checking latency | Time in the authorization check, measured separately from service/model time |
| End-to-end cost | Total episode runtime, model calls, tokens, and monetary estimate where available |

False denials under correct exact policies are a diagnostic, not a trade-off that must appear. Distinguish implementation defects, intentionally narrower configuration capability, and corrupted supplied permissions. Do not classify every denied call as unauthorized.

Compare C3 with C2 as the main task-context contrast; use C2 versus C1 to explain standing argument restrictions. Analyze each model under matched conditions before making cross-model observations. Account for related variants and repetitions when calculating uncertainty. For example, a paired bootstrap at scenario-family level may be suitable if justified in the protocol; do not treat every repeated episode as an independent task. Explain the chosen method and its assumptions.

Report results by scenario class alongside aggregate results. A zero observed violation rate is not proof of zero risk. If a model never attempts the relevant violation, say so and use the separately reported direct checks to explain the enforcement boundary.

Prepare a small set of useful figures/tables: coverage and sample counts; protection versus authorized completion by condition/model; cost; sensitivity; and a few representative failure traces. Use actual findings, including surprising or negative ones. Do not select examples only because they favor C3.

**Writing now:** results report what was measured; discussion explains what it means, answers each RQ, compares with prior work, and addresses limitations. State the limits of the synthetic workflow, model sample, scenario coverage, trusted permissions, and complete mediation assumptions.

**Exit check:** each conclusion points to evidence, analysis can regenerate the figures, and the full draft contains no invented results or unsupported claims of industrial generality.

## 10. How to write the thesis alongside the work

Use the supplied [CSE template](<C:/Users/canba/Desktop/university/thesis/reference/thesis_instructions/CSE_ThesisTemplate_EN.doc>) as a starting reference and check the current official template before committing formatting. Maintain references as you read, using accurate original-source metadata and the required citation style.

An illustrative 65-page allocation is below. It is a planning aid, not a minimum, maximum, or approved chapter structure. Confirm with Simo how his 60–70-page target counts front matter, references, and appendices.

| Part | Approximate pages | Reader's question |
|---|---:|---|
| Front matter | 6 | What is this work about? |
| Introduction | 4 | Why this problem, these RQs, and this scope? |
| Background and related work | 12 | What concepts and earlier findings are needed? |
| Research methodology and experimental design | 8 | How will the comparison produce credible answers? |
| System design and implementation | 10 | What was built, how does it work, and why these choices? |
| Results | 10 | What happened in the experiments? |
| Discussion | 7 | What do the findings mean and where do they apply? |
| Conclusion | 2 | What can we now answer? |
| References | 6 | Which original sources support the work? |
| **Total** | **65** | Appendices only where useful; counting to be confirmed |

Method and implementation chapters may be reorganized once the work is clearer. Put exhaustive prompts, schemas, case inventories, and supplementary tables in appendices or an accompanying artifact where appropriate, while keeping enough detail in the main text to understand and assess the study.

### Make the explanation accessible without making it repetitive

Assume an educated computing reader who has not built agent authorization systems. For each important concept, use this sequence:

1. Plain-language meaning.
2. Concrete example from the order workflow.
3. Precise definition or mechanism used in this thesis.
4. Why it matters to the experiment.

For example, explain the evaluator as a program you wrote that checks recorded actions and outcomes against scenario rules, then explain its separation from the gateway. Define task permissions, standing restrictions, intended authority, scenario families, and legitimate completion before using them in tables. Introduce acronyms once and use terms consistently. Figures need explanatory captions; a diagram is not a substitute for describing its assumptions.

Aim for enough detail that another researcher could reconstruct the comparison. Avoid dumping source code or describing routine programming steps merely to add pages. Ask a reader unfamiliar with the topic to explain your method back to you; misunderstandings reveal missing definitions.

Keep a short weekly writing session even during development. Record decisions immediately, then turn the notes into prose you understand and own. Write the abstract and polish the introduction last, after the findings are settled.

### Ownership and AI assistance

The supplied Oulu guide requires discussing AI use with the supervisor and disclosing its actual role. Agree the permitted uses with Simo before preparing submitted thesis text, and keep an assistance log. The guide includes an introduction subsection titled **Author's Contributions and the Role of Artificial Intelligence**. These planning documents are aids, not ready-made thesis chapters. Verify source claims, inspect code and analysis, and be able to defend your decisions. Do not later describe substantial literature or implementation assistance as proofreading alone.

## 11. Phase 8: supervisor review, delivery, and optional publication

Send a complete draft early enough for meaningful revision. Agree review lead times rather than assuming immediate feedback. Work through comments in a response log: comment, change, location, and any unresolved question.

Check the supplied evaluation criteria against the finished thesis: clarity of problem, justified methods, personal contribution, evaluation quality, critical discussion, and presentation. Verify references, figures, terminology, reproducibility instructions, and the required English/Finnish titles and abstracts. Follow current degree-programme instructions for final submission and graduation tasks; no exact May deadline has been established by this roadmap. Use the [official Oulu thesis entry page](https://www.oulu.fi/en/for-students/thesis-and-graduation/graduation-masters-degree/masters-thesis) to locate the applicable current guidance, and confirm timing with the programme before the final months.

Prepare a clean artifact package: code, dependency/version information, synthetic scenarios, policies, experiment configurations, permitted logs, analysis scripts, and instructions to reproduce checks and figures. Keep credentials and confidential company material out. If company input is introduced, settle what can be published before the study depends on it.

Discuss publication with Simo and collaborators after there is a concrete contribution and sound evidence. A paper would select a tighter argument and adapt to a venue; it is not simply the thesis with a different cover. Publication is optional and must not become a dependency for completing the MSc. Candidate A can become a later study informed by the observed failure and recovery patterns.

## 12. Manage scope and keep progress visible

| Risk or uncertainty | Planned response |
|---|---|
| Jussi/company response is delayed | Continue the synthetic core; use later feedback to improve plausibility without rebuilding everything |
| Weak clean-task model performance | Diagnose tools/prompts on development data; choose capable accessible models before freezing |
| API cost or time is too high | Narrow optional combinations and sensitivity breadth first; retain useful family diversity and honest uncertainty |
| C1/C2 already work well | Report where simpler restrictions suffice; do not manufacture harder cases after viewing held-out results |
| C3 blocks legitimate work | Inspect specification, implementation, and contract quality separately; retain and explain valid findings |
| Evaluator and gateway share a mistake | Use separate specifications/checks and deliberately incorrect traces; seek focused design review |
| New ideas keep expanding the study | Put them in a future-work list; change the core only for a clear validity or feasibility reason |
| Writing falls behind | End each phase with its written section and reserve weekly writing time |

Maintain a decision log, reading notes, scenario inventory, experiment manifest, and weekly progress note. Keep local work under version control when development starts and maintain a backup. Suggested project areas are `src`, `tests`, `scenarios`, `configs`, `runs`, `analysis`, and `docs`; these are organizational suggestions, not a required framework.

A useful weekly note has five lines: completed; learned; evidence/artifact; current blocker; next concrete outcome. A useful supervisor update links a specific artifact and asks for focused feedback on the important unresolved issue.

## 13. Your first week: 2–8 November

- [ ] Skim the CSE guide and evaluation rubric; record the writing and disclosure requirements.
- [ ] Skim Fatih's thesis using the structural questions above; obtain Suutari's thesis for a second example.
- [ ] Read the selected P21 passages and P01's mechanism/evaluation; write a short note for each.
- [ ] Create your own thesis outline and a small glossary in plain language.
- [ ] Work through one normal order update and one wrong-record case on paper: task, intended authority, C1/C2/C3 decision, and evaluator verdict.

**The first milestone is understanding and a clear specification, not a polished demo.** By the end of this week, you should be able to explain what you will build, what you will measure, why the comparison is fair, and which questions remain open for Simo and Jussi.

## 14. Evidence boundary and supporting documents

This roadmap synthesizes the current research plan, your stated decisions and Simo's feedback, the existing literature/feasibility analysis, the supplied Oulu guidance, and a structural inspection of the downloaded example thesis. It does not report new experimental results, certify the latest university procedures, or establish formal supervisor/company commitments. The calendar, implementation order, and phase gates are planning recommendations rather than requirements imposed by the papers.

For a specific “why this question/method?” discussion, use the [feasibility evidence matrix](<C:/Users/canba/Desktop/university/thesis/idea1-Authorization/literature/CANDIDATE_B_FEASIBILITY_2026-10-14.md>) and [mock supervisor Q&A](<C:/Users/canba/Desktop/university/thesis/idea1-Authorization/literature/SUPERVISOR_MOCK_QA_2026-10-14.md>), then verify the cited passage in the original paper. Keep a trace from source evidence to your design choice and from your experimental evidence to each conclusion.

## 15. Miro companion

The accompanying editable mind map is designed to summarize phases, reading priorities, writing outputs, and the first-week actions. This Markdown document holds the detailed rationale and completion checks. Update the document and board together when substantive scope or scheduling decisions change.

**Creation status, 2 November:** the complete Canvas Composer layout is saved in [THESIS_ROADMAP_MIRO_2026-11-02.svg](<C:/Users/canba/Desktop/university/thesis/idea1-Authorization/THESIS_ROADMAP_MIRO_2026-11-02.svg>). This is Miro authoring data for editable shapes and connectors, not a finished preview image. The layout has three sections, 42 labeled nodes, and 32 connectors, with valid XML and connector references. An empty board was created before Can reported switching Miro accounts. After the switch, Miro connector calls returned “Unknown tool,” including after Can confirmed reconnection in Codex. No layout has yet been uploaded, and the new account has not been verified. Resume by checking the current connection/account and selecting or creating the appropriate board; then upload, verify the resulting layout, and show the populated board. Do not mistake the earlier empty board for a delivered mind map.
