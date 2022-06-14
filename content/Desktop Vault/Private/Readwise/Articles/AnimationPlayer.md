# AnimationPlayer

![rw-book-cover](https://readwise-assets.s3.amazonaws.com/static/images/article1.be68295a7e40.png)

## Metadata
- Author: [[Godot Docs]]
- Full Title: AnimationPlayer
- Category: #articles #animation
- URL: https://docs.godotengine.org/en/stable/classes/class_animationplayer.html?highlight=animationplayer

## Highlights
- An animation player is used for general-purpose playback of Animation resources. It contains a dictionary of animations (referenced by name) and custom blend times between their transitions. Additionally, animations can be played and blended in different [[channels]].
- AnimationPlayer is more suited than Tween for animations where you know the final values in advance. For example, fading a screen in and out is more easily done with an AnimationPlayer node thanks to the animation tools provided by the editor. That particular example can also be implemented with a Tween node, but it requires doing everything by code.
  Updating the target properties of animations occurs at process time.
