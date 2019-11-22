---
layout: post
title: Map Collisions Research
categories: Project Pico8 Research
---

Throughout Pico-8, i've been really needing Map collisions for my game, this is so you can't just phase through the map and go out into the void, With research I have figured out that in order to check for a sprite, you will need;


To add a 'hitbox' which is an invisible rectangle infront of your character which checks for areas towards the place you're facing.

To label the sprites that I do want collision with flags.

- and then using code check if there is a sprite on the hitbox - If there is a sprite, check for the flag, if there is a flag on that position, do not allow them to walk on the sprite

I still cannot code this effectively but i'm researching ways in order to do it

