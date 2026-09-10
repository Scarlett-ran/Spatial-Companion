# Autonomous Spatial Companion — Product Roadmap

This roadmap guides the project from problem exploration to productization. Each stage addresses the most important current uncertainty and uses an evidence gate to decide **Go / Kill / Redirect**.

## Product thesis and validation levels

**Baobao has a life of his own. Sometimes, that life intersects with yours.** Scout explores whether an autonomous spatial companion can create meaningful companionship through quiet co-presence, mutual recognition, and lightweight interaction without care obligations. “Recognition” currently refers to the intended experience of being noticed and receiving a response, not implemented identity recognition or memory across sessions.

**Presence → Relationship → Product** asks three sequential but independent questions: does Baobao feel present in the user's space; does that presence become companionship without obligations; and does that companionship justify device requirements and product form? Assess D1 spatial presence, D2 contact, and U1 companionship separately. U2 is split into U2a concept acceptance and U2b device adoption. A 2D version may provide similar companionship; stronger presence does not directly establish the need for a spatial form.

The six stages below describe development and resource decisions, not the three value levels. Within them, research proceeds in separate rounds: interaction understanding → spatial presence → contact → passive co-presence → repeated encounters → actual adoption, with Baobao World explored in the longer term. Each round focuses on one major risk. Prototypes may be reused, but results need separate interpretation. User segments, device habits, and platform conditions can be investigated early, without replacing the corresponding experiments. See the [Product Thesis and Validation Framework](./01_Scout_EN/02_Product_Thesis_and_Validation_Framework.md).

The project is currently in Scout exploration and browser preparation: video and documents exist, but browser implementation, external user research, and on-device validation are incomplete. There is no commitment of devices or engineering support. TRL labels remain planning markers, not evidence of passing a maturity assessment; browser validation does not advance XR technical maturity.

## Roadmap overview

| Stage | Question to answer | Main methods | Stage outcome |
|---|---|---|---|
| **1. Scout — TRL 1–2** | Are the user problem and candidate solution clear, and which judgments remain assumptions? | Problem decomposition, segment hypotheses, concept expression, and risk prioritization | Define the browser's main question, scope, and evidence boundary. |
| **2. Browser Validation — Does Not Advance XR TRL** | Is behavior understandable and coherent, is there initial perceived autonomy, and is the engineering reference specific? | Browser testing; Concept Video + Browser for engineering discussions | Decide on a limited device-resource request based on behavioral evidence and remaining risks. |
| **3. XR Feasibility Prototype — TRL 3–4** | Can the platform support the first presence experiment, and what conditions will later input/contact work require? | Platform review, minimum spatial prototype, and contact extensions as needed | Confirmed technical baseline, repeatable experiments, and failure modes. |
| **4. On-device Experience Validation — TRL 5–6** | Can Level 1 presence/contact and Level 2 companionship without obligations each hold up? | Separate spatial-contact and low-disruption coexistence tests, plus repeated use | Validated experience evidence and a dependency/risk map. |
| **5. Pitch & Pilot Gate — TRL 7** | Is a limited investment in a real-world pilot justified? | Live demo, evidence review, resource and pilot plans | A scoped, owned, and time-bounded Pilot Go / No-go. |
| **6. Productize & Launch — TRL 8–9** | Can the validated experience be delivered reliably, safely, and maintainably to target users? | Engineering, QA, privacy and accessibility, operations, and launch validation | Pilot/MVP launch, monitored results, and Scale / Iterate / Stop decisions. |

## Working principles across stages

Before validation begins, define five things: the main risk and assumption, the lowest-cost method, observable evidence, success/failure thresholds, and conclusions the results cannot support. Each experiment focuses on one major risk, with other observations as supporting information. Set success criteria before testing. Findings may support, refute, or leave an assumption unresolved; one round does not promise to eliminate every risk.

Record evidence separately:

- **Concept evidence:** whether users understand the solution and interaction causality.
- **Behavioral evidence:** what users actually do, including voluntary repetition, keeping, returning, or closing.
- **Experience evidence:** spatial presence, contact, delight, or burden.
- **Technical evidence:** stability, latency, false triggers, permissions, performance, and recovery.
- **Product evidence:** target context, adoption barriers, resource costs, ownership, and delivery path.

Prototypes support only conclusions that match their conditions: the browser checks logic and timing under proxy inputs; one experience does not prove long-term companionship; a closed single-app test does not establish cross-app coexistence.

