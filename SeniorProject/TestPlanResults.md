# TestPlanResults

Test plan with results.

## Functional

Test A: Plugin can successfully compile with a game in Unreal Engine.
 - Results: Example game project CharacterDemo compiles with the plugin.

Test B: Plugin provides a way to put together modular characters made up of meshes that share animation.
 - Results: The AttachmentAttacher component allows you to attach modular attachments to your character.

Test C: Plugin supports animation sharing across different characters.
 - Results: Although the plugin does not provide a direct animation sharing solution, it does support this.

Test D: SkinlessSkeletalMesh component can use the character mesh component as a host for an animated skeleton.
 - Results: When choosing a skeleton to use, the character mesh turns into an animated skeleton.

Test E: AttachmentAttacher component can use attach actor attachments to the character.
 - Results: The actors are spawned and attached upon adding them in the blueprint editor.

Test F: We can make a first-person portrayal for only the character to see.
 - Results: Only the character can see his first-person portrayed meshes in the example CharacterDemo game project.

## Look and Feel
Test G: Plugin's default character animation should look appealing.
 - Results: The CharacterDemo game project has appealing animation results by using the mannequin assets.

## Usability
Test H: Plugin does *not* require the game to inherit any base classes.
 - Results: The only base classes apparent are functional example classes which are not required.

Test I: Plugin provides animation features that are usable *without* the game needing to use the whole character animation setup.
 - Results: SkinlessSkeletalMesh, AttachmentAttacher, and PortrayalAssignment component are separated from each other. The game does not need to use all of them.

Test J: Character animation setup works with first-person, third-person, and any camera style.
 - Results: The portrayal system provides a workflow for using components in different views.

Test K: Our plugin code is configurable and overridable by the game.
 - Results: Virtual functions are overridable and delegates are provided for external implementations.

Test L: Our plugin's design is intuitive and easy to use.
 - Results: Components are well-designed and intuitive for advanced users but may be complex for beginners.

## Performance
Test M: Plugin code should avoid runtime errors and/or crashes.
 - Results: No runtime errors occured while developing and running the CharacterDemo example project.
