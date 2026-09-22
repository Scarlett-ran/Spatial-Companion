# Baobao — Product Definition

[Scout index](README.md) · [中文](../01_Scout_CN/01-product-definition.md) · [Project index](../README.md)

## 1. Product proposition and problem hypothesis

Baobao is a non-speaking virtual harp seal pup with a daily rhythm of its own. Through everyday encounters, we hope users will gradually form an emotional bond with Baobao: come to care about it, enjoy its company, and perhaps feel comforted by its presence. This bond begins with simply spending time together. While users go about their own activities, Baobao sleeps, lounges, or plays nearby, occasionally approaching them on its own. Users can interact with it or leave it to itself. Direct interaction is one way to build a bond; quiet time together matters too.

The design draws on the concept of a **safe haven** in attachment theory: when distressed or under pressure, a person can turn to an attachment figure for comfort and a sense of safety. Baobao aspires to be a companion users want to turn to at such moments, offering comfort through shared presence and nonverbal interaction. Spending time with Baobao does not depend on providing care or maintaining the relationship. Users can decline interaction, leave, and return without keeping Baobao alive or repairing a relationship damaged by their absence.

The questions to explore are what users gain from spending time with Baobao, which experiences make them want to see it again, and whether an emotional bond gradually develops. People may use it for fun, companionship, relaxation, or comfort; they need not share a single motivation. Safe haven is a design reference, not evidence that Baobao already serves that function.

## 2. Intended users and use cases

### Intended users

People who are open to a virtual companion and would like companionship and enjoyment in their everyday life at home.

### Use cases

**1. Checking on Baobao after coming home**

After arriving home, users want to see where Baobao is and what it is doing. Once they find it, they might interact for a while or simply take a look.

**2. Taking a short break after concentrating**

After working, studying, or focusing on something at home, users take a break and look for Baobao to play with. If it is asleep, they can watch briefly and leave, or poke it awake.

**3. Spending quiet time together at home**

While reading, listening to music, or daydreaming, users can pick Baobao up and bring it nearby. They continue their own activity while Baobao rests or plays beside them. They may interact occasionally, and Baobao can also wander off on its own.

**4. Spending a little time with Baobao before bed**

Users can check on Baobao before bed or bring it onto the bed to spend time together. After taking off the glasses, they may still feel that Baobao is nearby even though they can no longer see it.

**5. Turning to Baobao when feeling low**

When tired, upset, or uneasy, users can look for Baobao or bring it close. They do not have to talk or do anything in particular; they can simply watch it or spend time beside it.

## 3. Design principles

### Simply being together has value

Baobao does not need to keep drawing the user's attention. Users can watch it sleep, lounge, or play, or get on with their own activities. Baobao occasionally approaches on its own. If the user does not respond, it resumes its activities without repeatedly seeking attention or becoming less affectionate toward them.

### Every encounter is with the same Baobao

Baobao retains a consistent appearance and a few recognizable habits, giving users a chance to get to know it over time.

### Users choose when to spend time together

Once users enable Baobao, it can continue to appear at home in later sessions without requiring confirmation each time. Users end the glasses experience by closing the app or taking off the glasses. The first version has no separate hide, show, or pause controls.

### Baobao follows its own rhythm

Baobao may not respond to every interaction. It may be absorbed in playing with its toy and continue what it is doing. Its actions should make its activity understandable, without prompting users to keep clicking for a response.

### No care obligations or relationship upkeep

The first version does not include feeding, daily check-ins, or a requirement to keep interacting. Leaving or taking a long break will not make Baobao ill or distant, and returning will not create a backlog of tasks. There are no check-in rewards, intimacy scores, or affectionate actions unlocked through repeated use.

### Baobao's life continues over time

Baobao's life progresses even after users close the app or take off the glasses. On their return, it may be doing something different or be elsewhere in the home. Its daily rhythm is influenced by local day and night, without a rigid schedule or a requirement for continuous background execution.

## 4. Alternatives and reasons to choose Baobao

People already have many options for companionship, relaxation, or brief interaction. The table compares what those options offer with the experience Baobao aims to provide. These are possible reasons to choose Baobao, not proven reasons for adoption.

| Existing option | What it offers | What it leaves open | Why someone might choose Baobao |
|---|---|---|---|
| Animal videos and livestreams | The enjoyment of watching animals, readily accessible during a break | The animals do not share the user's room and cannot be directly interacted with | Users can find Baobao in their own home, approach it, and pick it up. |
| Plush toys and character figures | Familiar physical company that can be touched, held, and invested with emotional meaning | They do not act independently or respond on their own | Baobao has its own rhythm and occasionally approaches the user. |
| Screen-based virtual pets | Character companionship, observation, and interaction; some include raising or caring for a pet | Encounters mainly take place on a screen; care mechanics may require ongoing effort | Baobao inhabits the real room without requiring feeding or care tasks. |
| Conversational AI companions | Conversation, a place to share feelings, and verbal responses | Finding something to say can become a burden when users do not feel like talking | Users can spend quiet time together or interact occasionally without speaking or coming up with a topic. |
| Real pets | A shared life with a real animal, a relationship, physical contact, and responses | They require care and depend on housing, time, and other practical conditions | Baobao offers another kind of animal-companion experience without responsibility for a real animal's care. |
| Physical companion robots | Physical presence, movement or sound responses, and sometimes touch interaction | Movement, interaction, and maintenance requirements vary by product; representative products need to be compared | Whether Baobao offers a better fit must be assessed alongside the burden of wearing glasses. |

## 5. First-version scope

The intended product is for lightweight mixed-reality (MR) glasses, centered on the feeling that “Baobao and I live in the same real space.” No device has been selected. Spatial display and input capabilities need to be checked on actual hardware; lightweight AI glasses should not be assumed to provide them. The work starts with a Functional Web Prototype (FWP), followed by user trials and refinement before proceeding to a prototype on glasses. See [Validation and Next Steps](04-validation-and-next-steps.md).

Baobao sleeps, lounges, or plays with its toy in the room and occasionally approaches the user. Users can find and watch it, pick it up and move it where they want, or poke it awake. It has its own rhythm and does not have to respond to every interaction.

Users end the glasses experience by closing the app or removing the glasses. The web version handles actual browser events such as closing the page or switching tabs. Baobao's life progresses with elapsed time and local day and night; its state and location may have changed when it next appears.

The first version excludes feeding, conversation, ball-throwing tasks, multiple pets, and outdoor use. The device and input methods remain to be determined.