Core metrics are defined in the [Assumption Map](./01_Scout_EN/05_Assumption_Map.md): Interaction Legibility, Perceived Autonomy, Spatial Presence, Contact Credibility, Passive Presence Value, Companionship Value, and Low-disruption Acceptance. Willingness to Keep Nearby is attitude and choice evidence for co-presence value. Not closing the character, finding him unobtrusive, or finding him cute cannot independently establish value.

## 1. Scout — TRL 1–2

**Stage goal:** prepare a clear thesis, scope, and research question for browser validation. The wider early exploration asks whether the behavioral model is understandable, coherent, and initially autonomous enough to justify on-device work. Document preparation and actual browser testing are separate milestones; long-term companionship and product adoption need not be established now.

**Work required:**

1. Define the problem, starting points, and available conditions. Retain the young-user framing and add pet-constrained, character-attached, and ambient-companionship seeking as unvalidated segments, without preselecting the most promising group.
2. Distinguish facts, personal observations, design decisions, user assumptions, experience assumptions, and technical assumptions.
3. Define the candidate experience and behavioral boundaries, including low disruption, no feeding, no check-ins, no punishment, and no long-term care obligations.
4. Make behavioral understanding and coherence the main browser focus, with autonomy and attention burden as supporting observations. Bound this round by risk and cost.
5. Confirm scope, investment, and execution arrangements with the Mentor before building. A defined direction does not mean resources are approved.

**Stage outputs:** problem statement, assumption map, concept demo, interaction experience specification, validation goal, and the corresponding Mentor decision record.

**Exit criteria:** candidate users and problem boundaries are clear, and the browser's main question, method, evidence boundary, and resourcing arrangements are actionable. Define the specific sample, tasks, and thresholds before testing. This completes validation preparation, not proof of behavior or companionship.

## 2. Browser Validation — Does Not Advance XR TRL

**Stage goal:** use an Interaction Logic Prototype / Baobao Behaviour & Interaction Reference to examine behavioral understanding, causality, states and timing, natural endings, and initial perceived autonomy, while preparing engineering materials. Whether users can explain why Baobao acts as he does is the main judgment. U1/U2a concept and companionship feedback is directional only.

**Minimum experience:** Baobao is already active at entry and may notice the user or continue his activity. The user can invite a lightweight response or never interact; afterward, both continue their own activities. Include resting and one non-sleeping activity without adding world, item, complex AI, or cross-app systems.

**Execution and deliverables:**

1. Confirm scope, investment, sample, tasks, viewing order, recording methods, and pass/revise/stop thresholds.
2. Use a few mouse or simulated-distance proxies for attention, approach, reaching, and withdrawal. Check that inputs, feedback, endings, and recovery are reliably repeatable.
3. Record unprompted behavioral explanations, misunderstandings, initial perceived autonomy, and attention burden. No interaction is also a valid path.
4. Deliver Concept Video + Browser: the video expresses the experience vision; the prototype explains states, causality, timing, and inputs/outputs. Arrange viewing order around the research purpose so the video does not supply answers in advance.
5. Submit capability mappings, permissions to confirm, observations, and remaining risks to support a scoped device-resource decision.

**Exit criteria:** use preset criteria to judge whether behavior is understandable and coherent enough, autonomy and disruption issues have been located, and engineering can discuss specific device needs. Concept appeal or another click does not replace this evidence. If results are insufficient, revise, adjust the method, or stop the current investment without claiming the spatial assumptions have been refuted.

**Rationale for device access:** only actual testing can establish which behavioral risks have been reduced. The browser cannot provide valid evidence for remaining questions about real scale, depth, spatial presence, actual inputs and contact, co-presence, or the target runtime. Device access is necessary for the next spatial evidence, not merely a demo upgrade. The first request focuses on presence; all subsequent risks do not belong in one development scope. See [07_Browser Demo Validation Goal](./01_Scout_EN/07_Browser_Demo_Validation_Goal.md) and [06_Next-Phase Decisions](./01_Scout_EN/06_Next_Phase_Decisions.md).

## 3. XR Feasibility Prototype — TRL 3–4

**Stage goal:** establish the technical baseline for RQ2 spatial presence first, then extend inputs and feedback for the separate RQ3 contact experiment. Review T1–T3 independently. The first round does not need every interaction, a complete product, or production-quality art.

