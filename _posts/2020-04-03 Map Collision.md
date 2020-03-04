---
layout: post
title: Map Collision
categories: Project Pico8 
---

Figuring out map collisions using the research was quite complex, and all you needed to do was add a **HIT** Function.

The hit function consists of checking if the flag is equal to red and if so, setting the collide = true

```lua
function hit(x,y,w,h)
  collide=false
  for i=x,x+w,w do
    if (fget(mget(i/8,y/8))==1)  or
         (fget(mget(i/8,(y+h)/8))==1) then
          collide=true
    end
  end
  ```
  This only checks for a y-direction
  
  
  Then doing the same thing for the x-direction you do
  
  ```lua
  for i=y,y+h,h do
    if (fget(mget(x/8,i/8))==1) or
         (fget(mget((x+w)/8,i/8))==1) then
          collide=true
    end
  end
  
  return collide
end
```

The collide is what we really need and checks if we have actually it, in each of our directional movement, we need to run the hit function, and if it hits it sets the position back 1, which therefore reverts it back to its previous position, like so.

```lua
if btn(⬇️) then
self.y+=1
self.cam_y += 1
if hit(self.x,self.y,6,6)
then
self.y-=1
self.cam_y-=1
end
w = true
end
```

The camera is an addition I made to the code, in order to make a fluent camera system.
