# Prototyping levels with CSG ¶

![rw-book-cover](https://readwise-assets.s3.amazonaws.com/static/images/article3.5c705a01b476.png)

## Metadata
- Author: [[Godot Docs]]
- Full Title: Prototyping levels with CSG ¶
- Category: #articles
- URL: https://docs.godotengine.org/en/stable/tutorials/3d/csg_tools.html

## Highlights
- CSG stands for Constructive Solid Geometry, and is a tool to combine basic shapes or custom meshes to create more complex shapes. In 3D modelling software, CSG is mostly known as "Boolean Operators".
  Level prototyping is one of the main uses of CSG in Godot. This technique allows users to create simple versions of most common shapes by combining primitives. Interior environments can be created by using inverted primitives.
- The CSG [[nodes]] in Godot are mainly intended for prototyping. There is no built-in support for UV mapping or editing 3D polygons (though extruded 2D polygons can be used with the CSGPolygon node).
- To apply triplanar mapping to a CSG node, select it, go to the Inspector, click the [empty] text next to Material Override (or Material for individual CSG [[nodes]]). Choose New SpatialMaterial. Click the newly created material's icon to edit it. Unfold the Albedo section and load a texture into the Texture property. Now, unfold the Uv1 section and check Triplanar. You can change the texture offset and scale on each axis by playing with the Scale and Offset properties just above. Higher values in the Scale property will cause the texture to repeat more often.
- You can copy a SpatialMaterial to reuse it across CSG [[nodes]]. To do so, click the dropdown arrow next to a material property in the Inspector and choose Copy. To paste it, select the node you'd like to apply the material onto, click the dropdown arrow next to its material property then choose Paste.
