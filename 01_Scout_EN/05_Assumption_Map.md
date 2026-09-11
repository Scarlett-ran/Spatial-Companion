# Exploration 05 — Assumption Map

This chapter is the source of truth for assumptions, metrics, and evidence boundaries. D denotes design assumptions, U user/product assumptions, and T technical assumptions. There is currently no external user or on-device evidence. During the Browser stage I can self-test T3; D3, D4, and need-related assumptions require feedback from other people.

## 1. Assumptions and validation

Current Browser-stage assumptions:

| ID | Assumption | Evidence and impact |
|---|---|---|
| D3 | Users can understand behavioral causality and how an interaction ends. | Browser interpretations, predictions, and need for prompting; informs whether the behavior model is ready to carry forward. |
| T3 | The selected states can be driven by rules and produce a coherent encounter. | Repeatable normal branches, conflicting input, exit, and recovery; on-device stability remains separate. |
| D4 | A few autonomous activities can create an initial sense that Baobao has a life of his own. | Attribution during periods without input; diagnostic in this stage, with sustained credibility assessed later. |
| U2a | Younger adults are willing to try the idea of an autonomous spatial companion. | Specific situations, alternatives, and reasons to try or reject it; does not establish device adoption. |
| U5 | Pet constraints, character attachment, and preference for ambient companionship may explain demand better than age. | Early experiences and overlapping segment membership; identifying the strongest predictor requires later research. |

The priority audience and need questions are defined in [01 — Problem Statement](./01_Problem_Statement.md). The remaining assumptions require their corresponding conditions; Browser reactions are directional only.

| ID | Assumption | Evidence and impact |
|---|---|---|
| D1 | Stable position, credible scale, an approachable body, and spatially consistent responses create a sense that Baobao is “right here.” | Assess position, scale, depth, and approach separately on-device; informs the spatial presentation. |
| T1 | Baobao can maintain a stable position at a credible scale. | Placement, viewing from different angles, approach, and relocalization; assess each capability separately. |
| D2 | Visual and behavioral responses can create credible subjective contact without physical haptics. | Compare synchronized, delayed, and absent responses on-device; failure does not automatically invalidate non-contact co-presence. |
| T2 | Available input can detect invitation, approach, contact, and withdrawal in time. | Permissions, precision, false positives/negatives, and latency; report gaze, head pose, hands, and controller proxies separately. |
| U1 | Co-presence, awareness, and response without care obligations can create companionship value. | Concrete co-presence accounts and reasons to keep or close Baobao; distinguish companionship from decoration, entertainment, and novelty. |
| U1a | Baobao's presence has value without active interaction. | Voluntary keep/hide choices during another task and comparison with/without Baobao. |
| U3 | After novelty fades, people still want to encounter the same Baobao again. | Relationship experience, voluntary return, and reasons for closing across repeated encounters. |
| U4 | Coexistence with other apps is more valuable than a standalone experience. | Task-based comparison, disruption, and trade-offs under forms the platform actually supports. |
| U6 | Spatial presentation adds meaningful companionship value beyond a 2D character. | 2D/on-device comparison with similar character, behavior, and duration; separate this from spatial-presence ratings. |
| U2b | The value is strong enough to justify real device conditions and repeated use. | Access, wearing, launching, and repeated choice; distinguish existing device use from wearing a device specifically for Baobao. |
| T4 | Cross-app coexistence and state continuity are feasible on the platform. | Verify coexistence, persistence, and recovery separately; saved state does not prove cross-app visibility. |

## 2. Metrics and interpretation

| Metric | Assumptions | Observation and context |
|---|---|---|
| M1 — Interaction legibility | D3, T3 | Explanation, prediction, understanding of endings, and prompting required; primary Browser metric. |
| M2 — Perceived autonomy | D4 | Whether no-input behavior is read as self-directed activity, waiting, a loop, randomness, or failure; diagnostic only. |
| M3 — Spatial presence | D1, T1 | Position, scale, depth, approach, and viewing from different angles; on-device. |
| M4 — Contact credibility | D2, T2 | Reports of approach, contact, penetration, withdrawal, and causal attribution; separate on-device experiment. |
| M5 — Passive co-presence value | U1a | Voluntary keep/hide choices and reasons during another task; formal co-presence study. |
| M6 — Companionship value | U1, U3, U6 | Co-presence and reunion experience; report short-term, repeated-use, and 2D-versus-spatial findings separately. |
| M7 — Low-disruption acceptance | U1, behavior constraints | Attention pressure, obligation to respond, and reasons for closing; Browser can reveal behavioral pressure, while on-device work must also assess spatial obstruction. |

These are project metrics, not validated scales. Perceived autonomy does not independently determine whether to seek on-device support. If it also creates confusion, guilt, or pressure, record that under M1 or M7.

1. Users do not need to name internal states, but their interpretation should fit the observed behavior and support a reasonable prediction.
2. Choosing not to interact, missing the control, not understanding it, and experiencing input failure are different outcomes. Leaving the Demo open or saying the character is cute does not establish value.
3. Record standard instructions, extra prompts, prior video exposure, and repeat sessions separately. Prompted understanding is not unprompted understanding.
4. Mark observations affected by faults. Missing or uninterpretable evidence remains unresolved rather than being counted as success; multi-part assumptions may be partly supported and partly challenged.
5. Limit conclusions to the actual version, participants, and conditions. Reassess old evidence after a major change to inputs, behavior, or tasks.

## 3. Research rounds and dependencies

| Round | Main focus | Entry relationship |
|---|---|---|
| RQ1 — Browser | Self-test T3; collect D3, D4, and M7 feedback when participants are available. | Current independent build stage; need interviews happen when practical. |
| RQ2 — Spatial presence | D1, T1 / M3 | Seek support after the Demo is mature; begin after obtaining hardware and confirming capabilities. |
| RQ3 — Contact | D2, T2 / M4 | Optional separate round when suitable hand or controller input is available; not required before co-presence. |
| RQ4a — Co-presence | U1a, U1 / M5–M7; an appropriate comparison may inform U6. | May follow positive spatial-presence evidence without contact. |
| RQ4b — Repeated encounters | U3, D4 / M2, M6 | Follows promising short-term co-presence evidence. |
| RQ5 — Adoption and form | U2b, U4 | Follows promising relationship value under real device conditions. |
| Long-term world | U3, U4, T4 | Consider only if earlier evidence supports further investment. |

Every round records assumptions, version and operating conditions, actual participants, tasks and branches, prompts, events and quotes, supported/challenged/unresolved findings, and limitations. Self-tests are not user samples. Without participant feedback, user assumptions remain unvalidated, though a mature Demo may still be used to seek on-device support. See [07 — Browser Demo Validation Goal](./07_Browser_Demo_Validation_Goal.md) for the current work and [06 — Next-Phase Decisions](./06_Next_Phase_Decisions.md) for stage transitions.
