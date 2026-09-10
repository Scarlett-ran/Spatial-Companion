# Exploration 07 — Browser Demo Validation Goal

Browser work is the current direction, formally defined as an **Interaction Logic Prototype / Baobao Behaviour & Interaction Reference**. It has not yet been built or tested. This document defines the planned work; scope, sample, and thresholds need to be set before starting.

## 1. Two purposes, one main research question

The research purpose is to examine whether users understand why Baobao behaves as he does, and whether inputs, state transitions, and endings are coherent. The core question is “How do you understand what just happened?” A companionship score is not the primary passing criterion. Initial perceived autonomy and attention burden support diagnosis; concept interest and companionship feedback provide directional signals only.

The engineering purpose is to translate experience intent into concrete behavior, input, and output requirements: how Scout would use a capability if the real device provides it, and which conditions still need review. Browser and the existing concept video form Vision + Logic: the video expresses the intended feeling, while the prototype explains the intended operation. See [04_Concept Demo](./04_Concept_Demo.md) for responsibilities.

## 2. Minimum experience and interaction causality

Use [03_Interaction Experience Specification](./03_Interaction_Experience_Specification.md) as the behavioral basis. Include at least resting and one non-sleeping autonomous activity, plus interaction, unnoticed-user, and no-interaction branches. Baobao is already active when the user enters and resumes his own activity afterward. Completing a fixed contact sequence is not necessary for a valid experience.

| Proxy for user intent | Candidate behavior | Main check |
|---|---|---|
| Look: hover or focus | Briefly notice when conditions are met, or continue the current activity. | Can users understand a response or lack of one without interpreting the system as random or broken? |
| Approach: simulated movement closer | Respond subtly while maintaining a natural distance. | Is the timing relationship between approach and response legible? |
| Reach: simulated reach or contact | Sniff, accept contact, or approach slightly after an explicit invitation. | Are approach, contact, and response clearly distinguished? A click must not be treated as an actual hand capability. |
| Disengage: withdraw the proxy input | End after a brief response and return to independent activity. | Does the ending feel natural, or does the user think something else is required? |
| No invitation | Continue autonomous activity without constantly facing the user or soliciting a response. | Does the character have his own rhythm, and does non-interaction create attention pressure? |

Select the specific proxies in the Demo Scope. A few controls can represent hover, pointer interaction, and simulated distance, without full navigation or a complex life system. Multiple characters, multiple contact regions, an item system, complex conversation, AI personality, cross-app implementation, and long-term growth are outside this round. Product principles and scope categories are defined in 02.

## 3. From browser proxies to device requirements

The following mappings need engineering confirmation. They are neither established target-device capabilities nor a commitment to obtain all six at once.

| Browser simulation | Desired device capability | Interaction it supports | Questions or alternatives to check |
|---|---|---|---|
| Cursor hover / focus | Gaze or another available attention input | Notice user attention and decide whether to respond. | Gaze access and data granularity; head direction, system focus, or explicit confirmation must be labeled as proxies. |
| Cursor / simulated movement | Relative head or body approach information | Respond subtly as the user moves closer. | Tracked objects, reference coordinates, and distance precision; head pose does not establish full-body tracking. |
| Mouse press / pointer interaction | Detection of hand approach, reaching, or contact | Sniff, accept touch, and stop responding after withdrawal. | Hand data, precision, occlusion, and permissions; controllers are a possible alternative, with experience evidence interpreted separately. |
| Simulated depth | Spatial distance, environment understanding, and stable positioning | Maintain scale, distance, and spatial relationships. | Coordinates, planes, anchors, relocalization, and occlusion; simulated depth does not establish real depth perception. |
| Animation feedback | Real-time visual and behavioral feedback | Align bodily responses with input. | Animation system, performance, and end-to-end latency; physical haptics are not assumed. |
| Browser state machine | Behavior logic on the target runtime | Autonomous activity, response, disengagement, pausing, and recovery. | Lifecycle, interruptions, operating modes, and performance; saved state does not establish cross-app coexistence. |

