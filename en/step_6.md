## Create a message

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Write a message and animate it using motion and colour effects. 
</div>
<div>
![An animated image showing the message falling then changing size and colour when it has reach the final message fall position.](images/falling-message.gif){:width="300px"}
</div>
</div>

What would you write in a birthday card to send to Code Club? It could be:
+ Your favourite thing about Code Club
+ A message about your fabulous Code Club leader
+ Details of what you want to make next with your coding skills

<p style="border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;">
The first Code Club projects were written in English but within a year they had been translated into Brazilian Portuguese, Dutch, German, Norwegian and Ukrainian. French, Greek and Spanish translations quickly followed and now some of the Code Club projects have been translated into <span style="color: #0faeb0">**28 native languages**</span>. Thank you to our awesome translation community!

![Multiple images saying Happy Birthday in various native languages.](images/birthday-languages.png)
</p>

--- task ---

Click on the **Message** sprite in the Sprite list and select the **Costumes** tab. 

The costume has some text saying 'Happy Birthday Code Club'. Double click (or tap and hold on a tablet) on the text to select the text editing tool.

![The costume editor with Text tool selected and text highlighted.](images/text-edit.png)

--- /task ---

--- task ---

You can now type your new Code Club birthday message. Press **Enter** on your keyboard to start a new line. 

**Tip:** Don't worry if your message is a bit too big for the box as you can resize it later.

![The text editor showing a new message has been typed in place of the old message.](images/new-text.png)

--- /task ---

--- task ---

**Choose:** Click on the Fill icon to open the colour dropdown menu. Move the fill sliders to the left or right to select your favourite color. 

![The Fill dropdown menu with sliders for color, saturation and brightness. The message has changed from green to purple.](images/font-colour.png)

--- /task ---

--- task ---

**Choose:** Click on the Font tool and a dropdown list of fonts will appear. The 'Pixel' font is selected in the starter project but you can use any of the fonts available. 

![The Font dropdown menu showing a choice of 9 different fonts. The 'Marker' font has been selected.](images/font-type.png)

--- /task ---

--- task ---

Click on the Select tool and 8 circles will appear around your message. Use these circles to resize your message by clicking on them and dragging them within the white box. 

![The Select tool is highlighted and the message has small circles in each corner and at the central vertical and horizontal borer points so that it can be resized in multile directions.](images/resize-message.png)

--- /task ---

Your message is ready, now you can add code to hide your message inside the piñata and make your message fall from the piñata after the 10th hit. 

--- task ---

Click on the **Code** tab then create a script to `hide`{:class="block3looks"} the message in the piñata when your project starts:

![The message sprite icon.](images/message-sprite.png)

```blocks3
when flag clicked
hide
set size to (10) % // change to 10 to start small
go to x: (0) y: (100) // inside the piñata
```

--- /task ---

--- task ---

Create a new script to start when the `party`{:class="block3events"} message has been received. 

Add a `repeat`{:class="block3control"} loop to animate the message. the message will `change size`{:class="block3looks"} to grow and `change y`{:class="block3motion"} position to fall as it animates:

![The message sprite icon.](images/message-sprite.png)

```blocks3
when I receive [party v]
show
repeat (20) // change to 20
change size by (5) // change to 5
change y by (-10) // change to -10
```

--- /task ---

--- task ---

**Test:** Run your project, hit the piñata 10 times to see the message fall.

![An animated image showing the pinata being hit 10 times. Treats appear after each hit and on the 10th hit the pinata breaks and the message falls to the bottom of the screen. It gets bigger as it falls.](images/falling-message.gif)

--- /task ---

--- save ---
