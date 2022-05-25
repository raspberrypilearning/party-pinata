## Agrega algunas golosinas

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Las piñatas están llenas de golosinas y cuando empiezan a romperse, las golosinas se caen. En este paso, animarás las golosinas internacionales para que caigan de la piñata cada vez que se golpee. ¿Reconoces alguna de las golosinas?
</div>
<div>
![Una imagen animada que muestra cómo golpean a la piñata varias veces. Con cada golpe, cuatro golosinas aleatorias caen en posiciones aleatorias y luego giran lentamente en un círculo.](images/spinning-treats.gif){:width="300px"}
</div>
</div>

<p style="border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;">
Un <span style="color: #0faeb0">**disfraz**</span> en Scratch es una imagen que cambia la apariencia de un objeto. Nuestros **diseñadores gráficos** les pidieron a los líderes de Code Club de todo el mundo que les dijeran qué golosinas tendrían en una fiesta. Con suerte, algunos de los disfraces que crearon te resultarán familiares y otros serán completamente nuevos.      
</p>

--- task ---

Haz clic en el objeto **Golosinas** en la lista de objetos y selecciona la pestaña **Disfraces**.

Hay 26 disfraces de golosinas, ¡y los vas a usar todos!

![Las imágenes de golosinas especialmente creadas que se muestran como una colección de golosinas.](images/treats.png)

--- /task ---

--- task ---

Haz clic en la pestaña **Código** y luego crea un script para `esconder`{:class="block3looks"} las golosinas en la piñata cuando comience tu proyecto:

![El ícono del objeto Golosinas.](images/treats-sprite.png)

```blocks3
when flag clicked
hide
go to x: (0) y: (100)
```

--- /task ---

Cuatro golosinas escaparán de la piñata cada vez que la golpeen. Al **clonar** el objeto **Golosinas**, puedes crear múltiples golosinas.

<p style="border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;">
Un <span style="color: #0faeb0">**clon**</span> en Scratch es una copia de un objeto. Tiene el mismo código, disfraces y sonidos del objeto original.      
</p>

--- task ---

Haz clic en el objeto **Piñata**.

Agrega un bucle `repetir`{:class="block3control"} en tu código existente. Cambia el valor a `4`{:class="block3control"} y luego agrega un bloque `crear clon de mí mismo`{:class="block3control"}. Usa la flecha desplegable para seleccionar el objeto `Golosinas`{:class="block3control"}:

![El ícono del objeto Piñata.](images/pinata-sprite.png)

```blocks3
when this sprite clicked
if <(golpes) < (10)> then
start sound [Boing v]
change [golpes v] by (1)
+ repeat (4) // Cambiar a 4
create clone of (Golosinas v) // Seleccionar golosinas
end
if <(golpes)=(10)> then
switch costume to (rota v)
broadcast (fiesta v)
```

**Sugerencia:** Usa el espacio libre en el área Código para crear tu nuevo código y luego arrástralo al script existente:

![Los bloques de repetición y clonación se ensamblan solos en el área de Código antes de arrastrarlos a su posición en el script.](images/code-area.gif)
--- /task ---

--- task ---

Haz clic en el objeto **Golosinas**.

Crea un nuevo script usando un bloque `al comenzar como clon`{:class="block3control"}.

Agrega bloques desde el menú de bloques `Apariencia`{:class="block3looks"} para controlar la apariencia de cada nuevo clon:

![El ícono del objeto Golosinas.](images/treats-sprite.png)

```blocks3
when I start as a clone
show
go to [back v] layer // Cambiar a atrás
switch costume to (Knafeh v)
```

--- /task ---

--- task ---

Puedes elegir golosinas al azar para que caigan al golpear la piñata. Usa un operador `elegir número al azar`{:class="block3operators"} para seleccionar un disfraz aleatorio de `1`{:class="block3operators"} a `26`{:class="block3operators"} cada vez que se crea un clon:

![El ícono del objeto Golosinas.](images/treats-sprite.png)

```blocks3
when I start as a clone
show
go to [back v] layer 
+ switch costume to (pick random (1) to (26)) // Cambiar a 26
```

--- /task ---

--- task ---

Por el momento, los clones **Golosinas** aparecerán detrás del sprite **Piñata**, pero las golosinas deberían caer de la piñata en una posición aleatoria.

Agrega código para hacer que los objetos clonados **Golosinas** `vayan a`{:class="block3motion"} una posición aleatoria:

![El ícono del objeto Golosinas.](images/treats-sprite.png)

```blocks3
when I start as a clone
show
go to [back v] layer
switch costume to (pick random (1) to (26))
+ glide (1) secs to (random position v) 
```

--- /task ---

--- task ---

**Prueba:** Ejecuta tu proyecto y golpea la piñata para ver cuatro clones del objeto **Golosinas** después de cada golpe. Los disfraces se seleccionarán al azar y las golosinas irán a una posición aleatoria.

![Una imagen animada que muestra cómo golpean a la piñata tres veces. Con cada golpe, cuatro golosinas aleatorias caen en posiciones aleatorias.](images/four-treats.gif)

--- /task ---

--- task ---

Agrega animación para hacer que los objetos clones **Golosinas** `giren`{:class="block3motion"} `por siempre`{:class="block3control"} cuando alcancen su posición aleatoria. Recuerda que las animaciones funcionan mejor cuando se usan pequeños movimientos, así que cambia el número de grados a `1`{:class="block3motion"}:

![El ícono del objeto Golosinas.](images/treats-sprite.png)

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

**Prueba:** Ejecuta tu proyecto y golpea la piñata para ver girar los clones del objeto **Golosinas**.

![Una imagen animada que muestra cómo golpean a la piñata varias veces. Cada vez, cuatro golosinas aleatorias caen en posiciones aleatorias y luego giran lentamente en un círculo.](images/spinning-treats.gif)

--- /task ---

--- save ---
