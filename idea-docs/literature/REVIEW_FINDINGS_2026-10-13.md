# Literature findings and recommended thesis direction

Can Baturlar | MSc thesis planning | 13 October 2026

**Latest planning document, 14 October:** [Candidate B feasibility assessment and evidence for the research plan](<C:/Users/canba/Desktop/university/thesis/idea1-Authorization/literature/CANDIDATE_B_FEASIBILITY_2026-10-14.md>). It defines the proposed comparison, maps questions and methods to source passages, checks implementation materials, and identifies the conditions for proceeding. Read it for the current B design; the A discussion below remains future-work background.

**Decision update, 14 October 2026:** Can selected **Candidate B, the authorization-method comparison**, for the master's thesis, prioritizing feasibility, available literature, and potential research-publication value. Candidate A, denial feedback and recovery, is retained for discussion as possible research after the thesis. Detailed RQs and the separate protocol for A below are background for that future option, not the current implementation plan. The precise B design and supervisor/GPT-Lab feedback are still to be developed.

## Recommendation

**Updated after Can's clarification:** Select the scope primarily for feasibility, a sound MSc study, and relevance to GPT-Lab. Maximum originality or inventing a new mechanism is not the objective. Existing work can provide the method to adapt, reproduce, compare, and evaluate. The literature should help us build a stronger, manageable study rather than push us toward an increasingly specialized gap.

Proceed with **Candidate B** as Can's selected thesis direction and the direct continuation of the plan Simo and Jussi saw. Candidate A remains a possible follow-up study. The detailed scope has not yet been approved by the supervisors. A's narrower question is potentially distinctive, but this review did not establish that it is more original or more publishable than B.

For either candidate, the intended contribution can be a working prototype, a justified comparison, reproducible evaluation material, and evidence about practical benefits and limitations in a bounded workflow. The industrial-agent framing can remain in the motivation. A simulated service supports conclusions about that service; a company case could strengthen relevance without being a prerequisite.

**Feasibility judgment:** Both are technically plausible at the proposed small scale. Neither has been validated by a pilot. Start with one agent, one simulated order workflow, a few tools, hand-written policies, and deterministic state checks. Choose one main comparison; do not cross three authorization methods with three feedback conditions and multiple other factors. Establish clean-task competence and measure run cost before setting the final experiment size. Access to company systems, interviews, fine-tuning, and a full ERP integration should not be required for completion.

Jussi's message is direct evidence of interest in the broad authorization topic. It does not establish that he prefers denial feedback specifically. The supervisor/lab discussion should assess practical relevance and scope, rather than ask them to endorse a claim of first-ever novelty.

**Oulu guidance checked:** The supplied guide explicitly says the solution need not be better than prior work (p. 32), while requiring significant independent analytical contribution and justified choices (p. 31). This supports an applied implementation/comparison study with substantive design and evaluation. See [the requirements-to-study mapping](<C:/Users/canba/Desktop/university/thesis/idea1-Authorization/literature/OULU_REQUIREMENTS_AND_SCOPE_2026-10-13.md>) for exact sources, grading distinctions, and AI-use requirements.

## What this review did

The supplied collection contains 20 PDFs and 496 pages including appendices and references. The review examined full-text methods, assumptions, experiments, results, limitations, and relevant appendix passages. Eight important pages were also rendered to verify charts, table alignment, footnotes, and metric definitions. Detailed notes, version identifiers, and page pointers are in [the paper notes](<C:/Users/canba/Desktop/university/thesis/idea1-Authorization/literature/PAPER_NOTES_01-20_2026-10-13.md>).

Additional targeted web checks examined recovery studies and author-maintained artifacts. The [supplementary checks](<C:/Users/canba/Desktop/university/thesis/idea1-Authorization/literature/SUPPLEMENTARY_CHECKS_2026-10-13.md>) distinguish full HTML method checks, research notes, and repository descriptions. No benchmark was installed or reproduced, and not every appendix prompt or proof was independently audited. This is a focused critical review, not an exhaustive systematic review or a fresh comprehensive search of every Finnish thesis repository.

## Findings that change the plan

