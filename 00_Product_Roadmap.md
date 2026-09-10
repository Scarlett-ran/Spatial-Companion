# Spatial Companion — Product Roadmap

This roadmap guides the project from problem exploration through productization. Each stage addresses the most important current uncertainty and ends with an evidence-gated **Go / Kill / Redirect** decision.

## Roadmap at a Glance

| Stage | Question to answer | Primary method | Stage outcome |
|---|---|---|---|
| **1. Scout — TRL 1–2** | Is the problem real, are its boundaries clear, and which judgments remain assumptions? | Problem decomposition, assumption mapping, concept expression, and risk prioritization | Define the next lowest-cost validation step and its claim boundary |
| **2. Browser Validation — Does Not Advance XR TRL** | Is the core interaction loop easy to understand, and are there early user signals worth pursuing? | Browser demo, observation, and interviews | Go / Kill / Redirect, followed by a decision on whether to request XR resources |
| **3. XR Feasibility Prototype — TRL 3–4** | What capabilities does Goertek’s target platform provide, and can spatial placement, input, feedback, and failure recovery form a repeatable loop? | Platform capability audit, minimum on-device prototype, and bench testing | Confirmed technical baseline, repeatable loop, failure modes, and resource assessment |
| **4. On-device Experience Validation — TRL 5–6** | Under real target-device constraints, do embodiment, subjective contact, and low-disruption value hold up? | Separate spatial-contact and low-disruption coexistence studies, followed by repeated use | Validated experience evidence and a dependency / risk map |
| **5. Pitch & Pilot Gate — TRL 7** | Is the evidence strong enough to justify a bounded real-world pilot? | Live demo, evidence review, and resource and pilot plan | A scoped, owned, and time-boxed Pilot Go / No-go |
| **6. Productize & Launch — TRL 8–9** | Can the validated experience be delivered to target users reliably, safely, and sustainably? | Engineering, QA, privacy and accessibility work, operations, and launch validation | Pilot / MVP launch, monitored results, and a Scale / Iterate / Stop decision |

## Working Principles Across All Stages

Before each validation effort begins, define five things: the assumption being tested, the lowest-cost method, the observable evidence, the success / failure threshold, and the conclusions the result cannot support. Success criteria must be set before testing to avoid redefining the goal after seeing the result.

Keep different forms of evidence separate:

- **Concept evidence:** whether users understand the concept and the causal relationship within the interaction.
- **Behavioral evidence:** what users actually do, including whether they repeat, keep, return to, or close the experience.
- **Experience evidence:** whether users perceive embodiment, contact, delight, or burden.
- **Technical evidence:** stability, latency, false triggers, permissions, performance, and failure recovery.
- **Product evidence:** target context, adoption friction, resource cost, ownership, and delivery path.

Each prototype can support only the conclusions that match its capabilities. Browser input cannot prove contact in physical space; one short experience cannot prove long-term companionship; and a closed, single-app immersive test cannot prove cross-app or multitasking coexistence.

## 1. Scout — TRL 1–2

**Stage goal:** establish that the project is worth validating. The current primary question is whether spatial computing can bring a virtual pet with no real-world care responsibilities into the user’s space and provide a more embodied companionship experience than a 2D pet.

**Work required:**

1. Define the problem, why now, why us, and the target users’ real constraints.
2. Separate facts, personal observations, established design decisions, user assumptions, experience assumptions, and technical assumptions.
3. Define the candidate experience and its behavioral boundaries, including low disruption and no feeding, check-ins, punishment, or long-term care obligations.
4. Prioritize risks by impact × uncertainty × validation cost, then choose the next lowest-cost validation step.
5. Submit the validation goal to the Mentor before building and obtain a Go or Redirect decision.

**Stage outputs:** problem statement, assumption map, concept demo, interaction experience specification, validation goal, and the corresponding Mentor decision record.

**Exit criteria:** the problem and target-user boundaries are sufficiently clear, and the next stage’s validation question, method, and claim boundary have been approved. The concept demo must not be treated as evidence of spatial placement, hand tracking, subjective contact, or companionship value.

## 2. Browser Validation — Does Not Advance XR TRL

**Stage goal:** before requesting XR engineering resources, use the lowest-cost method to screen whether the core interaction logic is legible and whether there are early user signals worth pursuing.

**Minimum interaction loop:**

`Baobao sleeps → The user attends to Baobao → Baobao notices and looks back without actively demanding interaction → The user pets Baobao → Baobao nuzzles toward the user → The user leaves → Baobao watches briefly, then returns to a quiet state`

