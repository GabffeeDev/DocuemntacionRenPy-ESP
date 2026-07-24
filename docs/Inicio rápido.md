# Inicio Rápido

## A quienes se atreven a crear

Desarrollar una novela visual es un acto de **valentía.**

Es decidir convertir una idea invisible en una experiencia que otras personas podrán sentir. Es enfrentarse a una página en blanco sin tener la certeza de que algún día habrá una versión terminada. Es aprender programación, escritura, narrativa, diseño, música, arte y muchas otras habilidades, no porque alguien lo exija, sino porque existe el deseo de contar una historia.

Habrá días en los que el progreso parezca insignificante. Días en los que un solo error ocupe horas de trabajo, o en los que una escena no consiga transmitir lo que imaginabas. Es parte del camino.

Cada línea de código escrita, cada diálogo revisado y cada problema resuelto son pasos hacia una obra que antes no existía. No importa si tu proyecto es pequeño o ambicioso; el simple hecho de intentarlo ya te coloca entre quienes decidieron crear en lugar de limitarse a observar.

Si esta documentación puede ayudarte a dar ese siguiente paso, entonces habrá cumplido su propósito.

***Sigue aprendiendo.***

***Sigue creando.***

Y, sobre todo, **no dejes que el miedo a no ser perfecto impida que tu historia llegue a existir.**

