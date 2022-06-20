---
layout: post
title:  "Ori Jumping"
date:   2022-06-19 12:12:00 -0700
categories: Ori
published: true
---

## Jumping

Jumping in Ori and the Will of The Wisps is broadly simple, with a lot of small weird caveats.

There are two kinds of jumps, neutral jumps where you don't have an x input and angled jumps where you do. Regardless of current velocity, if you aren't holding any x input you will jump straight up. If you are holding an x-input, you will jump at a set angle. Your horizontal speed will not affect this angle, it will always be the same no matter what.

The threshold for angled jumps is 41%, note that this is different from the 40% threshold for starting to move. So there is a deadzone the size of 1% of an xbox controller's input range that will have Ori slowly tiptoe forward but when you jump they will move straight up. It looks [quite strange.](/_images/walkingJump.mp4)

When the jump button is pressed, the jump force is applied immediately. The X and Y velocities are set to the jump values. The velocity values will then start to be gradually affected by forces. The X velocity will be affected by player input left and right, and the Y velocity will be affected by gravity.

After jumping, you can release the jump button at any time. While the button is held, the effect of gravity on the jump is lessened. When the button is released the jump effect goes away, allowing gravity to act fully on the jump.
There is a minimum height that happens when the button is pressed for 15 ms or less. The maximum height occurs around 450ms, but the height starts to level off closer to 350ms.


![jumpChart](/_images/jumpChart1.png)
###### numbers are not exact, especially near the start (see notes about timing in the intro)

There isn't a large difference between jumps at 350 and 450, there is very little extra height or extra airtime.

Horizontal speed does not affect jump height at all. A jump done from a standing position will be the same as one done from a full sprint.



### Slopes
Slopes are very odd with regards to jumps. They don't actually change the jump forces that are applied. A vertical jump on a slope is the same as on flat ground. There is a difference when landing on slopes however. The landing animation on slopes very slightly moves Ori down the slope. So it is possible to move  without inputting any direction just by jumping repeatedly on a slope. This is an absurdly slow form of movement, taking [dozens of jumps](/_images/slopeJump.mp4) just to move the width of Ori's body.

Another intensely minor form of movement is backflipping. When you jump, if you are holding down, Ori will do a backflip animation. This results in a jump where Ori moves slightly backwards. Notably, this style of jump is different from a normal jump in that it can't be shortened. How long the jump button is pressed does not change the height of the backflip. The height of the jump is the same as the maximum normal jump height.



### Jump Buffer and Coyote Time

Coyote Time is a mechanic present in most platformers that gives leniency to player inputs when moving off of ledges. For a certain amount of time after a player runs off of a corner into the air, they can still jump. Ori is interesting in that its coyote time window is incredibly small. It is present for a at most a couple frames after leaving the ground by running.

Another common platformer mechanic is buffering jump inputs. This means that if the jump button is hit early, the jump will still come out as if it was hit when Ori was on the ground. This does not seem to present at all for jumps. If it does exist at all, it would be very miniscule as I was unable to consistently get first frame jumps in testing.


[back to intro][intro]

[intro]:http://jxvd.games/Ori-Ground-Movement