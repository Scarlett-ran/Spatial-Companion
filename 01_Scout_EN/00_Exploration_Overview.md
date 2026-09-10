# Scout — Spatial Companion

**Domain:** Software / Spatial Interaction  
**Stage:** TRL 1–2 | Problem Exploration  
**Target Audience:** Gen Z and younger users

## Problem statement

Some young people want pet-like companionship but find it difficult to take on the ongoing responsibilities of caring for a real animal. Pet ownership requires a long-term commitment of time, energy, and money, and is also constrained by rental conditions, lifestyle, and which species can realistically be kept. Cats and dogs need daily care, and illness can create additional expenses; animals such as seals, in particular, are not a realistic option as household pets.

Virtual pets lower the barriers associated with real pet ownership, but 2D virtual pets on desktop and mobile devices remain confined to screen-based interfaces. They lack a spatial position shared with the user, a bodily scale, and a body that the user can approach. The limitation here concerns the conditions for expressing a sense of spatial embodiment; it does not mean that 2D pets cannot provide companionship. Whether spatial presentation improves the experience still needs to be validated through comparison.

This project therefore explores:

> **Can spatial computing bring a virtual pet—one that does not require the user to assume real-world care responsibilities—into the user’s space with scale, position, and bodily feedback, thereby providing a companionship experience with a stronger sense of embodiment than a 2D pet?**

Low disruption is a design constraint for this exploration. The pet should be able to exist quietly and respond briefly only when the user intentionally looks at it, approaches it, or reaches toward it. Its value should not depend on ongoing conversation, frequent interaction, or mandatory care.

## What is true vs. assumed

| Known fact / existing basis | Evidence boundary |
|---|---|
| Real pet ownership requires an ongoing commitment of time, energy, money, and long-term responsibility, and is constrained by housing conditions and the practical limits of keeping particular species. | It does not mean the strength of the target audience’s need or their willingness to adopt the concept has been confirmed. |
| 2D virtual pets on desktop and mobile devices provide a pet experience that does not depend on a real animal, with the character presented within a screen-based interface. | This identifies the comparison condition for the candidate solution; it does not prove that a spatial pet is better than a 2D pet. |
| I tried Apple Vision Pro and experienced virtual content as present in physical space, with gaze, hand movements, and visual feedback producing a sensation close to “touch.” | This is a record of personal experience. It cannot be generalized to users in general and is not equivalent to physical haptics. |

**Established design decisions:** The character is Baobao; character selection is no longer treated as an assumption to validate. Young users are the current target audience, but their acceptance of the concept still needs to be validated. Low disruption is a design constraint. The concept explicitly excludes feeding, check-ins, punishment, and long-term care obligations. A spatial pet is a candidate answer to the primary question, not yet a validated solution.

| Core assumption | Judgment to validate |
|---|---|
| D1 · Design assumption | With comparable characters and behaviors, a spatial presentation with three-dimensional scale, a stable position, and an approachable body creates a stronger sense of embodiment than a 2D presentation. |
| D2 · Design assumption | In the absence of physical haptic feedback, visual and behavioral feedback can still create a credible subjective sense of contact. |
| U1 · User assumption | A spatial pet with no long-term care obligations can still provide companionship value through quiet coexistence and lightweight responses. |
| U2 · User assumption | Gen Z and younger users are willing to accept this type of spatial pet and the device conditions it requires. |
| T1–T3 · Technical assumptions | Spatial positioning, the necessary inputs and feedback, state logic, and pause behavior under exceptional conditions can be combined into a usable experience. The existence of foundational platform capabilities does not mean this project’s feasibility has been proven. |

The current Browser stage prioritizes whether the rules and interaction causality within T3 are legible in a browser, while gathering early directional signals for U1 and U2. D2 remains the first experience objective for on-device validation. D1 and T1–T2 retain their own on-device evidence requirements; U3, U4, and T4 are deferred. See the [Assumption Map](./02_Assumption_Map.md) for details.

## Why now

The desire for pet companionship and the idea of virtual pets are not new; what has changed is the medium through which they can be realized. My firsthand experience of spatial presentation and eye-and-hand interaction on Apple Vision Pro provided the conceptual starting point for a virtual pet with position, scale, and responsive behavior, but Apple Vision Pro is not the target product platform. The final product is intended for Goertek’s own VR platform. Its specific device, operating system, engine, SDK, input permissions, runtime contexts, and stability have not yet been confirmed and must be reassessed once internal technical information is available. Feasibility on Goertek’s target platform cannot be inferred from Vision Pro’s capabilities. [Apple Vision Pro](https://www.apple.com/newsroom/2024/01/apple-vision-pro-available-in-the-us-on-february-2/)

## Why us

Goertek already has XR devices, technical knowledge-sharing, and relevant specialists, enabling the project to begin with a real spatial experience and, once the concept matures, to support further discussion of the implementation conditions for spatial positioning, hand tracking, and interaction feedback. This does not mean that the project has secured device access or engineering support, but it provides a path for subsequent validation that is closer to a real technical environment than purely conceptual speculation.

## Current scope

The current output is a [20-second concept demo](../demo.mp4), created to communicate the design intent of Baobao existing quietly, noticing the user, accepting touch, and naturally ending the interaction. It is not an on-device prototype for Goertek’s target VR platform and cannot prove that spatial positioning, hand tracking, cross-app coexistence, or companionship effects have been achieved; these remain assumptions to validate in later stages.

No external user research or browser-based interactive simulation has been completed. The current scope is limited to confirming and carrying out the next browser-based interaction validation step. The Mentor must first decide whether a browser demo is the appropriate low-cost validation method; if approved, the sequence is Demo Scope, Test Plan, Build, User Test, and a Go / Kill / Redirect decision. An on-device XR prototype is outside the current scope and should be considered only after the browser validation produces signals worth pursuing and a separate resource decision is made.
