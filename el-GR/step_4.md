## Χρησιμοποίησε ένα ραβδί

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Η πινιάτα συνήθως χτυπιέται με ένα ραβδί από ξύλο ή από χοντρή κάρτα που καλύπτεται με πολύχρωμες λωρίδες χαρτιού. Σε αυτό το βήμα, θα προσθέσεις κώδικα για να ελέγχεις το ραβδί πινιάτα και για την αναπαραγωγή μουσικής σε βρόχο όταν σπάσει η πινιάτα. 
</div>
<div>
![Μια κινούμενη εικόνα που δείχνει το αντικείμενο Stick να ακολουθεί τον δείκτη του ποντικιού γύρω από τη Σκηνή.](images/follow-stick.gif){:width="300px"}
</div>
</div>

--- task ---

Κάνε κλικ στο αντικείμενο **Stick** στη λίστα αντικειμένων. Πρόσθεσε κώδικα έτσι ώστε το ραβδί να μένει πάντα μπροστά από τα άλλα αντικείμενα και να ακολουθεί τον δείκτη του ποντικιού (ή το δάχτυλό σου σε ένα tablet).

Χρησιμοποίησε το μπλοκ `πήγαινε σε τυχαία θέση`{:class="block3motion"}, αλλά επίλεξε `δείκτη ποντικιού`{:class="block3motion"} από το αναπτυσσόμενο μενού:

![The Stick sprite icon](images/stick-sprite.png)

```blocks3
when flag clicked
forever
go to [front v] layer
go to (mouse-pointer v) // Change to mouse-pointer
```

--- /task ---

--- task ---

**Test:** Run your project and check the **Stick** sprite follows your cursor or finger around the Stage.

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
