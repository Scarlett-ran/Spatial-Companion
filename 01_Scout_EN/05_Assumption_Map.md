# Exploration 05 — Assumption Map

This document is the shared reference for assumptions, metrics, and evidence boundaries. D denotes design assumptions, U user or product assumptions, and T technical assumptions. Existing IDs are retained; D3, D4, U1a, and U5 add behavioral understanding, autonomy, passive co-presence, and user segmentation respectively.

## 1. Evidence status

The creative origin, personal Vision Pro experience, and practical conditions of pet ownership are starting points for exploration. The character and the constraints of low disruption and no care obligations are design choices. None automatically establishes user demand or experience effects. Concept video and documents exist; external user research, a browser interaction simulation, and target-device validation have not been completed.

“Unvalidated” means the relevant evidence is missing. “Deferred” means formal validation is not currently scheduled, not that the assumption is established. See [01_Problem Statement](./01_Problem_Statement.md) for the young-user framing and segments A/B/C, and [02_Product Thesis and Validation Framework](./02_Product_Thesis_and_Validation_Framework.md) for the three value levels and research sequence.

## 2. Design assumptions

| ID | Assumption to test | Current status | Evidence needed |
|---|---|---|---|
| D1 | Stable position, appropriate scale, an approachable body, and spatially consistent responses can make Baobao feel “right here.” Any presence gain over 2D is compared separately. | Unvalidated; the video expresses intent only. | On-device position, scale, and depth judgments; 2D/spatial comparisons with similar character and behavior, distinguishing spatial relationships from cuteness. |
| D2 | Visual and behavioral feedback can produce a credible subjective sense of contact without physical haptics. | Unvalidated; the video expresses intent only. | Action attribution after a real reach, descriptions of contact or penetration, and differences between synchronized, delayed, and absent responses. |
| D3 | Users can understand Baobao's behavior, input-response causality, and how interaction ends. | Unvalidated; the browser is the current primary validation medium. | Explanations of what just happened, differences between expectations and actual responses, misunderstandings, and guidance required, recorded by branch. |
| D4 | A few autonomous activities and natural transitions can initially make Baobao feel as though he has his own life. | Unvalidated; the browser can provide initial signals. | Spontaneous descriptions and attributions during non-interaction; distinguish autonomy, randomness, non-response, animation loops, and waiting for commands. Test sustained credibility separately. |

D3 legibility and D4 autonomy are different metrics. Responses to invitations should be explainable, while uninvited activities should have their own coherence. Attributing every behavior to clicking is insufficient evidence of autonomy; being unable to explain any behavior does not establish that the character “has a personality.”

## 3. User and product assumptions

| ID | Assumption to test | Current status | Evidence needed |
|---|---|---|---|
| U1 | Quiet co-presence, recognition, and autonomous responses can provide companionship without care obligations. | Unvalidated; browser feedback is directional only. | Specific co-presence contexts, experience descriptions, and reasons for keeping or closing the character; distinguish companionship, decoration, entertainment, and novelty. |
| U1a | Baobao's presence itself has value even without active interaction. | Formal validation belongs to the later co-presence stage. | Active choices to keep or hide him, reasons, and experience differences with and without him during non-interaction. Record stated intent separately. |
| U2a | Young users are willing to try the autonomous spatial companion concept. | Unvalidated. | Real contexts, existing alternatives, and reasons for trying or rejecting it; do not infer generation-wide acceptance or device adoption. |
| U2b | Companionship value is sufficient for users to accept actual XR device conditions and use the product. | Unvalidated; formal adoption research is deferred. | Actual access, wearing, launching, and repeated choices; distinguish already using a device from putting it on specifically for Baobao. |
| U3 | Relationship continuity without care obligations has value, and users still want to meet the same Baobao after novelty fades. | Deferred; no repeated-use evidence. | Relationship perceptions, voluntary return, and reasons for closing after repeated encounters; report continuity and usage frequency separately. |
| U4 | Coexisting with other applications is more valuable than appearing only in a standalone application. | Deferred; no comparison of product forms. | Value, disruption, and trade-offs during specific tasks, using conditions that match available platform capabilities. |
| U5 | Pet constraints, character attachment, or ambient-companionship preferences may explain differences in demand better than age. | Unvalidated; all three segments are candidates. | Recent real experiences, lifestyle, alternatives, and rejection reasons; record segment overlap, age, and device habits without selecting a “best segment” in advance. |

U1, U1a, and U3 address the relationship level. U2b, U4, and the sustained-use evidence within U3 address the product level. U2a and U5 can be investigated early; interest and demand signals do not replace evidence of effects.

## 4. Technical assumptions

| ID | Assumption to test | Minimum checks | Evidence boundary |
|---|---|---|---|
| T1 | Baobao can remain stably positioned at an appropriate scale in the user's space, with a credible position as the viewpoint changes. | Placement, approach, viewing from different angles, spatial position, and relocalization. | Unvalidated; target-device evidence is required. |
| T2 | Necessary invitations, approach, or contact can be detected and answered promptly under the target context and permissions. | Available inputs, precision, permissions, false/missed triggers, and end-to-end latency. | Unvalidated; record gaze, head direction, hand tracking, and controller proxies separately. |
| T3 | Five experience states and one safety state can be driven by rules to create a coherent encounter without complex AI. | Autonomous activity at entry, no interaction, invitations and responses, disengagement, pausing, and recovery. | Unvalidated; the browser checks simulated state logic only. Target-device runtime stability needs separate testing. |
| T4 | Baobao can coexist across apps and retain basic state between app switches or usage sessions. | Check coexistence conditions separately from saving/restoring state. | Deferred; saved state does not prove cross-app visibility, and the browser cannot validate this capability. |

