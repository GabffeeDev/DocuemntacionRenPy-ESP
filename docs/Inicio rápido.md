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

# ¿Por dónde empezar?

Si es la primera vez que desarrollas una novela visual, es normal preguntarse por dónde comenzar. **Ren'Py** ofrece muchas herramientas, y puede resultar tentador empezar a programar de inmediato. Sin embargo, una buena novela visual comienza mucho antes de escribir la primera línea de código.

Antes de abrir Ren'Py, dedica tiempo a planificar tu proyecto. Define la historia que quieres contar, quiénes serán tus personajes, qué papel desempeñará cada uno y cuál será el mensaje o la experiencia que deseas transmitir al jugador. Una base sólida hará que el desarrollo sea mucho más sencillo y **evitará** tener que rehacer grandes partes del proyecto más adelante.

A lo largo de esta documentación no solo aprenderás a utilizar Ren'Py, sino también algunas buenas prácticas que pueden ayudarte a organizar tu trabajo. Hablaremos sobre cómo definir personajes de forma coherente, cómo estructurar y administrar **imágenes**, **fondos** y **sprites**, cómo organizar archivos de **audio**, **música** y **efectos de sonido**, y cómo mantener un proyecto limpio y fácil de ampliar.

El objetivo es que, desde el principio, adquieras hábitos que te permitan concentrarte en lo más importante: contar una buena historia. Una estructura bien organizada no solo facilita el desarrollo, sino que también hace que el mantenimiento del proyecto sea mucho más cómodo cuando este crezca.

No existe una única forma correcta de crear una novela visual. **Cada desarrollador encuentra su propio flujo de trabajo con la experiencia.** Las recomendaciones que encontrarás aquí están pensadas para ayudarte a evitar errores comunes y ofrecerte un punto de partida sólido para que puedas dedicar más tiempo a crear y menos tiempo a resolver problemas de organización.

Comencemos construyendo una buena base. El resto del proyecto será mucho más fácil cuando cada pieza tenga su lugar.

---

Al abrir el launcher de Ren'py podrás **cambiar el idioma a Español**, como también crear un proyecto y elegir su nombre y resolución. Solo asegúrate de que las imágenes que pongas en Ren'py sean acorde a la resolución del proyecto.

![[Pasted image 20260723165844.png]]

En preferencias deberás elegir la carpeta en la cual se **guardaran** tus proyectos, en lo personal te recomiendo ser sumamente ordenado en ello. 

Por cierto te recomiendo que instales [Visual Studio Code]([Download Visual Studio Code - Free AI Code Editor for Mac, Linux, Windows](https://code.visualstudio.com/download?_exp_download=fb315fc982)) para que lo selecciones como editor de texto (de sistema para que no tengas que actualizarlo a cada rato), te servirá muchísimo.                                                             
![[Pasted image 20260723170121.png]]

Una vez hayas creado tu proyecto, en este caso lo nombre "NuevoProyecto" te darás cuenta que al lado derecho en la columna que dice "Editar archivo" aparecen unos scripts con extensión .rpy, que es el lenguaje que usa Ren'py. Pero de momento no los tocaremos ya que lo importante se encuentra en la columna derecha "Abrir carpeta", donde veras varias carpetas que podrás modificar o agregar recursos para usarlos en tu juego.

![[Pasted image 20260723171011.png]]

Normalmente antes de empezar a trabajar en un proyecto desearás agregar los recursos antes de empezar a programar la historia


### Definiendo personajes

La función `Character()` se utiliza para crear un personaje que participará en los diálogos de la novela visual. Este objeto almacena la configuración del personaje, como su apariencia durante las conversaciones y otras opciones relacionadas con la forma en que se muestran sus intervenciones.

Una vez creado, es habitual asignarlo a una **variable** mediante la instrucción `define`. Esa variable se utilizará posteriormente para identificar al personaje en los diálogos. Cuando Ren'Py encuentra esa variable al inicio de una sentencia de diálogo, sabe que el texto debe mostrarse utilizando la configuración asociada a ese personaje.

Por ejemplo:

```
define e = Character("Eileen")

e "¡Hola, mundo!"
```

![[Pasted image 20260723163724.png|293]]
En este caso, `Character()` crea un personaje con una configuración específica y la almacena en la variable `e`. Más adelante, cada vez que se utilice `e` en un diálogo, Ren'Py aplicará automáticamente esa configuración al mostrar el texto.

Aunque este ejemplo solo personaliza un aspecto visual, `Character()` admite numerosos parámetros que permiten modificar el comportamiento y la presentación de los diálogos, los cuales se explorarán en las siguientes secciones.


### Definiendo imágenes

Voy a comentar algo muy interesante sobre Ren'py que muchas desarrolladores no saben, ¡Ren'py crea variables automáticamente para las imágenes!