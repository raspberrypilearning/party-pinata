## Add some treats

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Piñatas are full of treats and when they start to break the treats fall out. In this step, animate global food treats to fall out of the piñata each time it is hit. 
</div>
<div>
![](images/image.png){:width="300px"}
</div>
</div>

<p style="border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;">
A <span style="color: #0faeb0">**costume**</span> in Scratch is an image that changes the way a sprite looks. Our graphic designers asked Code Club leaders around the world to tell them what treats they would have at a party. Hopefully some of these treat costumes will be familiar to you - and others completely new.      
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
got to x: (0) y: (100)
```

--- /task ---

Four treats will escape the piñata each time the piñata is hit. A `clone`{:class="block3control"} in Scratch is a copy of a sprite. It has all the same code, costumes and sounds of the original sprite. When the Treats sprite is cloned you can create multiple treats.

--- task ---

Click on the Piñata sprite and insert a `repeat`{:class="block3control"} loop into your existing code. Change the value to `4` then add a `create clone`{:class="block3control"} block. Use the drop down arrow to select the Treats sprite.

![The Pinata sprite icon](images/pinata-sprite.png)

when this sprite clicked
start sound [Boing v]
change [hits v] by (1)
+ repeat (4)
create clone of (Treats v)
end
if <(hits) = (10)> then
hide variable [hits v]
switch costume to (broken v)
broadcast (party v)

--- /task ---

--- task ---

Return to the Treats sprite and create a new script using the `when I start as a clone`{:class="block3events"} block. 

Add blocks from the `Looks`{:class="block3looks"} blocks menu to `show`{:class="block3looks"} the clone, make it `go to back layer`{:class="block3looks"} and `switch costume`{:class="block3looks"}:

![The Treats sprite icon](images/treats-sprite.png)

```blocks3
when i start as a clone
show
go to [back v] layer
switch costume to (Knafeh v)
```

--- /task ---

--- task ---

The only Treats costume the project will use with the current code is the last costume in the Costume list. Use a `pick random`{:class="block3operators"} operator to select a random costume from `1` to `26` each time a clone is created:

![The Treats sprite icon](images/treats-sprite.png)

```blocks3
when i start as a clone
show
go to [back v] layer
+ switch costume to (pick random (1) to (26)
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
switch costume to (pick random (1) to (26)
+ glide (1) secs to (random position v) 
```

--- /task ---

--- task ---

**Test:** Run your project and hit the piñata to see 4 clones of the Treats sprite after each hit. The costumes will be selected at random and glide to a random position.

--- /task ---

--- task ---

Add animation to make the Treat sprite clones `turn`{:class="block3motion"} `forever`{:class="block3control"} when the reach their random position. Remember animations work best when small movements are used so change the number of degrees to `1`:

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

--- /task ---

--- save ---