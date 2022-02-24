## Start the party

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
In this step, you will choose a piñata costume and code the piñata to swing.
</div>
<div>
![](images/image.png){:width="300px"}
</div>
</div>

--- task ---

Open the [Party piñata starter project](http://rpf.io/scratch-new){:target="_blank"}. Scratch will open in another browser tab.

[[[working-offline]]]

--- /task ---

The Scratch editor looks like this:

![An annotated screenshot of the Scratch editor, with the Stage, Stage pane, Sprite pane, Sprite list, and Code area labelled.](images/scratch-interface.png)

The **Stage** is where your project runs and a **backdrop** changes the way that the Stage looks. A Code Club party backdrop has been added for you. 

At the moment there is not much happening at this party. You can change that! 

--- task ---

A sprite can have code, costumes, and sounds to change the way that it looks and what it does.

Click on the **Piñata** sprite in the Sprite list and select the **Costumes** tab. 

There are two Code Club robots to choose from and each has 'whole' and 'broken' costumes. 

**Choose:** Click on the costumes to see them and decide which robot piñata costume you want to use at your party, **blah1** or **blah2**. 

--- /task ---

--- task ---

Click on the **Code** tab. Go to the `Looks`{:class="block3looks"} blocks menu and drag a `switch costume to`{:class="block3looks"} block to the Code area. 

Click on the costume name to open a drop-down menu then select your chosen 'whole' costume.

```blocks3
switch costume to ( v) // Your costume
```

--- /task ---

Blocks can be connected together in the Code area to run more than one at a time. Connected blocks will run in order from top to bottom.

--- task ---

Drag a `When flag clicked`{:class="block3events"} block from the `Events`{:class="block3events"} blocks menu and connect it to the top of your looks block in the Code area. The blocks will snap together.

```blocks3
+ when flag clicked
switch costume to ( v)
```

--- /task ---

--- task ---

The starting position of a piñata is always the same, it only starts moving when the piñata game is ready to play. 

In the `Motion`{:class="block3motion"} blocks menu, find the `go to x: 0 y: 180`{:class="block3motion"} and  `point in direction 90`{:class="block3motion"} blocks. Drag the blocks to the Code area and connect them to the bottom of your code.   

```blocks3
when flag clicked
switch costume to ( v)
+ go to x: (0) y: (180)
+ point in direction (90) // Ready position
```

--- /task ---

A `forever`{:class="block3control"} loop runs the code blocks inside it again and again. It is the perfect loop for a swinging piñata that is hard to hit.

--- task ---

Drag a `forever`{:class="block3control"} block from the `Control`{:class="block3control"} blocks menu and connect it to the bottom of your code.

```blocks3
when flag clicked
switch costume to ( v)
go to x: (0) y: (180)
point in direction (90)
+ forever
```

--- /task ---

A `repeat`{:class="block3control"} loop can be used to make the piñata repeat a small movement many times. This will make the piñata appear animated.

--- task ---

Drag a `repeat 10`{:class="block3control"} block from the `Control`{:class="block3control"} blocks menu and attach it inside your `forever`{:class="block3control"} loop. 

Go to the `Motion`{:class="block3motion"} blocks menu and drag a `turn right 15 degrees`{:class="block3motion"} block into the `repeat`{:class="block3control"} block. 

Change the `15` degrees to `1` degree so that the piñata only swings a small amount each time.

```blocks3
when flag clicked
switch costume to ( v)
go to x: (0) y: (180)
point in direction (90)
forever
+ repeat (10)
turn right (1) degrees // swing right 10 times
```

--- /task ---

--- task ---

**Test:** Run your project, by clicking on the **Green flag** above the stage, to see the piñata swing. 

Something is not quite right. When an object is hung from the ceiling, it will continue to swing not just to the right but also to the left. 

--- /task ---

--- task ---

Add code to your `forever`{:class="block3control"} loop so that the piñata swings from the centre back and forth continuously. 

```blocks3
when flag clicked
switch costume to ( v)
go to x: (0) y: (180)
point in direction (90)
forever
repeat (10)
turn right (1) degrees // swing right 10 times
end
+ repeat (20)
turn left (1) degrees // swing left 20 times
end
+ repeat (10)
turn right (1) degrees // swing right 10 times
end
```

--- /task ---

--- task ---

**Test:** Run your project to see the piñata swing. 

--- /task ---

--- save ---

