# you can find out whether an object is in front of the camera
##### [[2022-05-21]] > you can find out whether an object is in front of the camera | 05-21-2022

### How can I find if an object is in front of the camera?

We often need to compare where the ![](data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjE2IiB2aWV3Qm94PSIwIDAgMTYgMTYiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj48cGF0aCBkPSJtOSAxMDM4LjRhMyAzIDAgMCAwIC0yLjk4ODMgMi43Nzc0IDMgMyAwIDAgMCAtMi4wMTE3LS43Nzc0IDMgMyAwIDAgMCAtMyAzIDMgMyAwIDAgMCAyIDIuODI0M3YyLjE3NTdjMCAuNTU0LjQ0NTk5IDEgMSAxaDZjLjU1NDAxIDAgMS0uNDQ2IDEtMXYtMWwzIDJ2LTZsLTMgMnYtMS43Njk1YTMgMyAwIDAgMCAxLTIuMjMwNSAzIDMgMCAwIDAgLTMtM3oiIGZpbGw9IiNmYzljOWMiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDAgLTEwMzYuNCkiLz48L3N2Zz4K)`Camera` is relative to other objects. For example, enemies won’t attack you in some action games if they are behind the ![](data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjE2IiB2aWV3Qm94PSIwIDAgMTYgMTYiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj48cGF0aCBkPSJtOSAxMDM4LjRhMyAzIDAgMCAwIC0yLjk4ODMgMi43Nzc0IDMgMyAwIDAgMCAtMi4wMTE3LS43Nzc0IDMgMyAwIDAgMCAtMyAzIDMgMyAwIDAgMCAyIDIuODI0M3YyLjE3NTdjMCAuNTU0LjQ0NTk5IDEgMSAxaDZjLjU1NDAxIDAgMS0uNDQ2IDEtMXYtMWwzIDJ2LTZsLTMgMnYtMS43Njk1YTMgMyAwIDAgMCAxLTIuMjMwNSAzIDMgMCAwIDAgLTMtM3oiIGZpbGw9IiNmYzljOWMiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDAgLTEwMzYuNCkiLz48L3N2Zz4K)`Camera`.

The method `is_position_behind()` returns true if an object is behind the ![](data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjE2IiB2aWV3Qm94PSIwIDAgMTYgMTYiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj48cGF0aCBkPSJtOSAxMDM4LjRhMyAzIDAgMCAwIC0yLjk4ODMgMi43Nzc0IDMgMyAwIDAgMCAtMi4wMTE3LS43Nzc0IDMgMyAwIDAgMCAtMyAzIDMgMyAwIDAgMCAyIDIuODI0M3YyLjE3NTdjMCAuNTU0LjQ0NTk5IDEgMSAxaDZjLjU1NDAxIDAgMS0uNDQ2IDEtMXYtMWwzIDJ2LTZsLTMgMnYtMS43Njk1YTMgMyAwIDAgMCAxLTIuMjMwNSAzIDMgMCAwIDAgLTMtM3oiIGZpbGw9IiNmYzljOWMiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDAgLTEwMzYuNCkiLz48L3N2Zz4K)`Camera`. It considers the field of view, making it convenient to check if the player can see or interact with an object.

Imagine a chest with an area that controls when the player can interact with it. You may want to ensure that the player is facing the chest before opening it.

var can_see_object := not is_position_behind(object.global_position)

This method only works with global positions.

##### Tags: 