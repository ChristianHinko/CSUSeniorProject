# Requirements

Project Requirements.

## 1. Functional

ID Number: 1a
 - Type: Functional
 - Description: Plugin can successfully compile with a game in Unreal Engine
 - Rationale: The plugin must compile in order to be used
 - Fit Criterion: The game can enable this plugin and compile their game
 - Priority: Essential
 - Dependencies: N/A

ID Number: 1b
 - Type: Functional
 - Description: Plugin provides a way to put together modular characters made up of meshes that share animation
 - Rationale: This is a fundamental feature of the plugin for supporting modular setups
 - Fit Criterion: The implementing game can use this workflow to build their characters
 - Priority: Essential
 - Dependencies: 1a

ID Number: 1c
 - Type: Functional
 - Description: Provide a streamlined way for making an invisible skeleton that can perform animation on its own
 - Rationale: Skeletal animation should be independent of the meshes that use it
 - Fit Criterion: The game runs their animation on the animated skeleton - not the meshes
 - Priority: Essential
 - Dependencies: 1a

ID Number: 1d
 - Type: Functional
 - Description: Our plugin allows the game to use ACharacter::Mesh as a basis for animation
 - Rationale: The default Character's mesh component is commonly used and allows ACharacter::GetMesh() to work as expected
 - Fit Criterion: The game using us can run their animation on ACharacter::Mesh
 - Priority: High
 - Dependencies: 1a

ID Number: 1e
 - Type: Functional
 - Description: Plugin supports animation sharing across different characters
 - Rationale: Animation sharing is a difficult problem to solve and is often game-specific so we should make an effort to make it as easy as possible
 - Fit Criterion: The game uses this plugin and can share animations across different characters without this plugin disrupting it
 - Priority: Medium
 - Dependencies: 1a

ID Number: 1f
 - Type: Functional
 - Description: Plugin provides a character animation setup with basic ground locomotion
 - Rationale: Locomotion is the most foundational feature of character animation
 - Fit Criterion: The implementing game can use this locomotion setup in their Animation Blueprint
 - Priority: Medium
 - Dependencies: 1a

ID Number: 1g
 - Type: Functional
 - Description: Animation features are network replicated when necessary
 - Rationale: Network replication is essential for online multiplayer games and in-game replays
 - Fit Criterion: The game uses our provided animation features and sees that they are properly replicated
 - Priority: Essential
 - Dependencies: 1a

ID Number: 1h
 - Type: Functional
 - Description: Plugin cooperates with online multiplayer games
 - Rationale: We do *not* want to stop the game from being multiplayer
 - Fit Criterion: The game implements our plugin and sees that multiplayer is supported
 - Priority: Essential
 - Dependencies: 1g

ID Number: 1i
 - Type: Functional
 - Description: We provide a workflow that can set up item holding in a character's hands
 - Rationale: Holding items is a difficult problem that we want to try to streamline
 - Fit Criterion: The game uses this to have their character hold weapons in their hands
 - Priority: Low
 - Dependencies: 1a

## 2. Look and Feel

ID Number: 2a
 - Type: Look and Feel - Appearance
 - Description: Plugin's default character animation should look appealing
 - Rationale: It is important to show that this plugin is capable of yielding good results
 - Fit Criterion: The game uses the plugin's default animations and can see the capabilities
 - Priority: Low
 - Dependencies: 1a

## 3. Usability

ID Number: 3a
 - Type: Usability - Accessibility
 - Description: Plugin does *not* require the game to inherit any base classes
 - Rationale: Compositional design is a core motivation behind this project
 - Fit Criterion: The implementing game can use the provided animation features without the need to restructure their class hierarchy
 - Priority: Essential
 - Dependencies: N/A

ID Number: 3b
 - Type: Usability - Accessibility
 - Description: Plugin provides animation features that are usable *without* the game needing to use the whole character animation setup
 - Rationale: We want to keep things modular so, when possible, keep features outside of our character animation setup
 - Fit Criterion: The game can choose *not* to use our character animation setup *but* still make use of helpful animation features
 - Priority: Essential
 - Dependencies: N/A

