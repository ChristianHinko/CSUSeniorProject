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
Game developers should be able to use a generic character setup (animation and camera) that can be used across multiple games to avoid the making of duplicate code; however, existing solutions heavily intrude on the programmers' design and lock the game into specific design patterns. Many of these character setup plugins require games to inherit from the plugin's base classes. This takes away the ability for programmers to inherit from their own classes which is a necessary freedom.

A great example of plugins like these is MoveIt: https://www.unrealengine.com/marketplace/product/moveit-locomotion-system.

MoveIt is a character animation plugin that is generally known to be the best on the Unreal Engine Marketplace; however, MoveIt falls short in providing a modular design. To utilize MoveIt's animation and camera features, the game must lock itself into strict hierarchical structures; for example, the game must have its character inherit from MoveIt's MICharacter class and must have its movement component inherit from MoveIt's MICharacterMovementComponent class. This is stepping outside of the bounds of animation/camera tools and intruding on gameplay programming of character movement.

Making use of modular design patterns, this project will provide a character setup without forcing rigid designs on the game implementing it. Component-based design and modular injection will keep these plugins from stepping on toes of the game. Keeping the animation and camera systems away from gameplay code makes the plugins versatile. A variety of games will be able to take advantage of these systems while maintaining control over their design choices. Developers will be able to share the code of these plugins across many of their games.

Current character systems do not allow flexible game design while this project will provide modular solutions to implementing a character animation and camera setup.


## Project Description
A modular character animation and camera system implemented as plugins for games to use in Unreal Engine.

The AnimationSetup plugin will provide common setup for skeletal animation such as modular mesh handling and first person handling.

The CameraSetup plugin will provide tools and abstractions on top of the engine's existing camera functionality for working with and managing cameras.

These plugins will implement their systems as independently as possible. This will be achieved through compositional design so that the game is not limited to using solely the plugins' systems. The end product will be the two plugins where games can enable and use the given tools as they desire. The game should be able to pick and choose what they want from the plugins.

An example game project will combine the features of AnimationSetup and CameraSetup for easy character setup with modular meshes and first person support.


## Proposed Implementation Language(s)
Languages
- C++
- C#
- Blueprint Visual Scripting


## Libraries, Packages, Development Kits, etc. to be used in the proposed implementation languages(s)
Development Kits
- Unreal Engine


## Additional Software/Equipment Needed
Development Software
- Git
- Git Bash
- GitHub
- Visual Studio 2022
- Unreal Engine
- Blender


## Personal Motivation
Character animation is a very crucial and expressive element in video games. I have several years of experience with Unreal Engine but I have been primarily developing game systems as a foundation for future game development with little experience in real-time animation.

My personal motivation for this project is to build up that experience of real-time animation programming. Along with an animation setup, camera managing is necessary in order to support and test first-person views. Animation is an essential ingredient of games and I am excited to provide a modular solution for it!


## Outline of Future Research Efforts
I will begin my research in animation programming for Unreal Engine beginning Summer 2022. This will undoubtedly tap into the project implementation as I believe that implementation and experimentation are crucial parts of research.

I will begin my research of camera systems in Unreal Engine during the construction of the animation plugin. The moment I get to a point where I need camera functionality, I will switch gears and start on the camera plugin.

Expected project deliverables include the plugins themselves, and a demo game project for both demonstration and testing purposes.

AnimationSetup
- Animation Features
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
- Mesh
    - Modular meshes
    - Invisible skeletal mesh
    - SkeletalMeshMerge
    - USkinnedMeshComponent::MasterPoseComponent
    - First-person mesh
    - Separate meshes for first-person and external view
    - Sharing meshes between first-person and external view
    - Separate animations for first-person and external view

CameraSetup
- PlayerCameraManager
- CameraComponent
- MinimalViewInfo
- CameraModifier
- CameraAnim - deprecated?
- Replication of AController::ControlRotation
- Camera modes system
- Blending between several Camera Components (and view targets)
- Single Camera Component controlled procedurally or multiple Camera Components with blending?
- AActor::CalcCamera()
- Camera Component attached to socket on Skeleton?


## Schedule
May 2022
 - Begin research of animation programming in Unreal Engine
 - Create the AnimationSetup plugin repository
 - Create the CameraSetup plugin repository
 - Create the demo project repository

August 2022
 - Begin implementation of the AnimationSetup plugin and the demo project
 - Begin the making of a test plan to be used for the end product
 - Begin research in camera systems in Unreal Engine

December 2022
 - Begin implementation of the camera systems plugin
 - Begin research in character first-person setups
 - Begin project testing using the test plan and verify results
 - Report implementation progress

January 2023
 - Begin implementation of full character setup
 - Prepare the project for final implementation (last-minute polishing)
 - Begin the making and planning of a final report
 - Begin planning a project presentation

April 2023
 - Ensure the project passes test plans
 - Finish all construction of the project
 - Finish the making of the final report
 - Finish the making of the project presentation
 - Present project
