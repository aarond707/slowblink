# Reference

![rw-book-cover](https://readwise-assets.s3.amazonaws.com/static/images/article0.00998d930354.png)

## Metadata
- Author: [[Godot Docs]]
- Full Title: Reference
- Category: #articles
- URL: https://docs.godotengine.org/en/stable/classes/class_reference.html#class-reference

## Highlights
- Base [[class]] for any object that keeps a reference count. Resource and many other helper objects inherit this class.
  Unlike other Object types, References keep an internal reference counter so that they are automatically released when no longer in use, and only then. References therefore do not need to be freed manually with Object.free.
