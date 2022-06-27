---
layout: post
title:  "Ori and The Will of The Wisps Wall Movement"
date:   2022-06-21 12:12:00 -0700
categories: Ori
published: true
---

## Wall Movement

This section deals with all the movement options and specifics associated with the wall. I generally tested with the wall climb ability on. I include it as part of the main movement system because it just feels core to the game. It is technically optional but I can't imagine playing without it. I try to note the differences I found with having it on or off, but I generally tested with the ability equipped.

Wall movement starts in three ways, touching a wall from the air, jumping onto a wall from the ground, or running onto a wall from the ground. When you enter into this state, all previous momentum is set to zero if you have wall cling equipped. If you don't have the ability equipped, the y velocity will still affect Ori after they touch the wall.

Jumping while touching a wall from the ground is a specific movement option that is different from just jumping near the wall.  When sufficiently close, Ori will put their hands on the wall in a special animation state. Now when you jump, there will be a wall run animation up the wall. This way of jumping is different from normal jumps. If you release the jump button, the vertical movement will stop instantly. If the jump button is held to the end, Ori will slow to a stop at the top of the jump height and cling to the wall.

Jumping onto a wall in the air with upwards velocity is different from the grounded jump, but has some similarities. While it doesn't go as high as the grounded jump, some upwards movement is retained alongside a small wall run animation.
Touching a wall from the air without upwards velocity results in zero special animations or movement. If wall cling is equipped, all velocities are instantly set to zero.


### Wall Climbing
With wall cling equipped, wall movement is generally similar to ground movement in that the forces applied are either very quick or instantaneous. When the Y input is past 60% Ori moves up or down instantly. There is no ramp up of velocity, the number is just set to the movement value. The same is true of braking, when the Y input is below 60%, you stop instantly.

Wall cling generally causes the Y velocity to get set to zero whenever there isn't any y input. This is not the case when the ability isn't equipped. Without wall cling, the Y velocity is generally unaffected by the wall. There is no noticeable impact on speed when you start touching a wall with negative Y velocity. The wall does not make Ori start to move slower.

When moving up a wall, if Ori gets near the top of a wall with a walkable floor above it, Ori will go into a special mantle animation. In this animation, velocity is added to push Ori over the wall and onto the floor. This animation isn't a special state, it is just a set of forces getting applied to change position. Ori will generally enter the air because of this animation, making it possible to glide or double jump to cancel the animation.
What is interesting about this state is that it seems like every corner has a different set of forces applied. There doesn't seem to be a consistency to the state from wall to wall. 


### Wall Jumps

There are three different kinds of wall jumps, inwards, outwards, and neutral. Neutral jumps happen when there is no x input at all, this is a general 45 degree jump off the wall. Outwards jumps happen when the x input is at least 41% away from the wall, This is a jump that is much more horizontal than the neutral jump but is quite similar. Inwards jumps occur when the x input is at least 41% towards the wall. This jump is very different from the other two, being mostly vertical and is good for climbing the wall quickly, especially if you don't have wall cling equipped.  If the inward wall jump is done at the top of a wall, there will instead be a special jumping animation that is identical to the mantle animation, but goes much further than the other version.

Much like ground jumps, all wall jumps except the special mantle animation can be shortened. Occasionally, when inputting a neutral jump, Ori will run a few steps up the wall before jumping. This only happens if there is no y input, but it is not consistent.


The full away jump sets the Y Velocity to 23 units, the same number as normal jumps. Unlike grounded jumps however, the X Velocity is set by the jump before air acceleration forces kick in. In this case it is set to around 12 units, which is half the maximum horizontal air speed of around 24 units.

While the jumps holding away from the wall are consistent, Jumping off a wall with no x input is a lot less clear. The general case is that when the jump button is pressed, both X and Y are set to a given velocity, and then the X velocity stays the same for a set number of frames. Unlike normal air movement, with no X input, Ori does not immediately start to slow down. The issue is that all of these numbers seem highly variable based on the wall and Ori's position on it. In some cases the X velocity will be set to as low as 9 units. In other cases, seemingly when Ori bumps their head against the slope of the wall, the X velocity can be set to as high as 19 units.  The number the Y velocity is set to 


[back to intro][intro]
[forward to Special Movement][special]


[intro]:http://jxvd.games/Ori-Intro
[air]:http://jxvd.games/Nothing-Here-Yet