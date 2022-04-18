## पिनाटा को मारें

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
इस चरण में, आप पिनाटा को ध्वनि चलाने के लिए और हर बार पिनाटा क्लिक करने पर एक हिट की गणना करने के लिए कोड करेंगे।
</div>
<div>
![पिनाटा को दस बार क्लिक करते हुए दिखाने वाला एक एनिमेटेड चित्र। दसवीं बार के बाद, पोशाक टूटी हुई में बदल जाती है और वेरिएबल गायब हो जाता है।](images/break-pinata.gif){:width="300px"}
</div>
</div>

--- task ---

**Pinata** स्प्राइट के लिए **Sounds** टैब पर क्लिक करें और आपको **Boing** ध्वनि मिलेगी। ध्वनि सुनने के लिए **Play** आइकन पर क्लिक करें।

![The Sounds tab showing the Boing sound in the Sounds list with the Play icon (a white triangle in a blue circle) highlighted at the bottom.](images/play-boing.png)

--- /task ---

Scratch में जुड़े हुए खंडों के समूह को **स्क्रिप्ट** कहा जाता है। स्प्राइट्स में एक से अधिक स्क्रिप्ट हो सकती हैं।

--- task ---

**Code** टैब पर क्लिक करें। `Events`{:class="block3events"} से, एक `when this sprite clicked`{:class="block3events"} खंड को कोड क्षेत्र में खिसकाएं एक नई स्क्रिप्ट शुरू करने के लिए।

`Sound`{:class="block3sound"} खंड मेन्यू में, `start sound`{:class="block3sound"} खंड ढूंढें। इसे `when this sprite clicked`{:class="block3events"} खंड के नीचे खिसकाएं:

![The Piñata sprite icon.](images/pinata-sprite.png)

```blocks3
when this sprite clicked
start sound [Boing v]
```

--- /task ---

--- task ---

**परीक्षण:** मंच के ऊपर के **हरे झंडे** पर क्लिक करके अपना प्रोजेक्ट चलाएं। झूलते हुए पिनाटा पर क्लिक करें बोईंग ध्वनि को सुनने के लिए।

--- /task ---

`वेरिएबल`{:class="block3variables"} नंबर और/या टेक्स्ट को स्टोर करने का एक तरीका है। पिनाटा पर क्लिक करने की संख्या `hits`{:class="block3variables"} नामक एक वेरिएबल में संग्रहीत की जाएगी ताकि इसे किसी भी समय उपयोग किया जा सके।

--- task ---

`Variables`{:class="block3variables"} खंड मेन्यू से, **Make a Variable** बटन पर क्लिक करें।

![The variables blocks menu with the 'Makes a Variable' button.](images/make-variable.png)

अपने नए वेरिएबल को नाम दें **hits**:

![The 'New variable' pop-up window with the name 'hits' typed in the 'New variable name' box.](images/new-variable.png)

**ध्यान दें:** नया 'hits' वैरिएबल मंच पर दिखाई देता है और अब इसे `वेरिएबल`{:class="block3variables"} खंड में इस्तेमाल किया जा सकता है।

![The hits variable on the Stage.](images/variable-stage.png)

![The Variable blocks including new 'hits' block.](images/variable-blocks.png)

--- /task ---

--- task ---

हर बार प्रोजेक्ट शुरू होने पर, `hits`{:class="block3variables"} की संख्या को `0`{:class="block3variables"} पर रीसेट किया जाना चाहिए।

कोड क्षेत्र में पहली स्क्रिप्ट में `set hits to 0`{:class="block3variables"} खंड को खिसकाएं, `switch costume to`{:class="block3looks"} खंड और `go to x: (0) y: (180)`{:class="block3motion"} खंड के बीच।

आपका कोड इस प्रकार दिखना चाहिए:

![The Piñata sprite icon.](images/pinata-sprite.png)

