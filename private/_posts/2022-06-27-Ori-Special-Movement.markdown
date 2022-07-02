---
layout: post
title:  "Ori Special Movement"
date:   2022-06-27 12:12:00 -0700
categories: Ori
published: true
---

## Special Movement

This section covers most movement abilities that happen when you press a button.

### Dash

At any time, when you press the dash button, Ori will shoot forward in the direction of the current X input. If there is no X input, Ori will move in the direction they are facing. This is one of the few times that facing direction actually affects movement options. Just like with walking, the X input needed to turn around is 40%, while the threshold for air movement is 41%, so there is a very small range of inputs where Ori can be made to dash backwards without already moving in that direction. 

Dashing on the air vs the ground is largely similar with some small differences in how forces are applied.

In the air, previous velocity doesn't matter, dashing sets both the X and Y velocities to zero before applying forces. Once the velocities are set to zero, there is a small pause before the X velocity is very quickly ramped up to a high value. After hitting the maxium dash speed, the X velocity then more slowly descends to the normal maximum air speed. 

On the ground, the previous velocities are not set to zero, instead they are just very quickly accelerated up to the dash speed without the minor pause from the air dash. Ground dashes also decelerate a lot quicker than air dashes, resulting in an overall shorter distance covered. This is also due to the fact that ground dashes go along the slope of the ground instead of purely horizontal, so a lot of the dash force will be applied vertically, instead of purely horizontally. 

If a during a grounded dash, the X input is opposite to Ori's dashing direction, they will go into a turnaround animation as soon as they touch the ground instead of completing the roll animation. This results in a shorter overall dash

Ground dashes do not always follow the slope of the ground however, sometimes if a slope is steep enough, Ori will instead go into the air instead of following the walkable surface. A similar edge case is air dashes into corners. If Ori would just barely not make it over a wall, they will get bumped slightly upwards to avoid clipping the corner.


Also worth noting is that on the ground, dashes can be done in rapid succession. While in the air you can only dash once before touching a surface, just like with double jumps. This restriction isn't strictly followed, if you dash off a wall or corner, this counts as a grounded dash so it does not consume the Air Dash. Also if Ori happens to touch the ceiling, the air dash will be restored, which is not true for double jumps.


### Bash

When the Bash button is hit, Ori can then enter into the bash state for a set amount of time. It doesn't matter if Ori is close to an object they can bash off of, as long as they get close enough after pressing the button, a bash will occur. This input window is incredibly generous compared to most inputs in the game. This window does not care about other inputs, it is possible to hit the button, dash into range of a valid target, and initiate a bash. The bash window is not infinite, it isn't possible to just hold down the button and walk around looking for valid targets.

When the player enters the bash state they are slightly pulled towards the bash target, while having all their other movement slowed down to stop. Then after a set amount of time, or when the button is released, Ori's X and Y velocities are set to the bash values. After another short period of time, the velocities are decreased. Note that this happens even in scenarios where they would normally increase. Going downwards in the air normally has uncapped acceleration, but instead the Y velocity gets reduced until it gets below a threshold and then starts accelerating again.

The X velocity does not decrease in the same way as the Y velocity here. Normally when no horizontal input is held, Ori will quickly slow down to a stop. After a bash however, Ori's X velocity does not go down even with no input. What's more, the X velocity is above the normal speed cap for horizontal movement. Holding a horizontal direction in this instance will actually make Ori move slower because the X velocity will be slowed down to the cap.  


### Launch

Launch works similarly to Bash, when the ability is activated, Ori slows down to a stop, then will fly off in a direction when the button is released or the timer is up. The forces applied are similar to Bash, but differ in very minor ways. The beginning slowdown effect is much slower to actually hit zero. The deceleration is generally more severe, dropping the velocity values lower than Bash. The X velocity quirk from Bash does not show up here, with no X input held, the X velocity will decelerate to zero as normal. 





[back to intro][intro]
[forward to conclusion][conclusion]

[intro]:http://jxvd.games/Ori-Intro
[conclusion]:http://jxvd.games/Ori-Conclusion





