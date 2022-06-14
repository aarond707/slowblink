# 2D sprites can mark objects in 3D space
##### [[2022-05-21]] > 2D sprites can mark objects in 3D space | 05-21-2022

### How can I mark the position of a 3D object on the screen?

It’s common in triple-A games to have icons over essential objects in the world to help the player navigate and find critical objects.

You might want to mark these entities with crisp 2D icons rendered above everything else. This icon keeps them visible regardless of what’s happening in the game.

For this, you need to map the position of 3D models in the world to 2D screen coordinates. The camera node provides the `unproject_position()` method for this situation.

The camera projects the position onto the screen even if the object is behind
it so you need to check for that.

var is_object_in_front := not is_position_behind(global_position)
sprite.visible = is_object_in_front
if is_object_in_front:
    var screen_position := unproject_position(target.global_position)
    sprite.global_position = screen_position

##### Tags: 