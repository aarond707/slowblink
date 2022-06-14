# Introduction to shaders ¶

![rw-book-cover](https://readwise-assets.s3.amazonaws.com/static/images/article3.5c705a01b476.png)

## Metadata
- Author: [[Godot Docs]]
- Full Title: Introduction to shaders ¶
- Category: #articles
- Document Tags: [[Godot]] 
- URL: https://docs.godotengine.org/en/stable/tutorials/shaders/introduction_to_shaders.html

## Highlights
- Because of their parallel nature, though, shaders don't process information the way a typical program does. Shader code runs on each vertex or pixel in isolation. You cannot store data between frames either. As a result, when working with shaders, you need to code and think differently from other programming languages.
- Instead of supplying a general-purpose configuration for all uses (2D, 3D, particles), you must specify the type of shader you're writing. Different types support different render modes, built-in variables, and processing functions.
  In Godot, all shaders need to specify their type in the first line, like so:
  shader_type spatial;
  Here are the available types:
  spatial for 3D rendering.
  canvas_item for 2D rendering.
  particles for particle systems.
- Depending on the shader type, you can override different processor functions. For spatial and canvas_item, you have access to vertex(), fragment(), and light(). For particles, you only have access to vertex().
