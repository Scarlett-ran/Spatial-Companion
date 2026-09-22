# Baobao — Evidence and Decisions

[Scout index](README.md) · [中文](../01_Scout_CN/02-evidence-and-decisions.md) · [Project index](../README.md)

This document explains the basis for Baobao's product direction: what the research suggests, which choices we have made, and what remains to be explored. Research findings and product decisions are recorded separately so readers can understand the basis for each judgment.

## 1. Main interview findings

The five participants saw a concept video and heard a verbal explanation; none had used Baobao. The records cover their existing everyday and entertainment experiences as well as their reactions to the concept.

### Openness to digital technology does not imply openness to a virtual companion

E enjoys VR games and uses AI daily, but does not want to treat a virtual animal as an intimate emotional companion. B, by contrast, described spending time with game animals and becoming attached to them, and wanted familiar game animals to appear in her real space.

### Existing attachment shapes whom people want to see

A cared more about his own cat; B wanted to see animals she had already spent time with in a game. Both cared about companions with whom they had a shared history. Baobao would be a new character to its users.

### Device costs affect willingness to use the experience

A did not want to buy a headset specifically for a virtual animal. C had reduced headset use because of weight, the visual experience, and repetitive content. E had enjoyed VR games but did not feel the same experience justified another trip to where the equipment was available.

### People return to an experience for different reasons

B returned to games for their stories and shared experiences. C continued watching a series and revisited performances he liked. D valued friends' voices, actions, and feedback in games, emphasizing that this was more than companionship.

For Baobao, we need to understand what people look forward to when returning: seeing a familiar companion, enjoying an interaction, or finding new content. Describing all of these as a “need for companionship” would obscure the differences.

### Interactions still need to be understandable

C felt that movement and responses could make a character seem alive, while also pointing out the lack of touch and wanting clearer communication. D wondered why Baobao was in the home and how Baobao could notice an approaching hand while its eyes were closed.

## 2. Product choices and rationale

| Product choice | Rationale |
|---|---|
| Aim for an emotional bond, with both quiet time together and direct interaction as valid ways to connect | We hope users gradually care about Baobao, enjoy its company, and perhaps feel comforted by its presence. Direct interaction does not need to happen in every encounter. |
| Focus on people who are open to a virtual companion | The interviews show that interest in digital technology and openness to a virtual emotional relationship are not the same. The latter is more relevant to the intended experience. |
| Let Baobao share the user's real space, with lightweight MR glasses as the intended medium | Users can discover it at home, approach it, and bring it close. A lightweight device may reduce the burden of putting on equipment specifically for an interaction. |
| Keep the same appearance and a few consistent habits | Give users a chance to get to know Baobao and connect one encounter with the next. The first version does not unlock affectionate actions based on encounter count. |
| Communicate through movement and shared presence, without speech | Users do not have to find a topic or explain their feelings. When they feel low, Baobao keeps its usual behaviors; emotion recognition and special comforting actions are not required. |
| Preserve its own rhythm and allow it not to respond at times | Baobao can keep sleeping or playing instead of responding to every input. Its actions should make what it is doing understandable. |
| Require no repeated confirmation after enabling Baobao; end the glasses experience by closing the app or removing the glasses | Reduce repeated entry steps while letting users choose when to spend time together. An unanswered approach does not lead to repeated prompts. |
| Require no care or relationship upkeep; omit feeding from the first version | Users can leave and return freely, without punishment for absence or tasks to catch up on. |
| Let life progress with elapsed time and local day and night | Preserve the idea that Baobao has a life of its own. Its activity and location may change between encounters rather than remaining exactly as the user left them. |
| Focus the first version on one Baobao's life at home | Make watching, approaching, picking up and moving, and waking understandable before adding ball-throwing tasks, multiple pets, or outdoor use. |

See [Experience and Prototype](03-experience-and-prototype.md) for behavior and scope. Device selection, input methods, and implementation will be determined through experience design and technical assessment.

## 3. Key questions to explore

### What do users gain from spending time together?

Users may find Baobao fun, relaxing, or comforting, or simply enjoy having it nearby. Explore which moments make them want its company and which feel intrusive, without assuming everyone wants the same experience.

### Can repeated encounters gradually develop into an emotional bond?

Look for whether users begin to recognize Baobao's habits, think of it spontaneously, and have reasons to see it again. Initial curiosity or attraction to its appearance may gradually develop into caring about this particular Baobao.

### What does sharing a real space add?

Explore what it means to find, approach, and pick up Baobao in a room. If users do not value these experiences, first check whether spatial presentation and interaction work well enough. If they still add no value, reconsider the medium or product direction.

### Can users feel at ease while Baobao follows its own rhythm?

Observe how users interpret nonresponse, and whether ignoring or leaving Baobao makes them worry about hurting it or needing to make amends. Baobao can have its own activities without making users responsible for sustaining the relationship.

### Can the device and interactions fit everyday life?

Learn when users are willing to wear the glasses, and whether finding, picking up, waking, and returning to Baobao are convenient. Use actual experience to judge whether these costs get in the way of spending time together.

## 4. Questions to resolve for the minimum prototype

The FWP comes first. The questions below prepare for the later prototype on glasses; they do not imply that a device, 3D model, rig, or animation assets are already available. Technical checks can be made as needed, but do not replace trials with users.

| Area | Core question |
|---|---|
| Device and platform | Which available glasses best suit the prototype? Do they expose the required development capabilities, and do they need a companion phone or computer? |
| Spatial presentation | Can Baobao remain stable on a real floor or piece of furniture and move within a small area? What are the limits of positioning and occlusion? |
| Core interactions | Can petting, picking up, moving, putting down, and poking awake be implemented? What alternative input could the prototype use if gesture recognition is unreliable? |
| Character and behavior | Starting from the existing material, what additional art assets and development are needed for sleeping, lounging, playing, and approaching on its own? |
| Time and state continuity | On reopening, can Baobao's activity and location be updated from the previous state, elapsed time, and local day and night without continuous background execution? |