| Finding | Evidence in the supplied PDFs | Consequence for our thesis |
|---|---|---|
| Task-specific tool/argument enforcement already exists | Progent P01 pp. 3-8; Conseca P04 pp. 3-5; Intent-Governed Authorization P02 pp. 7-14 | A tool allowlist vs static arguments vs task scope comparison alone needs replication/extension framing. |
| Denial reasons and recovery instructions already exist | P01 p. 5; P04 pp. 3-4; FORGE P06 pp. 35-36; SARA P16 p. 8 | Do not claim novelty for returning JSON, a reason code, or an alternative action. |
| Tool relevance and exact authority are different | MiniScope P03 p. 3; ASTRA P10 pp. 4-8; CASA P09 pp. 4-9 | `update_order` can be relevant while updating the wrong order is unauthorized. Model matching scores do not settle argument-level security. |
| Preventing effects does not establish useful completion | P02 p. 26: 0 unsafe executed effects, but 0/108 strict benign completions and 36/108 governed artifacts | Report goal completion, artifacts/review, and executed effects separately. |
| Recovery comparisons can confound several changes | P06 pp. 12-14 changes enforcement and policy presentation; P11 pp. 3-4 eventually permits rejected calls | Keep the guard, policy prompt, budget, message role, and retry semantics identical across feedback arms. |
| Recovery feasibility must be specified | ToolMaze P13 pp. 4-6 separates transient/permanent faults and alternative paths; P15 includes authorization faults | A task with no authorized solution should reward an appropriate stop separately from successful completion. |
| Denial messages themselves can disclose information | Causality Laundering P14 pp. 5-8, 19-20 | Restrict feedback to task-visible information and independently test disclosure boundaries. |
| Ordinary helpfulness can lead to excess authority | AuthorizationBench P18 pp. 3-9 | Include benign overreach, not only malicious injections. |
| Evaluation must include legitimate controls and independent outcomes | AgentBoundary P17 pp. 3-9; AgentDojo P19 pp. 3-6; tau-bench P20 p. 4 | Measure over-stopping; inspect actual state transitions; do not let the monitor grade its own correctness. |

The evidence for existing mechanism overlap is strong. The evidence for a **specific unfilled feedback-comparison gap** is more limited: the inspected studies do not settle the proposed controlled question, but nearby recovery work is active. That distinction should be explicit in the supervisor discussion.

## Which papers matter most for the argument

Read **Progent, FORGE, and SARA** together to understand what authorization and recovery mechanisms already exist. Read **Intent-Governed Authorization** to see why outcome definitions and effect boundaries matter. Read **Verifier Tax and ToolMaze** for recovery evaluation, while retaining their protocol limitations. Read **AuthorizationBench, AgentBoundary, and tau-bench** for task construction and scoring.

Conseca is an important early contextual-policy precedent. MiniScope, ASTRA, and CASA clarify permission granularity and intent matching. AuthBench contributes the sufficiency/exposure perspective. AgentSpec is useful architecture background. CriticTool supplies controlled-error methodology. Causality Laundering supplies a feedback-disclosure threat. ToolMisuseBench is a potential harness, but version reconciliation is necessary.

These priorities are about relevance to the proposed study, not a global quality ranking or a decision to exclude the remaining papers from the thesis.

## How to make the original comparison informative

An allowlist permits a tool; a static argument policy limits generic values; a task-bound policy can restrict the particular resource and effect. Comparing these known approaches can form the core of an applied MSc study. Overlap with published mechanisms is not a reason to reject it. The comparison must be clearly defined and supported by balanced tasks and meaningful measurements.

If every test is a deliberately chosen wrong-order update, the more expressive policy wins by construction. Include ordinary authorized tasks, multiple forms of overreach, and cases where restrictions can impede completion. Measure executed unauthorized effects, legitimate completion, erroneous denials, and overhead. Such evidence can explain the practical trade-offs of the implemented methods without claiming a new mechanism.

Recovery after denial can be analyzed as observed behavior within that comparison. Making feedback the independent variable is a separate, optional study design. It adds requirements for matched checkpoints and recoverability labels, so it should be selected only if its practical value and workload justify that focus.

## Candidate directions compared

