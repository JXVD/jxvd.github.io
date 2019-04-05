---
layout: post
title:  "Looks at Common Input Devices"
date:   2019-04-01 12:12:00 -0700
categories: Physical Games
published: false
---

There are a lot of different input devices, [*a lot of different input devices*][input-devices]. So how do you even begin to grapple with what you'll let your player use? If you're like me, you probably only anticipate players using one specific kind of device for any one game you work on. This is reasonable as long as you are willing to take the hit when someone says "this game feels really bad on a Sega Bass Pro Fisherman rod." Personally, I just say what kind of input device I expect the player to use in a Readme file. This is good because you only have to design for one input system, but it can make your game unplayable for anyone who can't actually use that device. If you have infinite time, money, and energy, go ahead and make a game for [theremin][theremin]; for everyone else here is a look at how I choose what inputs to design for and how I try to make sure I pay attention to the advantages and limitations of the input. 

I have a hard enough time just making games, so I'm not making anything I don't currently have the ability to play myself. That means I'm choosing between controllers and mouse and keyboard. For most games in established genres, the expectations are already set. The standard setup for a fighting game doesn't use mouse input. 


I'm currently in the process of making a game that is ripping of Kentucky Route Zero, which is modeled after point-and-click adventure games. As the name implies, the expected idea is that you move the character with a mouse. This allows for interacting with various areas of the screen for selecting parts of the environment to interact with them. Much like KRZ, I don't plan on having puzzles, so player input only needs to control the main character and dialogue menus. When using a mouse, a player is directing a character where to go, they give directions and hope they get followed. When using a controller, there is generally a one to one correspondance from directional input to movement, they are the people navigating the environment. I think this is something that leads to a greater identification with the character that is getting moved on the screen. I don't need a mouse for anything in my game and see some benefits to using a controller, so I decided to go with that. 


Using a controller for a point-and-click styled game brings up specific issues that don't exist with a mouse setup. In a point and click adventure game, the standard is to move from screen to screen as you move through an environment. This works out quite well with mouse controls. The character will transition screens and the player can move the mouse to where to go next. This setup is even a benefit as it makes a player first scan through and discern what the layout of the space is before ever interacting with it. This makes players much more likely to notice things placed in the environment. With a controller however, a player won't stop holding a direction on the analog stick as they transition screens. This can lead to the very frustrating scenario of a player holding right to move off the screen and then as the scene transitions they appear from the right side of the screen and walk back to the first screen. If I want to include the traditional screen structure, but allow for interesting camera angles and shots, how do I do this without the player getting lost or walking back to where they just came from?

This is something that stumped me for a while. Level design is something that I don't spend enough time on so I don't have a lot of rules of thumb or insights into how to deal with most scenarios. The most immediate solution would be to just remove the individual screen structure and just let the player walk through the environment seamlessly. This didn't appeal to me because I wanted to tightly control the camera shots to give more interesting framing to the events that happen on screen. The next solution I thought of was using Tim Schafer's solution in Grim Fandango, tank controls. For those who don't know, tank controls are a style of controlling a character in a 3d perspective where the button to go forward is always relative to the character on the screen. This means that if a character is facing right, holding forward would result in the character walking right, and holding back would result in them walking backwards to the left. The character would pivot in place when right or left was held. 

This works as a solution because no matter the camera change from scene to scene, the character would always be walking forward. The player would have time to adjust mentally to the screen transition while not having to worry about walking right back into the room they came from. This works well to solve the problem, but most people don't like using tank controls. They feel very restrictive and take the player out of the game every time they have to minutely adjust their angle of movement. I decided that this wasn't the solution I wanted, but while looking at that I saw another thing that Grim Fandango did, it highlighted most transition points using in-enviroment lighting. A person's eye will be drawn to the highlighted parts of a picture, so if the part of the screen the character appears after a screen transition is lit up relative to the space around it, people can more easily find where the character is.

This still left the issue of a player holding one direction as they transitioned from screen to screen and then having the character walk that direction even when it was wrong. If I wasn't going to use a weird control scheme or a mouse, this was just always going to be a problem to deal with. I still wanted to use a controller, so this meant that I was going to have to change something else.



The solution came when I was figuring out how to code and create the environment the character would walk in. How was I even going to move the character from one screen to the next. At first I was messing around with teleporting the character and camera at the transition points. Eventually I figured out that it would just be easier to create the various scenes on one big stage and move the player and camera around on that. Then I moved on to just having the game be set in a space that the character seamlessly walked around, but the camera cut from place to place. Then I realized that if I set the camera to always be from one general perspective, the character would always move in one general direction for each directional input. As long as I kept to the [180-degree rule][180], I could still be somewhat elaborate in my camera placement but avoid the character moving in the wrong direction after screen transitions. This could be further helped by making sure to highlight the place the character was going to be after a transition if it was going to be a more ambitious camera shot.  (INCLUDE SHOTS OF OUTSIDE OF BAR + INSIDE).

Wrap it up idk










Almost everyone who is on a computer has both of these, and for those who don't, you probably weren't designing a game to run on a command line only Linux system. 

##Gamepad

The first and most basic advantage of gamepads is that they are custom built for video games. This means specialized hardware that you can design for. Analog sticks are a big deal if you want to be able to aim in more than eight directions easily. The triggers allow for analog button presses to let various actions happen, the most common being how hard a player pressing a pedal in a car. Vibrations allow for haptic feedback for a million different scenarios. 

Arcade Sticks 

In a lot of ways, designing for Arcade stick is like designing for keyboards. Modern arcade sticks only take inputs for eight directions, which is ideal if you are making a game that wants precise inputs. Additionally the button arangement makes hitting different buttons quickly and precisely, which can be harder on gamepads. I don't design games specifically for arcade sticks because they are more niche than other input devices,  but if I did, the first thing I would do is remove all analog input and only allow 8 directions. 

Switch Joycons
At first glance, the joycons seem similar to the Xbox or Playstation gamepads, two analog sticks, a d-pad, 4 face buttons, 4 trigger buttons. They are mostly the same, but the placement of the buttons relatve to the stick on the right side makes it drastically more difficult to switch from the right stick to the right buttons than on a normal gamepad. In addition, the right face buttons placements makes it hard to use the claw input method to mitigate the issue. If you know you are going to be making a game for switch that uses both joycons at once for one player, really try to avoid needing the right stick and the right buttons.


##Phone

If you are designing for touch devices, you should probably know that from the jump. I don't mess with these at all because I am a coward. But it would be remiss to not even mention them here. Direct tapping of specific points on the screen seems frustrating. The common solution to that is just having various gestures be inputs. Swiping in various ways, taps that don't care about position, number of taps, taps then swipes.


##VR Headset





[input-devices]: https://youtu.be/D51z4CWh-ko
[theremin]: https://youtu.be/Rt3jlSQ7E1Y
[180]: https://en.wikipedia.org/wiki/180-degree_rule

