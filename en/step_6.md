## Create a message

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Write a message and animate it using motion and colour effects. 
</div>
<div>
![](images/image.png){:width="300px"}
</div>
</div>

What would you write in a birthday card to send to Code Club? It could be something about:
+ Your favourite thing about Code Club
+ Your fabulous Code Club leader
+ Details of what you want to make next

<p style="border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;">
The first Code Club projects were written in English but within a year they had been translated into Brazilian Portuguese, Dutch, German, Norwegian and Ukrainian. French, Greek and Spanish translations quickly followed and now there are projects in <span style="color: #0faeb0">**28 native languages**</span>. Thank you to our awesome translation community!

![](images/birthday-languages.png)
</p>

--- task ---



--- /task ---

Create text costume with message
Hide and position in pinata at the start
When party show and do falling, zooming movement
When in position do effect changes forever

![The message sprite icon](images/message-sprite.png)

--- save ---


when flag clicked
hide
set size to (10) %
go to x: (0) y: (100)

when i receive [party v]
show
repeat (20)
change size by (5)
change y by (-10)
end
forever
change size by (20)
change [color v] effect by (25)
wait (0.5) seconds
change size by (-20)