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

انقر على تبويب **المقاطع البرمجية**. من قائمة `الأحداث`{: class = "block3events"} ، اسحب كتلة `عند نقر هذا الكائن`{: class = "block3events"} الى منطقة كتابة التعليمات البرمجية.

في قائمة كتل `الصوت`{:class="block3sound"} جد كتلة `ابدأ الصوت`{:class="block3sound"}. أضِف المقطع البرمجي `عند نقر هذا الكائن`{:class="block3events"}:

![كائن البنياتا.](images/pinata-sprite.png)

```blocks3
when this sprite clicked
start sound [Boing v]
```

--- /task ---

--- task ---

**اختبار:** قم بتشغيل المشروع، بالضغط على **العلم الاخضر**، حتى تتاكد بان البنياتا تتأرجح. انقر على piñata وهو يتأرجح لسماع صوت boing.

--- /task ---

`المتغير`{:class="block3variables"} هو وسيلة لتخزين الأرقام و/أو النصوص. سيتم تخزين عدد مرات النقر على بنياتا في متغير يسمى `الضربات`{: class = "block3variables"} بحيث يمكن استخدامه في أي وقت.

--- task ---

انقر على `متغيرات`{: class = "block3variables"} و ثم انقر على زر**انشاء متغير**.

![مجموعة كتل المتغيرات مع زر"انشاء متغير".](images/make-variable.png)

سمي المتغير الجديد الذي انشاته **الضربات**:

![النافذة المنبثقة "متغير جديد" مع كتابة الاسم "الضربات" في مربع "اسم متغير جديد".](images/new-variable.png)

**ملاحظة:** يظهر متغير "الضربات" الجديد على المنصة ويمكن استخدامه الآن في قائمة `المتغيرات`{: class = "block3variables"}.

![متغير الضربات على المسرح.](images/variable-stage.png)

![قائمة المتغيرات تتضمن الكتلة الجديدة "الضربات".](images/variable-blocks.png)

--- /task ---

--- task ---

في كل مرة يبدأ فيها المشروع ، يجب إعادة تعيين عدد `الضربات`{: class = "block3variables"} إلى `0`{: class = "block3variables"}.

اسحب كتلة`اجعل متغير"ضربات" مساوياً 0`{:class="block3variables"} الى النص البرمجي الاول، بين كتلة `غير المظهر الى`{:class="block3looks"} وكتلة `اذهب الى س: (0) ص: (180)`.

يجب أن تبدو التعليمات البرمجية خاصتك بالشكل التالي:

![كائن البينياتا.](images/pinata-sprite.png)

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

![كائن البينياتا.](images/pinata-sprite.png)

```blocks3
when this sprite clicked
start sound [Boing v]
+ change [hits v] by (1)
```

--- /task ---

--- task ---

**اختبار:** اختبر مشروعك عدة مرات. تأكد من أن عدد `ضربات`{: class = "block3variables"} يبدأ دائمًا عند `0`{: class = "block3variables"} ويزيد بمقدار `1`{: class = "block3variables"} في كل مرة تنقر فيها على **بنياتا**.

![المسرح يظهر العدد المخزون من عدد الضربات هو 8.](images/hits-increase.png)

--- /task ---

من الصعب كسر بنياتا لكنها لا تبقى إلى الأبد. ستصمد بنياتا لمدة `10 ضربات`{: class = "block3variables"} قبل ان تنكسر.

يمكن استخدام كتلة `إذا`{: class = "block3control"} لاتخاذ قرار بناءً على شرط ****.

<p style="border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;">
نحن نستخدم <span style="color: #0faeb0">**الشروط**</span> طوال الوقت لاتخاذ القرارات. يمكننا أن نقول "إذا كان قلم الرَّصاص غير حاد، فقم بشحذه". `وبالمثل ، تتيح لنا شروط `إذا` كتابة رمز يقوم بشيء مختلف اعتمادًا على ما إذا كان الشرط صحيحًا أم خطأ.
</p>

--- task ---

افتح قائمة الكتل البرمجية `التحكم` {:class="block3looks"}. اسحب كتلة `إذا`{: class = "block3control"} في منطقة التعليمات البرمجية اسفل كتلة `عند نقر هذا الكائن`:

![كائن البينياتا.](images/pinata-sprite.png)

```blocks3
when this sprite clicked
+ if <> then
start sound [Boing v]
change [hits v] by (1)