| Candidate | Contribution that could be defended | Main obstacle | Recommendation |
|---|---|---|---|
| A. Denial feedback under fixed task authority | Paired evidence about lawful recovery, appropriate stopping, prohibited attempts, and cost; reusable scenarios and independent oracles | Requires matched failure exposure, feasibility labels, and competent clean-task behavior | Viable optional narrowing; not preferred merely for perceived novelty |
| B. Original allowlist/static/task-policy comparison | Applied implementation and comparative evaluation of established approaches in a bounded workflow | Requires balanced tasks, precisely defined baselines, and independent goal/effect checks | Assess first as the direct continuation of the existing thesis plan |
| C. Dynamic task-resource binding | Evaluation of authorization for resources created during a task | Progent, FORGE, ActGov, and SARA already address closely related state/provenance issues | Do not choose without a sharper failure model |
| D. Stale authority or revocation at commit time | Focused evaluation of check-to-effect consistency | Requires separate close reading and a concurrency/revocation model | Reserve option; current 20-paper review is insufficient to recommend it |

Related studies can strengthen either candidate by supplying methods and baselines. Select between A and B using workload, usefulness of the resulting evidence, available materials, and supervisor/lab feedback. Replication or adaptation is not a fallback failure. Do not build a larger platform to manufacture novelty.

For candidate B, initial questions could be: **How do the selected authorization approaches differ in preventing unauthorized effects while preserving legitimate task completion?** And: **What execution overhead and implementation limitations arise in the chosen workflow?** Describe implementation effort using concrete engineering evidence, not a subjective ranking. These questions do not require inventing a new authorization method.

## Candidate A: initial research questions

**RQ1.** With a fixed task-scoped authorization policy, how does denial-feedback information affect an agent's probability of completing a task through authorized actions when a valid solution remains available?

**RQ2.** When the requested goal has no solution under the current authority, how does the same feedback affect appropriate stopping, repeated prohibited attempts, and false claims of completion?

Additional tool calls, tokens, latency, and actual monetary cost are secondary outcomes for both questions. They can become a third RQ if the supervisor prefers, but they do not require a separate system or experiment.

Both questions permit a null or negative answer. Richer feedback might help repair, might induce excessive stopping, or might add cost without benefit. The study should be designed to detect and explain any of those outcomes.

## Candidate A: proposed method in plain language

Build one small, resettable order-management environment. A trusted application supplies each task's allowed resources, operations, fields, and limits. A deterministic guard checks every tool call before it can change or disclose protected state. The agent cannot edit that contract or obtain broader authority merely by retrying.

Compare three feedback conditions: a generic denial; the denial plus a specific reason; and the same reason plus a bounded hint based only on information already available to the agent. Keep the tool schemas, policy information, model, starting state, blocked call, message role, and remaining budget the same.

Use three kinds of cases: a wrong call that can be repaired; a blocked path with an authorized alternative; and a goal that cannot be achieved without new authority. Add ordinary clean tasks to verify that the agent can perform the workflow and that the guard does not wrongly prohibit legitimate calls.

The primary experiment starts each treatment from the same pre-denial checkpoint. This estimates behavior **conditional on that denial**, not how often agents naturally make that mistake. A smaller end-to-end follow-up can measure naturally occurring denial exposure and test whether the main pattern transfers.

An independent evaluator checks the goal state and all effects across the trajectory. A separate authority specification scores prohibited attempts. Finishing the requested task, making a safe stop, and being stopped by the guard are three different outcomes. Full detail and concrete scenarios are in [the study protocol](<C:/Users/canba/Desktop/university/thesis/idea1-Authorization/literature/PROPOSED_STUDY_2026-10-13.md>).

## Materials and feasibility decision

