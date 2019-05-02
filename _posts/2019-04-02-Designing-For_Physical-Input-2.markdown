---
layout: post
title:  "Designing for Physical Input Part 2"
date:   2019-04-01 12:12:00 -0700
categories: Physical Games
published: true
---
# Designing for Physical Input 
## Part 2

Last Post I talked about how I ran into a specific issue that came about in my design because I was using a controller instead of a mouse for a point-and-click game. If I wanted to keep the standard screen to screen structure for the genre, I was going to have to compensate for the issues that came about due to nature of controller inputs. To quickly recap from the first post, because a player has to be consistently holding a direction to move their character, it is bad to ask them to change their input extremely quickly just to transition from screen to screen. This is especially true if the direction they need to hold on one screen, sends them in the wrong direction in the next screen.

This is something that stumped me for a while as I searched for solutions. The most immediate solution would be to just remove the individual screen structure and just let the player walk through the environment seamlessly. This didn't appeal to me because I wanted to tightly control the camera shots to give more interesting framing to the events that happen on screen. The next solution I thought of was using Tim Schafer's solution in Grim Fandango, tank controls. 

For those who don't know, tank controls are a style of controlling a character in a 3d perspective where the button to go forward is always relative to the character on the screen. This means that if a character is facing right, holding forward would result in the character walking right, and holding back would result in them walking backwards to the left. The character would pivot in place when right or left was held. 

###### If the player holds forward, with tank controls the character will walk towards the screen
![grim](/_images/grim_fandango.png)

Tank controls work as a solution for the screen transition problem because no matter the camera change from scene to scene, the character would always be walking forward. The player would have time to adjust mentally to the screen transition while not having to worry about walking right back into the room they came from. This works well to solve the problem, but most people don't like using tank controls. They feel very restrictive and take the player out of the game every time they have to minutely adjust their angle of movement. 

I decided that this wasn't the solution I wanted, but while looking at that I saw another thing that Grim Fandango did to solve the problem, it highlighted most transition points using in-enviroment lighting. A person's eye will be drawn to the highlighted parts of a picture, so if part of the screen is lit up, people can more easily find the character's position. This helps the problem of the player having to quickly understand an environment while actively controlling the character.

This still left the issue of a player holding one direction as they transitioned from screen to screen and then having the character walk that direction even when it was wrong. If I wasn't going to use a weird control scheme or a mouse, this was just always going to be a problem to deal with. I still wanted to use a controller, so this meant that I was going to have to change something else.

The next solution came when I was figuring out how to code and create the environment the character would walk in. How I was going to actually move the character from one screen to the next in the code. At first I was messing around with teleporting the character and camera at the transition points, each screen existing as its own separate world. Eventually I figured out that it would just be easier to create the various scenes on one big stage and move the player and camera around on that. Then I realized that if I set the camera to always be from one general perspective, the character would always move in one general direction for each directional input.  

As long as I kept to the [180-degree rule][180], I could still be somewhat elaborate in my camera placement but avoid the character moving in the wrong direction after screen transitions. This could be further helped by making sure to highlight the place the character was going to be after a transition if it was going to be a more ambitious camera shot. 

###### This is a shot of the outside of one central location, the transition point is the doorway. 
![outside](/_images/bar_outside.png)

###### The inside of the bar, note how the doorway in this shot is at a different screen position than in the last one. To compensate for this it is lit up.
![inside](/_images/bar_inside.png)

The design of both how the game was presented was improved by being cognisant of how the player was going to actually physically interact with the input device. I could do this especially well because I limited what the players were allowed to use. At no point would a mouse ever be in use, so I could avoid any designs that had to keep that in mind. I looked at solutions that other designers used for similar problems, and took what was relevant for my purposes. Keeping all of these things in mind let me make a thing that looked cool, but still felt good to actually use.

Next time I'll be writing about executional difficulty. If you want to get in touch with me for any reason, use [Twitter][twitter].


[180]: https://en.wikipedia.org/wiki/180-degree_rule
[twitter]: https://www.twitter.com/jxvd