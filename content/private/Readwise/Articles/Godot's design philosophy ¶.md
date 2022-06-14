# Godot's design philosophy ¶

![rw-book-cover](https://readwise-assets.s3.amazonaws.com/static/images/article3.5c705a01b476.png)

## Metadata
- Author: [[Godot Docs]]
- Full Title: Godot's design philosophy ¶
- Category: #articles
- URL: https://docs.godotengine.org/en/stable/getting_started/introduction/godot_design_philosophy.html#object-oriented-design-and-composition

## Highlights
- For one, Godot lets you compose or aggregate scenes. It's like nested prefabs: you can create a BlinkingLight scene and a BrokenLantern scene that uses the BlinkingLight. Then, create a city filled with BrokenLanterns. Change the BlinkingLight's color, save, and all the BrokenLanterns in the city will update instantly.
- Also note that Godot offers many different types of objects called [[nodes]], each with a specific purpose. Nodes are part of a tree and always inherit from their parents up to the Node [[class]]. Although the engine does feature some nodes like collision shapes that a parent physics body will use, most nodes work independently from one another. In other words, Godot's nodes do not work like components in some other game engines.
