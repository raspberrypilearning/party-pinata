## ابدأ الحفلة

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
في هذه الخطوة، سنختار ملابس بيناتا و نكتب كود التأرجح لها.
</div>
<div>
![صورة متحركة تظهر البيناتا في المنتصف وتتأرجح يميناً ويساراً.](images/swinging-pinata.gif){:width="300px"}
</div>
</div>

--- task ---

افتح [Party piñata starter project](https://scratch.mit.edu/projects/653082997/editor){:target="_blank"}. سيتم فتح Scratch في علامة تبويب متصفح أخرى.

[[[working-offline]]]

--- /task ---

يظهر محرر Scratch على النحو التالي:

![لقطة شاشة مشروحة لمحرر Scratch، مع تسمية لكل من المنصة، جزء المنصة، جزء الكائن، قائمة الكائن، ومنطقة كتابة الشفرة البرمجية.](images/scratch-interface.png)

**Stage** هي المكان الذي يعمل فيه المشروع، **backdrop** تغير مظهر مسرح العمل. تمت إضافة خلفية حفلة Code Club لك.

في Scratch ، تسمى الشخصيات والكائنات **sprites**، وتظهر في<0>Stage</0>. يمكنك رؤية **Piñata** و **Stick** sprites على المنصة.

![المسرح مع خلفية زرقاء منقوشة مع هدايا وبالونات. أيضا على خشبة المسرح توجد البنياتا والعصا.](images/backdrop-and-sprites.png)

حتى هذهِ اللحظة لم نبدأ بالاحتفال. يمكنك تغيير ذلك!

--- task ---

يمكن أن يكون للكائن تعليمة برمجية، مظاهر، وأصوات لتغيير الطريقة التي يظهر بها وما يفعله.

من قائمة الكائنات(spirit) اختار** Piñata**، بعدها اضغط على تبويب ** Costumes**. هناك نوعان من أزياء البنياتا ، أحدهما يسمى 'whole' والآخر يسمى 'broken'.

![صور جنبًا إلى جنب لمظهري البينياتا. اليسار عبارة عن بينياتا كاملة، واليمين بنياتا مكسورة.](images/pinata-costumes.png)

![علامة التبويب المظاهر (علامة التبويب الوسطى في أعلى اليسار).](images/costumes-tab.png)

--- /task ---

--- task ---

انقر فوق علامة التبويب **المقاطع البرمجية**. اذهب الى `الهيئة`{:" class="block3looks} 
قائمة الكتل ثم اسحب `غير المظهر إلى`{ ":class="block3looks} 
مجموعة لمنطقة التعليمات البرمجية.

اضغط على اسم المظهرليفتح قائمة **القائمة المنسدلة** اختار منها `whole`{:class="block3looks"} مظهر:

![كائن البينياتا.](images/pinata-sprite.png)

```blocks3
switch costume to (whole v) // Update to 'whole'
```

![صورة متحركة تعرض كتلة تبديل المظهر يتم سحبها من قائمة كتل المظهر إلى مساحة البرمجة.](images/switch-costume.gif)

--- /task ---

يمكن توصيل الكتل معًا في منطقة التعليمات البرمجية لتشغيل أكثر من كتلة في وقت واحد. سيتم تشغيل الكتل المتصلة بالترتيب من أعلى إلى أسفل.

--- task ---

اسحب كتلة `When flag clicked`{:class="block3events"} من قائمة `Events`{:class="block3events"} واربطها في اعلى الكتل الظاهرة في منطقة التعليمة البرمجية. الكتل سوف تلتصق ببعضها البعض:

![كائن البينياتا.](images/pinata-sprite.png)

```blocks3
+ when flag clicked
switch costume to (whole v)
```
![اضافة كتلة عند النقر فوق العلم إلى مساحة البرمجة وتوصيلها بكتلة غيّر المظهر الى.](images/add-flag-clicked.gif)

--- /task ---

موقع البنياتا هو نفسه دائماً في منتصف المسرح، يبدأ بالحركة فقط عندما تبدأ اللعب.

--- task ---

في `الحركة`{:class="block3motion"} قائمة الكتل `اذهب الى x: 0 y: 180`
{:class="block3motion"}
و `اتجه نحو الاتجاه 90`{:class="block3motion"} كتلة. اسحب الكتل إلى منطقة التعليمات البرمجية وقم بتوصيلها بأسفل التعليمات البرمجية الخاصة بك:

![كائن البينياتا.](images/pinata-sprite.png)

```blocks3
when flag clicked
switch costume to (whole v)
+ go to x: (0) y: (180)
+ point in direction (90) // Ready position
```

--- /task ---

تقوم حلقة `كرر باستمرار`{: class = "block3control"} بتشغيل كتل التعليمات البرمجية بداخلها مرارًا وتكرارًا. وهي الحلقة التكرارية المثالية للبنياتا المتأرجحة التي يصعب الوصول إليها.

--- task ---

اسحب كتلة `كرر بستمرار`{:class="block3control"} من قائمة الكتل `التحكم`{:class="block3control"} و وقم بتوصيلها باسفل التعليمات البرمجية التي استخدمتها:

![كائن البينياتا.](images/pinata-sprite.png)

```blocks3
when flag clicked
switch costume to (whole v)
go to x: (0) y: (180)
point in direction (90)
+ forever
```

--- /task ---

حلقة `تكرار`{:class="block3control"} 
يمكن استخدامها لجعل **Piñata** الكائن يكرر حركة صغيرة عدة مرات. هذا سيجعل البنياتا تظهر متحركة.

--- task ---

اسحب كتلة `كرر 10 مرات`{:class="block3control"} 
في منطقة التعليمات البرمجية وقم بإرفاقها داخل الحلقة `كرر بستمرار`{:class="block3control"} حلقه تكرارية.

اذهب الى قائمة`الحركة`{:class="block3motion"}، واسحب الكتلة`turn clockwise 15 degrees`{:class="block3motion"} block وضعها داخل `repeat`{:class="block3control"} block.

قم بتغيير الدرجة `15`{: class = "block3motion"} إلى `1`{: class = "block3motion"} بحيث يتأرجح piñata حركة صغيرة في كل مرة:

![كائن البينياتا.](images/pinata-sprite.png)

```blocks3
when flag clicked
switch costume to (whole v)
go to x: (0) y: (180)
point in direction (90)
forever
+ repeat (10) 
turn right (1) degrees // Change to 1
```
![يتم إضافة كتلة كرر داخل الكتلة كرر باستمرار ثم يتم إضافة كتلة في اتجاه عقارب الساعة داخلها.](images/add-repeat.gif)

--- /task ---

--- task ---

**Test:** قم بتشغيل المشروع، بالضغط على العلم الاخضر**green flag**، حتى تتاكد بان البنياتا تتأرجح.

**مم ، شيء ما ليس صحيحًا تمامًا!** عندما يتم تعليق شيء ما من السقف ، فإنه لن يدور في اتجاه واحد فقط ، بل سيتأرجح ذهابًا وإيابًا.

أوقف مشروعك بالضغط على **أيقونة التوقف الحمراء** أعلى المنصة.

![ايقونات العلم الأخضر والتوقف معروضة جنبًا إلى جنب.](images/start-stop.png)

--- /task ---

--- task ---

أضف شفرة برمجية الى الحلقة التكرارية `كررّ باستمرار`{:class="block3control"}، بحيث تتأرجح البنياتا من المركز ذهاباً واياباً مثل البندول:

![كائن Piñata مع الأسهم أسفله يوضح أنه يتأرجح في اتجاه عقارب الساعة من المركز، ثم عكس اتجاه عقارب الساعة عبر المركز ، ثم في اتجاه عقارب الساعة إلى المركز.](images/pinata-swing.png)

![كائن البينياتا.](images/pinata-sprite.png)

```blocks3
when flag clicked
switch costume to (whole v)
go to x: (0) y: (180)
point in direction (90)
forever
repeat (10) // Swings 10 degrees clockwise from the centre
turn right (1) degrees 
end
+ repeat (20) // Swings 20 degrees anticlockwise through the centre
turn left (1) degrees // Change to 1
end
+ repeat (10) // Swings 10 degrees clockwise back to the centre
turn right (1) degrees // Change to 1
end
```

--- /task ---

--- task ---

**اختبار:** قم بتشغيل المقطع البرمجي الخاص بك لرؤية النتيجة.

**تصحيح:** إذا لم يتأرجح piñata بشكل صحيح:
+ انظر إلى الكود الخاص بك للتأكد من أن الكتل `repeat`{: class = "block3control"} في الموضع الصحيح
+ تأكد من صحة `دوران في اتجاه عقارب الساعة`{: class = "block3motion"} و `انعطاف عكس اتجاه عقارب الساعة`{: class = "block3motion"}
+ تأكد من أنك استخدمت الأرقام من الشفرة البرمجية

![صورة gif متحركة تُظهر المنصة مع كائن Piñata موضوع في أعلى المنتصف ويتأرجح ذهابًا وإيابًا.](images/swinging-pinata.gif)

--- /task ---

--- save ---

