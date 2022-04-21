## कुछ पकवान जोड़ें

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
पिनाटा पकवानो से भरे हुए होते हैं और जब वे टूटने लगते हैं, तो पकवान बाहर गिर जाते हैं। इस चरण में, आप हर बार मारने पर पिनाटा से बाहर निकलने के लिए अंतरराष्ट्रीय खाद्य पकवानो को चेतन करेंगे। क्या आप किसी भी पकवान को पहचानते हैं?
</div>
<div>
![एक एनिमेटेड छवि जिसमें पिनाटा को कई बार मारते हुए दिखाया गया है। हर बार, चार यादृच्छिक पकवान यादृच्छिक स्थिति में आते हैं और फिर धीरे-धीरे एक घेरे में घूमते हैं।](images/spinning-treats.gif){:width="300px"}
</div>
</div>

<p style="border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;">
Scratch में <span style="color: #0faeb0">**पोशाक**</span> एक ऐसी छवि है जो स्प्राइट के दिखने के तरीके को बदल देती है। हमारे **ग्राफिक डिजाइनरों** ने दुनिया भर के Code Club नेताओं से उन्हें यह बताने के लिए कहा कि वे एक समारोह में कौन से पकवान रखेंगे। उम्मीद है, उनके द्वारा बनायीं गयी कुछ पकवान पोशाकें आपके लिए परिचित होंगी - और अन्य पूरी तरह से नयी।      
</p>

--- task ---

स्प्राइट सूची में **Treats** स्प्राइट पर क्लिक करें, फिर **Costumes** टैब पर क्लिक करें।

26 पकवान पोशाकें हैं - और आप उन सभी का उपयोग करने जा रहे हैं!

![The specially created treat images shown as a collection of treats.](images/treats.png)

--- /task ---

--- task ---

**Code** टैब पर क्लिक करें, फिर अपना प्रोजेक्ट शुरू होने पर पिनाटा में पकवानो को `hide`{:class="block3looks"} करने के लिए एक स्क्रिप्ट बनाएं:

![The Treats sprite icon.](images/treats-sprite.png)

```blocks3
when flag clicked
hide
go to x: (0) y: (100)
```

--- /task ---

Four treats will escape the piñata each time the piñata is hit. By **cloning** the **Treats** sprite, you can create multiple treats.

<p style="border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;">
A <span style="color: #0faeb0">**clone**</span> in Scratch is a copy of a sprite. It has all the same code, costumes, and sounds of the original sprite.      
</p>

--- task ---

Click on the **Piñata** sprite.

Insert a `repeat`{:class="block3control"} loop into your existing code. Change the value to `4`{:class="block3control"} then add a `create clone of myself`{:class="block3control"} block. Use the drop-down arrow to select the `Treats`{:class="block3control"} sprite:

![The Pinata sprite icon.](images/pinata-sprite.png)

```blocks3
when this sprite clicked
if <(hits) < (10)> then
start sound [Boing v]
change [hits v] by (1)
+ repeat (4) // Change to 4
create clone of (Treats v) // Select Treats
end
if <(hits)=(10)> then
switch costume to (broken v)
broadcast (party v)
```

**Tip:** Use the spare space in the Code area to build your new code then drag it into the existing script:

![The repeat and clone blocks are assembled on their own in the Code area before being dragged into position in the script.](images/code-area.gif) --- /task ---

--- task ---

Click on the **Treats** sprite.

Create a new script using the `when I start as a clone`{:class="block3control"} block.

Add blocks from the `Looks`{:class="block3looks"} blocks menu to control the appearance of each new clone:

![The Treats sprite icon.](images/treats-sprite.png)

```blocks3
when I start as a clone
show
go to [back v] layer // Change to back
switch costume to (Knafeh v)
```

--- /task ---

--- task ---

You can pick random treats to be released when the piñata is hit. Use a `pick random`{:class="block3operators"} operator to select a random costume from `1`{:class="block3operators"} to `26`{:class="block3operators"} each time a clone is created:

![The Treats sprite icon.](images/treats-sprite.png)

```blocks3
when I start as a clone
show
go to [back v] layer 
+ switch costume to (pick random (1) to (26)) // Change to 26
```

--- /task ---

--- task ---

At the moment, the **Treats** clones will appear behind the **Piñata** sprite, but treats should fall from the piñata to a random position.

Add code to make the cloned **Treats** sprites `glide`{:class="block3motion"} to a random position:

![The Treats sprite icon.](images/treats-sprite.png)

```blocks3
when I start as a clone
show
go to [back v] layer
switch costume to (pick random (1) to (26))
+ glide (1) secs to (random position v) 
```

--- /task ---

--- task ---

**Test:** Run your project and hit the piñata to see four clones of the **Treats** sprite after each hit. The costumes will be selected at random and the treats will each glide to a random position.

![An animated image showing the pinata being hit three times. Each time, four random treats fall out to random positions.](images/four-treats.gif)

--- /task ---

--- task ---

Add animation to make the **Treats** sprite clones `turn`{:class="block3motion"} `forever`{:class="block3control"} when they reach their random position. Remember animations work best when small movements are used, so change the number of degrees to `1`{:class="block3motion"}:

![The Treats sprite icon.](images/treats-sprite.png)

```blocks3
when I start as a clone
show
go to [back v] layer
switch costume to (pick random (1) to (26)
glide (1) secs to (random position v) 
+ forever
turn right (1) degrees
```

--- /task ---

--- task ---

**Test:** Run your project again to see the **Treats** sprite clones spin.

![An animated image showing the pinata being hit multiple times. Each time, four random treats fall out to random positions then slowly rotate in a circle.](images/spinning-treats.gif)

--- /task ---

--- save ---