```

--- /task ---

تحتوي الكتلة `إذا`{: class = "block3control"} على مدخلات على شكل سداسي حيث يمكنك بناء شرط.

--- task ---

يجب أن يقوم كائن ** Piñata ** بتشغيل صوت وزيادة عدد `الضربات` {:class="block3variables"} **`اذا`{:class="block3control"}** كان عدد `الضربات`{:class="block3variables"} `اصغر من `{:class="block3operators"} `10`{:class="block3variables"}.

أولًا، أضف العملية `<`{:class="block3operators"} إلى الإدخال على الشكل السداسي:

![كائن البينياتا.](images/pinata-sprite.png)

```blocks3
when this sprite clicked
+ if <() < ()> then
start sound [Boing v]
change [hits v] by (1)

```

--- /task ---

--- task ---

قم بإنهاء بناء شرط `إذا`{: class = "block3control"} عن طريق سحب متغير`الضربات`{: class = "block3variables"} على يسار العملية `<`{:class="block3operators"} واكتب القيمة "10" على اليمين:

![كائن البنياتا.](images/pinata-sprite.png)

```blocks3
when this sprite clicked
+ if <(hits) < (10)> then
start sound [Boing v]
change [hits v] by (1)

```

--- /task ---

--- task ---

**اختبار:** قم بتشغيل مشروعك. قم بضرب البنياتا 10 مرات لسماع الصوت وتاكد بان عدد`الضربات` يزيد عند كل ضربة مقدار 1.

اضرب البنياتا عدة مرات. لن يتجاوز متغير `الضربات`{: class = "block3variables"} العدد 10 لأن هذا الشرط لم يعد "صحيحًا" لذا لن يتم تشغيل الكود داخل كتلة `إذا`{: class = "block3control"}.

--- /task ---

--- task ---

اضف كتلة `إذا`{:class="block3control"}مرة ثانية داخل الحلقة الاولى. هذه المرة سيتحقق الشرط مما إذا كانت عدد`الضربات` {: class = "block3variables"} `مساوياً`{: class = "block3operators"} 10 وإذا كان 'true' سيتغير الزي إلى `مكسور`{: class = "block3looks"}:

![كائن البينياتا.](images/pinata-sprite.png)

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

**اختبار:** اختبر مشروعك عدة مرات. تاكد من أن **البنياتا** تظهر بالمظهر الكامل عند بدء اللعبة، ثم تتغير الى المظهر المكسور بعد `10ضربات`{:class="block3variables"}.

![صورة متحركة gif تظهر بان تم النقر 10 مرات على كائن البينياتا. بعد المرة العاشرة ، يتغير مظهر البنياتا إلى مكسور.](images/break-pinata.gif)

--- /task ---

عندما ينكسر كائن **Piñata** ، تحتاج جميع الكائنات الأخرى إلى معرفة أن الحفلة قد بدأت.

في Scratch ، يمكن استخدام كتلة `البث`{: class = "block3events"} **لإرسال** رسالة بحيث يمكن لجميع الكائنات ** استلامها**.

--- task ---

أضف كتلة `بث`{: class = "block3events"} من قائمة `الاحداث`{: class = "block3events"}:

![كائن البينياتا.](images/pinata-sprite.png)

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

![تعرض القائمة المنسدلة في كتلة البث خيار "رسالة جديدة".](images/new-message.png)

![النافذة المنبثقة للرسالة الجديدة مع تمييز مربع "اسم الرسالة الجديدة" والكلمة المكتوبة "حفلة".](images/party-message.png)

ستبدو كتلة البث `{`class = "block3events"} على النحو التالي:

```blocks3
broadcast (party v)
```

--- /task ---

--- save ---
