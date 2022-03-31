## Gebruik een stok

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Piñata's worden meestal geraakt met een stok van hout of dik karton die is bedekt met kleurrijke stroken papier. In deze stap voeg je code toe om de stok te besturen en herhaalmuziek af te spelen wanneer de piñata breekt. 
</div>
<div>
![Een geanimeerde afbeelding die de Stok-sprite toont die de muisaanwijzer rond het werkgebied volgt.](images/follow-stick.gif){:width="300px"}
</div>
</div>

--- task ---

Klik op de **Stok** sprite in de Sprite-lijst. Voeg code toe zodat de stok altijd voor de andere sprites blijft en de muisaanwijzer (of je vinger op een tablet) volgt.

Gebruik het `ga naar willekurige positie`{:class="block3motion"} blok, maar selecteer `muisaanwijzer`{:class="block3motion"} in het vervolgkeuzemenu:

![Het pictogram van de Stok-sprite](images/stick-sprite.png)

```blocks3
wanneer op de groene vlag wordt geklikt
herhaal
ga naar laag [voorgrond v]
ga naar (muisaanwijzer v) // Verander naar muisaanwijzer
```

--- /task ---

--- task ---

**Test:** Voer je project uit en controleer of de sprite **Stok** je cursor of vinger over het speelveld volgt.

![Een geanimeerde afbeelding waarin de Stok-sprite de muisaanwijzer in het speelveld volgt.](images/follow-stick.gif)

--- /task ---

Er zijn veel verschillende soorten geluiden in Scratch, van stem- en dierengeluiden tot meer dan 100 andere geluidseffecten.

Scratch heeft ook **herhaalgeluiden** die kunnen worden gebruikt in een `herhaal`{:class="block3control"} of `herhaal tot`{:class="block3control"} lusen zodat het klinkt alsof ze continu worden afgespeeld.

--- task ---

Ga naar het **Geluiden** tabblad en klik op het **Kies een geluid** pictogram.

![Het pictogram Kies een geluid met het pop-upmenu Geluiden. Indien geselecteerd, is het pictogram 'Kies een geluid' een witte luidspreker op een groene cirkel.](images/sound-icon.png)

--- /task ---

--- task ---

Vanuit de **Kies een geluid** bibliotheek kies je de **Lussen** categorie.

![De Geluidsbibliotheek met de categorie 'Lussen' oranje gemarkeerd om aan te geven dat deze is geselecteerd. De andere categorieën zijn in het blauw.](images/loops-category.png)

--- /task ---

--- task ---

**Kies:** Beweeg over de **speel** iconen om de herhaalgeluiden te horen. Voeg je favoriet toe door erop te klikken.

![Het 'Hiphop' geluid met het afspeelpictogram gemarkeerd in de rechterbovenhoek van het geluidspictogram.](images/play-icon.png)

Het geluid verschijnt dan in je lijst Geluiden:

![Het 'Hiphop' geluid in de Geluidenlijst op het tabblad Geluiden.](images/added-sound.png)

--- /task ---

--- task ---

Klik op het tabblad **Code** en maak een nieuw script om het geluid `continu`{:class="block3control"} te herhalen wanneer het bericht `feest`{:class="block3events"} is ontvangen:

![Het pictogram van de Stok-sprite.](images/stick-sprite.png)

```blocks3
wanneer ik signaal [feest v] ontvang
herhaal
start geluid [Hip Hop v] en wacht // Kies je geluid
```

--- /task ---

--- task ---

**Test:** Voer je project uit en klik tien keer op de piñata om de feestmuziek te horen.

--- /task ---

--- save ---