**Confirm the target platform first:** before writing XR code or selecting asset formats, have Goertek XR engineers confirm the device model, operating system, recommended engine/SDK, deployment method, and available development resources. Create a one-page capability matrix covering at least:

- Eye tracking, head direction, hand skeletons, or controller inputs, and the data granularity available to the application.
- Plane/scene understanding, spatial anchoring, occlusion, persistence, and relocalization.
- Whether the application can coexist with other content or must use a closed single-app immersive mode.
- Permissions, user authorization, data restrictions, and fallback behavior for each capability.
- Recommended 3D asset formats, animation systems, rendering capability, performance budgets, and on-device debugging tools.

**Build the minimum Baobao next:** use existing PNGs as character references and create a low-complexity real-time model supported by the target engine. Prioritize silhouette, scale, position, and a few autonomous activities. Build only the movements needed for the first spatial experiment; add responses such as `sniff` and `nuzzle` as needed in the contact round. Six complete animation groups are not a prerequisite for the spatial experiment. Do not lock into USDZ, FBX, glTF, or authoring tools before platform confirmation.

**Extend the technical scope by experiment:**

- If the platform supports real-environment understanding, place Baobao on a table or floor and use its anchoring mechanism to check position, scale, and recovery on re-entry. Otherwise, record a core experience gap; a fixed position in a fully virtual scene cannot substitute for spatial-anchoring evidence.
- In the contact round, create one simple collision/trigger region on the forehead using supported hand or controller input. Interpret their evidence separately; a controller proxy does not establish real hand contact.
- The contact round may use sniffing, nuzzling, and settling to express Autonomous Activity → Awareness → Response / Optional Approach → Disengagement → Autonomous Activity. Animation names do not define a separate state model. Continue autonomous activity without invitations and enter Safe Pause according to 03 when tracking or input becomes unreliable.
- Record spatial drift, end-to-end response latency, false/missed triggers, animation interruption, recovery time, frame rate, and permission failures.
- Do not add mandatory feeding, check-ins, or care pressure. Long-term growth, multiple characters, multiple contact areas, complex navigation, and production-quality art are also outside this round.

“Baobao notices the user's gaze” remains an intended experience, not an assumption that the device exposes raw gaze data. Head direction, system focus events, or explicit confirmation must be labeled as proxies, with separate assessment of whether they support the experience.

**Exit criteria:** target-platform engineers have confirmed the capability matrix; the technical loop required by this round's main experiment is repeatable, failure modes are understood, and fallback is safe. Assess spatial and contact rounds separately; an unfinished contact round does not automatically fail the spatial round. If a capability essential to the current experience is missing, adjust the mechanism or platform first. Estimate device, engine, 3D, engineering, and research investment separately.

## 4. On-device Experience Validation — TRL 5–6

**Stage goal:** under real device and usage constraints, examine Level 1 presence and contact, then Level 2 companionship without obligations after positive presence signals. Report D1, D2, and U1 separately rather than making one prototype or aggregate score answer everything.

### A. Level 1 — Separate presence and contact rounds

- Compare 2D and spatial conditions with similar character, behavior, and duration, and balanced order. Examine whether position, scale, an approachable body, and spatially consistent responses create presence “right here.” Record device and input differences separately.
- Run a separate contact round comparing synchronized, delayed, and absent responses. Check whether users attribute Baobao's reaction to their hand movements. Contact is not a presumed prerequisite for companionship.
- Record when users perceive approach, contact, penetration, delay, or simply an animation trigger.
- Check direct contact's reachability, comfort, tracking stability, and Safe Pause.

This path can supply evidence about spatial position, inputs, and subjective contact. A closed single-app implementation cannot establish cross-app or multitasking coexistence.

### B. Level 2 — Relationships and companionship without obligations

- Focus the co-presence round first on Passive Presence Value (U1a/M5). Let Baobao accompany a short task and allow users to ignore, move, hide, or close him. Record active choices about his presence or absence and their reasons.
- Record Low-disruption Acceptance (M7) separately, checking obstruction, attention, and pressure to respond. Not closing the character or finding him unobtrusive is insufficient evidence of co-presence value.
- Collect neutral experience descriptions first, then explore feeling noticed, Perceived Autonomy (M2), and Companionship Value (M6) separately. “Am I disturbing him?” needs to be distinguished as a sense of agency or guilt, rather than immediately counted as success.
- Where needed, compare the presence or absence of recognition or autonomous activity while controlling other conditions. Record spatial/2D companionship gains independently of presence differences.
- Run repeated encounters as a separate round focused on U3 relationship continuity and voluntary return. Distinguish novelty from sustained value; do not add relationship decay or automatically treat infrequent use as failure.

