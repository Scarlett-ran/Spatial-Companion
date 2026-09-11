# Autonomous Spatial Companion — Product Roadmap

This roadmap describes the conditions for moving from a solo concept exploration to on-device validation and, later, product development. The current path has two stages: I will first complete the Browser Demo independently; once it is mature enough to communicate the idea clearly, I will seek hardware access and external support. A pilot and productization are conditional future paths, not current commitments.

## 1. Product thesis and validation levels

**Baobao has a life of his own. Sometimes, that life intersects with yours.** The project explores whether an autonomous spatial companion can create meaningful companionship through quiet co-presence, mutual awareness, and lightweight interaction without care obligations.

| Level | Question | Primary evidence |
|---|---|---|
| Presence | Does Baobao feel present in the user's space? | Position, scale, depth, approach, and viewing from different angles on actual hardware. |
| Relationship | Does active and passive time with Baobao provide companionship without creating pressure? | Short co-presence, voluntary keep/hide choices, low-disruption feedback, and repeated encounters. |
| Product | Is that value strong enough to justify device conditions, repeated use, and a particular product form? | Actual access, wearing, launching, repeated choice, and form-factor trade-offs. |

The levels are assessed separately. Stronger spatial presence does not establish companionship or adoption, and contact credibility is its own question. The Browser Demo can test simulated logic and express the intended experience; it cannot provide spatial evidence.

## 2. Current status

Chinese and English exploration documents, character references, and an approximately 20-second concept video are available. The Browser Demo has not yet been built. There is no external user research or on-device evidence, and there is no commitment of hardware or engineering support. I am currently working independently in the Browser stage.

See [Interaction Experience Specification](./01_Scout_EN/03_Interaction_Experience_Specification.md), [Browser Demo Validation Goal](./01_Scout_EN/07_Browser_Demo_Validation_Goal.md), and [Next-Phase Decisions](./01_Scout_EN/06_Next_Phase_Decisions.md) for behavior, execution, and maturity criteria. Assumptions and metrics are maintained in the [Assumption Map](./01_Scout_EN/05_Assumption_Map.md).

## 3. Roadmap overview

| Stage | Core question | Work | Exit |
|---|---|---|---|
| **1. Browser** | Can the candidate behavior run reliably and become a clear demonstration and engineering reference? | Solo implementation, rule-based self-testing, presentation refinement, packaging, and feedback when practical. | The Demo is repeatable, core faults are addressed, and known limitations and minimum on-device questions are clear. |
| **2. On-device** | Can the target platform support credible spatial presence and, later, relationship and product value? | After obtaining hardware and necessary support, review the platform and study presence, co-presence, and adoption in separate rounds; contact is optional. | Spatial, experience, adoption, and resource evidence support a decision about a bounded pilot. |
| **Conditional future path** | Can validated value be delivered safely, reliably, and sustainably? | Pilot, engineering, QA, privacy, distribution, and operational validation. | Pilot Go/No-go, followed by Scale/Iterate/Stop decisions. |

Browser and on-device work are the two current progression stages. Research rounds within the on-device stage separate risks; they do not imply a commitment to build every capability at once.

## 4. Stage 1 — Browser Demo

### Goal

Independently build a repeatable interaction-logic prototype. Resting, observing, noticing, an invited response, and a natural ending express “separate lives, occasional encounters.” Hide, Close, Safe Pause, and recovery preserve user control and handle interruptions.

### Work sequence

| Sequence | Work | Completion signal |
|---|---|---|
| Sample | Review available assets and connect one input to one movement. | The chosen approach is feasible for a solo build. |
| Complete Demo | Implement both autonomous activities, simulated input, response, exit, and session controls. | The encounter runs from beginning to end. |
| Self-test and refine | Check trigger counts, repeated input, disengage, hide, close, and recovery; tune timing and transitions. | No known issue blocks the demonstration, and implementation matches the written rules. |
| Feedback and package | Invite participants when practical; organize the working version, recording, rules, observations, and limitations. | The package clearly separates what is complete from what requires on-device evidence. |

The Browser stage does not depend on external approval or a fixed number of participants. Self-testing can establish that the simulated logic runs; it cannot establish user understanding, companionship value, or spatial presence. If no participants are available, those assumptions remain unvalidated.

### Scope

The current build is a single-scene 2D character with two autonomous activities, mouse-based Look/Approach/Reach/Disengage proxies, and essential session controls. It excludes real hand or gaze tracking, spatial movement by the character, multiple contact zones, sound, a world or object system, complex AI, long-term growth, and cross-app behavior.

