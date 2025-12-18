<img width="692" height="553" alt="image" src="https://github.com/user-attachments/assets/88a0d8e0-22d9-49ec-a6c3-13c6f2cfe210" />


## `scene1_wanted_notice`

**Purpose**  
Introduces the main story objective.

**What happens**
- Displays the Wanted Notice image.
- Explains that the player is a hired gun.
- Reveals the target: **Crow Master**.

**Story meaning**
- Confirms the bounty contract.
- Makes the main mission clear.

**Triggered by**
- After `scene1_conversation_end`.

---

## `scene1_wanted_notice_lock_indicator`

**Purpose**  
Prevents repeated triggering of the wanted notice.

**What happens**
- Locks the wanted notice interaction.
- Ensures the notice appears only once.

**Triggered by**
- Immediately after `scene1_wanted_notice`.

---
