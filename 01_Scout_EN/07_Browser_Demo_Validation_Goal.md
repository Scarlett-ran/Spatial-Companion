# Exploration 07 — Browser Demo Validation Goal

This is the execution draft for Browser v0.1, an interaction-logic prototype and behavior reference. See [03 — Interaction Experience Specification](./03_Interaction_Experience_Specification.md) for behavior, [05 — Assumption Map](./05_Assumption_Map.md) for evidence, and [06 — Next-Phase Decisions](./06_Next_Phase_Decisions.md) for stage transitions.

## 1. Build scope

Use a single-scene, 2D character experience in a desktop browser. Build a small animation set from the existing character reference; do not require a real-time 3D model or spatial navigation. Before implementation, check for usable transparent character art and rest, observe, turn, sniff, and exit transitions. The concept video is not assumed to provide production-ready interactive assets. If assets are missing, account for that work and first test one input-to-motion sample.

| Item | Browser v0.1 choice |
|---|---|
| Activity and feedback | Two starting activities—resting and observing—plus a brief notice, one sniff response, and a natural exit. |
| Look | Toggle simulated attention. The control names the user's action without revealing an internal state or expected outcome. |
| Approach | Toggle far/near to simulate relative distance; Baobao does not move. |
| Reach | A single click sends one invitation without requiring a hold; it may trigger directly from autonomous activity. |
| Disengage | Explicitly withdraw the invitation and clear attention; remaining near does not automatically retrigger. |
| Session controls | Hide/Show, Close/Restart; page reload starts a new session. |
| Research controls | Configure the starting activity, reset the scene, simulate input failure/recovery, and export an event log; keep these controls out of the participant view. |

Do not implement real hand or gaze tracking, spatial approach by the character, multiple contact zones, sound, a world or object system, complex AI, growth, or cross-app behavior. Record the browser, window size, and input device; the first version supports mouse input only.

## 2. Build and self-test

| Required branch | Check |
|---|---|
| No interaction / no notice | Starting the session does not interrupt the activity. Look alone does not interrupt rest; sustained Look may trigger during observation. Doing nothing remains a complete path. |
| Uninvited notice | Approach or eligible Look triggers at most once. Repeated distance changes, Hide/Show, and pause/recovery do not reset the count. |
| Invitation, disengage, and reinvitation | Reach can trigger directly. Repeated clicks do not extend or queue a response. Disengage stops it; a new Reach may smoothly interrupt Exit. |
| Hide, close, and restart | Recovery never reveals a user-hidden character. Close requires Restart. A new session resets input and counts. |
| Interruption and recovery | Page blur, backgrounding, or simulated failure enters Safe Pause. Repeated failure does not replay old input; ongoing failure remains paused; recovery waits for new input. |
| No input versus failure | No user input continues autonomous activity. Only confirmed input failure enters Safe Pause. |
| Session and count | Initial load, reload, or Restart creates a new session and resets Notice. Hide/Show, page switching, and pause/recovery do not. |

When inputs arrive together, process them in this order: Close/Hide, Safe Pause, Disengage, Reach, Approach, then Look. Turning Look off does not cancel an active Reach; Disengage clears Look and the current invitation. If the user disengages while still near, they must move far and approach again before Notice can retrigger, and the once-per-session limit still applies.

Normal input is ignored while hidden, closed, or safely paused. Show returns Baobao to autonomous activity unless the system is still unreliable. Recovery clears simulated attention and proximity, so recovery itself is never treated as a new approach.

## 3. Feedback when participants are available

First complete a stable version, then collect feedback from people I can reasonably reach. No fixed sample is required. Invite people matching the audience in 01 when possible and record overlapping segments and device familiarity. Participation does not imply engineering or organizational support. If nobody is available, continue self-testing and leave user understanding and need assumptions unvalidated.

A roughly 25-minute session can be used to find concrete problems; it does not estimate population-level rates.

| Part | Suggested time | Task and record |
|---|---|---|
| Context interview | 5 min | Before showing Baobao, ask about a recent time alone, what the person used, and what worked or was missing. “No need” is a valid response. |
| Free exploration | 3 min | Do not show the video or explain behavior rules. Allow no interaction; record control discovery and spontaneous interpretation. |
| Branch tasks | 10 min | Explain only what each control simulates. In both activities, observe for about 45 seconds before trying Look, Approach, Reach, Disengage, and reinvitation. |
| Neutral review | 5 min | Ask what happened, why, what another action would do, when they wanted to stop, and whether they felt pressure; relate it back to the earlier context. |
| Video and concept feedback | 2 min | Show the video last. Record interest and expectations separately from prior behavior understanding. |

With multiple participants, alternate the order of resting and observing; use a new session for each activity. I will create opportunities to experience the key branches without explaining the expected response. Record free exploration, understanding after standard control instructions, and performance after extra prompting separately.

Choosing not to interact is valid. A branch left incomplete after the participant declines remains missing rather than being forced. Hide and recovery are primarily self-tested. Mark feedback affected by a real fault and repeat only when useful.

## 4. Solo work plan and outputs

I am responsible for design, asset preparation, implementation, self-testing, feedback notes, and iteration during the Browser stage. Work proceeds as time allows. Each pass addresses a defined problem; once the maturity criteria in 06 are met, package the result instead of expanding the scope while waiting for external support.

| Sequence | Work | Checkpoint |
|---|---|---|
| Prepare and sample | Review assets and implement one input-to-motion sequence. | Confirm the approach is feasible for a solo build and record any necessary simplification. |
| Complete Demo | Connect both activities, interaction, exit, and session controls. | The core encounter can be demonstrated end to end. |
| Self-test and refine | Run the checks above and refine timing and transitions; collect feedback when practical. | Core faults are resolved and known limitations are clear. |
| Package | Save a working version, record the Demo, and organize behavior notes, self-tests, and available feedback. | Use 06 to decide whether to seek on-device support. |

After each work session, note the current version, completed items, main issue, and next action. Keep participant feedback separate from self-testing. Retest affected branches after changing a core input or behavior. The first-version schedule and iteration pace depend on my actual availability.

## 5. Reference for later on-device discussions

| Capability | Use and question | Priority |
|---|---|---|
| Spatial placement, scale, and rendering | Placement, viewing from different angles, approach, relocalization, and stability under the actual operating mode. | Required for the first RQ2 round. |
| Attention and relative approach input | Support Look/Approach; determine whether gaze is exposed and whether head pose or system focus can serve as a proxy. | Review as needed, not a requirement for every part of the first round. |
| Hand/controller input and feedback | Support Reach, contact, and withdrawal; assess precision, occlusion, false triggers, and latency. | Extension for the RQ3 contact round. |
| Lifecycle, coexistence, and persistence | Distinguish interruption recovery, cross-app visibility, and state continuity. | Review interruption first; defer cross-app and persistence. |

Device, engine, permissions, and deployment must be confirmed on the actual platform. Browser evidence applies only to the simulated input; if on-device input changes the causal structure, behavior understanding must be revisited.
