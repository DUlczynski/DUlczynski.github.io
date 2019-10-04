---
layout: post
title: Drawing and moving a sprite
categories: Project Pico8 C# Programming
---
In the first script, you set the variables of where you want your character to spawn

```lua
p={}
p.x= (xValue)
p.y= (yValue)
```

Then to draw it, in another script you need to use the draw function 
```lua
function _draw()
	cls()
	spr(0,p.x,p.y)
end
```

Then moving it, with another script, you need to use the update function, so when you press any of the mouse buttons, it will check when a key is pressed and move it responsively, https://pico-8.fandom.com/wiki/Btn
```lua
function _update()
if btn(0) then p.x-=1 end
if btn(1) then p.x+=1 end
if btn(2) then p.y-=1 end
if btn(3) then p.y+=1 end
end
```
