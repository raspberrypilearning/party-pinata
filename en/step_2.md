## Start the party

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
In this step, you will choose a piñata costume and code the piñata to swing.
</div>
<div>
![An animated gif showing the stage with the pinata sprite positioned at the top centre and swinging left to right.](images/swinging-pinata.gif){:width="300px"}
</div>
</div>

--- task ---

Open the [Party piñata starter project](https://scratch.mit.edu/projects/653082997/editor){:target="_blank"}. Scratch will open in another browser tab.

[[[working-offline]]]

--- /task ---

The Scratch editor looks like this:

![An annotated screenshot of the Scratch editor, with the Stage, Stage pane, Sprite pane, Sprite list, and Code area labelled.](images/scratch-interface.png)

The **Stage** is where your project runs and a **backdrop** changes the way that the Stage looks. A Code Club party backdrop has been added for you. 

In Scratch, characters and objects are called **sprites**, and they appear on the Stage. You can see the Piñata and Stick sprites on the Stage.

![The stage with a patterned blue backdrop with presents and balloons. Also on the stage are piñata and stick sprites.](images/backdrop-and-sprites.png)

At the moment there is not much happening at this party. You can change that! 

--- task ---

A sprite can have code, costumes, and sounds to change the way that it looks and what it does.

Click on the **Piñata** sprite in the Sprite list and select the **Costumes** tab. There are two piñata costumes one named 'whole' and the other named 'broken'. 

![Side by side images of the two piñata costumes. The left is a whole piñata, the right has broken open.](images/pinata-costumes.png)

--- /task ---

--- task ---

Click on the **Code** tab. Go to the `Looks`{:class="block3looks"} blocks menu then drag a `switch costume to`{:class="block3looks"} block to the Code area. 

Click on the costume name to open a drop-down menu then select the 'whole' costume:

![The Piñata sprite icon.](images/pinata-sprite.png)

```blocks3
switch costume to (whole v) 
```

![An animated image showing the switch costume block being dragged from the Looks blocks menu to the Code area.](images/switch-costume.gif)

--- /task ---

Blocks can be connected together in the Code area to run more than one at a time. Connected blocks will run in order from top to bottom.

--- task ---

Drag a `When flag clicked`{:class="block3events"} block from the `Events`{:class="block3events"} blocks menu and connect it to the top of your looks block in the Code area. The blocks will snap together:

![The Piñata sprite icon.](images/pinata-sprite.png)

```blocks3
+ when flag clicked
switch costume to (whole v)
```
![when flag clicked block being added to the code area and connected to the switch costume block](images/add-flag-clicked.gif)

--- /task ---

--- task ---

The starting position of a piñata is always the same, it only starts moving when the piñata game is ready to play. 

In the `Motion`{:class="block3motion"} blocks menu, find the `go to x: 0 y: 180`{:class="block3motion"} and  `point in direction 90`{:class="block3motion"} blocks. Drag the blocks to the Code area and connect them to the bottom of your code:

![The Piñata sprite icon.](images/pinata-sprite.png)

```blocks3
when flag clicked
switch costume to (whole v)
+ go to x: (0) y: (180)
+ point in direction (90) // Ready position
```

--- /task ---

A `forever`{:class="block3control"} loop runs the code blocks inside it again and again. It is the perfect loop for a swinging piñata that is hard to hit.

--- task ---

Drag a `forever`{:class="block3control"} block from the `Control`{:class="block3control"} blocks menu and connect it to the bottom of your code:

![The Piñata sprite icon.](images/pinata-sprite.png)

```blocks3
when flag clicked
switch costume to (whole v)
go to x: (0) y: (180)
point in direction (90)
+ forever
```

--- /task ---

A `repeat`{:class="block3control"} loop can be used to make the piñata repeat a small movement many times. This will make the piñata appear animated.

--- task ---

Drag a `repeat 10`{:class="block3control"} block from the `Control`{:class="block3control"} blocks menu and attach it inside your `forever`{:class="block3control"} loop. 

Go to the `Motion`{:class="block3motion"} blocks menu and drag a `turn right 15 degrees`{:class="block3motion"} block into the `repeat`{:class="block3control"} block. 

Change the `15` degrees to `1` degree so that the piñata only swings a small amount each time:

![The Piñata sprite icon.](images/pinata-sprite.png)

```blocks3
when flag clicked
switch costume to (whole v)
go to x: (0) y: (180)
point in direction (90)
forever
+ repeat (10) 
turn right (1) degrees // change to 1
```
![repeat block being added within the forever block and then a turn right block added within it](images/add-repeat.gif)

--- /task ---

--- task ---

**Test:** Run your project, by clicking on the **Green flag** above the stage, to see the piñata swing. 

Mmm, something is not quite right! When an object is hung from the ceiling, it won't just rotate in one direction, it will also swing back to the left. 

Stop your project by clicking on the **red stop sign** above the stage.

--- /task ---

--- task ---

Add code to your `forever`{:class="block3control"} loop so that the piñata swings from the centre back and forth continuously:

![The Piñata sprite icon.](images/pinata-sprite.png)

```blocks3
when flag clicked
switch costume to (whole v)
go to x: (0) y: (180)
point in direction (90)
forever
repeat (10)
turn right (1) degrees // swing right 10 times
end
+ repeat (20) // change to 20
turn left (1) degrees // change to 1
end
+ repeat (10) // change to 10
turn right (1) degrees // change to 1
end
```

--- /task ---

--- task ---

**Test:** Run your project to see the piñata swing to the left and right. 

**Debug:** If the piñata does not swing correctly: 
+ look at your code to make sure the `repeat`{:class="block3control"} blocks are in the correct position
+ check that the `turn left`{:class="block3motion"} and `turn right`{:class="block3motion"} arrows are correct
+ make sure that you have used the numbers from the code above

![An animated gif showing the stage with the pinata sprite positioned at the top centre and swinging left to right.](images/swinging-pinata.gif)

--- /task ---

--- save ---

