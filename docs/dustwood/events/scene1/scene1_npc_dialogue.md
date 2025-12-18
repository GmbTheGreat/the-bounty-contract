# Scene 1 – Station Interaction & Objective Setup

This document explains all gameplay events used in **Scene 1** after the opening cutscene ends.  
Scene 1 begins when the player interacts with the NPC at the railway station.

---

## Event Flow Overview

Order of events in Scene 1:

1. `scene1_begin`
2. `scene1_conversation_2`
3. `scene1_conversation_3`
4. `scene1_conversation_4`
5. `scene1_conversation_end`
6. `scene1_wanted_notice`
7. `scene1_wanted_notice_lock_indicator`
8. `scene1_npc_disappear`

---

## `scene1_begin`

**Purpose**  
Starts Scene 1 after the opening cutscene.

**What happens**
- Triggered when the player interacts with the NPC at the station.
- Begins the Scene 1 conversation flow.

**Triggered by**
- Player interaction.

---

## `scene1_conversation_2`

**Purpose**  
NPC welcomes the player.

**What happens**
- NPC confirms the sheriff informed him about the player.

**Dialogue example**
> “Nice to see you here. The sheriff said you would come.”

**Triggered by**
- Automatically after `scene1_begin`.

---

## `scene1_conversation_3`

**Purpose**  
Explains the condition of the town.

**What happens**
- NPC briefly talks about Dustwood being abandoned and unsafe.
- Sets the tone of the town.

**Triggered by**
- Automatically after `scene1_conversation_2`.

---

## `scene1_conversation_4`

**Purpose**  
Assigns the first gameplay task.

**What happens**
- NPC tells the player what to do next.
- Warns about danger.

**Dialogue example**
> “You should find a revolver in town before someone else finds you.”

**Triggered by**
- Automatically after `scene1_conversation_3`.

---

## `scene1_conversation_end`

**Purpose**  
Ends the NPC conversation.

**What happens**
- Dialogue UI closes.
- Player regains full control.
- Scene switches to exploration mode.

**Triggered by**
- Automatically after `scene1_conversation_4`.

---

## `scene1_npc_disappear`

**Purpose**  
Cleans up the scene.

**What happens**
- NPC disappears from the station.
- Prevents repeated interaction.
- Improves performance and narrative clarity.

**Triggered by**
- After the wanted notice sequence is complete.

---
