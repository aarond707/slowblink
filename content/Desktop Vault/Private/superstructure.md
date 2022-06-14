# superstructure
## The Pitch
[[superstructure is a marxian play on megastructure]]

[[superstructure is small in scope but with big windows out]]
## References
### Docs
[[Godot Toolbox]]
### Inspirations
- [[Godspeed You! Black Emperor]]
	- "[[We're all trapped in the belly of this horrible machine]], and the machine is bleeding to death." This metaphor can be literalized.
		- The liberal response is to climb to the surface, the [[base]], and transform it from within. This isn't the radical answer, and it allows the superstructure to continue being a universe-consuming singularity.
- [[STALKER]] 
	- I want this game to also take advantage of [[the benefits of matching player and npc rules and actions]].
- [[FromSoftware]]
	- [[message retrieval]] is a mechanic idea.
	- I want to try [[stretching the meter-management loop]] in this game.
- [[Kentucky Route Zero]]
- [[Iron Lung]]
- [[A Bewitching Revolution]]
- [[Citizen Sleeper]]
	- [[clocks and project mech]]
- [[Blame!]]
	* The [[superstructure (concept)]] is a reference to the Megastructure


## Pipelines
When I'm not sure what to work on, these are aspects of the game that can always be fed or carried down to line to other aspects. This isn't necessarily a to-do in that a lot of it is work that can be repeated.
### Research Pipeline
#### [[Aseprite]]
##### Color mixing systems
#### Godot
https://graydwarf.itch.io/godot-companion
##### [[gdscript]]
##### [[nodes]]
##### References
##### Patterns and Recipes
- [[Art books]]
### Prototyping Pipeline
#### Gameplay Features
##### Mech Movement
If the mech has a throttle system, then its forward and backward movement can still be bound to W and S, but those will increase and decrease forward movement rather than switching forward and backward on and off. They will also lock the mech into a state from which strafing is not possible. Strafing can only be done when in a [[strafe state]] rather than the [[walk state]]. Firing a weapon is also mutually exclusive with the strafe or walk states, and can override them. This is the [[firing state]]. The [[grapple state]] is what we enter when preparing a jump or when hanging onto the side of a wall. This system will require a [[finite state machine]] (see also: [[Private/Readwise/Articles/Finite State Machine in Godot · GDQuest]]).
##### Mech Turning
The mouse inputs currently are modulated by mouse dpi * a variable that controls the rate of turning per mouse movement. Rather than this function controlling the head rotation of the player character node, this should control a crosshair for the player's view.

Whether it directly controls the 2D screen space crosshair or simply an invisible rotator that then controls the 2D crosshair I haven't decided. Doing this should be the first step, because the actual player head then follows this crosshair and its own rate with easing applied. Or no easing, potentially. Lots of sound effects, though.
#### Playtesting
### Content Pipeline
#### Visuals
##### [[Color Palettes]]
##### 2D
- Wall textures
- Character designs
- Sketching
##### 3D
#### Audio
##### SFX
##### OST
## [[_this horrible machine_]]