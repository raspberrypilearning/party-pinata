## استخدم عصا

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
عادة ما يتم ضرب Piñatas بعصا مصنوعة من الخشب أو ورق مقوى مغطاة بشرائط ملونة من الورق. في هذه الخطوة ، ستضيف شفرة برمجية 
للتحكم في عصا piñata وتشغيل الموسيقى عندما تنكسر البنياتا. 
</div>
<div>
! [صورة متحركة gif تُظهر كائن العصا يتتبع مؤشر الماوس حول المسرح.] (images / follow-stick.gif) {: width = "300px"}
</div>
</div>

--- task ---

انقر فوق ايقونة **عصا** في قائمة الكائنات. أضف شفرة برمجية بحيث تظل العصا دائمًا أمام الكائنات المتحركة الأخرى وتتبع مؤشر الماوس (أو إصبعك على الكمبيوتر اللوحي).

استخدم كتلة `اذهب إلى موضع العشوائي`{: class = "block3motion"} ، ولكن حدد `مؤشر الماوس`{: class = "block3motion"} من القائمة المنسدلة:

![The Stick sprite icon](images/stick-sprite.png)

```blocks3
when flag clicked
forever
go to [front v] layer
go to (mouse-pointer v) // Change to mouse-pointer
```

--- /task ---

--- task ---

**اختبار:** قم بتشغيل مشروعك وتحقق من أن **العصا** تتبع المؤشر أو إصبعك حول المسرح.

![An animated image showing the Stick sprite following the mouse-pointer around the Stage.](images/follow-stick.gif)

--- /task ---

There are many different types of sounds in Scratch from voice and animal noises to over 100 other sound effects.

Scratch also has **looping sounds** that can be used in `forever`{:class="block3control"} or `repeat`{:class="block3control"} loops to sound like they are playing continuously.

--- task ---

Go to the **Sounds** tab and click on the **Choose a sound** icon.

![The Choose a sound icon with the sounds pop-up menu. When selected, the choose a sound icon is a white speaker on a green circle.](images/sound-icon.png)

--- /task ---

--- task ---

From the **Choose a sound** gallery, select the **Loops** category.

![The Sound gallery with 'Loops' category highlighted in orange to show it has been selected. The other categories are in blue.](images/loops-category.png)

--- /task ---

--- task ---

**Choose:** Hover over the **play** icons to hear the looping sounds. Add your favourite by clicking on it.

![The 'Hip hop' sound with play icon highlighted in the top-right corner of the sound icon.](images/play-icon.png)

The sound will then appear in your Sounds list:

![The 'Hip hop' sound in the Sound list on the Sounds tab.](images/added-sound.png)

--- /task ---

--- task ---

Click on the **Code** tab and create a new script to loop the sound `forever`{:class="block3control"} when the `party`{:class="block3events"} message has been received:

![The Stick sprite icon.](images/stick-sprite.png)

```blocks3
when I receive [party v]
forever
play sound [Hip Hop v] until done // Choose your sound
```

--- /task ---

--- task ---

**Test:** Run your project, and click on the piñata ten times to hear the looping party music.

--- /task ---

--- save ---