ID Number: 3c
 - Type: Usability - Accessibility
 - Description: Character animation setup works with first-person, third-person, and any camera style
 - Rationale: This plugin should be able to integrate with any game with any camera setup
 - Fit Criterion: The game switches between first and third person camera modes and our character animation setup supports it
 - Priority: High
 - Dependencies: 1a

ID Number: 3d
 - Type: Personalization and Internationalization
 - Description: Our plugin code is configurable and overridable by the game
 - Rationale: The game should be able to configure this plugin for its needs and override code for any custom functionality
 - Fit Criterion: The game uses this plugin and sees that they can tweak and change the base functionality of the plugin, e.g., functions are marked as virtual and properties are exposed for tweaking
 - Priority: High
 - Dependencies: N/A

ID Number: 3e
 - Type: Usability - Ease of Use
 - Description: Our plugin's design is intuitive and easy to use
 - Rationale: The plugin should be comprehensive for the game because the plugin's design becomes a part of the game's design
 - Fit Criterion: The game using this plugin understands how we fit in with their game design and knows how to integrate us
 - Priority: High
 - Dependencies: N/A

## 4. Performance

ID Number: 4a
 - Type: Performance - Robustness or Fault-Tolerance
 - Description: Plugin code should avoid runtime errors and/or crashes
 - Rationale: The game cannot use this plugin in production if there are potential runtime errors
 - Fit Criterion: The game uses this plugin without it producing any extra possible runtime errors
 - Priority: Essential
 - Dependencies: 1a

ID Number: 4b
 - Type: Performance - Safety-Critical
 - Description: Plugin code should log warnings, errors, and fatal crashes
 - Rationale: It is important for us to inform the game of any problems or incorrect usage
 - Fit Criterion: The game uses this plugin and is notified of any potential problems or notified about incorrect usage of any features
 - Priority: High
 - Dependencies: 1a

ID Number: 4c
 - Type: Performance - Speed and Latency
 - Description: Our character animation code should avoid running on the game thread, via staying on the fast-path worker threads
 - Rationale: Asynchronous animation code is very achievable and this plugin should not take this possibility away from the game
 - Fit Criterion: The game uses the plugin's character animation setup without receiving any fast-path warnings
 - Priority: High
 - Dependencies: 1a

ID Number: 4d
 - Type: Performance - Capacity
 - Description: Network replicated features stay lightweight over the network
 - Rationale: We do *not* want our plugin to bottleneck the game's network bandwidth and replay file storage
 - Fit Criterion: The game using this plugin can safely use any of our network replicated features
 - Priority: High
 - Dependencies: 1g

## 5. Maintainability and Support

ID Number: 5a
 - Type: Maintainability and Support
 - Description: This project utilizes source control for development
 - Rationale: Source control is essential to maintaining code bases, tracking changes, and having a speedy development workflow
 - Fit Criterion: The game sees that this plugin is held in source control and sees that it is maintainable by its developers
 - Priority: Essential
 - Dependencies: N/A

ID Number: 5b
 - Type: Maintainability and Support
 - Description: Our plugin does *not* step outside of the scope of animation
 - Rationale: This is strictly an animation plugin and should not care about gameplay code
 - Fit Criterion: The game can implement this plugin knowing exactly what they are getting from it
 - Priority: Essential
 - Dependencies: N/A

ID Number: 5c
 - Type: Maintainability and Support
 - Description: Our features provided are well-documented
 - Rationale: The plugin features need to be understood by the game in order for them to use them
 - Fit Criterion: The game wants to use a feature provided by this plugin and understands its usage and behavior
 - Priority: High
 - Dependencies: N/A

## 6. Security

ID Number: 6a
 - Type: Security - Immunity
 - Description: This project keeps backups of its content and source code
 - Rationale: Keeping backups, via source control, makes us immune from losing our work and keeps the game safe from losing this plugin
 - Fit Criterion: The game sees that backups of the plugin are being kept by the developers and knows that it will remain safe
 - Priority: Essential
 - Dependencies: 5a

## 7. Cultural
