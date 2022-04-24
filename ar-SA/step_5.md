## أضف بعض الحلويات

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
العاب البنياتا مليئة بالحوليات وعندما تبدأ بالتكسر تسقط منها الحلوى. في هذه الخطوة، ستقوم بتحريك الأطعمة العالمية لتسقط من البينياتا في كل مرة يتم ضربها. هل تعرف أي من هذه الحلويات؟
</div>
<div>
![صورة متحركة تظهر ضرب البنياتا عشر مرات. في كل مرة، تسقط أربع حلويات عشوائية في مواضع عشوائية ثم يتم تدويرها ببطء في دائرة.](images/spinning-treats.gif){:width="300px"}
</div>
</div>

<p style="border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;">
<span style="color: #0faeb0">** المظهر **</span> في برنامج in Scratch هي صورة تغير شكل الكائن. طلب ** مصممو الرسوم ** لدينا من قادة Code Club حول العالم إخبارهم بما يحصلون عليه في الحفلة. نأمل أن تكون بعض اشكال الحلوى التي ابتكروها مألوفة بالنسبة لك - والبعض الآخر جديد تمامًا.      
</p>

--- task ---

انقر فوق الكائن **حلوى** في قائمة الكائنات وحدد علامة التبويب **المظاهر**.

هناك 26 مظهر - وستستخدمها جميعًا!

![يتم عرض صور الحلوى التي تم إنشاؤها خصيصًا كمجموعة من الحلوى.](images/treats.png)

--- /task ---

--- task ---

انقر فوق علامة التبويب **المقاطع البرمجية** ثم قم بإنشاء نص برمجي `يخفي`{:class="block3looks"} الحلوى في البنياتا عند بدء مشروعك:

![كائن حلوى.](images/treats-sprite.png)

```blocks3
when flag clicked
hide
go to x: (0) y: (100)
```

--- /task ---

ستهرب أربع قطع حلوى من البنياتا في كل مرة يتم ضربها. من خلال **استنساخ** كائن **حلوى**، يمكنك إنشاء العديد من المكافآت.

<p style="border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;">
<span style="color: #0faeb0">** الاستنساخ **</span> في برنامج Scratch هو نسخة من كائن. يحتوي على نفس الكود والمظاهر وأصوات الكائن الأصلي.      
</p>

--- task ---

انقر على الكائن ** Piñata **.

أدخل حلقة `كرر`{: class = "block3control"} في الكود الموجودة. غيّر القيمة إلى `4`{: class = "block3control"} ثم أضف `إنشاء نسخة من نفسي`{: class = "block3control"} block. استخدم سهم القائمة المنسدلة لاختيار كائن `حلوى`{: class = "block3control"}:

![كائن البينياتا.](images/pinata-sprite.png)

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

**نصيحة:** استخدم المساحة الاحتياطية في منطقة الكود لإنشاء كودك الجديد ثم اسحبه إلى البرنامج النصي الحالي:

![يتم تجميع كتل التكرار والاستنساخ بمفردها في منطقة المقاطع البرمجية قبل سحبها إلى موضعها في نص البرنامج.](images/code-area.gif) --- /task ---

--- task ---

انقر على كائن **حلوى**.

قم بإنشاء نص برمجي جديد باستخدام كتلة `عندما تبدأ نسخة مني`{:class="block3control"}.

أضف كتل من قائمة الكتل `الهيئة`{:class="block3looks"} للتحكم في مظهر كل نسخة جديدة:

![كائن حلوى.](images/treats-sprite.png)

```blocks3
when I start as a clone
show
go to [back v] layer // Change to back
switch costume to (Knafeh v)
```

--- /task ---

--- task ---

يمكنك اختيار حلوى عشوائية ليتم تحريرها عند ضرب البنياتا. استخدم العملية `عدد عشوائي`{:class="block3operators"} لتحديد مظهر عشوائي من `1`{:class="block3operators"} إلى `26`{:class="block3operators"} في كل مرة يتم فيها إنشاء نسخة:

![كائن حلوى.](images/treats-sprite.png)

```blocks3
when I start as a clone
show
go to [back v] layer 
+ switch costume to (pick random (1) to (26)) // Change to 26
```

--- /task ---

--- task ---

في الوقت الحالي، ستظهر نسخ **الحلوى** خلف كائن **Piñata**، ولكن يجب أن تسقط الحلوى من البنياتا إلى موضع عشوائي.

أضف كود لجعل نسخة كائن **الحلوى** `ينزلق`{:class="block3motion"} إلى موضع عشوائي:

![كائن حلوى.](images/treats-sprite.png)

```blocks3
when I start as a clone
show
go to [back v] layer
switch costume to (pick random (1) to (26))
+ glide (1) secs to (random position v) 
```

--- /task ---

--- task ---

**اختبار:** شغّل مشروعك واضرب البنياتا لرؤية اربع نسخ من كائن الـ**حلوى** بعد كل ضربة. سيتم اختيار المظاهر عشوائيًا وستنزلق الهدايا إلى موضع عشوائي.

![صورة متحركة تظهر ضرب البنياتا ثلاث مرات. في كل مرة، تسقط أربع قطع حلوى عشوائية في مواضع عشوائية.](images/four-treats.gif)

--- /task ---

--- task ---

أضف حركة لجعل نسخ كائن **الحلوى** `تدور`{:class="block3motion"} `باستمرار`{:class="block3control"}عندما يصلون إلى موضعهم العشوائي. تذكر أن الرسوم المتحركة تعمل بشكل أفضل عند استخدام حركات صغيرة، لذا قم بتغيير عدد درجات الدوران إلى `1`{:class="block3motion"}:

![كائن حلوى.](images/treats-sprite.png)

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

**اختبار:** شغّل مشروعك مرة أخرى لترى أن **حلوى** المستنسخة تدور.

![صورة متحركة تظهر ضرب البنياتا عدة مرات. في كل مرة، تسقط أربع قطع حلوى عشوائية في مواضع عشوائية ثم يتم تدويرها ببطء في دائرة.](images/spinning-treats.gif)

--- /task ---

--- save ---
