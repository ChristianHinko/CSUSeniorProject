# Proposal

## Student Name
Christian Hinkle

## Degree and Major
Computer Science (B.S. Degree)

## Project Advisor Name
Lin, Yu-Ju

## Expected Graduation Date
May 2023

## Problem Statement
Game developers should be able to use a generic character animation setup that can be used across multiple games to avoid the making of duplicate code; however, existing solutions heavily intrude on the programmers’ design and lock the game into specific design patterns. Many of these animation plugins require games to inherit from the plugin’s base classes which takes away the ability for programmers to inherit from their own which is a necessary freedom.
A great example of plugins like these would be MoveIt: https://www.unrealengine.com/marketplace/product/moveit-locomotion-system.
MoveIt is a character animation plugin that is generally known to be the best on the Unreal Engine Marketplace; however, MoveIt falls short in providing a modular design. To utilize MoveIt’s animation features, the game must lock itself into strict hierarchical structures; for example, the game must have its character inherit from MoveIt’s AMICharacter class and must have its movement component inherit from MoveIt’s UMICharacterMovementComponent class. This is stepping outside of the bounds of animation and intruding on actual gameplay programming of character movement.
Making use of modular design patterns, this project will provide a character animation setup without forcing rigid designs on the game implementing it. Component-based design and modular animation injection will keep this plugin from stepping on toes of the game. Keeping the animation system away from gameplay code makes the plugin versatile. A variety of games will be able to take advantage of this system while maintaining control over their design choices. Developers will be able to share this plugin code across many of their games.
Current character animation systems do not allow flexible game design while this project will provide modular solutions to implementing a character animation setup.

## Project Description
A modular character animation system implemented as a plugin for games to use in Unreal Engine.
This plugin will provide common character animation features such as basic ground locomotion. This plugin will provide these features compositionally meaning that the game is not limited to using solely the plugin's animation setup. The end product will be a plugin that games can enable and chose to use the given character animation systems as they desire.

## Proposed Implementation Language(s)
- C++
- C#
- Blueprint Visual Scripting

## Libraries, Packages, Development Kits, etc. to be used in the proposed implementation languages(s)
- Unreal Engine

## Additional Software/Equipment Needed
- Git
- GitHub
- Visual Studio Community 2022
- Unreal Engine
- Blender

## Personal Motivation
Character animation is a very crucial and expressive element in video games. I have several years of experience with Unreal Engine but I have been primarily developing game systems as a foundation for future game development with little experience in real-time animation.
My personal motivation for this project is to build that experience of real-time animation programming. Animation is an essential ingredient of games and I am excited to provide a modular solution for it!

## Outline of Future Research Efforts
I will begin my research in animation programming for Unreal Engine beginning Summer 2022. This will undoubtedly tap into the project implementation as I believe that implementation and experimentation are crucial parts of research.
Expected project deliverables include the character animation plugin itself and a demo game project for both demonstrating and testing purposes.
- Necessary research:
	- Animation Instance and Animation Blueprint
	- Control Rig
	- Linked Anim BP
	- Animation Layer Interfaces
	- Jiggle bones, physics, and Anim Dynamics
	- Full Body IK
	- Animation warping
	- Turn in place solutions
	- Animation sharing across separate Skeletal Meshes
	- Utilizing IK for animation sharing
	- Virtual Bones
	- Pose Driver for using Pose Assets (morph targets) based on bone rotation
	- Accounting for animation curves for materials and morph targets
	- Integrating Game Features and Modular Gameplay?
	- Use Gameplay Tags for driving animation?
	- Integration with Gameplay Ability System?

## Schedule
- May 2022
	- Begin research of animation programming in Unreal Engine
	- Create the character animation plugin repository
	- Create the animation demo project repository
- August 2022
	- Begin implementation of the character animation plugin and the demo project
	- Begin the making of a test plan to be used for the end product
- December 2022
	- Begin project testing using the test plan and verify results
	- Report implementation progress
- January 2023
	- Prepare the project for final implementation (last-minute polishing)
	- Begin the making and planning of a final report
	- Begin planning a project presentation
- April 2023
	- Ensure the project passes test plans
	- Finish all construction of the project
	- Finish the making of the final report
	- Finish the making of the project presentation
	- Present project
