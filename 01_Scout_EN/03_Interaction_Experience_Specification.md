# Exploration 03 — Interaction Experience Specification

This is the proposed behavior baseline for Browser v0.1. I will refine it through independent implementation and self-testing; it has not yet been validated with users. Input mappings are defined in [07 — Browser Demo Validation Goal](./07_Browser_Demo_Validation_Goal.md). On-device rules will be revisited once the actual platform is known.

## 1. States and transitions

The current build uses four experience states plus a safe pause. Baobao remains in a fixed location and begins in the middle of either resting or observing.

| State | Entry and behavior | Exit |
|---|---|---|
| Autonomous activity | At the start or after an interaction, continue the selected rest/observe activity without automatically facing the user. | Enter Notice when its condition is met; Reach may go directly to Respond. |
| Notice | Without Reach, briefly turn toward the user the first time they reliably move near, or after Look is held while Baobao is observing. Look alone does not interrupt rest. | Return to autonomous activity after the brief response; Reach may interrupt and enter Respond; Disengage enters Exit. |
| Respond | Reach is an explicit invitation and does not require Look or Approach first. Baobao sniffs once and pauses briefly without changing position. | Enter Exit when the response finishes or the user disengages. |
| Exit | Reduce movement and attention, then return smoothly to the previous activity. | Return to autonomous activity; a new Reach may interrupt the exit smoothly. |
| Safe pause | When the page loses focus, simulated input fails, or presentation becomes unreliable, stop interaction and clear unfinished input and motion. Hide Baobao if his position cannot be maintained. | After conditions remain reliable for the recovery threshold, return to autonomous activity without replaying old invitations. |

## 2. Interaction priority and recovery

1. **The user's decision to stop takes priority.** Disengage ends the current response; Hide or Close stops the experience immediately. Recovery never overrides a user choice. If the user hides Baobao and returns to the page, he stays hidden until explicitly shown.
2. **One invitation produces one response.** Repeated input does not restart, indefinitely extend, or queue the animation. A new invitation is accepted only after the current response finishes. Rapid Reach clicks still produce a single sniff.
3. **Recovery does not continue old input.** When the page is interrupted or input fails, unfinished actions are cleared. Baobao returns to autonomous activity after recovery and waits for new input.

No input means Baobao continues his activity; it is not an error. Reloading the page or choosing Restart begins a new experience. Hide/Show and pause/recovery remain part of the current experience. Detailed repetition, counting, and reset checks are listed in [07 — Browser Demo Validation Goal](./07_Browser_Demo_Validation_Goal.md).

Disengage explicitly ends an invitation; loss of page focus indicates interruption. The Demo does not read other apps or infer what the user is doing.

## 3. Browser v0.1 tuning values

Use 0.8 seconds of continuous Look as the initial Notice threshold. Notice lasts about 1 second, a Reach response lasts no more than 3 seconds, and the exit transition lasts about 0.8 seconds. Resume only after conditions have remained reliable for 1 second; any new failure restarts that timer.

These are implementation starting points, not user-experience pass criteria. They may change during self-testing, but every demonstrable version should record its actual values so feedback from different versions is not mixed.