The format depends on the capability matrix. If the platform supports app or spatial-content coexistence, test in those real conditions. Otherwise, record cross-app coexistence as a platform limitation and test low disruption in multitasking, overlays, or other representative contexts permitted by the device. Do not report substitute-context results as cross-app evidence.

This path can examine low disruption and coexistence tendencies, but controller input, system focus events, and other limited inputs cannot establish complete hand or eye tracking.

After positive signals at the preceding two levels, formally validate Level 3 access, wearing, repeated launch, and product-form choices under actual device conditions. Adoption risks may be recorded earlier, but stated interest is not an adoption conclusion.

**Evidence to record by level:** spatial stability, response latency, and recovery data; presence differences between spatial and browser/2D versions; synchronized feedback's contribution to contact; whether users still choose to keep Baobao when he can be ignored or closed without care obligations; and adoption barriers involving device access, wearing duration, privacy permissions, and operating modes.

**Exit criteria:** the experience is reproducible in representative environments; main assumptions have supported, refuted, or unresolved findings; the risk map covers technology, experience, users, resources, privacy/safety, and adoption; and the team can estimate the people, time, and cost required for a pilot.

## 5. Pitch & Pilot Gate — TRL 7

**Stage goal:** enable decision makers to judge whether a bounded real-world pilot merits investment, without claiming that all risks have disappeared.

**Work required:**

1. State the real problem, target user, and why now in one sentence.
2. Demonstrate the validated core loop live and specify its operating mode.
3. Use an evidence matrix to distinguish validated, refuted, unknown, and deferred questions.
4. Present the main technical, experience, privacy, adoption, and resource risks and their mitigations.
5. Define pilot users, context, duration, devices, success metrics, stopping conditions, and data handling.
6. Make a specific request for roles, devices, budget, timeline, owner, and the next decision date.

**Exit criteria:** a scoped Pilot Go, a return to the relevant stage for more evidence, or a No-go based on known risks. Presentation quality must not replace evidence, and the request must not be a vague appeal for “continued support.”

## 6. Productize & Launch — TRL 8–9

**Stage goal:** turn the validated research demo into a product that can be delivered reliably, maintained, and evaluated.

**Work required:**

- Engineer the code and character assets for production: performance budgets, resource loading, state persistence, version migration, crashes, and tracking recovery.
- Complete privacy minimization, permission explanations, data-retention rules, safety boundaries, and platform distribution/enterprise deployment requirements.
- Cover different spaces, lighting, seated/standing postures, hand conditions, accessibility needs, and extended wearing in QA.
- Define product metrics consistent with platform data boundaries. Unless capability, authorization, and necessity are confirmed, do not depend on raw gaze data. Prioritize explicit interactions, session retention, voluntary closure, repeated use, and recovery.
- Establish content and character-asset workflows so added actions do not break low-disruption principles or the state machine.
- Start with a limited pilot and expand gradually, reassessing experience value, technical cost, and adoption barriers at each expansion.

**Outcome decisions:**

- **Scale:** core value, reliability, and the resource model hold; expand users and contexts.
- **Iterate:** value exists but a specific element is insufficient; revise at the relevant stage and retest.
- **Stop:** user value, technical reliability, or the resource model cannot work within acceptable limits; stop further investment.

Launch is not the end of the roadmap. Continue monitoring novelty decay, repeated use, closing reasons, performance, and permission failures. Major features should re-enter the assumption → lowest-cost validation → evidence gate cycle.

## Long-term North Star and the current minimum experience

**Baobao's world ↔ Baobao travels ↔ User's digital world**: the Baobao App represents his world, like “visiting Baobao at home.” Other apps represent the user's digital world, which Baobao occasionally visits from his own. Visit format, value, and feasibility need research. A permanent overlay across every app is not the default.

For now, a few preset activities express that Baobao has his own life. A complete world, hunting, resources and items, cross-app runtime, complex AI, long-term growth, memory, and offline simulation are deferred candidates, not current MVP requirements. Mandatory feeding, hunger upkeep, check-ins, punishment, affection maintenance, relationship decay, and care debt conflict with product principles and must not be presented as features to add later. See [02_Product Thesis and Validation Framework](./01_Scout_EN/02_Product_Thesis_and_Validation_Framework.md) for scope definitions.
