### Train Departure Transition (Optimization Event)

<img width="1252" height="755" alt="image" src="https://github.com/user-attachments/assets/d769bb54-ede5-408f-85e1-d0bf0965551c" />

At the start of Scene 1, the train arrives at Dustwood as part of the opening cinematic.
Once the cinematic is complete and the train moves out of the playable area, it is no longer required in the scene.

To optimize performance and reduce unnecessary world objects, the train is removed after its final movement.

- The train uses a Transition system with multiple states to control its cinematic movement:

  - Initial State:
    Train is positioned at the station during the opening cutscene.

  - State 1:
    Train starts moving forward from the station.

  - State 2:
    Train continues moving away from the playable area.

  - State 3:
    Train moves further toward the mountains until it is completely out of view.

- The transition is configured as:
  - Play On: On Start

- Once State 3 is completed, the transition triggers the `disappear_train` event.

- This event removes or hides the train from the world, ensuring it does not consume resources after the cinematic ends.

<img width="315" height="613" alt="image" src="https://github.com/user-attachments/assets/91f7f5b4-6315-4bdd-bb32-a0bb781f4941" />

The train is only needed for storytelling during the opening cutscene.
After the player gains control, the train has no gameplay purpose.

Removing it after the cutscene:
- Improves performance
- Avoids unnecessary rendering
- Keeps Scene 1 focused on exploration

