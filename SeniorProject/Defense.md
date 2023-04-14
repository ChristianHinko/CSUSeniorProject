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

The research strategy for this project started off very confused and scattered due to my lack of experience in realtime character animation.

Part of the research was figuring out what exactly I needed the plugin to do. I knew that I wanted to make progress on creating video games and that character animation was the next step on the path. I knew that I wanted the functionality separated into a portable plugin for use in several games. I just needed to know what to implement.

I began by reading the entire "Skeletal Mesh Animation System" documentation which is comprised of 131 individual webpages. I did this to make myself aware of all animation features so that I can avoid reinventing already-existing ones and use them to my advantage where possible.

I then researched approaches to animation that other games take. While digging through Epic Games' sample game project, "Lyra", I stumbled upon their "invis" Skeletal Meshes. These are essentially skeletons that can animate independently while attached meshes can copy their poses.

With my newly-learned information, I was a little overwhelmed. Do I make generic animation solutions such as ground locomotion, animation sharing, and turn-in-place? Do I make a first-person mesh and third-person mesh system for different camera views?

The plugin should focus on fundamental character mesh setup instead of making animation-specific features. I concluded this after adding characters to a game and realizing that there was no workflow for assembling modular characters while having animation logic separated from the meshes.

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
