# Exploration 03 — Interaction Experience Specification

This document translates the relationship of “separate lives, occasional encounters” in [02_Product Thesis and Validation Framework](./02_Product_Thesis_and_Validation_Framework.md) into candidate behavior. These rules have not been implemented. Browser work currently serves as the interaction reference; real spatial conditions and inputs require separate validation.

## 1. Express autonomy through a few behaviors

The design principle is **Less interaction, more meaning per interaction.** Baobao is already doing something when the user enters. He may notice the user or continue his activity. An invitation can lead to a response or a small approach, after which he naturally resumes his own activity. An encounter without interaction is also a complete path.

`Autonomous Activity → Optional Awareness → Optional Response / Approach → Disengagement → Autonomous Activity`

Autonomous activity and responses to the user need separate design: the former follows its own rhythm, while the latter makes the connection between invitation and feedback understandable. Autonomy does not mean randomness or malfunction, and legibility does not require instant obedience to every click. Rules and a few preset variations can express a sense of agency without a complete AI personality or a life simulation running in the background.

| Behavioral expression | Treatment in this round |
|---|---|
| Activity already in progress at entry | Required. Start partway through resting or a non-sleeping activity rather than always waiting for the user to wake him. |
| Not always facing the user | A no-invitation branch is required. He may continue observing the environment; arrival does not force an immediate turn toward the user. |
| Looking, approaching, and reaching | Under defined conditions, he may briefly notice, respond subtly, or accept contact. These are candidate input intentions, not a fixed sequence that must trigger every time. |
| The user leaves or withdraws | End after a brief acknowledgment, without following or requiring a goodbye, and return to his own activity. |
| Playing with an object, changing position, or bringing something back | Candidate examples of autonomy only. Observing from a fixed position can supply the current non-sleeping activity; navigation, an item system, and hunting are not required. |

Gaze, approach, and touch describe intended experiences. Target-platform inputs, precision, and permissions remain unknown, and direct access to gaze data is not assumed. See 07 for browser proxy mappings. Feedback durations and trigger thresholds need to be defined in the test plan; words such as “subtle” and “brief” are not confirmed parameters.

## 2. Five experience states and one safety state

| State | Experience purpose | Entry condition | Allowed behavior | Exit |
|---|---|---|---|---|
| Autonomous Activity | Show that Baobao has his own life without user input. | Session starts or interaction ends; select an activity already in progress at entry. | Resting, just waking, observing the environment, or gentle self-directed play; include at least resting and one non-sleeping variation. | Continue the activity or briefly notice the user; do not automatically turn toward the user at launch. |
| Awareness | Express limited awareness without demanding a response. | Sustained gaze or deliberate approach. Without an invitation, the first reliable detection of entry into proximity may trigger at most one brief acknowledgment per session; no acknowledgment is also allowed. | Turn his head, open his eyes, raise his head slightly, or briefly observe. | Move to Response if the invitation continues; otherwise return to Autonomous Activity. |
| Response | Acknowledge deliberate user action. | The user reaches, lightly touches, or continues approaching. | Watch the hand, sniff, nuzzle, or accept brief stroking. | May continue briefly while invited; otherwise move to Disengagement. |
| Optional Approach | Offer a clearer interaction moment without imposing it. | An explicit invitation with reliable spatial and input conditions. | Make a small position adjustment, maintain a safe distance, and avoid obstructing primary content. | Stop approaching when ignored and move to Disengagement. |
| Disengagement | Clearly end an interaction. | The user looks away, withdraws their hand, or resumes their main activity. | Reduce movement, shift attention away, and settle again. | Return to Autonomous Activity. |
| Safe Pause | Avoid incorrect, abrupt, or unsafe spatial behavior. | Tracking loss, uncertain input, insufficient space, or an application interruption. | Stop movement and interaction. Hide the character when position cannot be maintained reliably; continued visibility is not required during an application interruption. | Return to Autonomous Activity once conditions are reliable; otherwise remain paused. |

## 3. Hand actions and Baobao's responses

