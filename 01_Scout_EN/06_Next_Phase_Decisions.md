# Exploration 06 — Next-Phase Decisions

The browser interaction logic prototype is the current direction. This document explains how to start the round, assess its results, and determine what evidence supports a request for real devices. See [07_Browser Demo Validation Goal](./07_Browser_Demo_Validation_Goal.md) for the specific work.

## 1. Success criterion for the current exploration

The aim is to determine **whether Baobao's behavioral model is understandable, coherent, and initially autonomous enough to justify testing spatial presence on a real device.** It should also produce a concrete behavior and capability reference so engineering can assess what is needed next.

This does not require proof of long-term companionship, purchase intent, sustained use, or the viability of the entire product. Distinguish two milestones: completing Scout documents and scope makes browser validation ready to arrange; completing actual browser testing makes a conclusion about the behavioral model possible. The project is still preparing for the first milestone and has no browser test results.

## 2. What must be completed before browser work starts?

| Area | Existing basis | Still to confirm |
|---|---|---|
| Questions and metrics | The main question is behavioral understanding and coherence; autonomy and attention burden are supporting observations. | Select specific observations and branches for this round using 05 and 07. |
| Prototype scope | A few autonomous activities, interaction and no-interaction paths, proxy inputs, and natural endings. | Activities, input mappings, feedback durations, implementation effort, and verification arrangements. |
| Research plan | Three candidate user segments and evidence boundaries are defined. | Sample size, recruitment criteria, tasks, duration, viewing order, and recording method. |
| Decision criteria | Research results and engineering references are separate deliverables. | Observable pass/revise/stop thresholds, set before testing, with contradictory feedback and unresolved findings retained. |
| Resources and ownership | Browser work is the current direction. | Mentor confirmation of scope and investment, execution owner, schedule, effort cap, and review date. |

A defined direction does not mean internal resources are approved. There is no commitment of devices or engineering support; unresolved details must not be written as settled facts.

## 3. How will browser results justify continuing?

| Assessment dimension | Evidence to submit | What to assess |
|---|---|---|
| Understandable, coherent behavior | User explanations, misunderstandings, prompts required, states, and timing, organized by branch. | Users understand responses to invitations and natural endings; implementation failures can be distinguished from behavior-design problems. |
| Initial autonomy and low disruption | Descriptions during non-interaction, behavioral attribution, attention pressure, and ending feedback. | Do not misclassify randomness, non-response, or guilt as autonomy; identify remaining adjustments. |
| A usable engineering reference | Video + Browser, states and branches, inputs/outputs, timing, recovery notes, and capability mappings. | Engineering can discuss specific inputs, permissions, operating conditions, and a minimal experiment rather than just a character concept. |
| Clear remaining risks | A list of examined, unresolved, and browser-inaccessible questions. | Identify what can still be corrected in the browser and what requires real hardware. |

These are dimensions of completion criteria, not passed results. Numerical thresholds and acceptable issue limits need to be set before testing in light of the sample and tasks. Concept appeal, another click, or stated willingness to coexist are supporting information; they do not replace the main judgments or independently decide entry into on-device work.

## 4. Why does the next set of questions require a real device?

The request must follow the evidence: first report which browser-testable risks this round reduced, then explain why proxy inputs cannot provide valid evidence for the remaining core questions. No testing has occurred yet, so risk reduction cannot be claimed in advance.

Real spatial presence, bodily scale, depth, actual gaze and hand inputs, subjective contact, spatial coexistence, and target-runtime stability all require appropriate device conditions. **Device access is necessary to obtain the next set of spatial evidence. The request exists to answer those questions, not simply to create a more polished demo.** Capabilities, permissions, and prototype conditions must still be reviewed after access is granted.

The first device request should prioritize RQ2: confirm the target platform, establish stable scale and position, and examine spatial presence while approaching and viewing from different angles. Real contact belongs to a later, separate experiment. Full gaze access, hand inputs, and cross-app capability are not all required in the first round. Platform discussions can begin early; cross-app implementation remains deferred.

The request should specify the minimum research question, required device and capabilities, permissions and deployment requirements, engineering roles, effort and duration, expected evidence, and stopping conditions. Concrete details need confirmation with engineering. The full list of questions the browser cannot validate defines the boundary of later research, not the development scope of a single request.

## 5. Decisions and records

| Outcome | Next action | Conclusion boundary |
|---|---|---|
| Go — Request limited on-device resources | Once the behavioral model and reference meet the preset conditions, submit a scoped request for device access and engineering support. | No automatic approval; spatial presence, contact, and product value are not established. |
| Iterate — Revise the browser prototype | Correct and recheck identifiable problems in understanding, timing, or autonomy. | Missing device evidence is not a reason to keep adding features that the browser cannot validate. |
| Redirect — Adjust the method or mechanism | Use new evidence to record changes needed in the question, input, or validation conditions. | Retain the browser's dual purpose; changing one experiment does not cancel the overall direction. |
| Stop / Hold — Stop or pause investment | State the reason in terms of resources, the behavioral model, or research conditions. | Applies to the current investment or mechanism, not proof that every spatial-companion assumption is false. |

Record the date, decision maker, prototype and sample conditions, observations/participant quotes, assumption conclusions, limitations, resource request, and next steps. There are no test or Mentor resource-decision records for this round yet. See the [Product Roadmap](../00_Product_Roadmap.md) for later stages.
