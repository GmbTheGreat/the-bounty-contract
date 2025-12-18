# Scene 1 – Opening Cutscene Dialogue Captions

## Purpose
The opening cutscene uses a **caption-based narration system** instead of a single long dialogue box.  
This approach keeps the text readable, matches narration timing, and works smoothly within Zimension’s event system.

---

## Why This System Is Used
- Long paragraphs do not display well in a single message box.
- Captions must stay **in sync with narration audio** (lip-sync feel).
- Zimension handles short, timed UI messages more reliably.
- Improves cinematic feel without complex scripting.

---

## System Overview
- The narration is split into **multiple short lines**.
- Each line is triggered using a **separate event**.
- Every event:
  - Displays one caption
  - Waits for a manually set delay
  - Triggers the next caption event

This creates a smooth, sequential caption flow during the cutscene.

---

## Event Naming Convention
All caption events follow this format:

This makes the order clear and easy to manage.

---

opening_cutscene_dialogue_caption_1
opening_cutscene_dialogue_caption_2
opening_cutscene_dialogue_caption_3
...
opening_cutscene_dialogue_caption_10

<img width="333" height="498" alt="image" src="https://github.com/user-attachments/assets/3f21e304-31b7-41cd-afc9-af27394bb4a5" />

## Caption Breakdown
The original narration is divided into short, readable lines:

1. **This is Dustwood.**
2. **An abandoned town.**
3. **When I arrived**
4. **I saw no one.**
5. **No one lives here now**
6. **Only gangs remain.**
7. **I came here**
8. **Because of a deal with the sheriff.**
9. **He wants me to catch a dangerous bounty hunter**
10. **Crow Master.**

Each line is displayed as a separate caption.

---

## Event Flow Logic
- `opening_cutscene_dialogue_caption_1` starts the sequence.
- After its delay, it triggers:
  opening_cutscene_dialogue_caption_2
- This continues sequentially until:
  opening_cutscene_dialogue_caption_10

<img width="1700" height="368" alt="image" src="https://github.com/user-attachments/assets/a76090b5-3a87-4f4b-a73e-70383dad7bc4" />

Delays are **manually adjusted** to match narration timing.

---

## Benefits of This Approach
- Clean and readable captions
- Easy narration synchronization
- Simple event-based structure
- No complex scripting required
- Easy to edit or extend later

---

## Notes for Future Cutscenes
- Reuse this event-based caption pattern.
- Keep each caption short (one line).
- Adjust delays according to voice pacing.
- Prefer multiple caption events over one long dialogue.

---

## Scene Context
This caption system is part of **Scene 1 – Arrival at Dustwood**, which introduces the setting and story before player interaction begins.

