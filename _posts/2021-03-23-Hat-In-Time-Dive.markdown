---
layout: post
title:  "Rolling Out in A Hat In Time"
date:   2021-03-23 12:12:00 -0700
categories: Movement
published: true
---

## Rolling Out in A Hat in Time

A Hat in Time is an interesting 3d platformer that makes some weird movement system decisions. The decisions aren't mistakes, it is clear a lot of time went into making the game feel the way it does. The end goal of the system seems like it was to create the 3d Mario game movement system while adding some minor twists. This isn't a bad goal, but I think that the twists that were added run into a common design mistake. The additions tend to add difficulty without making that difficulty interesting. The best example of this is the dive and roll out mechanic. 

The dive mechanic for A Hat in Time is taken directly from the 3d Mario games. In the Mario games, when in the air or moving on the ground at a sufficient speed, you can press a button to dive forward. This dive is fully committal. You will remain diving until you hit a wall, an enemy, or the ground. There is a slight amount of steering to the left or right that is possible, but general direction is set until you connect with something.

When you hit the ground after this dive, you start sliding. While sliding, you experience friction, slowing down until you come to a stop. At any point during this slide, you can hit a button to roll out of the slide. This roll out will preserve all remaining momentum and occasionally add some momentum back, depending on the game.

In the Mario games, this is the entirety of the mechanic. When you hit the ground you slide, slowing down until you stop. You can roll out of the slide as long as you are still moving. 

A Hat in Time adds a few extra bells and whistles to this mechanic. To start, during the dive you can hold back on the control stick or hit the jump button to do a small pop-up out of the dive. This kills almost all momentum, but you exit the Dive state. This pop-up is performable at any time. During the dive, if you hit the ground and then roll out later, you accelerate very similarly to the mario games. However if you time the button press to exactly when you touch the ground you get a much higher burst of speed. This burst of speed is a fast movement option, and is highlighted with some flashing lights and effects whenever you time the button press right. 

These are two very similar implementations of this mechanic. Deliberately so, even the animations for the Hat in Time version skew very close to the Mario ones. But the Hat in Time version frustrates me quite a bit, both due to a lot of small details being off and just a weird philosophical design choice.

The Hat in Time roll out is finicky. There are three discrete states you can end up at with nothing in between. The button to roll out is the same button as the dive pop-up. If you press the roll out button early, you pop-up instead, gaining a little bit of height and full control at the cost of all your speed. If you press the button late to avoid this, you roll out like in Mario, popping up to a standing position without much change in speed. If you time the button press perfectly, you gain speed instead. There is a wide spectrum where the same button press puts you in drastically different positions.

This isn't necessarily a bad thing, but the lack of nuance in outcomes means that any slight mistake is magnified. If you hit a button slightly early, you don't go slightly slower, you lose all speed. What this means is that until you become incredibly proficient with the game, you are actively punished for attempting to go fast but only mildly punished if you don't try to do the fun thing.

With the Mario system for rolling out, there is no punishment for pressing the button early or even mashing. There isn't a huge downside to being late on the input. The game still puts you in the same place, Mario just gets there a little later and with a little less momentum. There is a large spectrum of outcomes when interacting with the mechanic. The outcomes aren't all that distinct, but there is a lot of play in how early or late the button press occurs.

I wouldn't dislike the Hat in Time version so much if it wasn't compromised by other systemic problems. Namely the camera and lack of external positional tells. The camera is very swingy, with large variations between distance from the character and the angle it is pointed. This means that I would have a very hard time accurately judging my position as I played. 

This issue is often fixed by having external tells that show where the character is in the world. In the 3d Mario games for example, the shadow below Mario always shows where he will land, and it darkens as he gets closer to the ground. Hat in Time has almost none of these tells. Both of these problems wouldn't be that important, but the roll out mechanic explicitly wants precise knowledge of when the character will be touching the ground.

These small details help immensely when trying to judge the positions of characters and objects quickly. But even if these details were done correctly, I still have issues with the underlying design principles for the system. The roll out mechanic design confuses having something be hard to do with having it be fun or interesting. 

On a very basic level, the Hat in Time implementation of this mechanic makes sense. If the goal is a game with a high skill ceiling, then making the game harder is an easy way to achieve that. The problem is instead of making the mechanic more interesting, they only  made it more difficult. It isn't engaging to fail a basic movement mechanic, but it is frustrating. 

If you are a master of A Hat in Time, I imagine it probably feels pretty good to move around in the game at high speeds. Unfortunately, I am mediocre at playing A Hat in Time, and trying to play quickly and confidently tends to be frustrating and unreliable.

If I just wanted to play the game at a basic level, I would most likely have a much better time. Because I am directly punished for trying to go past my abilities, I find less play in the space. Instead of trying to mess around and see what is possible, I feel like I am being told to just do the bare minimum to beat the game.

In a 3d platformer, I personally don't want the difficult part to be competently controlling the character. Instead I want to feel like I am using my skills to tackle an interesting and difficult world.


Next time, I'll probably be writing another thing about movement systems. As always, if you want to get in touch with me for any reason, use [Twitter][twitter].


[twitter]: https://wwww.twitter.com/jxvd