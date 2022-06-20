---
layout: post
title:  "Ori Ground Movement"
date:   2022-06-12 12:12:00 -0700
categories: Ori
published: true
---

## Ground Movement

This section deals with how Ori moves along the ground when when you move the analog stick. Compared to every other part of the system, ground movement is definite and simple.

To start, lets look at how walking works. To make Ori start moving at all, the analog stick needs to be pushed to 40% of the way to full. At that point Ori starts tip toeing forward. As you move the stick forward more, the speed Ori moves increases linearly until you hit 79%. When the stick hits 80% there is a large jump in speed as Ori switches animation to running, at which point the speed is capped out. There is no noticeable difference between having the stick at 80% and at 100%.

![groundChart](/_images/groundChart1.png)
###### these numbers are not exact

This was tested over relatively flat ground. Slopes do affect Ori's overall speed, but the speed is affected similarly going up and down hills. Ori's overall x and y velocities will fluctuate based on the ground, but the overall velocity remains in a relatively tight range. This is to say that Ori's running speed is stable, but how much distance is covered on a pure left to right basis will change based on the slope.

There is a small amount of acceleration from a standstill to the full speed value. It is very quick but the speed value does ramp up from zero to whatever the X input dictates. This is not the case for when Ori stops running. If the X input is zero, the speed value will not ramp downwards, instead it will just be set to zero. This happens the first frame that the game detects no X input value.

Running into a wall is much the same as braking, Ori's X velocity is not ramped down, it is set. However, instead of being set to zero, it will be set to slightly away from the wall. This is presumably to push Ori slightly away from the wall for better positioning for animations and general movement. After a couple frames, the speed is set to zero.


If the player hits down when running, no matter their X input, they will stop running. This is identical to letting go of the X input. The threshold is 61% in the y direction. This is the same threshold for choosing to drop through platforms.
There is no restriction on holding up, the only change is that Ori will start looking upwards if you aren't past the running X-Input threshold of 80%.


### Animation oddities
With ground movement, Ori's facing direction isn't relevant for anything other than animations. If Ori is facing to the right and the x-input is 74% to the left, Ori will do a small turn around animation as they start to move to the left. Their speed would be exactly the same as if they started facing to the left. The animation is just visual and masks how the movement system works.
The same turnaround animation also plays when running full speed and changing directions. The reason it happens is actually because the X Input hits the deadzone when going from left to right. The input is read as zero, so that instantaneous braking occurs.

If the analog input goes from 100% in one direction, to 100% in the opposite instantly, never hitting the deadzone, Ori will immediately snap to the running animation for a few frames before the turning animation plays. This isn't noticeable to player but it can be seen in slow motion.


[back to intro][intro]

[intro]:http://jxvd.games/Ori-Ground-Movement