In the browser, mouse hover serves as a proxy for gaze, and mouse input serves as a proxy for petting. The purpose is to test whether users understand that their action caused Baobao’s response, not whether mouse interaction can reproduce XR.

**Work required:**

1. **Goal Approval:** confirm first that a browser demo is the right next validation method.
2. **Demo Scope:** retain only the core loop above and the feedback required to communicate it; exclude progression systems, multiple characters, multiple touch regions, and full product functionality.
3. **Test Plan:** define tasks, observations, interview questions, and Go / Kill / Redirect thresholds before testing.
4. **Build & QA:** ensure triggers, animations, exits, and re-entry work reliably and repeatedly.
5. **User Test:** observe whether users can complete the loop without difficulty, understand the causal relationship, and repeat the interaction voluntarily; ask whether they would use it again and whether they would let Baobao remain present while doing other things.
6. **Decision:** record comprehension, actual behavior, and stated intent separately, then decide whether the evidence justifies requesting XR resources.

**Permitted conclusions:** the legibility of the core loop and the relationship between input and response, plus early directional signals about repeat interaction, reuse, and willingness to coexist with Baobao under low-disruption conditions.

**Exit criteria:** if the interaction is legible and the signals are positive, Go to the XR Feasibility Prototype; if user-value signals are insufficient, Kill or reshape the concept; if the Mentor determines that technical feasibility is the more important current risk, Redirect to a narrower XR feasibility spike.

## 3. XR Feasibility Prototype — TRL 3–4

**Stage goal:** validate the T1–T3 technical loop with the smallest on-device prototype, without building a complete product or requiring production-quality art.

**Confirm the target platform first:** before writing XR code or choosing an asset format, work with Goertek XR engineers to confirm the target device model, operating system, recommended engine / SDK, deployment method, and available development resources. Capture the result in a one-page capability matrix covering at least:

- Whether the platform provides eye tracking, head orientation, hand skeletons, or controller input, and the level of data the application can actually access.
- Whether it supports plane / scene understanding, spatial anchoring, occlusion, persistence, and relocalization.
- Whether the application can coexist with other content or must run in a closed, single-app immersive mode.
- The permissions, user authorization, data restrictions, and fallback behavior required for each capability.
- Recommended 3D asset formats, animation systems, rendering capabilities, performance budgets, and on-device debugging tools.

**Then build the minimum Baobao:** continue using the existing PNGs as character-design references. Create a low-complexity 3D model suitable for real-time rendering, with credible physical scale, simplified materials, skeletal / facial controls, and six named animations: `sleep`, `wake`, `look`, `sniff`, `nuzzle`, and `settle`. Use formats for the model, skeleton, and animations that the target engine supports reliably; do not lock into USDZ, FBX, glTF, or a specific authoring tool before the platform is confirmed. Establish silhouette, scale, and motion intent before increasing fur or material fidelity.

**On-device technical scope:**

- If the target platform supports real-environment understanding, place Baobao on a table or floor and use the platform’s spatial anchoring mechanism to test position, scale, and recovery when the experience is reopened. If it does not, record this as a core experience gap; a fixed position in a fully virtual scene is not evidence of spatial anchoring.
- Create only one simplified collision / trigger region on the forehead, using the hand or controller input actually supported by the platform to detect approach, contact, and withdrawal.
- Drive a `Resting → Aware → Contact → Nuzzle → Settle → Resting` state machine from input; enter `Safe Pause` when tracking is lost or input is uncertain.
- Record spatial drift, end-to-end response latency, false positives / missed triggers, animation interruption, recovery time, frame rate, and permission failures.
- Exclude feeding, check-ins, long-term progression, multiple characters, multiple touch regions, complex navigation, and production-quality art.

“Baobao notices the user’s gaze” remains an experience intention and does not assume that the target device exposes raw gaze data to the application. If only head orientation, a system focus event, or an explicit confirmation input is available, mark it as a proxy and evaluate separately whether it is sufficient to support the intended experience.

**Exit criteria:** the capability matrix has been confirmed by target-platform engineers; the core loop runs repeatedly on the target device; major failure modes are understood; the experience can degrade safely when permission is denied, input is unavailable, or tracking is lost; and the team can determine the required device, engine, 3D, XR engineering, and research resources. If the target device lacks spatial or input capabilities essential to the core experience, Redirect the product mechanism or target platform before building a complete demo.

## 4. On-device Experience Validation — TRL 5–6

