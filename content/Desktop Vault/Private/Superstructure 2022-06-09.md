I'm trying to make the head and body rotation on my mech controller work the way I'm envisioning it and it's giving me hell, but it's a good exercise.

The head rotation is 1:1 with the mouse currently, but I've decoupled it from turning the actual body.

- [x] The next step is to make the body (Player node) rotate to follow the head rotation. I think I have it lerp to the rotation of the head, but I'm having tons of trouble just getting these things to reference each other. 

I am also using a position3D to place my follow cursor, but I'm not sure if I'm having success there yet. That placement also is not yet important.

[[I found a good FPS template]]

I landed on this weird non-solution where I'm trying to make the two nodes rotate to meet each other half-way, and it's not what I actually need. I want to change the world-rotation of the head, not its relative rotation. Or rather, I need to make it ignore rotations from the body, or counter-rotate.

So I've got it doing counter-rotations. I still don't love this solution given that it's very drifty and is moving and counter-moving, but it works for right now. I think I need to make the head just ignore the rotations of the parent, or I need a way to just make the head entirely independent and _only_ adopt the position from the parent.