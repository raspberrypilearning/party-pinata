## اضرب البنياتا

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
في هذه الخطوة ، سنقوم باضافة شفرة برمجية لبنياتا لتشغيل الصوت ونحسب ضربة واحدة في كل مرة يتم فيها النقر فوق البنياتا.
</div>
<div>
[صورة متحركة تظهر النقر على piñata عشر مرات. بعد المرة العاشرة ، يتغير المظهر إلى مكسور.] (images / break-pinata.gif) {: width = "300px"}
</div>
</div>

--- task ---

انقر فوق علامة التبويب **الصوت** لـ**بنياتا** وستجد صوت **Boing**. انقر فوق زر **تشغيل** حتى تتمكن من سماع الصوت.

![تعرض علامة تبويب الأصوات ،صوت Boing في قائمة الأصوات مع تمييز أيقونة التشغيل (مثلث أبيض في دائرة زرقاء) في الأسفل.](images/play-boing.png)

--- /task ---

مجموعة الكتل المتصلة في سكراتش تسمى **نص**. يمكن أن تحتوي الكائنات على أكثر من نص.

--- task ---

انقر على تبويب **المقاطع البرمجية**. من `الأحداث`{: class = "block3events"} ، اسحب كتلة `عند النقر على هذا الكائن`{: class = "block3events"} الى منطقة كتابة الشفرة البرمجية.

في قائمة كتل `الصوت`{:class="block3sound"} جد كتلة `ابدأ الصوت`{:class="block3sound"}. أضِف المقطع البرمجي `عند نقر هذا الكائن`{:class="block3events"}:

![كائن البنياتا.](images/pinata-sprite.png)

```blocks3
when this sprite clicked
start sound [Boing v]
```

--- /task ---

--- task ---

**Test:** قم بتشغيل المشروع، بالضغط على العلم الاخضر**green flag**، حتى تتاكد بان البنياتا تتأرجح. انقر على بنياتا وهو يتأرجح لسماع صوت boing.

--- /task ---

`المتغير`{:class="block3variables"} هو وسيلة لتخزين الأرقام و/أو النصوص. سيتم تخزين عدد مرات النقر على بنياتا في متغير يسمى `الضربات`{: class = "block3variables"} بحيث يمكن استخدامه في أي وقت.

--- task ---

انقر على `متغيرات`{: class = "block3variables"} و ثم انقر على زر**انشاء متغير**.

![The variables blocks menu with the 'Makes a Variable' button.](images/make-variable.png)

سمي المتغير الجديد الذي انشاته **الضربات**:

![The 'New variable' pop-up window with the name 'hits' typed in the 'New variable name' box.](images/new-variable.png)

**ملاحظة:** يظهر متغير "الضربات" الجديد على المنصة ويمكن استخدامه الآن في قائمة `المتغيرات`{: class = "block3variables"}.

![The hits variable on the Stage.](images/variable-stage.png)

![The Variable blocks including new 'hits' block.](images/variable-blocks.png)

--- /task ---

--- task ---

في كل مرة يبدأ فيها المشروع ، يجب إعادة تعيين عدد `الضربات`{: class = "block3variables"} إلى `0`{: class = "block3variables"}.

اسحب كتلة`اجعل متغير"ضربات" مساوياً 0`{:class="block3variables"} الى النص البرمجي الاول، بين كتلة `غير المظهر الى`{:class="block3looks"} وكتلة `اذهب الى س: (0) ص: (180)`.

يجب أن تبدو التعليمات البرمجية خاصتك بالشكل التالي:

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

في كل مرة يتم النقر على **بنياتا** ،يجب زيادة عدد `ضربات`{: class = "block3variables"}.

أضف كتلة لتغيير عدد `ضربات`{: class = "block3variables"} بمقدار `1`{: class = "block3variables"} عند النقر على كائن **بنياتا**:

![The Piñata sprite icon.](images/pinata-sprite.png)

```blocks3
when this sprite clicked
start sound [Boing v]
+ change [hits v] by (1)
```

--- /task ---

--- task ---

**اختبار:** اختبر مشروعك عدة مرات. تأكد من أن عدد `ضربات`{: class = "block3variables"} يبدأ دائمًا عند `0`{: class = "block3variables"} ويزيد بمقدار `1`{: class = "block3variables"} في كل مرة تنقر فيها على **بنياتا**.

![The Stage showing the number stored in the hits variable is '8'.](images/hits-increase.png)

--- /task ---

من الصعب كسر بنياتا لكنها لا تبقى إلى الأبد. ستصمد بنياتا لمدة `10 ضربات`{: class = "block3variables"} قبل ان تنكسر.

