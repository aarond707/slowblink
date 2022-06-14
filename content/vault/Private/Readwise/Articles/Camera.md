# Camera

![rw-book-cover](https://readwise-assets.s3.amazonaws.com/static/images/article2.74d541386bbf.png)

## Metadata
- Author: [[Godot Docs]]
- Full Title: Camera
- Category: #articles
- URL: https://docs.godotengine.org/en/stable/classes/class_camera.html#class-camera

## Highlights
- Camera is a special node that displays what is visible from its current location. Cameras register themselves in the nearest Viewport [[node]] (when ascending the tree). Only one camera can be active per viewport. If no viewport is available ascending the tree, the camera will register in the global viewport. In other words, a camera just provides 3D display capabilities to a Viewport, and, without one, a scene registered in that Viewport (or higher viewports) can't be displayed.
