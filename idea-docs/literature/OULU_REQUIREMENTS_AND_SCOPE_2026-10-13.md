# Oulu thesis guidance: implications for this project

Reviewed 13 October 2026. This note distinguishes what the supplied university documents say from our interpretation for Can's authorization thesis. It is planning material, not a substitute for the principal supervisor's assessment.

## Sources and version boundary

- [CSE thesis guide](<C:/Users/canba/Desktop/university/thesis/reference/thesis_instructions/CSE_diploma_thesis_instructions.pdf>): 41 pages; cover dated June 2026. The foreword says it applies to theses starting or completing from September 2025. The cover retains a `TODO` prefix and the foreword mixes revision dates; this review follows the supplied contents without independently certifying that this is the latest official release.
- [Evaluation instructions](<C:/Users/canba/Desktop/university/thesis/reference/thesis_instructions/Evaluation_Instructions.pdf>): two pages; no visible issue date. The rubric calls its criteria guidelines to be applied with individual consideration. Aspect scores are not a formula from which we can promise a final thesis grade.

Page references below are physical PDF pages. Relevant guide passages and both evaluation pages were read; the evaluation tables and guide pp. 31-32 were also visually inspected.

## Main conclusion

**The guidance supports an applied engineering thesis based on established methods, provided that Can makes a significant personal contribution through analytical problem-solving, justified choices, implementation or other substantive work, and evaluation. It does not make a globally novel algorithm or superiority over prior work a general requirement.**

The clearest sentence is in the guide's discussion section, p. 32: **“Your solution does not have to be better”**. The surrounding paragraph still requires analysis of how the objectives were met and comparison with the state of the art.

This supports retaining the original authorization-method comparison as a serious candidate. It does not mean that merely assembling existing code, following a recipe, or reporting a few successful demonstrations would meet the expected contribution.

## Requirements mapped to our thesis

| What the supplied guidance says | Source | Implication for our project (interpretation) |
|---|---|---|
| A typical thesis solves a relatively extensive technical problem and develops independent engineering skills | Guide p. 9 | One workflow can be bounded while still requiring substantive authorization design and evaluation. Do not reduce the work to a trivial demo. |
| Thesis work can include designing, building, and testing software | Guide p. 11; p. 16 | A prototype plus controlled experiments is a compatible thesis form. |
| Introduce research questions, methodology, objectives, and the justification for scope | Guide pp. 29-30 | Explain why this workflow, these authorization baselines, and these measurements answer a useful question. |
| Avoid objectives that are too challenging, because failure to meet them can reduce the grade | Guide p. 30 | Prefer an achievable core experiment; keep company integration and extra domains optional. |
| Prior solutions and research should justify the chosen approach | Guide p. 30; rubric aspect 4 | Related work is a foundation for method selection, not evidence that our area is disqualified. |
| A separate theoretical section is not necessary when it does not naturally fit | Guide p. 30 | Explain the security assumptions and concepts needed for the design; no artificial formalism or new theorem is required. |
| The author must contribute significantly rather than simply follow others' instructions, weigh alternatives, and justify selections | Guide p. 31 | Can's contribution can include the task/authority model, baseline adaptation, design decisions, scenario construction, and experimental analysis. |
| Test the solution against its requirements and distinguish measured outcomes from estimates | Guide pp. 31-32 | Specify independent checks for legitimate completion and unauthorized effects; label pilot estimates and illustrative sample sizes. |
| Analyze reliability; strong conclusions require sufficiently large samples | Guide p. 32 | Determine experiment scale from the intended claims and pilot evidence. The guide does not give a fixed number of agent models or scenarios here. |
| Compare results with objectives and similar work; superiority is not required | Guide p. 32; rubric aspect 6 | Null results, utility losses, and limitations can be useful findings when the analysis is sound. |
| Discuss significance to engineering/science and the company, organization, or project | Rubric aspects 6-7 | Explain what a deployment team can learn about authority boundaries and practical trade-offs. GPT-Lab relevance needs its own discussion with Jussi. |
| Independence, initiative, clear language, and presentation contribute to evaluation | Rubric aspects 3, 8-10 | Maintain a decision log, understandable methods, and regular progress discussions. Good engineering alone does not replace clear documentation. |

## What originality means in this rubric

