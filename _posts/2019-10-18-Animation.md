---
layout: post
title: Animating A Sprite
categories: Project Pico8 Programming
---
First you set the variables, The starting sprite, and the starting counter, and a set variable to control the flip of the character
```lua
s=1 -- Sprite
x=15 -- X Coordinate
y=25 -- Y Coordinate
d=4 -- Timer
f=true -- Flip
```
Then you need to draw the sprite
```lua
function _draw()
	cls()
map(0,0,0,0,15,9)
	spr(s,x,y,1,1,f)
end
```

Then you need to make a function which 'walks'
```lua
function walking()
d=d-1 -- Timer decreases
if d<0 then -- Once timer decreases
s=s+1 -- Move on to next sprite
if s>3 then s= 1 end -- Once it reaches the end sprite, move back to first sprite
d=4 -- Set the timer = 4
end
end
```

Then within your Update function, you need to account for the following, "Is it walking at this time, is it flipped at this time, as well as calling the function
```lua
function _update()
w = false -- walking is false

if btn(0) then 
x-=1  -- move left
f=true -- flipped is true
w=true -- walking is true
end

if btn(1) 
then
x+=1 -- move right
f=false --flipped is not true
w=true -- walking is true
end

if btn(2) then
y-=1 -- move up
w=true --walking is true
end

if btn(3) then
y+=1 -- move down
w=true --walking is true
end
if w then -- if w is true
walking() --call the function
else
s=1 -- if not, sprite is set to the non walking sprite
end
```
