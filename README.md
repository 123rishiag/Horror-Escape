# Horror Escape Game

A spine-chilling horror escape game where players must survive, collect keys, unlock doors, and manage their sanity in a dark, immersive environment. The game incorporates the Observer Pattern to handle in-game events, such as lights turning off due to ghostly influences, object interactions, and environmental challenges like Rat Rush and Skull Drop that test the player’s sanity management.

## Features

### Game Mechanics
- **Key Collection and Door Unlocking**: Players must find all required keys to unlock the final door and progress through the game. Each door requires a specific number of keys to be unlocked.
- **Sanity Management**: The player's sanity is affected by various environmental triggers. When lights turn off unexpectedly, the player's sanity meter increases rapidly. Environmental challenges like Rat Rush and Skull Drop cause sudden spikes in sanity, adding pressure and tension to the gameplay. Potions can be used to decrease sanity levels, helping players regain composure.
- **Interactable Objects**: Players can interact with various objects, such as doors, light switches, keys, and potions, each impacting their progress and survival.

### Project Structure

#### Player Files
- `PlayerSanity.cs`: Manages the player's sanity and reactions to events.
- `PlayerController.cs`: Controls player movements and interactions.
- `PlayerView.cs`: Acts as a view component for handling player-related interactions in the game world.
- `PlayerState.cs`: Defines player states (e.g., Calm, High Anxiety).
- `PlayerScriptableObject.cs`: Stores player-specific data.

#### Interactables
- `IInteractable.cs`: Interface defining interactions for all interactable objects.
- `DoorView.cs`: Controls door behavior and unlocking logic.
- `DoorState.cs`: Represents door states (e.g., Locked, Unlocked).
- `LightSwitchView.cs`: Manages interactions with light switches.
- `SwitchState.cs`: Tracks switch state (On/Off).
- `PotionView.cs`: Allows players to decrease their sanity levels, helping regain composure.
- `KeyView.cs`: Represents collectible keys.

#### Event System
- `EventService.cs`: Manages and broadcasts events using the Observer Pattern.
- `EventController.cs`: Handles event subscriptions and interactions.
- `LightsOffByGhostEvent.cs`: Represents a ghostly event where lights are turned off, causing a rapid increase in player sanity.
- `SkullDropEvent.cs`: An event involving falling skulls that causes a sudden spike in player sanity.
- `RatRushEvent.cs`: An event involving a sudden rush of rats that causes a sudden spike in player sanity.
- `PlayerEscapedEvent.cs`: Event triggered when the player successfully escapes.

#### Sound Management
- `SoundView.cs`: Manages in-game sound effects.
- `Sounds.cs`: Defines sound-related properties and effects.
- `SoundType.cs`: Enum for categorizing different sound types.

#### Camera Management
- `CameraView.cs`: Handles camera positioning and movement.

#### UI Files
- `MainMenuUIView.cs`: Manages the main menu interface.
- `GameUIView.cs`: Handles in-game HUD elements, including sanity levels and key counts.
- `InstructionView.cs`: Displays instructions during gameplay.
- `InstructionType.cs`: Enum for instruction categories.
- `InstructionScriptableObject.cs`: Stores instruction data for UI.

#### Utility Files
- `GenericMonoSingleton.cs`: Utility script for implementing singletons.

#### Services
- `GameService.cs`: Manages game state transitions and core game logic.

## Learning Outcomes
- **Observer Pattern Implementation**: Applied an event-driven system using the Observer Pattern for flexible interactions and events.
- **Key and Door Mechanics**: Developed a key collection system tied to door unlocking logic and environmental triggers.
- **Sanity System**: Designed a reactive sanity management system affected by environmental triggers, with rapid increases from lights turning off and sudden spikes from environmental challenges, mitigated by potion usage.
- **UI Design and Interaction**: Created an engaging and reactive UI for real-time player feedback.

## Setting Up the Project
1. Clone the Repository:
   ```bash
   git clone https://github.com/123rishiag/Horror-Escape.git
   ```
2. Open the project in Unity.

## Video Demo
[Watch the Video Demo](https://www.loom.com/share/5a0cf68828dd41e3b91bdf38c4543852?sid=89901b89-3cf0-4a73-b019-12bcc4ea4fd8)

## Play Link
[Play the Game](https://outscal.com/narishabhgarg/game/play-horror-escape-46-game)