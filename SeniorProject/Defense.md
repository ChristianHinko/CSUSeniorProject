# AnimationSetup

May 2023

Christian Hinkle

Bachelor of Science in Computer Science

Lin, Yu-Ju

## Statement of Purpose (with the Problem Statement)

Game programmers should have the ability to use a generic character animation setup that can be used across multiple games to avoid making duplicate code; however, existing solutions heavily intrude on the programmers' design and lock the game into specific design patterns. Many of these character setup plugins require games to inherit from the plugin's base classes. This takes away the ability for programmers to inherit from their own classes which is a necessary freedom.

An example of plugins like these is MoveIt: https://www.unrealengine.com/marketplace/product/moveit-locomotion-system.

MoveIt is a character animation plugin that is generally known to be the best on the Unreal Engine Marketplace; however, MoveIt falls short in providing a modular design. To utilize MoveIt's animation features, the game must lock itself into strict hierarchical structures; for example, the game must have its character inherit from MoveIt's MICharacter class and must have its movement component inherit from MoveIt's MICharacterMovementComponent class. This is stepping outside of the bounds of animation tools and intruding on gameplay programming of character movement.

Making use of modular design patterns, this project will provide a character setup without forcing rigid designs on the game implementing it. Component-based designs and procedural programming will keep this plugin from stepping on toes of the game project. Keeping the animation system away from gameplay code makes the plugin versatile. A variety of games will be able to take advantage of these systems while maintaining control over their design choices. Developers will be able to share the code of this plugin across many of their games.

Current character systems do not allow flexible game design while this project will provide modular solutions to implementing a character animation setup.

## Research & Background

## Project Language(s), Software, and Hardware

Programming Languages
- C++
- Blueprint Visual Scripting
- C#

Software
- Unreal Engine
- Git
- Git Bash
- GitHub
- Visual Studio
- Blender

Hardware
- Personal computer

## Project Requirements

[Requirements](./Requirements.md)

## Project Implementation Description & Explanation

The Animation Setup plugin provides tools for putting together modular characters and performing common character mesh setup.

The skinless Skeletal Mesh system generates an animated skeleton that serves as the foundation for attaching modular character parts. The attached meshes may copy the animation, e.g., a character's arm moving, while others may perform their own animation, e.g., a character's gun shooting. This separation allows skeletal animation to be independent of Skeletal Meshes.

## Test Plan

## Test Results

## Challenges Overcome

## Future Enhancements

## Defense Presentation Slides