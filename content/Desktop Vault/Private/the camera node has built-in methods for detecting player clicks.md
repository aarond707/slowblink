# the camera node has built-in methods for detecting player clicks
##### [[2022-05-21]] > the camera node has built-in methods for detecting player clicks | 05-21-2022

### Detecting where the player clicked

In some games, the player needs to interact with 3D objects in the game world using their mouse or touchscreen as a 2D input.

A camera comes with two methods: `project_ray_normal()` and `project_ray_origin()`. These methods project 2D positions from the screen into the 3D world. `project_ray_normal()` returns the surface’s normal direction, while `project_ray_origin()` returns the 3D position in the 3D world.

However, these two methods only calculate points in space. You can use the `PhysicsDirectSpaceState` singleton to convert these points in space into a ray cast.

func _cast_ray_from_mouse() -> Dictionary:
    var mouse_position := get_viewport().get_mouse_position()
    # Project the 2D mouse position onto the camera.
    var from: Vector3 = project_ray_origin(mouse_position)
    # Project the 2D mouse position into the world from the camera.
    var to: Vector3 = from + project_ray_normal(mouse_position) * 1000
    # Ask the physics engine to do a raycast and return the result.
    return get_world().direct_space_state.intersect_ray(from, to, [self])

The function above returns an empty dictionary if the calculated ray does not intersect with anything. If the ray touches something, the dictionary gives you the position of the collision, the collider it hit, the collision normal, and other information if needed.

var result := _cast_ray_from_mouse()
if not result.empty():
    var collision_point: Vector2 = result.position
    var collision_normal: Vector2 = result.normal
    var collider: PhysicsBody2D = result.collider

You can find all the details in Godot’s [PhysicsDirectSpaceState documentation](https://docs.godotengine.org/en/stable/classes/class_physicsdirectspacestate.html#class-physicsdirectspacestate-method-intersect-ray).

##### Tags: #gdquest