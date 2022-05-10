## Golpea la piñata

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
En este paso, programarás la piñata para reproducir un sonido y contarás un golpe cada vez que se haga clic en la piñata.
</div>
<div>
![Una imagen animada que muestra cómo se hace clic diez veces en la piñata. Después de la décima vez, el disfraz cambia a rota y la variable desaparece.](images/break-pinata.gif){:width="300px"}
</div>
</div>

--- task ---

Haz clic en la pestaña **Sonidos** para el objeto**Piñata** y encontrarás un sonido llamado **Boing**. Haz clic a en el botón **Reproducir** para escuchar el sonido.

![La pestaña Sonidos que muestra el sonido Boing en la lista de Sonidos con el icono Reproducir (un triángulo blanco en un círculo azul) resaltado en la parte inferior.](images/play-boing.png)

--- /task ---

Un grupo de bloques conectados en Scratch se llama **script**. Los sprites pueden tener más de un script.

--- task ---

Haz clic en la pestaña **Código**. Arrastra un bloque `al hacer clic en este objeto`{:class="block3events"} desde `Eventos`{:class="block3events"}, al área Código para iniciar un nuevo script.

En el menú de bloques `Sonido`{:class="block3sound"}, busca el bloque `iniciar sonido`{:class="block3sound"}. Arrástralo debajo del bloque `al hacer clic en este objeto`{:class="block3events"}:

![El icono del objeto Piñata.](images/pinata-sprite.png)

```blocks3
when this sprite clicked
start sound [Boing v]
```

--- /task ---

--- task ---

**Prueba:** Ejecuta tu proyecto haciendo clic en la **bandera verde** sobre el escenario. Haz clic en la piñata mientras se balancea para escuchar el sonido boing.

--- /task ---

Una `variable`{:class="block3variables"} es una forma de almacenar números y/o texto. La cantidad de veces que se hace clic en la piñata se almacenará en una variable llamada `golpes`{:class="block3variables"} para que pueda usarse en cualquier momento.

--- task ---

En el menú de bloques `Variables`{:class="block3variables"}, haz clic en el botón **Crear una variable**.

![El menú de bloques de variables con el botón 'Crear una variable'.](images/make-variable.png)

Llama **golpes** a tu nueva variable:

![La ventana emergente 'Nueva variable' con el nombre 'golpes' escrito en el cuadro 'Nuevo nombre de variable'.](images/new-variable.png)

**Aviso:** La nueva variable 'golpes' aparece en el escenario y ahora se puede usar en los bloques `Variable`{:class="block3variables"}.

![La variable golpes en el escenario.](images/variable-stage.png)

![Los bloques de variables, incluido el nuevo bloque 'golpes'.](images/variable-blocks.png)

--- /task ---

--- task ---

Cada vez que se inicia el proyecto, el número de `golpes`{:class="block3variables"} debe restablecerse a `0`{:class="block3variables"}.

Drag the `set hits to 0`{:class="block3variables"} block into the first script in the Code area, between the `switch costume to`{:class="block3looks"} block and the `go to x: (0) y: (180)`{:class="block3motion"} block.

Your code should look like this:

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

Every time the **Piñata** sprite is clicked, the number of `hits`{:class="block3variables"} should increase.

Add a block to change `hits`{:class="block3variables"} by `1`{:class="block3variables"} when the **Piñata** sprite is clicked:

![The Piñata sprite icon.](images/pinata-sprite.png)

```blocks3
when this sprite clicked
start sound [Boing v]
+ change [hits v] by (1)
```

--- /task ---

--- task ---

**Test:** Run your project a couple of times. Check that `hits`{:class="block3variables"} always starts at `0`{:class="block3variables"} and increases by `1`{:class="block3variables"} each time you click on the **Piñata** sprite.

![The Stage showing the number stored in the hits variable is '8'.](images/hits-increase.png)

--- /task ---

A piñata is hard to break but it does not last forever. Your piñata will last for `10 hits`{:class="block3variables"} before breaking open.

An `if`{:class="block3control"} block can be used to make a decision based on a **condition**.

<p style="border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;">
We use <span style="color: #0faeb0">**conditions**</span> all the time to make decisions. We could say “if the pencil is blunt, then sharpen it”. `If` blocks and conditions let us write code that does something different depending on whether a condition is true or false.
</p>

--- task ---

Go to the `Control`{:class="block3control"} blocks menu. Drag an `if`{:class="block3control"} block into the Code area and insert it around the blocks in your `when this sprite clicked`{:class="block3events"} script:

![The Piñata sprite icon.](images/pinata-sprite.png)

```blocks3
when this sprite clicked
+ if <> then
start sound [Boing v]
change [hits v] by (1)

```

--- /task ---

The `if`{:class="block3control"} block has a hexagon-shaped input where you can build a condition.

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
