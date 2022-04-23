## قم بإنشاء رسالة

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
في هذه الخطوة، ستكتب رسالة وتحركها باستخدام تأثيرات الحركة واللون. 
</div>
<div>
![صورة متحركة توضح سقوط الرسالة ثم يتغير الحجم واللون عندما تصل إلى موضع سقوط الرسالة النهائي.](images/falling-message.gif){:width="300px"}
</div>
</div>

ماذا ستكتب في بطاقة عيد ميلاد لإرسالها إلى Code Club؟ من الممكن أن تكون:
+ الشيء المفضل لديك في Code Club
+ رسالة عن قائد Code Club الرائع الخاص بك
+ تفاصيل عن ما تريد القيام به لاحقا مع مهارات البرمجة الخاصة بك

<p style="border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;">
تمت كتابة اول مشاريع Code Club باللغة الإنجليزية، ولكن في غضون عام تمت ترجمتها إلى البرتغالية البرازيلية والهولندية والألمانية والنرويجية والأوكرانية. سرعان ما تم اتباعها بترجمات للغة الفرنسية واليونانية والإسبانية، والآن تمت ترجمة بعض مشاريع Code Club إلى <span style="color: #0faeb0">** 28 لغة أصلية **</span>. شكرا لمجتمع الترجمة الرائع لدينا!

![صور متعددة تقول "عيد ميلاد سعيد" بلغات أصلية مختلفة.](images/birthday-languages.png)
</p>

--- task ---

انقر فوق الكائن **رسالة** في قائمة الكائنات وحدد علامة التبويب **مظاهر**.

يحتوي الزي على نص يقول "عيد سعيد Code Club". انقر نقرًا مزدوجًا (أو اضغط باستمرار على جهاز لوحي) على النص لتحديد أداة تحرير النص.

![محرر المظاهر مع تحديد أداة النص وتمييز النص.](images/text-edit.png)

--- /task ---

--- task ---

يمكنك الآن كتابة رسالة عيد ميلاد Code Club الجديدة الخاصة بك. اضغط على **Enter** في لوحة المفاتيح الخاصة بك لبدء سطر جديد.

**نصيحة:** لا تقلق إذا كانت رسالتك كبيرة جدًا بالنسبة للمربع يمكنك تغيير حجمها لاحقًا.

![محرر النص يظهر رسالة جديدة بدلاً من الرسالة القديمة.](images/new-text.png)

--- /task ---

--- task ---

**اختر:** انقر على أيقونة **ملء** لفتح القائمة المنسدلة للألوان. حرك شريط التمرير للملء يسارا ويمينا لتحديد اللون المفضل لديك.

![القائمة المنسدلة للملء مع منزلقات للون والتشبع والسطوع. تم تغيير الرسالة من الأخضر إلى الأرجواني.](images/font-colour.png)

--- /task ---

--- task ---

**اختر:** انقر فوق أداة **الخط** وستظهر قائمة منسدلة بالخطوط. يتم تحديد نوع الخط "Pixel" في مشروع البداية، ولكن يمكنك استخدام أي من الخطوط المتاحة.

![The Font drop-down menu showing a choice of nine different fonts. The 'Marker' font has been selected.](images/font-type.png)

--- /task ---

--- task ---

Click on the **Select** tool and eight circles will appear around your message. Use these circles to resize your message by clicking on them and dragging them within the white box.

![The Select tool is highlighted and the message has small circles in each corner and at the central vertical and horizontal borer points so that it can be resized in multiple directions.](images/resize-message.png)

--- /task ---

Your message is ready, now you can add code to hide your message inside the piñata and make your message fall from the piñata after the tenth hit.

--- task ---

Click on the **Code** tab then create a script to `hide`{:class="block3looks"} the message in the piñata when your project starts:

![كائن الرسالة.](images/message-sprite.png)

```blocks3
when flag clicked
hide
set size to (10) % // Change to 10 to start small
go to x: (0) y: (100) // Inside the piñata
```

--- /task ---

--- task ---

Create a new script to start when the `party`{:class="block3events"} message has been received.

Add a `repeat`{:class="block3control"} loop to animate the message. The message will `change size`{:class="block3looks"} to grow and `change y`{:class="block3motion"} position to fall as it animates:

![كائن الرسالة.](images/message-sprite.png)

```blocks3
when I receive [party v]
show
repeat (20) // Change to 20
change size by (5) // Change to 5
change y by (-10) // Change to -10
```

--- /task ---

--- task ---

**Test:** Run your project. Hit the piñata ten times to see the message fall.

![An animated image showing the pinata being hit ten times. Treats appear after each hit and on the tenth hit the pinata breaks and the message falls to the bottom of the screen. تكبر كلما سقطت.](images/falling-message.gif)

--- /task ---

--- save ---
