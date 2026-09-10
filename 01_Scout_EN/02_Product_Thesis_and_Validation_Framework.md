# Exploration 02 — Product Thesis and Validation Framework

This document defines Scout's relationship thesis, research questions, and scope. Specific behavior is covered in 03, assumptions and metrics in 05, and execution and decisions for the current stage in 06 and 07.

## 1. Product thesis: separate lives, occasional encounters

> **Baobao has a life of his own. Sometimes, that life intersects with yours.**

Scout is positioned as an Autonomous Spatial Companion. It explores whether a spatial character with autonomous activities can create meaningful companionship through quiet co-presence, mutual recognition, and lightweight interaction without requiring the user to take on care responsibilities.

| Principle | Meaning in this project |
|---|---|
| Autonomous | Baobao has his own activities and rhythm. The user's arrival does not mean he must immediately wait for instructions. |
| Spatial | Baobao should have a credible position, scale, approachable body, and coherent responses. These perceptions need on-device evidence. |
| Companion | Baobao and the user have separate lives and connect by noticing each other and occasionally sharing a moment. |
| Without care obligations | The relationship is not maintained through feeding, check-ins, punishment, or mandatory upkeep. |

## 2. Relationship mechanisms: co-presence and mutual recognition

Baobao is a harp seal pup with his own thoughts, interests, activities, and world. When the user enters, he may already be resting, observing, or playing on his own. He may notice the user or continue his activity. An encounter does not have to involve interaction; afterward, both return to their own activities.

Virtual-pet mechanics centered on care often build connection through repeated caregiving. Scout explores another relationship: living separate lives, noticing each other, and occasionally sharing a moment. This is a distinction between mechanisms, not a claim that all virtual pets work alike or that either relationship is inherently more valuable.

The current exploration concerns co-presence-based attachment and a recognition-based relationship. Later research will examine whether autonomy and relationship continuity support sustained companionship. “Recognition” currently means making the user feel that Baobao has noticed and responded to them; it does not mean implemented identity recognition or memory across sessions. “Baobao knows I am here” is an intended experience, not a user finding.

The internal design principle is: **Baobao does not wait for the user to give him a life.** A few preset activities can express this without simulating an entire life in the background. Future work may explore continuity through subtle differences at reunions, remembering an interaction, or bringing an object, without relationship decay or pressure to return.

## 3. Three levels for assessing value

| Level | Independent question | Assessment boundary |
|---|---|---|
| Level 1 — Presence | Does Baobao feel present in the user's space? | Position, scale, depth, and approachability require on-device evidence. Contact credibility is assessed separately and is not physical haptic feedback. |
| Level 2 — Relationship | Can an autonomous Baobao provide companionship value both during and outside active interaction? | Distinguish the value of presence, low disruption, entertainment, novelty, and companionship. A sustained relationship requires evidence from repeated encounters. |
| Level 3 — Product | Is that value sufficient to justify device conditions and a product form that supports sustained use? | Distinguish concept interest from actual access, wearing, launching, and repeated use. Standalone and coexistence forms need separate assessment. |

These levels are a framework for assessing value, not three experiments or an established causal chain. Strong spatial presence does not establish companionship, and 2D may provide similar companionship. Even a valuable experience may fail as a product if users are unwilling to use XR. Subjective contact is not assumed to be necessary for companionship; failures in the contact mechanism should be diagnosed separately.

## 4. Research sequence: one major risk per round

| Research question | Main method | The key judgment for the round |
|---|---|---|
| RQ1 — Interaction | Browser interaction logic prototype | Is behavior understandable, and are inputs, responses, and natural endings coherent? Observe initial perceived autonomy as supporting information. |
| RQ2 — Presence | First on-device spatial prototype | Do appropriate scale, stable position, depth, and approachability make Baobao feel present? |
| RQ3 — Contact | Separate on-device contact experiment | Can visual and behavioral responses produce a credible subjective sense of contact without physical haptics? |
| RQ4 — Companionship | Short passive co-presence study, followed by a separate repeated-encounter study | First assess whether quiet presence has value, then whether autonomous behavior and relationship continuity support sustained companionship. |
| RQ5 — Product Value | Later adoption study under actual device conditions | Is the value sufficient for users to accept device conditions and choose to use the experience again in specific contexts? |
| Long-term question — Baobao World | Deferred research | Can Baobao maintain a believable independent life across his own world and the user's digital world? |

Browser work reduces behavioral risks that can be examined before spatial research; it does not directly validate the three value levels. User segments, existing device habits, and platform capabilities can be investigated early. Formal conclusions about spatial effects, relationships, and adoption still need evidence from the appropriate conditions. See [05_Assumption Map](./05_Assumption_Map.md) for the mapping between research questions and assumptions.

## 5. Now / Next / Later / Future

The table below describes the direction of work.

| Stage | Focus | Scope boundary |
|---|---|---|
| NOW — Browser | Behavioral causality, states and timing, natural endings, and initial perceived autonomy; an engineering reference and rationale for device access. | A minimal prototype yet to be built. It does not establish spatial presence, contact, or long-term companionship. |
| NEXT — First XR round | Review the platform and validate scale, position, and spatial presence first; examine available inputs and contact feedback separately afterward. | Gaze, hand inputs, and permissions remain unconfirmed. The first round need not implement every interaction. |
| LATER — Companionship and adoption | Passive presence value, low disruption, repeated encounters, relationship continuity, voluntary return, and actual device choices. | Short co-presence, sustained relationships, and adoption are assessed in separate rounds and cannot substitute for one another. |
| FUTURE — Baobao World | An independent world, activities and journeys, returning home, bringing objects back, cross-app visits, and continuity across worlds. | A long-term North Star, not a current MVP requirement or a committed feature list. |

## 6. Minimum experience and long-term world concept

The minimum experience needs only a few high-quality behaviors: activity already in progress at entry, optional awareness, responses to invitations, optional contact, and a natural return to Baobao's own activity. Baobao is the fixed character, with at least one resting and one non-sleeping autonomous activity. The prototype is a research tool, not yet a deliverable product.

The long-term structure could be **Baobao's world ↔ Baobao travels ↔ User's digital world**. The Baobao App represents his own world: opening it feels like “visiting Baobao at home.” Other Apps represent the user's digital world, which Baobao occasionally visits from his own. This world concept offers a natural explanation for cross-app companionship. The form, value, and feasibility of visits still need research; a permanent overlay across every app is not the default.

| Scope category | Treatment |
|---|---|
| Build now | A few autonomous activities, interaction and no-interaction branches, necessary responses, and endings. See 03 for behavior rules. |
| Not now; select later based on evidence | A complete world, hunting, resource and item systems, cross-app runtime, complex conversation and AI personality, long-term growth, memory, and offline life simulation. |
| In conflict with product principles | Mandatory feeding for survival, hunger upkeep, check-in tasks, affection maintenance, punishment for leaving, relationship decay, and care debt. These are not merely deferred features. |

[03_Interaction Experience Specification](./03_Interaction_Experience_Specification.md) translates these principles into behaviors this round can represent.