### Exit criteria

The Demo is ready to support an on-device request when:

1. Both autonomous activities and the complete interaction path run reliably and repeatedly.
2. The key rules—user stop takes priority, one invitation produces one response, and recovery does not continue old input—pass self-testing.
3. Motion and state changes feel coherent without manual workarounds or verbal explanations that hide faults.
4. A working version, short recording, behavior notes, known issues, and minimum device needs are ready.
5. Self-testing, personal judgment, and participant feedback are clearly separated, and unvalidated questions are not presented as findings.

If these conditions are not met, I may continue refining, redirect the mechanism, or hold the work. A mature Demo remains a completed Browser stage even if external support is not yet available. Waiting for hardware is not a reason to keep expanding the Browser scope.

## 5. Stage 2 — On-device validation

This stage starts only after hardware access and necessary support are available. The target device, operating system, engine/SDK, deployment route, permissions, accessible data, and collaborators will be confirmed at that point rather than presented as existing commitments.

### A. Platform review and spatial presence

The first round focuses on RQ2 and does not require contact or cross-app behavior:

- Confirm spatial placement, scale, environment understanding, occlusion, relocalization, and operating mode.
- Build a minimal character that can be placed, approached, and viewed from different angles, prioritizing silhouette, position, and a small autonomous activity set.
- Record drift, recovery, frame rate, permission failures, and other failure modes.
- Compare 2D and spatial versions when practical while separating differences in character, input, and hardware.

Browser simulation and a fixed position in a purely virtual scene cannot substitute for spatial-presence evidence. If the target platform lacks a core capability, revise the mechanism, experiment, or platform.

### B. Later research rounds

| Round | Entry condition | Main question |
|---|---|---|
| RQ3 — Contact | Suitable hand or controller input is available and the round is worth pursuing. | Can visual and behavioral feedback create credible subjective contact without physical haptics? |
| RQ4a — Passive co-presence | Spatial presence shows promise. | While doing something else, do users still choose to keep Baobao around without attention or care pressure? |
| RQ4b — Repeated encounters | Short-term co-presence shows value. | After novelty fades, do relationship experience and voluntary return persist? |
| RQ5 — Adoption and product form | Relationship value shows promise. | Will users accept the actual device conditions, and how should standalone and coexistence forms be weighed? |

Contact is not a prerequisite for co-presence. Cross-app coexistence, state persistence, and repeated use require separate evidence; a closed standalone test does not establish cross-app value. Each round addresses one main risk and records supported, challenged, or unresolved conclusions.

### Exit from on-device validation

Consider a bounded pilot only when the experience can be reproduced under representative conditions, key assumptions have appropriately scoped conclusions, and the team can estimate the required hardware, people, time, and cost. Insufficient evidence returns to the relevant round. Missing core capabilities, experience value, or acceptable resources may lead to a redirect or stop decision.

## 6. Conditional pilot and productization

A **pilot** is a small real-world trial used to decide whether the validated core experience justifies broader investment. Before it begins, define the participants, context, duration, devices, success and stop criteria, data handling, roles, budget, and next decision date.

Productization follows only if the pilot provides encouraging evidence. It includes performance and asset loading, state and version migration, failure recovery, privacy and permissions, accessibility, QA across different environments, distribution, and the content pipeline. After launch, continue monitoring novelty effects, repeat use, reasons for closing, and technical failures, then decide whether to Scale, Iterate, or Stop.

## 7. Evidence rules

1. Before each evaluation, define the primary assumption, lowest-cost method, observable evidence, and conclusions the result cannot support. Formal comparative studies also require thresholds set in advance.
2. Keep concept, behavior, experience, technical, and product evidence separate; no single metric substitutes for another level.
3. Label personal experience, self-testing, participant feedback, and target-platform data by source.
4. Limit conclusions to the actual prototype and conditions. Reassess earlier evidence after material changes to input, behavior, hardware, or tasks.
5. Character appeal, leaving the experience open, and stated interest do not independently establish companionship or adoption.

## 8. Long-term direction and fixed boundaries

The long-term direction is **Baobao's world ↔ Baobao visits ↔ the user's digital world**. The value and feasibility of visits, cross-app behavior, memory, and continuity depend on later evidence. Permanent presence across every app is not the default.

Mandatory feeding, hunger upkeep, check-ins, punishment, intimacy maintenance, relationship decay, and offline care debt conflict with the product thesis. A full world, objects, complex personality, growth, memory, and cross-app runtime remain later options rather than requirements for the Browser Demo or first on-device round.