| User action | Intended response | Disallowed response |
|---|---|---|
| Hand approaches slowly | Stay in place, track the hand with his eyes, tilt his head slightly, and sniff once when safe. | Lunge at the hand, jump instantly closer, or repeatedly seek attention. |
| Light touch on the forehead or cheek | Relax his expression, close his eyes slightly, or gently nuzzle the fingers. | Exaggerated bouncing or forcing a prolonged interaction. |
| Brief, gentle stroking | Maintain a stable posture and respond through breathing, expression, and small body movements. | Hold the user, prevent the hand from leaving, or demand repeated input. |
| A fast reach or sudden approach | Recoil slightly or pause while maintaining a safe distance. | Attack, punish the user, or sustain negative emotion. |
| Hand withdraws | Stop responding and gradually return to autonomous activity after a brief look. | Follow, repeatedly approach, or vocalize demands to continue. |

Hand contact refers only to a future simulation of contact through visual, animation, and sound feedback. It does not imply that the device provides physical haptics.

## 4. Low-disruption rules

1. Quiet coexistence is a valid state, not an empty interval waiting for user input.
2. Without an invitation, Baobao may transition from Autonomous Activity to user-directed Awareness at most once per session, without escalating intensity. This does not restrict quiet spontaneous activity.
3. Baobao must not frequently enter central vision, obstruct primary content, or repeat sounds.
4. Ignoring him must not cause punishment, negative emotion, lost progress, or stronger reminders.
5. Continuous gestures or conversation are not required. Care-obligation rules are defined below.
6. Do not continuously listen to the environment, infer the user's emotions, or read other applications' content.

## 5. Rules for no care obligations

| Constraint | Behavioral requirement |
|---|---|
| No feeding | No hunger, thirst, or resource meters requiring replenishment; feeding must not maintain health, survival, or closeness. |
| No check-ins | No daily tasks, login-streak rewards, or mandatory periodic returns. |
| No punishment | Ignoring, leaving, or closing the experience must not cause weakness, illness, death, relationship decline, lost progress, or guilt-based reminders. |
| No long-term care obligations | No mandatory cleaning, medical, or growth-related upkeep. No tasks accumulate while offline, and returning requires no catch-up care. |

Users may end interaction, hide Baobao, or close the experience at any time without a goodbye action or a promise to return. His rest and recovery do not depend on user care. Any future state persistence must not introduce offline depletion or care debt. These rules define a relationship that is not maintained through care; co-presence and companionship value still need validation under U1 and U1a.

## 6. Natural-ending rules

- Withdrawing a hand, looking away, or resuming the main activity ends the invitation.
- After one brief response, Baobao should reduce activity rather than ask again or approach again.
- Disengagement should move from response to a settled posture without an abrupt freeze or a looping goodbye animation.
- Resume quiet activity with continuous position and scale.
- Uncertain input or tracking takes priority through Safe Pause rather than guessing user intent.

## 7. Implementation scope and validation links

This round uses a few activities, states, and responses to express one encounter. It does not add feeding, hunger upkeep, check-ins, affection meters, punishment, or care debt. Complex conversation, a full personality, long-term growth, a complete world, items, and cross-app systems are also outside this round. See 02 for the distinction between prohibited mechanisms and deferred candidates.

The hand-action table describes possible responses; it does not require multiple contact areas in this round. The first later on-device contact experiment starts with one forehead region. Observing in place is sufficient as a non-sleeping autonomous activity, with no need for items or spatial movement. If Optional Approach is retained, it represents only a small adjustment under an explicit invitation and reliable conditions.

D3/M1 examine behavioral legibility, and D4/M2 examine initial perceived autonomy. Low disruption and passive presence value are recorded separately and cannot substitute for one another. See [05_Assumption Map](./05_Assumption_Map.md) for metrics, [07_Browser Demo Validation Goal](./07_Browser_Demo_Validation_Goal.md) for browser scope, and [04_Concept Demo](./04_Concept_Demo.md) for the coverage of existing work.
