## Hit the piñata

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
In this step, you will code the piñata to play a sound and count one hit every time the piñata is clicked.
</div>
<div>
![](images/image.png){:width="300px"}
</div>
</div>

--- task ---

Click on the **Sounds** tab for the **Piñata** sprite and you will find a **Clown Honk** sound. Click on the **Play** icon to hear the sound.

![desc](images/play-sound.png)

--- /task ---

A group of connected blocks in Scratch is called a **script**. Sprites can have more than one script.

--- task ---

Click on the **Code** tab. From the `Events`{:class="block3events", drag a `when this sprite clicked`{:class="block3events"} block into the Code area to start a new script. 

In the `Sound`{:class="block3sound"} blocks menu, find the `start sound`{:class="block3sound"} block. Drag it underneath the `when this sprite clicked`{:class="block3events"} block. 

```blocks3
when this sprite clicked
start sound [Clown Honk v]
```

--- /task ---

--- task ---

**Test:** Run your project by clicking on the **Green flag** above the stage. Click on the piñata as it swings to hear the Clown Honk sound. 

--- /task ---

A `variable`{:class="block3variables"} is a way of storing numbers and/or text. The number of hits will be stored in a variable so it can be used at any time.

--- task ---

From the `Variables`{:class="block3variables"} blocks menu, click the **Make a Variable** button.

Call your new variable **hits**:

![desc](images/new-variable.png)

**Notice:** The new 'hits' variable appears on the Stage and can now be used in the `Variable`{:class="block3variables"} blocks.

--- /task ---

--- task ---

Each time the project starts the number of `hits`{:class="block3variables"} should be shown on the Stage and the count reset to `0`.

Drag the `show variable hits`{:class="block3variables"} and `set hits to 0`{:class="block3variables"} blocks into the first script in the Code area, between the `switch costume to`{:class="block3looks"} block and the `go to x: (0) y: (180)`{:class="block3motion"} block. A gap will open up and the block will snap into place.

![desc](images/inserting-code.gif)

Your code should look like this:

```blocks3
when flag clicked
switch costume to ( v)
+ show variable [hits v]
+ set [hits v] to (0)
go to x: (0) y: (180)
point in direction (90)
forever
repeat (10)
turn right (1) degrees
end
repeat (20)
turn left (1) degrees
end
repeat (10)
turn right (1) degrees
end
```

--- /task ---

--- task ---

Every time the **Piñata** sprite is clicked the number of `hits`{:class="block3variables"} should increase`.

Add a block to change `hits`{:class="block3variables"} by `1` when the **Piñata** sprite is clicked:

```blocks3
when this sprite clicked
start sound [Clown Honk v]
+ change [hits v] by (1)
```

--- /task ---

--- task ---

**Test:** Run your project a couple of times. Check that `hits`{:class="block3variables"} always starts at `0` and increases by `1` each time you click on the **Piñata** sprite.

--- /task ---

A Piñata is hard to break but it does not last forever. Your piñata will last for `10` `hits`{:class="block3variables"} before breaking open.

An `if`{:class="block3control"} block can be used to check `if`{:class="block3control"} a condition is 'true'. 

--- task ---

Add an `if`{:class="block3control"} block to the **Piñata** sprite’s `when this sprite clicked`{:class="block3events"} script:

```blocks3
when this sprite clicked
start sound [Clown Honk v]
change [hits v] by (1)
+ if <> then
```

--- /task ---

The `if`{:class="block3control"} has a hexagon-shaped input. This means you can put a **condition** here.

--- task ---

The **Piñata** sprite should break open `if`{:class="block3control"} it has `10` `hits`{:class="block3variables"}.

First add an `=`{:class="block3operators"} operator into the hexagon-shaped input:

```blocks3
when this sprite clicked
start sound [Clown Honk v]
change [hits v] by (1)
+ if <() = ()> then
```

--- /task ---

--- task ---

Finish building the  `if`{:class="block3control"} condition by dragging in the `hits`{:class="block3variables"} to the left of the `=`{:class="block3operators"} operator and typing the value `10` on the right:

```blocks3
when this sprite clicked
start sound [Clown Honk v]
change [hits v] by (1)
+ if <(hits) = (10)> then
```

--- /task ---

--- task ---

Add blocks so that `if`{:class="block3control"} the condition is 'true' then the `hits`{:class="block3variables"} will hide from the Stage and the **Piñata** sprite will change to a broken costume:

```blocks3
when this sprite clicked
start sound [Clown Honk v]
change [hits v] by (1)
if <(hits) = (10)> then
+ hide variable [hits v]
+ switch costume to ( v) // Your broken costume
```

--- /task ---

--- task ---

**Test:** Run your project a couple of times. Check that the `hits`{:class="block3variables"} shows at the start then hides when you have clicked the **Piñata** sprite `10` times. 

Also check that the **Piñata** sprite starts with a 'whole' costume then changes to a 'broken' costume after `10` `hits`{:class="block3variables"}.  

--- /task ---

When the **Piñata** sprite has broken, all the other sprites need to know that the party has started.

In Scratch, the `broadcast`{:class="block3events"} block can be used to **send** a message that all sprites can **receive**.

--- task ---

Add a `broadcast message`{:class="block3events"} block.

```blocks3
when this sprite clicked
start sound [Clown Honk v]
change [hits v] by (1)
if <(hits) = (10)> then
hide variable [hits v]
switch costume to ( v)
+ broadcast (message1 v)
```

 Click on `message1` and choose **New message**. Name the new message `party`:

![desc](images/new-message.png)

Your `broadcast`{:class="block3events"} block will look like this:

```blocks3
broadcast (party v)
```

--- /task ---

--- save ---