D3 records whether people understand behavior; T3 records whether the rules run coherently. They cannot be collapsed into one “interaction success rate.” A platform providing a capability also does not mean this project has completed technical validation.

## 5. Core metrics and observation methods

These are project-specific metric definitions, not validated scales or agreed passing thresholds. In each round, record neutral observations and participants' own words before using direct questions to help interpret them.

| Metric | Related assumptions | Observation method | Applicable stage and limits |
|---|---|---|---|
| M1 — Interaction Legibility | D3; related to T3 | Ask users to explain what just happened and why. Record branches correctly explained without guidance, misunderstandings, and trigger timing. | Primary browser metric; applies only to the tested proxy input and prototype conditions. |
| M2 — Perceived Autonomy | D4; related to U1 | Start with “What was he doing when you weren't interacting, and how could you tell?” Record attributions to his own activity, waiting for commands, randomness, or malfunction. | Initial browser observations, revisited across later encounters; not evidence of background life or AI capability. |
| M3 — Spatial Presence | D1, T1 | Examine judgments and experience changes involving position, scale, depth, approach, and viewing from different angles. | On-device; 3D appearance, a visible body, and cuteness do not substitute for evidence. |
| M4 — Contact Credibility | D2, T2 | Record sensations and attribution during hand approach, contact, and withdrawal; compare synchronized, delayed, and absent responses. | A separate on-device experiment; subjective contact is not physical haptic feedback. |
| M5 — Passive Presence Value | U1a | While users do something else without active interaction, compare choices and reasons for keeping or hiding Baobao, and differences with and without him. | Formally assessed during co-presence research. Similar browser feedback is directional only. |
| M6 — Companionship Value | U1, later U3 | Neutrally record co-presence, mutual recognition, and reunion experiences; distinguish companionship, entertainment, decoration, and novelty. | Report short co-presence and repeated encounters separately. One moving experience does not establish long-term attachment. |
| M7 — Low-disruption Acceptance | U1; related to behavior constraints in 03 | Record interruptions, obstruction, pressure to respond, closing behavior, and reasons. | Browser work checks initial behavioral pressure; actual disruption needs on-device contexts. Being unobtrusive does not establish companionship value. |

Willingness to Keep Nearby provides attitude and choice evidence for M5 and is compared with disruption feedback under M7. It is not counted again as an independent value conclusion. Leaving the character enabled by default, forgetting to close it, or saying it is appealing cannot independently establish the value of actively keeping it nearby.

“Am I disturbing him?” may indicate a sense of agency, or guilt and burden; ask why. “He ignored me” may also reflect a malfunction or misunderstanding. Spontaneous references to Baobao's own activities can be clues, but these statements must not become leading questions or predefined successful answers.

## 6. Main risk per round and subsequent methods

| Research question | Main risk / assumptions | Method and interpretation boundary |
|---|---|---|
| RQ1 — Browser | Behavior is hard to understand: D3, T3; supporting D4. | Cover invitations, no invitation, withdrawal, and recovery; record M1, M2, and M7 by branch. Collect early directional feedback only for U1/U2a. |
| RQ2 — First device round | Spatial presence does not emerge: D1, T1. | Begin with stable scale, position, and approach. Where 2D/spatial comparisons are needed, keep character, behavior, and duration similar, balance order, and record device/input differences. |
| RQ3 — Contact experiment | Contact is not credible: D2, T2. | Start with one forehead region; compare synchronized, delayed, and absent responses. Check false triggers and recovery separately; contact failure does not invalidate the whole spatial concept. |
| RQ4a — Co-presence | No value outside active interaction: U1a, U1. | Let users complete a short task and freely keep, hide, or close the character. Where needed, compare presence/absence or one behavioral mechanism; interpret M5, M6, and M7 separately. |
| RQ4b — Repeated encounters | The relationship does not persist: U3, D4. | Later compare minimal relationship traces with reset conditions and observe voluntary return and relationship perceptions. Add no care pressure; infrequent use is not automatically failure. |
| RQ5 — Adoption | Value is insufficient to justify device conditions: U2b, U4. | Observe choices and trade-offs with actual devices and available product forms. Another browser click does not establish adoption. |
| Long-term research | Life and continuity across worlds are not credible: U3, U4, T4. | Defer assessment of the independent world and visits. Obtain separate evidence for coexistence, state persistence, and user value. |

Evidence records should include the assumption/metric, prototype version, input and operating conditions, sample characteristics, observations/participant quotes, supported/refuted/unresolved status, limitations, and next steps. Define success/failure thresholds before the relevant test. The execution plan still needs the specific sample, tasks, and duration. See [07_Browser Demo Validation Goal](./07_Browser_Demo_Validation_Goal.md) for the current task and [06_Next-Phase Decisions](./06_Next_Phase_Decisions.md) for stage decisions.
