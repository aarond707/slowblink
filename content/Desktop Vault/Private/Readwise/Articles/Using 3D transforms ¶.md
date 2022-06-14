# Using 3D transforms ¶

![rw-book-cover](https://readwise-assets.s3.amazonaws.com/static/images/article2.74d541386bbf.png)

## Metadata
- Author: [[Godot Docs]]
- Full Title: Using 3D transforms ¶
- Category: #articles
- URL: https://docs.godotengine.org/en/stable/tutorials/3d/using_transforms.html#introduction

## Highlights
- Depending on the type of game or effect desired, the order in which you want axis rotations to be applied may differ. Therefore, applying rotations in X, Y, and Z is not enough: you also need a rotation order.
- The result of all this is that you should not use the rotation property of Spatial [[nodes]] in Godot for games. It's there to be used mainly in the editor, for coherence with the 2D engine, and for simple rotations (generally just one axis, or even two in limited cases). As much as you may be tempted, don't use it.
- Godot uses the Transform datatype for orientations. Each Spatial node contains a transform property which is relative to the parent's transform, if the parent is a Spatial-derived type.
  It is also possible to access the world coordinate transform via the global_transform property.
- A transform has a Basis (transform.basis sub-property), which consists of three Vector3 vectors. These are accessed via the transform.basis property and can be accessed directly by transform.basis.x, transform.basis.y, and transform.basis.z. Each vector points in the direction its axis has been rotated, so they effectively describe the node's total rotation. The scale (as long as it's uniform) can also be inferred from the length of the axes. A basis can also be interpreted as a 3x3 matrix and used as transform.basis[x][y].
- It is recommended you not scale [[nodes]] that are going to be manipulated; scale their children [[nodes]] instead (such as MeshInstance). If you absolutely must scale the node, then re-apply it at the end:
- You might be thinking at this point: "Ok, but how do I get angles from a transform?". The answer again is: you don't. You must do your best to stop thinking in angles.
  Imagine you need to shoot a bullet in the direction your [[player]] is facing. Just use the forward axis (commonly Z or -Z).