The highest descriptors for achievement and significance mention substantial research/development contributions, remarkable improvements, new results, publication, or patents. These are indicators at the upper end of particular assessment aspects, not blanket conditions that every thesis must invent a new method or publish a paper.

The rubric also evaluates scope and challenge. Therefore, “doable” should mean a bounded, substantive problem, not the smallest possible implementation. Our aim should be enough depth to demonstrate independent judgment without adding unnecessary systems or experimental factors.

A method comparison can provide that depth through realistic task constraints, carefully justified baselines, sound experimental controls, and analysis of when restrictions protect the workflow or impede legitimate work. The final suitability of the exact scope remains for Simo to assess.

## Practical consequences for scope selection

The original comparison and feedback study are both compatible in form with the guide. The guide does not choose between them. Under Can's stated priorities, assess the original comparison first because it directly develops the plan already discussed with Simo and Jussi.

A defensible minimum research package for that candidate would contain:

1. A clear order-management problem and an explicit definition of who may do what to which resources.
2. A literature-based choice of authorization approaches, with honest descriptions of differences and shared assumptions.
3. A working, resettable implementation and traceable design decisions.
4. Balanced legitimate and unauthorized-action scenarios, with independent checks of both goal completion and actual effects.
5. An experiment whose size, models, controls, and costs fit the intended claims.
6. Critical analysis of the results, limitations, and usefulness to agent deployment.

This list is our proposed operationalization of the guidance, not a university-prescribed six-item checklist. The feedback experiment is optional; it should not be added merely to make the thesis appear more original.

Interviews are not imposed by these design passages. Page 31 gives interviewing experts as one example of identifying requirements. A university research unit can act as commissioner (p. 11), so an external company is not the only route. Commissioner/supervision arrangements still need to be settled through the normal thesis process.

## Literature coverage

The guide describes the literature survey as close to exhaustive and requires original sources, accurate attribution, and IEEE references (pp. 33-34). For our planning, this means checking coverage of the selected question and its closest alternatives rather than assuming that a count of 20 papers is sufficient. A well-bounded scope makes that coverage achievable. The existing paper notes are working aids; scientific claims in the thesis should cite and be verified against the original papers.

## AI assistance and Can's independent contribution

The guide is explicit about our collaboration (pp. 9-10, 13, 20-21): discuss AI use with the supervisor before writing; use AI assistance with the supervisor's approval; remain personally responsible for accuracy and originality; and include an introduction subsection titled **Author's Contributions and the Role of Artificial Intelligence**. The disclosure should identify tools, purposes, and the parts of the work affected. AI is not a source of scientific facts.

Page 20 says, “As a general rule, do not generate parts of your thesis,” and warns against presenting content not produced by the author as their own. It lists brainstorming, planning, information retrieval, visuals, and proofreading as assistance uses subject to supervisor approval; other uses also require approval.

Accordingly, our review documents are planning and analysis aids. Can should verify the sources, understand and own the research decisions, and follow the agreed AI-use arrangements when preparing the submitted thesis. Record the actual assistance provided; do not later describe AI-assisted literature analysis or implementation as proofreading alone. This review does not establish that Simo has already approved a particular AI-use arrangement.

## Later writing and collaboration considerations

- The guide recommends a short project plan covering background, motivation, objectives, timetable, and risks (p. 12), and writing alongside the implementation (p. 21).
- It describes 50-80 pages as usual, not a mandatory minimum or maximum (p. 16). Its two-to-three-month full-time estimate concerns writing; it should not be treated as the duration of the entire research project (p. 21).
- It requires an English and Finnish title/abstract for an English thesis, including international students (pp. 16, 29).
- It describes the thesis as a public document and asks that company-publication arrangements be discussed early (pp. 14-15). If a company case is used, plan a publishable evaluation rather than depend on confidential details that cannot appear in the thesis.
- Administrative dates, current template availability, and operational submission procedures should be checked against the university's current instructions when they become relevant. They are not being scheduled from this local-file review.

## Result of this check

There is document-based support for Can's preference: choose a useful, feasible engineering study with a clear personal contribution and rigorous analysis. We should not keep narrowing the topic solely to find a unique mechanism. The remaining planning work is to specify and validate the particular experiment and obtain Simo/Jussi's feedback on its scope and relevance.
