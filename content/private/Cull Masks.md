# Cull Masks
##### [[2022-05-21]] > Cull Masks | 05-21-2022

What are Cull Masks?

Culling is the process of hiding some geometry from rendering. Godot comes with rendering layers you can use to hide objects and lights from specific cameras.

You can assign any 3D mesh or light node to different rendering layers.

![](data:image/png;base64,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)

If you unset the corresponding bit on a ![](data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjE2IiB2aWV3Qm94PSIwIDAgMTYgMTYiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj48cGF0aCBkPSJtOSAxMDM4LjRhMyAzIDAgMCAwIC0yLjk4ODMgMi43Nzc0IDMgMyAwIDAgMCAtMi4wMTE3LS43Nzc0IDMgMyAwIDAgMCAtMyAzIDMgMyAwIDAgMCAyIDIuODI0M3YyLjE3NTdjMCAuNTU0LjQ0NTk5IDEgMSAxaDZjLjU1NDAxIDAgMS0uNDQ2IDEtMXYtMWwzIDJ2LTZsLTMgMnYtMS43Njk1YTMgMyAwIDAgMCAxLTIuMjMwNSAzIDMgMCAwIDAgLTMtM3oiIGZpbGw9IiNmYzljOWMiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDAgLTEwMzYuNCkiLz48L3N2Zz4K)`Camera` node’s _Cull Mask_ property, the related geometry and lights don’t render when the ![](data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjE2IiB2aWV3Qm94PSIwIDAgMTYgMTYiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj48cGF0aCBkPSJtOSAxMDM4LjRhMyAzIDAgMCAwIC0yLjk4ODMgMi43Nzc0IDMgMyAwIDAgMCAtMi4wMTE3LS43Nzc0IDMgMyAwIDAgMCAtMyAzIDMgMyAwIDAgMCAyIDIuODI0M3YyLjE3NTdjMCAuNTU0LjQ0NTk5IDEgMSAxaDZjLjU1NDAxIDAgMS0uNDQ2IDEtMXYtMWwzIDJ2LTZsLTMgMnYtMS43Njk1YTMgMyAwIDAgMCAxLTIuMjMwNSAzIDMgMCAwIDAgLTMtM3oiIGZpbGw9IiNmYzljOWMiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDAgLTEwMzYuNCkiLz48L3N2Zz4K)`Camera`’s active.

![](data:image/png;base64,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)

You can use that property to make objects invisible unless the player uses a special item or spell. It can also help with rendering performance as culled objects don’t render.

##### Tags: 