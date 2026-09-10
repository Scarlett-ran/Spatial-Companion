# Exploration Phase 02 — Assumption Map

## 1. Known Facts and Established Design Decisions

| Category | Content | Boundary |
|---|---|---|
| Real-world conditions | Real pet ownership requires an ongoing commitment of time, energy, money, and responsibility, and is constrained by housing conditions and the practical limits of keeping particular species. | This does not mean the strength of the target audience’s need has been confirmed. |
| Existing alternative | 2D virtual pets do not depend on real animals; the character is presented within a screen-based interface. | This does not mean that 2D pets have no companionship value, nor does it prove that 3D is better. |
| Personal experience | When I tried Vision Pro, I experienced virtual content as located in physical space and had a sensation close to “touch.” | This is a personal experience and cannot be generalized into a user conclusion or treated as physical haptics. |
| Current output | A 20-second concept demo has been created; no external user research, browser-based simulation, or on-device XR prototype has been completed. | For reference only. |
| Established character | Use Baobao. | The character has been fixed and is no longer treated as an assumption to validate. |
| Established constraints | Low disruption; no feeding, check-ins, punishment, or long-term care obligations. | These are solution requirements and do not mean that users have accepted this type of experience. |
| Target audience definition | Gen Z and younger users. | This defines the research audience; it is not validated evidence of acceptance. |

## 2. Design Assumptions: Whether Presentation and Feedback Produce the Intended Experience

| ID | Assumption | Current evidence status | Evidence required |
|---|---|---|---|
| D1 | With comparable characters and behaviors, a spatial presentation with three-dimensional scale, a stable position, and an approachable body creates a stronger sense of embodiment than a 2D presentation. | The video communicates the intent of spatial presentation, but there has been no experiential comparison between 2D and spatial presentation. | Descriptions of the sense of embodiment, the specific basis for participants’ judgments, and contrary feedback from the comparison; spatial relationships must be distinguished from the character’s cuteness. |
| D2 | In the absence of physical haptic feedback, visual and behavioral feedback can still create a credible subjective sense of contact. | The video illustrates the intended touch response. | Descriptions after actually reaching out to interact, whether the response is attributed to the participant’s own action, and how the experience differs when feedback is incoherent. |

## 3. User Assumptions: Whether the Concept Is Needed and Accepted

| ID | Assumption | Current evidence status | Evidence required |
|---|---|---|---|
| U1 | A spatial pet with no long-term care obligations can still provide companionship value through quiet coexistence and lightweight responses. | Unvalidated; the demo is insufficient to distinguish companionship from decoration or novelty. | Specific usage contexts, reasons for keeping or intentionally closing the pet, and understanding of the no-care design; recording only “cute” or “I like it” is insufficient. |
| U2 | Gen Z and younger users are willing to accept this type of spatial pet and the device conditions it requires. | Unvalidated. | Real-world barriers to pet ownership, existing alternatives, reasons to try or reject the concept, and how device conditions affect the choice. |
| U3 | After the novelty wears off, users will still want to see the same Baobao again. | Deferred; there is no evidence from repeated use. | Voluntary return, keep-or-close behavior, and the reasons behind these actions after multiple uses. |
| U4 | Coexisting with other apps is more valuable than appearing only in a standalone pet app. | Deferred; there has been no comparison across contexts. | Needs and tradeoffs within specific tasks, and the incremental value or disruption created by coexistence. |

U1 examines whether the low-care concept has value; U2 examines whether the target audience is willing to adopt it. Neither can substitute for the other. U3 and U4 also cannot be inferred from a single round of concept feedback.

## 4. Technical Assumptions: Whether the Intended Experience Can Operate

Foundational platform capabilities provide only candidate implementation paths; they do not prove this project is feasible. None of the following capabilities has been validated on-device for this project, and the available input methods and operating conditions also need to be reviewed.

| ID | Assumption | Minimum scope of testing | Validation boundary |
|---|---|---|---|
| T1 | Baobao can remain stably positioned in the user’s space at an appropriate scale and maintain a credible position as the viewpoint changes. | Placement, approach, viewing from different angles, and positional stability. | Must be tested on-device. |
| T2 | Under the input and permission conditions available in the target operating context, the system can detect the necessary invitations and the hand’s approach or contact, then respond promptly. | Available input, permissions, contact detection, false triggers, and feedback latency; the availability of gaze input must be reviewed separately. | Do not assume that the app can directly access gaze data; specific inputs and feedback timing require on-device validation. |
| T3 | Five rule-driven experience states and one safety state are sufficient to create a coherent loop without complex AI. | Entry, response, natural exit, and pause-and-resume behavior under uncertain input or tracking anomalies. | A browser simulation tests rules only; tracking anomalies and runtime stability must be validated on-device. |
| T4 | Baobao can coexist with other apps and maintain basic state across app switches or separate usage sessions. | Test coexistence conditions separately from state persistence and restoration. | Deferred; the two capabilities must be documented separately, and state persistence cannot be used as evidence of cross-app visibility. |

## 5. Validation Priorities and Disposition

The current Browser stage prioritizes whether the rules and interaction causality within T3 are legible in a browser, while gathering early directional signals for U1 and U2. This does not validate T3 in full, companionship value, or target-audience acceptance. D2 remains the first experience objective for on-device validation; D1 and T1–T2 also require their own on-device evidence. U3, U4, and T4 are deferred.