[Descarga Ren'py](https://www.renpy.org/latest.html)

## ¿Por dónde empezar?

Si es la primera vez que desarrollas una novela visual, es normal preguntarse por dónde comenzar. **Ren'Py** ofrece muchas herramientas, y puede resultar tentador empezar a programar de inmediato. Sin embargo, una buena novela visual comienza mucho antes de escribir la primera línea de código.

Antes de abrir Ren'Py, dedica tiempo a planificar tu proyecto. Define la historia que quieres contar, quiénes serán tus personajes, qué papel desempeñará cada uno y cuál será el mensaje o la experiencia que deseas transmitir al jugador. Una base sólida hará que el desarrollo sea mucho más sencillo y **evitará** tener que rehacer grandes partes del proyecto más adelante.

A lo largo de esta documentación no solo aprenderás a utilizar Ren'Py, sino también algunas buenas prácticas que pueden ayudarte a organizar tu trabajo. Hablaremos sobre cómo definir personajes de forma coherente, cómo estructurar y administrar **imágenes**, **fondos** y **sprites**, cómo organizar archivos de **audio**, **música** y **efectos de sonido**, y cómo mantener un proyecto limpio y fácil de ampliar.

El objetivo es que, desde el principio, adquieras hábitos que te permitan concentrarte en lo más importante: contar una buena historia. Una estructura bien organizada no solo facilita el desarrollo, sino que también hace que el mantenimiento del proyecto sea mucho más cómodo cuando este crezca.

No existe una única forma correcta de crear una novela visual. **Cada desarrollador encuentra su propio flujo de trabajo con la experiencia.** Las recomendaciones que encontrarás aquí están pensadas para ayudarte a evitar errores comunes y ofrecerte un punto de partida sólido para que puedas dedicar más tiempo a crear y menos tiempo a resolver problemas de organización.

Comencemos construyendo una buena base. El resto del proyecto será mucho más fácil cuando cada pieza tenga su lugar.

---

## Crear un proyecto en Ren'Py

Al abrir el _Launcher_ de Ren'Py podrás **cambiar el idioma a español**, crear un proyecto nuevo y elegir su nombre y resolución.

Lo más importante es que la resolución del proyecto coincida con la de las imágenes que utilizarás. De esta forma evitarás tener que escalarlas constantemente y conservarás una mejor calidad visual.

![Launcher de Ren'Py mostrando la creación de un proyecto](images/renpy-launcher.png)

## Configurar las preferencias

En **Preferencias** puedes elegir la carpeta donde se guardarán todos tus proyectos.

Te recomiendo mantener una estructura de carpetas ordenada desde el principio. Aunque al inicio parezca un detalle sin importancia, con el tiempo agradecerás saber exactamente dónde está cada proyecto.

Además, te recomiendo instalar **Visual Studio Code** y configurarlo como editor de texto del sistema. Así Ren'Py lo utilizará automáticamente para abrir los archivos `.rpy` y no tendrás que volver a configurarlo después de cada actualización.

[Visual Studio Code - Descargar](https://code.visualstudio.com/download?_exp_download=fb315fc982)

![Preferencias de Ren'Py con opciones de carpeta de proyectos y editor](images/renpy-preferencias.png)

## Conociendo la estructura del proyecto

Una vez creado el proyecto (en este ejemplo llamado **NuevoProyecto**), observarás que en la sección **Editar archivo** aparecen varios archivos con la extensión `.rpy`. Estos contienen el código de tu novela visual.

Por ahora no nos centraremos en ellos. Lo importante es la sección **Abrir carpeta**, donde encontrarás la estructura del proyecto y las carpetas en las que agregarás los recursos que utilizará tu juego.

![Estructura inicial del proyecto en el launcher de Ren'Py](images/estructura-proyecto.png)

## Organizando los recursos

Antes de comenzar a programar la historia, lo habitual es importar todos los recursos del proyecto. Desde el principio intenta mantener una estructura organizada.

También te recomiendo aprender a utilizar **Git** y **GitHub**. No les tengas miedo: son herramientas indispensables para cualquier desarrollador y te ayudarán a mantener un historial de cambios, realizar copias de seguridad y colaborar con otras personas.

En la carpeta `images`, por ejemplo, puedes separar los recursos de la siguiente manera:

- `backgrounds` para los fondos.
    
- `cgs` para las ilustraciones especiales.
    
- `sprites` para los personajes.
    

Dentro de `sprites`, lo ideal es crear una carpeta para cada personaje y guardar allí todas sus expresiones y poses.

Puede parecer una organización excesiva al principio, pero cuando el proyecto crezca te ahorrarás mucho tiempo buscando archivos. Un proyecto ordenado también transmite profesionalidad y facilita el mantenimiento.

![Carpeta images organizada por tipo de recurso](images/carpeta-images.png)

Con la carpeta `audio` ocurre lo mismo. Lo recomendable es separar la música de los efectos de sonido en carpetas independientes.

Por ejemplo:

- `music`
    
- `sfx`
    

Esta pequeña organización hará que encontrar un recurso específico sea mucho más rápido a medida que tu proyecto aumente de tamaño.

![Carpeta audio separada en music y sfx](images/carpeta-audio.png)

¡Una vez terminado de organizar tus recursos ya podemos empezar a programar!

---

A continuación abriremos el archivo **`script.rpy`**.

Por ahora **nos centraremos únicamente en este archivo**, ya que contiene todo lo necesario para comenzar a desarrollar una novela visual desde cero. Más adelante profundizaremos en cada una de las opciones y en las características más avanzadas de Ren'Py.

Al abrir **`script.rpy`**, encontrarás un contenido similar al siguiente:

![Archivo script.rpy abierto desde el launcher de Ren'Py](images/script-rpy.png)

**A partir de aquí aprenderás todo lo necesario para empezar a programar tu novela visual. Es sencillo, ¡no te desanimes!**

### Definir personajes

Como puedes observar en **`script.rpy`**, estamos utilizando la función **`Character()`**, la cual se asigna a la variable **`e`**, correspondiente a **Eileen**. Esta función recibe como parámetro una **cadena de texto** (`string`) con el valor **`"Eileen"`**, que será el nombre que aparecerá en la caja de diálogo del juego cada vez que el personaje hable.

![Ejemplo de definición de un personaje con Character](images/definir-character.png)


```renpy
define e = Character("Eileen")
```

Puedes ponerle **el nombre que quieras** a una variable, aunque lo recomendable es que sea corto o una abreviatura, ya que esa variable solo la utilizarás **tú** como programador o programadora.

Así que... **¡hazlo lo más cómodo posible!**

No te preocupes si todavía no entiendes qué es una variable o cómo funciona la programación. No es un concepto complicado y lo irás comprendiendo conforme avances en esta guía.

Aun así, **sí te recomendaría aprender un poquito de Python**. No es obligatorio para hacer una novela visual, pero créeme, te ayudará muchísimo cuando quieras hacer cosas más avanzadas.

Como dato curioso, la función **`Character()`** te ahorra muchísimo tiempo, ya que evita que tengas que escribir el nombre del personaje cada vez que habla.

Por ejemplo, usando `Character()` escribirías:

```renpy
define y = Character("Yuri")

label start:

    y "Hola."
    y "¿Cómo estás?"
    y "Espero que tengas un buen día."
```

Observa que únicamente escribimos **`y`**, y Ren'Py ya sabe que el nombre que debe mostrar en pantalla es **Yuri**.

Sin embargo, también es completamente válido escribir los diálogos sin definir un personaje:

```renpy
label start:

    "Yuri" "Hola."
    "Yuri" "¿Cómo estás?"
    "Yuri" "Espero que tengas un buen día."
```

Como puedes notar, el nombre **"Yuri"** debe escribirse en cada línea de diálogo. No es un problema cuando el personaje habla una o dos veces, pero si aparece durante toda la historia terminarás escribiendo su nombre cientos de veces.

Por eso, para los personajes principales siempre es recomendable utilizar **`Character()`**.

Si un personaje solo aparecerá una vez o tendrá muy pocas líneas de diálogo, no pasa absolutamente nada por escribir su nombre directamente.

Por ejemplo:

```renpy
label start:

    "Doctor" "Los resultados ya están listos."
```

En este caso crear un personaje con `Character()` sería innecesario.

En cambio, si ese doctor aparecerá varias veces a lo largo de la historia, entonces sí conviene definirlo:

```renpy
define d = Character("Doctor")
```

Y utilizarlo de esta forma:

```renpy
d "Los resultados ya están listos."
d "Necesitamos hacer más estudios."
d "Nos veremos la próxima semana."
```

Como regla general, piensa que **`Character()`** está para hacerte la vida más fácil. Cuanto más aparezca un personaje en tu juego, más sentido tendrá definirlo con esta función.

### Definiendo imágenes

Para que Ren'Py pueda mostrar una imagen, **primero debes definirla** mediante la sentencia `image`.

Su sintaxis es la siguiente:

```
image nombre_de_la_imagen = "ruta/del/archivo.png"
```

Pero... **voy a comentarte algo muy interesante sobre Ren'Py que muchos desarrolladores principiantes no conocen...**

**¡Ren'Py puede registrar automáticamente las imágenes y el audio que defines para que puedas utilizarlos sin escribir la ruta del archivo cada vez!**

Esto es una maravilla, porque una vez declarados tus recursos solo tendrás que referirte a ellos por su nombre, haciendo que tu código sea mucho más limpio y fácil de leer.

Por eso quiero darte **otra de mis recomendaciones**.

Además de ser organizado, **sé descriptivo** con el nombre de tus imágenes, audios y variables. Puede parecer un detalle sin importancia, pero créeme: **te hará la vida mucho más fácil conforme tu proyecto vaya creciendo.**

Y no te preocupes, no estás solo. Para eso estoy aquí. A lo largo de esta guía te enseñaré varias buenas prácticas para organizar tus recursos y evitar dolores de cabeza en el futuro.

A continuación veremos un concepto **importantísimo**.

> **Aquí está la diferencia entre simplemente programar en Ren'Py y programar de forma ordenada y profesional.**

#### Etiqueta y atributo

Las imágenes en Ren'Py se identifican mediante un **nombre de imagen**, el cual está compuesto por dos partes:

- **Etiqueta (Tag)**
    
- **Atributo (Attribute)**
    

La **etiqueta** identifica al personaje o recurso principal, mientras que los **atributos** describen su estado, expresión, ropa, ubicación o cualquier otra característica.

Por ejemplo **si quieres hacerlo manualmente**:

```renpy
image yuri casual happy = "images/sprites/yuri/casual_happy.png"
```

En este caso:

- **Etiqueta:** `yuri`
    
- **Atributos:** `casual` y `happy`
    

Otro ejemplo:

```renpy
image monika school angry = "images/sprites/monika/school_angry.png"
```

Aquí Ren'Py interpreta:

- **Etiqueta:** `monika`
    
- **Atributos:** `school` y `angry`
    

Fíjate que **los espacios son importantes**. Cada palabra forma parte del nombre de la imagen y Ren'Py las interpreta como una etiqueta seguida de uno o más atributos.

Esto permite que el motor entienda qué personaje estás mostrando y cuáles son sus características sin necesidad de utilizar nombres gigantes como:

```renpy
image monika_school_uniform_angry_expression = "images/sprites/monika/school_angry.png"
```

En su lugar, basta con escribir:

```renpy
image monika school angry = "images/sprites/monika/school_angry.png"
```

Otro ejemplo. **Si no quieres escribir la declaración manualmente**, puedes aprovechar el nombre del propio archivo.

Supongamos que tienes el siguiente sprite en **images** nombrado como:

```text
Yuri Happy.png
```


- `yuri` será la **etiqueta**.
    
- `happy` será el **atributo**.
    

Después podrás mostrarla utilizando la sentencia **`show`** seguida del nombre de la imagen.

```renpy
show yuri happy
```

No te preocupes si todavía no entiendes qué hace la sentencia **`show`**. Más adelante la veremos en profundidad.

**IMPORTANTE**

Ren'Py **no distingue entre mayúsculas y minúsculas en el nombre de las imágenes que registras**. Internamente convierte el nombre de la imagen a minúsculas.

Por ejemplo, estas definiciones son equivalentes:

```renpy
image Yuri Happy = "images/sprites/yuri/Yuri_Happy.png"
```

```renpy
image yuri happy = "images/sprites/yuri/Yuri_Happy.png"
```

Y en ambos casos la imagen se muestra exactamente igual:

```renpy
show yuri happy
```

Aun así, **te recomiendo escribir siempre las etiquetas y los atributos en minúsculas**. Es una buena práctica que hará tu código más consistente y fácil de leer.
Quizá ahora te estés preguntando...

> **¿Y para qué sirve todo esto?**

La respuesta es: **te ayudará muchísimo más adelante**, cuando empieces a cambiar las expresiones y poses de tus personajes.

Gracias al sistema de **etiquetas** y **atributos**, Ren'Py sabe que todas estas imágenes pertenecen al mismo personaje:

```
image yuri happy = "images/sprites/yuri/happy.png"
image yuri sad = "images/sprites/yuri/sad.png"
image yuri angry = "images/sprites/yuri/angry.png"
```

Entonces, si Yuri ya está en pantalla y escribes:

```
show yuri happy

y "¡Hola!"
```

Más adelante podrás cambiar su expresión simplemente haciendo:

```
show yuri sad

y "No me siento muy bien..."
```

Ren'Py reemplazará automáticamente la imagen anterior porque ambas comparten la misma **etiqueta** (`yuri`).

Esto tiene una ventaja enorme: **no tendrás que ocultar al personaje cada vez que cambie de expresión.**

Existe la instrucción `hide`, cuya función es quitar una imagen de la pantalla.

Por ejemplo:

```
hide yuri
```

Después tendrías que volver a mostrarla:

```
show yuri sad
```

Aunque esto funciona perfectamente, **no es la forma más habitual de trabajar** cuando simplemente quieres cambiar la expresión, la ropa o la pose de un personaje.

Lo normal es dejar que Ren'Py haga el trabajo por ti gracias a las **etiquetas** y los **atributos**.

Generalmente `hide` se utiliza cuando realmente quieres que un personaje desaparezca de la escena, cuando vas a mostrar un **CG**, cuando cambias de escenario o cuando el guion requiere que un elemento deje de estar visible.

- `image` indica a Ren'Py que vas a registrar una imagen.
- `etiqueta atributo otro_atributo` es el nombre con el que posteriormente podrás referirte a ella.
- `=` asigna un recurso a ese nombre.
- `"ruta/del/archivo.png"` indica dónde se encuentra el archivo dentro de tu proyecto.

Por ejemplo:

```
image yuri happy = "images/sprites/yuri/happy.png"
```

En este caso ocurre lo siguiente:

- La **etiqueta** es `yuri`.
- El **atributo** es `happy`.
- El archivo que utilizará Ren'Py es `images/sprites/yuri/happy.png`.

## Sentencia show y hide

Una vez registrada la imagen, podrás mostrarla cuando quieras con la sentencia `show`.

```
show yuri happy
```

Ren'Py buscará la imagen llamada `yuri happy` y mostrará el archivo que registraste anteriormente.

---

Si después defines otra imagen del mismo personaje:

```
image yuri sad = "images/sprites/yuri/sad.png"
```

Podrás cambiar la expresión simplemente escribiendo:

```
show yuri sad
```

Como ambas imágenes tienen la misma **etiqueta** (`yuri`), Ren'Py reemplazará automáticamente la expresión anterior por la nueva.

Gracias a este sistema, normalmente **no es necesario utilizar** `hide` para cambiar la expresión de un personaje.

Por ejemplo, esta forma funciona:

```
hide yuri
show yuri sad
```

Pero es innecesaria.

Lo habitual es escribir simplemente:

```
show yuri sad
```

Ren'Py ocultará la imagen anterior y mostrará la nueva automáticamente porque ambas pertenecen a la misma etiqueta.

La sentencia `hide` suele reservarse para situaciones donde realmente quieres que una imagen desaparezca de la pantalla. Por ejemplo:

- Cuando un personaje abandona la escena.
- Antes de mostrar un **CG**.
- Al cambiar de escenario.
- Cuando un elemento ya no debe permanecer visible.

---

## ¿Y si no quiero usar la sentencia `image`?

También es completamente válido mostrar un archivo indicando su ruta directamente.

```
show "images/sprites/yuri/happy.png"
```

En este caso Ren'Py cargará esa imagen sin necesidad de haberla registrado antes.

Muchos desarrolladores utilizan este método para imágenes que solo aparecerán una vez, pruebas rápidas o recursos temporales.

Sin embargo, para personajes que cambiarán constantemente de expresión, la sentencia `image` resulta mucho más cómoda y mantiene el código limpio y organizado.

