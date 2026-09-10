# Exploration Phase 05 — Interaction Experience Specification

## 1. Core Experience

| Problem or constraint | Candidate solution response | Related assumption or boundary |
|---|---|---|
| Practical constraints and burden of responsibility associated with real pet ownership | Use the established virtual character, Baobao; no feeding, check-ins, punishment, or long-term care obligations. | U1, U2: Whether reduced care requirements have value and whether users accept the concept remain to be validated; device conditions still apply. |
| 2D pets lack a sense of spatial embodiment | Maintain an appropriate bodily scale and relatively stable position, allowing the user to perceive the body through changes in viewpoint and physical approach, followed by coherent responses. | D1, T1: Both the experiential advantage and the stability of spatial presentation remain to be validated. |
| Feedback relationship when approaching the body | Hand approach, contact, and withdrawal each correspond to an understandable bodily response; no physical haptic feedback is provided. | D2, T2: Both the subjective sense of contact and the feasibility of input and feedback remain to be validated. |
| Low-disruption design constraint | Rest by default, let the user invite interaction, do not escalate when ignored, and exit naturally when the interaction ends. | This is a behavioral requirement, not a new primary question or an established companionship effect. |

Baobao defaults to quiet coexistence. Baobao can notice the user but does not continuously demand attention. Interaction develops further only after the user extends an invitation by looking, approaching, or touching. When the user stops interacting, Baobao should exit naturally and return to a quiet state.

Gaze, approach, and touch describe the intended experience. Whether the target device provides the corresponding inputs with sufficient accuracy and under suitable permission conditions still needs to be validated; direct access to gaze data must not be assumed.

The experience flow is:

`Resting Nearby → Awareness → Response → Optional Approach → Exit Interaction → Resting Nearby`

## 2. Five Experience States and One Safety State

| State | Experience purpose | Entry condition | Allowed behavior | Exit path |
|---|---|---|---|---|
| Resting Nearby | Establish a shared presence that requires no interaction. | Session starts, an interaction ends, or there has been no user invitation for an extended period. | Breathing, subtle posture adjustments, and occasional observation of the environment. | May briefly enter Awareness; otherwise continue resting. |
| Awareness | Express limited awareness without forcing the user to respond. | The user maintains gaze, approaches, or generates a single low-frequency trigger. | Turn the head, open the eyes, lift the head slightly, or observe briefly. | Enter Response if the user continues the invitation; otherwise return to rest. |
| Response | Acknowledge the user’s intentional action. | The user reaches out, touches gently, or continues to approach. | Observe the hand, sniff, nuzzle the hand, or accept a brief stroke. | May be maintained briefly if the user continues the invitation; otherwise enter Exit Interaction. |
| Optional Approach | Provide a clearer but non-mandatory moment of interaction. | The user clearly invites it, and the spatial and input conditions are reliable. | Adjust position slightly while maintaining a safe distance and avoiding obstruction of primary content. | If ignored, stop approaching and enter Exit Interaction. |
| Exit Interaction | Clearly end an interaction. | The user looks away, withdraws their hand, or returns to their primary activity. | Reduce movement, shift attention away, and settle again. | Return to Resting Nearby. |
| Safety Pause | Prevent incorrect, abrupt, or unsafe spatial behavior. | Tracking is lost, input is uncertain, space is insufficient, or the app is interrupted. | Stop movement and interaction; hide the character if a reliable spatial position cannot be maintained, and do not require it to remain visible if the app is interrupted. | Return to rest once the environment is reliable again; otherwise remain paused. |

## 3. Hand Movements and Pet Responses

| User action | Baobao’s intended response | Disallowed response |
|---|---|---|
| Hand approaches slowly | Remain in place, track the hand with the eyes, tilt the head slightly, and sniff once after confirming safety. | Lunge toward the hand, approach suddenly, or repeatedly seek attention. |
| Gentle touch on the forehead or cheek | Relax the expression, close the eyes slightly, or gently nuzzle toward the finger. | Jump dramatically or force entry into a prolonged interaction. |
| Brief, gentle stroking | Maintain a stable posture and respond through breathing, facial expression, and subtle body movements. | Hold onto the user, prevent the hand from leaving, or demand repeated interaction. |
| Rapid reach or sudden approach | Pull back slightly or pause while maintaining a safe distance. | Attack, punish the user, or continue displaying negative emotion. |
| Hand withdraws | Stop responding, observe briefly, and gradually return to rest. | Chase, approach repeatedly, or use sound to demand continuation. |

Hand contact refers only to contact that the system may eventually simulate through visual, animation, and audio feedback; it does not imply that the device can provide real physical haptics.

## 4. Low-Disruption Rules

1. Quiet coexistence is a valid state, not an empty state waiting for user input.
2. Without a user invitation, Baobao may transition from Resting Nearby to Awareness at most once and must not continue escalating the intensity of its behavior.
3. Baobao must not frequently enter the center of the user’s view, obstruct primary content, or repeatedly make sounds.
4. When the user ignores Baobao, there must be no punishment, negative emotion, loss of progress, or more forceful reminder.
5. Continuous gestures or conversation are not required; the specific rules for eliminating care obligations are defined in the next section.
6. Do not continuously listen to the environment, infer the user’s emotions, or access content from other apps.

## 5. No-Care-Obligation Rules

| Explicit constraint | Behavioral requirement |
|---|---|
| No feeding | Do not include hunger, thirst, or any resource meter that must be replenished. Feeding must not be required to maintain health, survival, or relationship status. |
| No check-ins | Do not include daily tasks, login streak rewards, or recurring requirements to return. |
| No punishment | Ignoring, leaving, or closing the experience must not cause deterioration, illness, death, relationship decay, loss of progress, or guilt-inducing reminders. |
| No long-term care obligations | Do not assign mandatory maintenance tasks such as cleaning, medical care, or growth progression. Do not accumulate tasks while the user is offline or require make-up care when they return. |

The user can end the interaction, hide Baobao, or close the experience at any time without a farewell action or a promise to return. Baobao’s rest and recovery do not depend on user care. If state is saved in the future, it must not introduce offline resource depletion or care debt. These requirements directly address the burden of responsibility associated with real pet ownership; their companionship value remains subject to validation under U1.

## 6. Natural Exit Rules

- The user withdrawing their hand, looking away, or returning to their primary activity all indicate the end of an invitation.
- After one brief response, Baobao should reduce the intensity of its movements and must not prompt or approach the user again.
- The exit should transition from a response into a settled posture, avoiding sudden freezing or a looping farewell animation.
- After exiting, return to Resting Nearby while maintaining continuity of position and scale.
- Any uncertainty in input or tracking takes priority and should trigger Safety Pause rather than a guess about the user’s intent.

## 7. Current Implementation Boundary

The concept demo presents the visual intent of resting, awareness, touch response, and natural exit, but it does not implement the state logic described above. In the next phase, a browser-based simulation will validate only whether states, triggers, and feedback form a coherent sequence. Real gaze input, hand tracking, spatial positioning, occlusion, and cross-app coexistence must wait for on-device XR validation.
