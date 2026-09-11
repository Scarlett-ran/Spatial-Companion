# Exploration 06 — Next-Phase Decisions

The project currently has two stages. I will independently design, build, self-test, refine, and package the Browser Demo. Only after it is reasonably mature will I seek hardware access and external support for on-device work. Building, informal feedback, and refinement are activities within the Browser stage, not separate approval gates.

## 1. Two stages

| Stage | How it proceeds | Result |
|---|---|---|
| Browser | Build a working Demo independently, test its rules and failure cases, refine it as time allows, and collect feedback when practical. | A stable, understandable behavior reference that is ready for external discussion. |
| On-device | Use the mature Demo and a focused question to seek equipment and necessary collaboration, then review the platform and build a minimal spatial prototype. | Evidence about real scale, position, approach, and spatial presence, followed by decisions about contact and co-presence. |

I decide the scope, pace, and version trade-offs during the Browser stage. Whether external support is available and how other people participate will be determined only when the mature Demo is used to request on-device work.

## 2. When is the Browser Demo mature enough?

| Dimension | Completion criterion |
|---|---|
| Complete demonstration | Both autonomous activities and the invitation, response, and exit flow run end to end and can be repeated after restart. |
| Reliable behavior and recovery | Priority, trigger count, disengage, hide, close, and recovery rules pass self-testing, with no known issue that blocks the core flow. |
| Coherent presentation | Movement transitions naturally and input/response timing is clear without manual workarounds or explanations that hide faults. |
| Transferable package | A working version, short recording, behavior notes, known issues, and minimum device needs clearly show what is complete and what still requires evidence. |
| Honest evidence | Self-testing, personal judgment, and participant feedback are kept separate. D3/M1 and other user-experience judgments remain unvalidated if no participant evidence exists. |

Meeting these criteria supports a request for the next stage; it does not establish user value or behavioral understanding.

## 3. Decisions after Browser work

| Decision | When it applies | Next action |
|---|---|---|
| Seek on-device support | The Demo meets the maturity criteria and the remaining core question requires hardware. | Share the package with a focused support request. |
| Continue refining | A core flow, transition, or recovery problem is specific and fixable. | Address one defined issue, then retest without expanding the feature set. |
| Redirect | The mechanism no longer expresses the intent, or available feedback challenges the audience or need assumptions. | Change the relevant premise and state which earlier evidence still applies. |
| Hold or stop | Personal capacity or current conditions are insufficient, or the mechanism no longer justifies more work. | Record the condition for resuming or the exact work being stopped. |

A mature Browser Demo remains a completed stage even if external support is not yet available. Waiting for hardware should not become a reason to keep adding Browser features.

## 4. Requesting and starting on-device work

The external package should include the mature Demo and recording, behavior and input notes, self-test results and any participant feedback, known limitations, and a minimum request for hardware and collaboration. The concept video is described in [04 — Concept Demo](./04_Concept_Demo.md); the Browser work plan is in [07 — Browser Demo Validation Goal](./07_Browser_Demo_Validation_Goal.md).

The first request focuses on RQ2: the target device and operating mode, credible scale, stable position, approach, and viewing from different angles. Contact and cross-app behavior are not part of the minimum request. Scope, permissions, deployment, roles, and timing for on-device work are defined only after equipment and necessary support are available.

Each self-review or external discussion records the date, version, resolved and unresolved issues, decision, and next step. Browser work follows my available time; external resources are not presented as commitments before the on-device stage begins.