**Stage goal:** validate spatial-contact experience and low-disruption coexistence separately under real device and usage constraints. Use different runtime modes and evidence for the two questions rather than forcing one prototype to answer everything.

### A. Spatial and Contact Study

- Test whether Baobao’s position and scale create credible embodiment.
- Compare synchronized, delayed, and absent responses to determine whether users attribute Baobao’s reaction to their own hand movement.
- Record when users report approach, contact, pass-through, delay, or merely triggering an animation.
- Test the reachability and comfort of direct contact, tracking stability, and Safe Pause behavior.

This path can provide evidence about spatial placement, input, and subjective contact. If it runs in a closed, single-app mode, it cannot prove cross-app or multitasking coexistence.

### B. Low-disruption Coexistence Study

- Let Baobao remain present alongside a short task or other content, allowing users to ignore, move, hide, or close it at any time.
- Observe whether Baobao obscures primary content, captures attention, or causes users to close it.
- Ask whether users would keep and use it again, while recording actual keep / close behavior.
- Gradually introduce repeated-use studies to distinguish character novelty from sustained companionship value.

The exact format depends on the capability matrix. If the target platform supports application or spatial-content coexistence, test under real coexistence conditions. If it does not, record cross-app coexistence as a platform limitation and test low disruption in multitasking, overlay, or another representative mode that the target device permits. Do not present evidence from a substitute context as cross-app evidence.

This path can test low-disruption and coexistence tendencies, but controller input, system focus events, or other limited inputs must not be treated as evidence of full hand or eye tracking.

**Combined evidence required:** spatial stability, response latency, and failure recovery data; differences in embodiment between the spatial and Browser / 2D versions; the effect of synchronized feedback on subjective contact; whether users still choose to keep Baobao when it can be ignored or closed and creates no care obligation; and adoption friction caused by device access, wearing duration, privacy permissions, and runtime modes.

**Exit criteria:** the experience can be reproduced reliably in representative environments; major assumptions have supported, refuted, or unresolved findings; the risk map covers technology, experience, users, resources, privacy and safety, and product adoption; and the team can estimate the people, time, and cost required for a pilot.

## 5. Pitch & Pilot Gate — TRL 7

**Stage goal:** not to prove that every risk has disappeared, but to let decision-makers judge whether a bounded real-world pilot is worth the investment.

**Work required:**

1. State the real problem, target user, and why now in one sentence.
2. Demonstrate the validated core loop live and identify the demo’s runtime mode.
3. Use an evidence matrix to distinguish what is validated, refuted, still unknown, or deferred.
4. Present the most important technical, experience, privacy, adoption, and resource risks, along with their mitigations.
5. Define pilot users, context, duration, devices, success metrics, stop conditions, and data-handling practices.
6. Make a concrete request covering roles, devices, budget, timeline, owner, and the next decision date.

**Exit criteria:** receive a Pilot Go with a bounded scope; return to the relevant stage if evidence is insufficient; or reach a No-go based on known risks. The pitch must not substitute packaging for evidence or ask vaguely for “continued support.”

## 6. Productize & Launch — TRL 8–9

**Stage goal:** turn the validated experience from a research demo into a product that can be delivered reliably, maintained sustainably, and evaluated meaningfully.

**Work required:**

- Engineer the prototype code and character assets for production, including performance budgets, resource loading, state persistence, version migration, crashes, and tracking recovery.
- Complete privacy minimization, permission explanations, data-retention rules, safety boundaries, and the target platform’s application-distribution / enterprise-deployment requirements.
- Perform QA across different spaces, lighting conditions, seated / standing postures, hand conditions, accessibility needs, and extended-wear scenarios.
- Define product metrics consistent with the target platform’s data boundaries. Unless capability, authorization, and necessity are all confirmed, do not depend on raw gaze data; prioritize explicit interactions, session retention, voluntary closure, repeat use, and failure recovery.
- Establish a content and character-asset pipeline so that new behaviors do not undermine the low-disruption principles or the state machine.
- Begin with a bounded pilot and expand gradually; reassess experience value, technical cost, and adoption friction at every expansion.

**Outcome decisions:**

- **Scale:** the core value, reliability, and resource model hold; expand to more users and contexts.
- **Iterate:** value exists but a specific element is insufficient; return to the relevant stage, revise it, and retest.
- **Stop:** user value, technical reliability, or the resource model cannot work within acceptable constraints; stop further investment.

Launch is not the end of the roadmap. After launch, continue monitoring novelty decay, repeat use, reasons for closing, performance, and permission failures. Any major new feature should re-enter the cycle of assumption → lowest-cost validation → evidence gate.