يمكن استخدام كتلة `إذا`{: class = "block3control"} لاتخاذ قرار بناءً على شرط ****.

<p style="border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;">
نحن نستخدم <span style="color: #0faeb0">**الشروط**</span> طوال الوقت لاتخاذ القرارات. يمكننا أن نقول "إذا كان قلم الرَّصاص غير حاد، فقم بشحذه". `وبالمثل ، تتيح لنا شروط `إذا` كتابة رمز يقوم بشيء مختلف اعتمادًا على ما إذا كان الشرط صحيحًا أم خطأ.
</p>

--- task ---

افتح قائمة الكتل البرمجية `التحكم` {:class="block3looks"}. اسحب كتلة `إذا`{: class = "block3control"} في منطقة التعليمات البرمجية اسفل كتلة `عند نقر هذا الكائن`:

![The Piñata sprite icon.](images/pinata-sprite.png)

```blocks3
when this sprite clicked
+ if <> then
start sound [Boing v]
change [hits v] by (1)

```

--- /task ---

تحتوي الكتلة `إذا`{: class = "block3control"} على مدخلات على شكل سداسي حيث يمكنك بناء شرط.

--- task ---

يجب أن يقوم</strong>بنياتا**بتشغيل صوت وزيادة عدد</code>الضربات`{:class="block3variables"} <strong x-id="1"><code>if`{:class="block3control"}** the number of `الضربات`{:class="block3variables"} is `less than`{:class="block3operators"} `10`{:class="block3variables"}.

أولًا، أضف العملية `<`{:class="block3operators"} إلى الإدخال على الشكل السداسي:

![The Piñata sprite icon.](images/pinata-sprite.png)

```blocks3
when this sprite clicked
+ if <() < ()> then
start sound [Boing v]
change [hits v] by (1)

```

--- /task ---

--- task ---

قم بإنهاء بناء شرط `إذا`{: class = "block3control"} عن طريق سحب متغير`الضربات`{: class = "block3variables"} على يسار عامل التشغيل</code> `&lt;{: class = "</0>"} واكتب القيمة "10" على اليمين:</p>

<p spaces-before="0"><img src="images/pinata-sprite.png" alt="The Piñata sprite icon." /></p>

<pre><code class="blocks3">when this sprite clicked
+ if <(hits) < (10)> then
start sound [Boing v]
change [hits v] by (1)

`</pre>

--- /task ---

--- task ---

**اختبار:** قم بتشغيل مشروعك. قم بضرب البنياتا 10 مرات لسماع الصوت وتاكد بان عدد`الضربات` يزيد عند كل ضربة مقدار 1.

اضرب البنياتا عدة مرات. لن يتجاوز متغير `الضربات`{: class = "block3variables"} العدد 10 لأن هذا الشرط لم يعد "صحيحًا" لذا لن يتم تشغيل الكود داخل كتلة `إذا`{: class = "block3control"}.

--- /task ---

--- task ---

اضف كتلة `إذا`{:class="block3control"}مرة ثانية داخل الحلقة الاولى. هذه المرة سيتحقق الشرط مما إذا كانت عدد`الضربات` {: class = "block3variables"} `مساوياً`{: class = "block3operators"} 10 وإذا كان 'true' سيتغير الزي إلى `مكسور`{: class = "block3looks"}:

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

**اختبار:** اختبر مشروعك عدة مرات. Check that the **Piñata** sprite starts with the 'whole' costume then changes to the 'broken' costume after `10 hits`{:class="block3variables"}.

![An animated image showing the piñata being clicked ten times. After the tenth time, the costume changes to broken.](images/break-pinata.gif)

--- /task ---

When the **Piñata** sprite has broken, all the other sprites need to know that the party has started.

In Scratch, the `broadcast`{:class="block3events"} block can be used to **send** a message that all sprites can **receive**.

--- task ---

أضف كتلة `بث الرسالة`{: class = "block3events"} من قائمة الاحداث `Events`{: class = "block3events"}:

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

انقر على `الرسالة1`{:class="block3events"} واختر 'رسالة جديدة'. قم بتسمية الرسالة الجديدة `حفلة`{:class="block3events"}.

![The drop-down menu on the broadcast block showing the 'New message' menu option.](images/new-message.png)

![The New message pop-up window with 'New message name' box highlighted and the typed word 'party'.](images/party-message.png)

ستبدو كتلة البث `{`class = "block3events"} على النحو التالي:

```blocks3
broadcast (party v)
```

--- /task ---

--- save ---
