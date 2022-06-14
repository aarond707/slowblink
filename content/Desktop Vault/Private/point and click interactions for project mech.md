# point and click interactions for project mech
##### [[2022-05-08]] > point and click interactions for project mech | 05-09-2022

- I just need to make my first-person controller press a damn button 
	- [RayCast — Godot Engine (stable) documentation in English](https://docs.godotengine.org/en/stable/classes/class_raycast.html)
		- Raycast is the thing I need to use to see whether or not the player is looking at a button. The next thing I need to check is how close the player is to the button, which I don't know the function for.
		- I think I might have found what I need to do in order to get the distance between two spatial nodes, or objects.
		- If both of those conditions are met and we're not in the middle of something (use a bool), then we interact with whatever we looked at. The interaction that occurs depends on what was interacted with, and possibly other flags. 
			- It could be another bool, but that bool could change depending on many others. Keeping possible states binary

##### Tags: 