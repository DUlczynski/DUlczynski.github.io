---
layout: post
title: Drawing and moving a sprite
categories: Project Pico8 Programming
---
first, you set the variables of where you want your character to spawn

```lua
p={} --creates an array of values
p.x= (xValue) -- sets the x value
p.y= (yValue) -- sets the y value
```

Then to draw it, you need to use the draw function 
```lua
function _draw()
	cls()
	spr(0,p.x,p.y) --draws the sprite, 0 at p.x and p.y
end
```

Then moving it, with another script, you need to use the update function, so when you press any of the mouse buttons, it will check when a key is pressed and move it responsively, you can use this wiki for the keys. https://pico-8.fandom.com/wiki/Btn
```lua
function _update()
if btn(0) then p.x-=1 end -- when left arrow key pressed, go left
if btn(1) then p.x+=1 end -- when right arrow key pressed, go right
if btn(2) then p.y-=1 end -- when up arrow key pressed, go up
if btn(3) then p.y+=1 end -- when down arrow key pressed, go down
end
```
