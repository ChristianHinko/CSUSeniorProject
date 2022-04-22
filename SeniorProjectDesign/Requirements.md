# Requirements

## 1. Functional
- ID Number: 1a
	- Type: Functional
	- Description: Plugin can successfully compile with a game in Unreal Engine
	- Rationale: The plugin can not be used if it cannot compile
	- Fit Criterion: The game can enable this plugin and compile his game
	- Priority: Essential
	- Dependencies: N/A
- ID Number: 1b
	- Type: Functional
	- Description: Plugin provides a setup for basic ground locomotion animation
	- Rationale: Locomotion is the most foundational feature of character animation
	- Fit Criterion: The implementing game can use this locomotion setup in his Animation Blueprint
	- Priority: Essential
	- Dependencies: 1a

## 2. Look and Feel
- ID Number: 2a
	- Type: Look and Feel
	- Description: 
	- Rationale: 
	- Fit Criterion: 
	- Priority: 
	- Dependencies: N/A

## 3. Usability
- ID Number: 3a
	- Type: Usability - Accessibility
	- Description: Plugin does NOT require the game to inherit any base classes
	- Rationale: Modularity is a core motivation behind this project
	- Fit Criterion: The implementing game can use the provided animation features without the need to restructure their class hierarchy
	- Priority: Essential
	- Dependencies: N/A

## 4. Performance
- ID Number: 4a
	- Type: Performance
	- Description: 
	- Rationale: 
	- Fit Criterion: 
	- Priority: 
	- Dependencies: N/A

## 5. Maintainability and Support
- ID Number: 5a
	- Type: Maintainability and Support
	- Description: The plugin does NOT step outside the scope of animation
	- Rationale: This is strictly an animation plugin and should not care about gameplay code (for example)
	- Fit Criterion: The game can implement this plugin knowning exactly what he is getting from it
	- Priority: Essential
	- Dependencies: N/A

## 6. Security
- ID Number: 6a
	- Type: Security
	- Description: 
	- Rationale: 
	- Fit Criterion: 
	- Priority: 
	- Dependencies: N/A

## 7. Cultural
- ID Number: 7a
	- Type: Cultural
	- Description: 
	- Rationale: 
	- Fit Criterion: 
	- Priority: 
	- Dependencies: N/A
