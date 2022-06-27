---
layout: post
title:  "Ori Air Movement"
date:   2021-06-19 12:12:00 -0700
categories: Ori
published: true
---

## Air Movement

This section covers general movement in the air. 

When in the air, holding left or right causes you to start accelerating in that direction. Unlike ground movement, the actual value of the X input doesn't matter. As long as you are past the 41% threshold, acceleration happens. There is no difference in speed or acceleration between holding the stick all the way or just barely past the necessary value. The maximum air speed gained this way is equal to the maximum ground speed achieved by running. Holding full right is equally fast on the ground as in the air, though air movement doesn't have to deal with slopes changing velocities.

Note that the movement threshold in the air is 1% different from the 40% threshold for ground movement.

Unlike ground movement, stopping in the air is not instantaneous. When there is no X input, the velocity is quickly linearly ramped down to zero from whatever value it was at.
Accordingly, changing directions is also not instant, with no instant brake in place, going from left to right requires the x velocity to linearly go from negative values to positive ones.

The maximum X velocity in the air is the same as on the ground, there is no difference in horizontal speed when jumping or running. The maximum y velocity however seems to be uncapped for most purposes. It is possible that the number can't go arbitrarily high, but it can get up to at least 2-3 times the x velocity cap. (-132.03 units is the largest speed I've seen, compared to the 23 speed max for X movement)

### Double Jumping and Gliding

Double jumping cancels all vertical velocity up or down. It is one of the few instantaneous actions in the air. it doesn't affect X velocity at all. It just sets the Y velocity to the double jump value, regardless of what the velocity was before, positive or negative.

Gliding seems to slow down any and all Y velocity changes, instead of speeding up forever, downwards velocity is given a cap of 8 units, one third of the maximum horizontal speed. The maximum horizontal speed is unchanged from normal air and ground movement.

Interestingly, glide seems to slow down any changes to vertical momentum. If you jump while holding glide, you still move upwards while gliding but it will decay the y-velocity slightly slower than not doing so. Doing a full jump this way results in jumping about 6% higher than not doing so.

One small note is that air vents will push you upward while gliding. They also reset your dash if you glide after the dash so you can move quite quickly by gliding for a short time then dashing. This is repeatable so horizontal movement in areas with air vents can be incredibly quick.


[back to intro][intro]
[forward to Wall Movement][wall]

[intro]:http://jxvd.games/Ori-Intro
[wall]:http://jxvd.games/Ori-Wall-Movement