```blocks3
when flag clicked
switch costume to (whole v)
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

हर बार **Piñata** स्प्राइट पर क्लिक करने पर, `hits`{:class="block3variables"} की संख्या बढ़नी चाहिए।

`hits`{:class="block3variables"} को `1`{:class="block3variables"} से बदलने के लिए एक खंड जोड़ें जब **Piñata** स्प्राइट क्लिक किया जाता है:

![The Piñata sprite icon.](images/pinata-sprite.png)

```blocks3
when this sprite clicked
start sound [Boing v]
+ change [hits v] by (1)
```

--- /task ---

--- task ---

**परीक्षण:** अपने प्रोजेक्ट को कुछ बार चलाएँ। जांचें कि `hits`{:class="block3variables"} हमेशा `0`{:class="block3variables"} से शुरू होता है और हर बार जब आप **Piñata** स्प्राइट पर क्लिक करते हैं तो `1`{:class="block3variables"} से बढ़ जाता है।

![The Stage showing the number stored in the hits variable is '8'.](images/hits-increase.png)

--- /task ---

एक पिनाटा तोड़ना मुश्किल है लेकिन यह हमेशा के लिए नहीं रहता। आपका पिनाटा टूटकर खुलने से पहले `10 मारों`{:class="block3variables"} तक चलेगा।

**शर्त** के आधार पर निर्णय लेने के लिए `if`{:class="block3control"} ब्लॉक का उपयोग किया जा सकता है।

<p style="border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;">
हम निर्णय लेने के लिए हर समय <span style="color: #0faeb0">**conditions**</span> का उपयोग करते हैं। हम कह सकते हैं "यदि पेंसिल कुंद है, तो उसे तेज करें"। `if` खंड और शर्तें हमें कोड लिखने देती हैं जो इस बात पर निर्भर करता है कि कोई शर्त सही है या गलत।
</p>

--- task ---

`Control`{:class="block3control"} खंड मेन्यू पर जाएं। कोड क्षेत्र में `if`{:class="block3control"} खंड को खिसकाएं और अपने `when this sprite clicked`{:class="block3events"} स्क्रिप्ट के आस पास दाल दें:

![The Piñata sprite icon.](images/pinata-sprite.png)

```blocks3
when this sprite clicked
+ if <> then
start sound [Boing v]
change [hits v] by (1)

```

--- /task ---

`if`{:class="block3control"} ब्लॉक में एक षट्भुज के आकार का इनपुट होता है जहां आप एक शर्त बना सकते हैं।

--- task ---

The **Piñata** sprite should play a sound and increase the count of `hits`{:class="block3variables"} **`if`{:class="block3control"}** the number of `hits`{:class="block3variables"} is `less than`{:class="block3operators"} `10`{:class="block3variables"}.

First add a `<`{:class="block3operators"} operator into the hexagon-shaped input:

![The Piñata sprite icon.](images/pinata-sprite.png)

```blocks3
when this sprite clicked
+ if <() < ()> then
start sound [Boing v]
change [hits v] by (1)

```

--- /task ---

--- task ---

Finish building the `if`{:class="block3control"} condition by dragging in the `hits`{:class="block3variables"} variable to the left of the `<`{:class="block3operators"} operator and typing the value '10' on the right:

![The Piñata sprite icon.](images/pinata-sprite.png)

```blocks3
when this sprite clicked
+ if <(hits) < (10)> then
start sound [Boing v]
change [hits v] by (1)

```

--- /task ---

--- task ---

**Test:** Run your project again. Hit the piñata 10 times to hear the sound and see the `hits`{:class="block3variables"} variable increase.

Hit the piñata a few more times. The `hits`{:class="block3variables"} variable will not go above 10 because that condition is no longer 'true' so the code inside the `if`{:class="block3control"} block won't run.

--- /task ---

--- task ---

Add a second `if`{:class="block3control"} block inside the first. This time the condition will check if `hits`{:class="block3variables"} `=`{:class="block3operators"} 10 and if 'true' the costume will change to `broken`{:class="block3looks"}:

![The Piñata sprite icon.](images/pinata-sprite.png)

```blocks3
when this sprite clicked
if <(hits) < (10)> then
start sound [Boing v]
change [hits v] by (1)
+ if <(hits)=(10)> then
switch costume to (broken v)

```

--- /task ---

--- task ---

**Test:** Run your project a couple of times. Check that the **Piñata** sprite starts with the 'whole' costume then changes to the 'broken' costume after `10 hits`{:class="block3variables"}.

![An animated image showing the piñata being clicked ten times. After the tenth time, the costume changes to broken.](images/break-pinata.gif)

--- /task ---

When the **Piñata** sprite has broken, all the other sprites need to know that the party has started.

In Scratch, the `broadcast`{:class="block3events"} block can be used to **send** a message that all sprites can **receive**.

--- task ---

Add a `broadcast message`{:class="block3events"} block from the `Events`{:class="block3events"} blocks menu:

![The Piñata sprite icon.](images/pinata-sprite.png)

```blocks3
when this sprite clicked
if <(hits) < (10)> then
start sound [Boing v]
change [hits v] by (1)
if <(hits)=(10)> then
switch costume to (broken v)
+ broadcast (message1 v)
```

Click on `message1`{:class="block3events"} and choose **New message**. Name the new message `party`{:class="block3events"}.

![The drop-down menu on the broadcast block showing the 'New message' menu option.](images/new-message.png)

![The New message pop-up window with 'New message name' box highlighted and the typed word 'party'.](images/party-message.png)

Your `broadcast`{:class="block3events"} block will look like this:

```blocks3
broadcast (party v)
```

--- /task ---

--- save ---