Structure the engineering handoff as “capability X → interaction Y → validation question Z,” distinguishing essential capabilities for the first presence experiment from optional extensions for later contact experiments. The device model, engine, SDK, permissions, deployment conditions, and engineering support all need actual confirmation.

## 4. What this round can and cannot validate

| Evidence the browser can provide | Questions requiring the corresponding real conditions |
|---|---|
| Simulated state logic, behavioral causality, and basic comprehension | Real spatial presence, bodily scale, depth perception, and spatial approachability |
| Timing, state transitions, and natural endings under proxy input | Actual gaze behavior, real hand tracking, and end-to-end response timing |
| Initial understanding of a few autonomous activities | Credible subjective contact without physical haptics, sustained autonomy, and relationship continuity |
| Directional feedback on the character concept, low disruption, and co-presence | Real spatial coexistence, cross-app feasibility, target-device runtime stability, and actual adoption |

Smooth browser operation demonstrates only that the current simulation runs. Finding the character cute or wanting another click does not establish spatial, companionship, or adoption outcomes. Real-device access is necessary to obtain the remaining spatial evidence, but appropriate prototypes, tasks, and tests are still required within the target capabilities.

## 5. Test observations

Metric definitions are maintained in [05_Assumption Map](./05_Assumption_Map.md). Start with free observation and neutral follow-up questions before asking about specific feelings. To examine unprompted behavioral understanding, let participants try the browser before watching the concept video, or record viewing order separately, so the video does not supply the answers in advance.

| Observation | Recording method | Role in the decision |
|---|---|---|
| Behavior and causality understanding (M1) | Ask “What just happened, and why do you think it happened?” Record whether the explanation matches the actual state, prompts needed, and misunderstood branches. | The primary research evidence for this round. |
| State transitions and timing (M1/T3) | Record triggers, feedback, withdrawal, interruptions, and recovery, including when users perceive responses as early, late, or incoherent. | Distinguish implementation failures from comprehension problems; do not extrapolate to device latency. |
| Initial perceived autonomy (M2) | Observe spontaneous descriptions without input and ask “What is he doing, and how can you tell?” Distinguish independent activity, waiting, randomness, and non-response. | Supports changes to behavioral expression; does not establish sustained companionship. |
| Natural endings and attention pressure (M1/M7) | After an invitation ends, observe continued demands for input, repeated attention, closing, or a perceived obligation to continue. | Check that a few behaviors do not introduce extra demands. |
| Concept and co-presence feedback (U1/U2a, directional M5) | Record voluntary repetition, keeping/closing, and specific reasons; separate attitudes from actions. | Exploratory signals, not replacements for the main metrics or an independent gate into device work. |

Choosing not to interact is not an interaction failure. Forgetting to close the character is not an active choice to keep him nearby. “Am I disturbing him?” may signal burden. There is no need to lead users into saying he “has a life of his own” to establish autonomy.

## 6. Execution and deliverables

1. **Confirm scope and investment:** Select activities, branches, proxies, an owner, and an effort cap. Do not add features because of the long-term vision.
2. **Complete the test plan:** Specify the sample and recruitment criteria, tasks, duration, observation method, viewing order, and preset pass/revise/stop criteria.
3. **Build and verify:** Make input, feedback, endings, re-entry, and simulated exceptions repeatable.
4. **Test and attribute:** Collect unprompted explanations, actions, participant quotes, and contradictory feedback; separate implementation failures, behavioral misunderstandings, and experience judgments.
5. **Deliver evidence and engineering references:** Submit the video and prototype, state and branch tables, input/output mappings, timing and recovery notes, observations, capabilities needing confirmation, and a minimal device-resource request.

Sample size, numerical thresholds, precise feedback durations, and specific device permissions have not been determined. This document must not be treated as an executed Test Plan. See [06_Next-Phase Decisions](./06_Next_Phase_Decisions.md) for completion criteria and the rationale for device access.