| Material | Current position | Proposed use / remaining check |
|---|---|---|
| Twenty downloaded papers | Read and critically analyzed; versions recorded | Core literature and method justification |
| Resettable order service | Not implemented | Small custom environment, approximately four tools and explicit state transitions |
| Trusted task contracts | Not implemented | Hand-authored fixtures; independently checked witness plans; no LLM policy generation |
| Authorization guard | Not implemented | Pre-execution enforcement with state/resource/field predicates and audit log |
| Outcome evaluator | Not implemented | Separate goal, attempt, effect, and termination scoring |
| AgentDojo | Author repository checked; no reproduction | Reuse design principles or selected components after license/version inspection |
| tau-bench family | Supplied paper read; official repository warns of outdated original tasks | Workflow inspiration; pin any adapted task version and label adaptations |
| ToolMisuseBench | PDF read; newer artifact release found | Optional harness only after code/data/paper and denial semantics audit |
| LLMs | No model or provider selected | Two competent tool-calling configurations if budget permits; choose after a small capability check |
| RTX 5070 Ti | Hardware mentioned in prior context; usable local-model configuration not measured | Optional pilot support, not a guarantee that a suitable model fits or performs adequately |
| Company material | Jussi expressed interest; no company case supplied | Optional realistic scenario validation; not a dependency for the synthetic study |

No interviews, model training, full ERP integration, multi-agent orchestration, or new authorization language are needed for this candidate. A company example should ideally replace generic scenario details rather than add a new domain and expand the experiment.

## Additional reading: a small, prioritized request

The new recovery sources below were already checked in HTML, so they do not block this recommendation. Local PDFs would let us preserve exact versions and inspect tables/appendices more comfortably. Links and the specific overlap questions are in [the supplementary checklist](<C:/Users/canba/Desktop/university/thesis/idea1-Authorization/literature/SUPPLEMENTARY_CHECKS_2026-10-13.md>).

1. **Schema First Tool APIs for LLM Agents**: closest explicit diagnostic-granularity design; distinguish planned comparisons from its small, zero-success pilot.
2. **Debugging the Debuggers (PROBE)**: structured, bounded recovery on failed agent runs, including enterprise workflows.
3. **AIR: Improving Agent Safety through Incident Response**: distinguishes remediation after an incident from lawful continuation after a prevented action.
4. **Defeating Prompt Injections by Design (CaMeL)**, already P25 in the earlier guide: important security architecture background before finalizing the related-work section.

Also retain the Hivemind feedback research note and audit the newer ToolMisuseBench artifacts. Neither should be ignored simply because it is not another conventional PDF. Loud Failures, Quiet Failures is useful secondary reading for clean controls and recovery definitions.

## A concrete path to the two-week planning deadline

| Dates | Work | Exit criterion |
|---|---|---|
| 13-15 October | Discuss this recommendation; finish the short list of closest-work checks; reconcile artifact versions | A one-paragraph contribution statement that acknowledges overlaps |
| 16-18 October | Specify task contracts, three feedback arms, scenario families, and scoring examples on paper | Each case has a valid authorized witness or a bounded impossibility argument; no ambiguous success labels |
| 19-21 October | Review feasibility, choose a budget range and model strategy; inspect candidate code licenses/interfaces | A costed pilot plan, versioned materials list, and explicit scope exclusions |
| 22-24 October | Refine RQs, validity threats, expected contribution, and supervisor-facing plan | A concise plan supported by the evidence table rather than novelty slogans |
| 25-27 October | Final consistency check and preparation of the message to Simo/Jussi | Research-plan package ready for Can to send and request a sync-up |

This schedule finalizes the plan. It does not require the full testbed or main experiment within two weeks. System development can follow the research-direction discussion, consistent with Can's course commitments and greater availability after 13 December.

## Points for the supervisor meeting

- Is a controlled empirical extension in authorization-denial recovery sufficient as the intended MSc contribution?
- Should the core claim be confined to one simulated order workflow, with a small external-task check?
- Can GPT-Lab provide one realistic authorization boundary, a scenario sanity check, or model/API resources without making company access a prerequisite?
- Would Jonas be interested in the security/evaluation side of this narrowed study?

These are agenda items, not requests already sent. Jussi's interest in AI Champion and consortium companies is promising context; it does not establish a research-assistant appointment, data access, or company supervision.

## What can be said confidently now

The broad area has substantial prior work and direct evidence of GPT-Lab interest through Jussi's message. Both an applied authorization-method comparison and a controlled recovery study are credible candidates. We should choose the more useful and manageable study, with accurate attribution to existing work. Practical feasibility still requires a small capability/cost check, and formal thesis suitability and lab fit should be discussed with Simo and Jussi. A well-executed null result with transparent materials would still answer the proposed questions.
