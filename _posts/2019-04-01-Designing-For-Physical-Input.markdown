---
layout: post
title:  "Designing for Physical Input"
date:   2019-04-01 12:12:00 -0700
categories: Physical Games
published: true
---

## Designing For Physical Input

### Part 1

There are a lot of different input devices, [*a lot of different input devices*][input-devices]. So how do you even begin to grapple with what you'll let your player use? If you're like me, you probably only anticipate players using one specific kind of device for any game you work on. This is reasonable as long as you are willing to take the hit when someone says, "this game feels really bad on a Sega Bass Pro Fisherman rod." I prefer to design games with one specific input device in mind. This makes designing a good system much easier, it also makes the game unplayable for anyone who can't use that device. If you have infinite time, money, and energy, go ahead and make a game for [theremin][theremin]. For everyone else, here is a look at how I choose what inputs to design for and how I try to make sure I pay attention to the advantages and limitations of the input.

Making games is hard enough, so I'm not making anything I don't currently have the ability to play myself. That means I'm choosing between controllers and mouse and keyboard. For most games in established genres, the expectations are already set. The standard setup for a fighting game doesn't use mouse input, while the standard setup for an RTS does. When you have an idea that works in a genre space, but would benefit from non-standard input, you need to spend the time to consider all the parts of that.

I'm a big fan of Kentucky Route Zero, so I'm making a game that is ripping it off. Kentucky Route Zero is modeled after point-and-click adventure games. As the name of the genre implies, the expected idea is that you move the characters with a mouse. This allows for interacting with various areas of the screen with the cursor. The player can interact with the environment separate from the character they are controlling. This is especially useful for dealing with interactive puzzles because the player is not limited to the parts of the screen where the characters are.

 However, much like Kentucky Route Zero, I don't plan on having puzzles. Player input only needs to control the main character and dialogue menus, so what input device should I use? When interacting with menus, mouse and controllers feel about the same to me. They can both deal with small menus quickly and fluidly. This is not true when moving a character through a standard point-and-click environment, there are significant differences between the two inputs. When using a mouse, a player is directing a character where to go, they give directions and hope they get followed. When using a controller, there is generally a one to one correspondence from directional input to movement. The player is the person navigating the environment. I think this is something that leads to a greater identification with the character that is getting moved on the screen. I don't need a mouse for anything in my game and see some benefits to using a controller, so I decided to go with that. 

Using a controller for a point-and-click styled game brings up specific issues that don't exist with a mouse setup. In a point-and-click adventure game, the standard is to move from screen to screen as you move through an environment. This means that when the character hits the edge of the screen, the game will transition to the next one in a hard visual cut. The character will appear somewhere on that screen and the player can navigate from there. This works out quite well with mouse controls. The character will transition screens and the player can move the mouse to where to go next. This setup is even a benefit as it makes a player look through and understand the layout of the space before interacting with it. This makes the player much more likely to notice things placed in the environment. 

 With a controller, there are issues with the screen to screen setup. The main problem is with the moment when the character hits the edge of the screen. To actually move the character, a player will be holding a direction on an analog stick or d-pad. When the character hits the transition point, the player will still be holding that direction. If the character walks through a door on the left side of the screen, and then after the screen transition, the character appears *from* the left side of the screen, the player will still be holding left and walk back to where they came from. To state this more clearly, if a player starts holding a single direction and end up right back where they started, it sucks. 

 I like the screen to screen setup that point-and-click games use. I think it allows for very composed shots of environments. The setup also can interact very badly with using a controller. If I want to include the traditional screen structure, and have interesting angles and shots, how do I do this without the player getting lost or walking back to where they just came from? 

 Next time I'll talk about how I solved this problem.  If you want to get in touch with me for any reason, use [twitter][twitter].

[input-devices]: https://youtu.be/D51z4CWh-ko
[theremin]: https://youtu.be/Rt3jlSQ7E1Y
[twitter]: https://www.twitter.com/jxvd

