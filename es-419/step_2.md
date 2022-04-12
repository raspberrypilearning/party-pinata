## Empieza la fiesta

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
En este paso, elegirás un disfraz de piñata y programarás la piñata para balancearse.
</div>
<div>
![Un gif animado que muestra el escenario con el objeto piñata colocado en la parte superior central y balanceándose de izquierda a derecha.](images/swinging-pinata.gif){:width="300px"}
</div>
</div>

--- task ---

Abre el [proyecto inicial Piñata de fiesta](https://scratch.mit.edu/projects/653082997/editor){:target="_blank"}. Trinket se abrirá en otra pestaña del navegador.

[[[working-offline]]]

--- /task ---

El editor de Scratch se ve así:

![Una captura de pantalla anotada del editor de Scratch, con el escenario, el panel de escenario, el panel de objetos, la lista de objetos y el área de programación etiquetados.](images/scratch-interface.png)

El **escenario** es donde se ejecuta tu proyecto y un **fondo** cambia la forma en que se ve el escenario. Hemos agregado un fondo de fiesta de Code Club por ti.

En Scratch, los personajes y cosas se denominan **objetos**y aparecen en el escenario. Puedes ver los objetos**Piñata** y **Stick** en el escenario.

![El escenario con un fondo azul estampado con regalos y globos. También están en el escenario los objetos Piñata y Stick.](images/backdrop-and-sprites.png)

Por el momento no está pasando mucho en esta fiesta. ¡Puedes cambiarlo!

--- task ---

Un objeto puede tener código, disfraces y sonidos para cambiar su aspecto y lo que hace.

Haz clic en el objeto **Piñata** en la lista de ovjetos y selecciona la pestaña **Disfraces**. Hay dos disfraces piñata, uno se llama 'whole' (entera) y el otro se llama 'broken' (rota).

![Imagen lado a lado de los dos disfraces de la piñata. El de la izquierda es la piñata entera, en el de la derecha está rota y abierta.](images/pinata-costumes.png)

![La pestaña de Disfraces (la pestaña del medio arriba a la izqierda).](images/costumes-tab.png)

--- /task ---

--- task ---

Haz clic en la pestaña **Código**. Ve al menú de bloques `Apariencia`{:class="block3looks"} y arrastra un disfraz de `cambiar disfraz a:`{:class="block3looks"} al área de código.

Haz clic en el nombre del disfraz para abrir un **menú desplegable** y luego selecciona el disfraz `whole (entera)`{:class="block3looks"}:

![El icono del objeto Piñata.](images/pinata-sprite.png)

```blocks3
cambia el disfraz a (v whole) // Actualiza a 'whole (entera)'
```

![Una imagen animada que muestra el bloque cambiar disfraz a: quee se arrastra desde el menú de bloques Apariencia al área de código.](images/switch-costume.gif)

--- /task ---

Los bloques se pueden conectar entre sí en el área de código para ejecutar más de uno a la vez. Los bloques conectados se ejecutarán en orden de arriba a abajo.

--- task ---

Arrastra un bloque `Al presionar bandera`{:class="block3events"} desde el menú de bloques `Eventos`{:class="block3events"} y conéctalo a la parte superior de tu bloque Apariencia en el área de codigo. Los bloques se unirán:

![El icono del objeto Piñata.](images/pinata-sprite.png)

```blocks3
+ when flag clicked
switch costume to (whole v)
```
![El bloque Al presionar la bandera, se agrega al área de código y se conecta al bloque de cambiar disfraz.](images/add-flag-clicked.gif)

--- /task ---

La posición inicial de una piñata es siempre la misma, solo comienza a moverse cuando el juego de la piñata comienza.

--- task ---

In the `Motion`{:class="block3motion"} blocks menu, find the `go to x: 0 y: 180`{:class="block3motion"} and `point in direction 90`{:class="block3motion"} blocks. Drag the blocks to the Code area and connect them to the bottom of your code:

![The Piñata sprite icon.](images/pinata-sprite.png)

```blocks3
when flag clicked
switch costume to (whole v)
+ go to x: (0) y: (180)
+ point in direction (90) // Ready position
```

--- /task ---

A `forever`{:class="block3control"} loop runs the code blocks inside it again and again. It is the perfect loop for a swinging piñata that is hard to hit.

--- task ---

Drag a `forever`{:class="block3control"} block from the `Control`{:class="block3control"} blocks menu and connect it to the bottom of your code:

![The Piñata sprite icon.](images/pinata-sprite.png)

```blocks3
when flag clicked
switch costume to (whole v)
go to x: (0) y: (180)
point in direction (90)
+ forever
```

--- /task ---

A `repeat`{:class="block3control"} loop can be used to make the **Piñata** sprite repeat a small movement many times. This will make the piñata appear animated.

--- task ---

Drag a `repeat 10`{:class="block3control"} block into the Code area and attach it inside your `forever`{:class="block3control"} loop.

Go to the `Motion`{:class="block3motion"} blocks menu and drag a `turn clockwise 15 degrees`{:class="block3motion"} block into the `repeat`{:class="block3control"} block.

Change the `15`{:class="block3motion"} degrees to `1`{:class="block3motion"} degree so that the piñata only swings a small amount each time:

![The Piñata sprite icon.](images/pinata-sprite.png)

```blocks3
when flag clicked
switch costume to (whole v)
go to x: (0) y: (180)
point in direction (90)
forever
+ repeat (10) 
turn right (1) degrees // Change to 1
```
![Repeat block being added within the forever block and then a turn clockwise block added within it.](images/add-repeat.gif)

--- /task ---

--- task ---

**Test:** Run your project, by clicking on the **green flag** above the Stage, to see the piñata swing.

**Mmm, something is not quite right!** When an object is hung from the ceiling, it won't just rotate in one direction, it will swing back and forth.

Stop your project by clicking on the **red stop icon** above the Stage.

![Green flag and stop icons shown side by side.](images/start-stop.png)

--- /task ---

--- task ---

Add code to your `forever`{:class="block3control"} loop so that the piñata swings from the centre back and forth continuously like a pendulum:

![The Piñata sprite with arrows underneath showing that it swings clockwise from centre, then anticlockwise through the centre, then clockwise back to the centre.](images/pinata-swing.png)

![The Piñata sprite icon.](images/pinata-sprite.png)

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

**Test:** Run your project to see the piñata swing.

**Debug:** If the piñata does not swing correctly:
+ Look at your code to make sure the `repeat`{:class="block3control"} blocks are in the correct position
+ Check that the `turn clockwise`{:class="block3motion"}  and `turn anticlockwise`{:class="block3motion"} arrows are correct
+ Make sure that you have used the numbers from the code above

![An animated gif showing the Stage with the Piñata sprite positioned at the top centre and swinging back and forth.](images/swinging-pinata.gif)

--- /task ---

--- save ---

