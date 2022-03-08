## Add some treats

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Piñatas are full of treats and when they start to break the treats fall out. In this step, animate international food treats to fall out of the piñata each time it is hit. Do you recognise any of the treats?
</div>
<div>
![An animated image showing the pinata being hit multiple times. Each time 4 random treats fall out to random positions then slowly rotate in a circle.](images/spinning-treats.gif){:width="300px"}
</div>
</div>

<p style="border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;">
A <span style="color: #0faeb0">**costume**</span> in Scratch is an image that changes the way a sprite looks. Our **graphic designers** asked Code Club leaders around the world to tell them what treats they would have at a party. Hopefully some of these treat costumes they created will be familiar to you - and others completely new.      
</p>

--- task ---

Click on the **Treats** sprite in the Sprite list and select the **Costumes** tab. 

There are 26 treat costumes - and you are going to use them all! 

![The specially created treat images shown as a collection of treats.](images/treats.png)

--- /task ---

--- task ---

Click on the **Code** tab then create a script to `hide`{:class="block3looks"} the treats in the piñata when your project starts:

![The Treats sprite icon](images/treats-sprite.png)

```blocks3
when flag clicked
hide
go to x: (0) y: (100)
```

--- /task ---

Four treats will escape the piñata each time the piñata is hit.  When the Treats sprite is **cloned** you can create multiple treats.

<p style="border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;">
A <span style="color: #0faeb0">**clone**</span> in Scratch is a copy of a sprite. It has all the same code, costumes and sounds of the original sprite.      
</p>

--- task ---

Click on the **Piñata** sprite. 

Insert a `repeat`{:class="block3control"} loop into your existing code. Change the value to `4`{:class="block3control"} then add a `create clone of myself`{:class="block3control"} block. Use the drop down arrow to select the `Treats`{:class="block3control"} sprite:

![The Pinata sprite icon](images/pinata-sprite.png)

```blocks3
when this sprite clicked
if <(hits) < (10)> then
start sound [Boing v]
change [hits v] by (1)
+ repeat (4) // change to 4
create clone of (Treats v) // select Treats
end
if <(hits)=(10)> then
switch costume to (broken v)
broadcast (party v)
```

**Tip:** Use the spare space in the Code area to build your new code then drag it into the existing script:

![The repeat and clone blocks are assembled on their own in the Code area before being dragged into position in the script.](images/code-area.gif)
--- /task ---

--- task ---

Click on the **Treats** sprite.

Create a new script using the `when I start as a clone`{:class="block3events"} block. 

Add blocks from the `Looks`{:class="block3looks"} blocks menu to control the appearance of each new clone:

![The Treats sprite icon](images/treats-sprite.png)

```blocks3
when i start as a clone
show
go to [back v] layer // change to back
switch costume to (Knafeh v)
```

--- /task ---

--- task ---

You can pick random treats to be released when the Piñata is hit. Use a `pick random`{:class="block3operators"} operator to select a random costume from `1`{:class="block3operators"} to `26`{:class="block3operators"} each time a clone is created:

![The Treats sprite icon](images/treats-sprite.png)

```blocks3
when i start as a clone
show
go to [back v] layer 
+ switch costume to (pick random (1) to (26)) // change to 26
```

--- /task ---

--- task ---

At the moment, the Treat clones will appear behind the piñata sprite but treats should fall from the piñata to a random position. 

Add code to make the cloned Treats `glide`{:class="block3motion"} to a random position:

![The Treats sprite icon](images/treats-sprite.png)

```blocks3
when i start as a clone
show
go to [back v] layer
switch costume to (pick random (1) to (26))
+ glide (1) secs to (random position v) 
```

--- /task ---

--- task ---

**Test:** Run your project and hit the piñata to see 4 clones of the Treats sprite after each hit. The costumes will be selected at random and glide to a random position.

![An animated image showing the pinata being hit 3 times. Each time 4 random treats fall out to random positions.](images/four-treats.gif)

--- /task ---

--- task ---

Add animation to make the Treat sprite clones `turn`{:class="block3motion"} `forever`{:class="block3control"} when they reach their random position. Remember animations work best when small movements are used so change the number of degrees to `1`{:class="block3motion"}:

![The Treats sprite icon](images/treats-sprite.png)

```blocks3
when i start as a clone
show
go to [back v] layer
switch costume to (pick random (1) to (26)
glide (1) secs to (random position v) 
+ forever
turn right (1) degrees
```

--- /task ---

--- task ---

**Test:** Run your project again to see the Treat sprite clones spin.

![An animated image showing the pinata being hit multiple times. Each time 4 random treats fall out to random positions then slowly rotate in a circle.](images/spinning-treats.gif)

--- /task ---

--- save ---