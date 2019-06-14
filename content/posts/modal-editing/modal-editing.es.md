---
title: "Edición modal, la mejor manera de editar texto"
date: 2019-05-26T15:29:34+02:00
draft: false
language: es
tags:
- vim
- emacs
---

<center>![](https://lcom.static.linuxfound.org/images/stories/vim-logo.jpg)</center>

Bueno vale, igual me he pasado. Realmente me da igual la manera en la
que edites texto, lo recomentable es que uses lo que más cómodo te
sea. Lo que realmente me gustaría decir con este texto es que hay más
maneras de editar texto que **la tradicional**, la que la mayoría de
gente usa cuando le enseñan a utilizar un ordenador.

Con este texto no pretendo hacer sentir mal a la gente que no le
apetece aprender la manera en la que yo hago las cosas. No es una
guerra sobre editores, ni sobre cómo cada una edita texto. Si estás
leyendo esto es porque te interesa aprender sobre un concepto que no
es tan común, no vengo aquí a convencer a nadie de cómo tiene que
hacer las cosas.

Esto tampoco es un tutorial de cómo usar *Vim*, quiero centrarme en lo
que implica usar un editor modal, el porqué, el cómo y el cómo no. Voy
a dar algunos recursos e ideas que pueden ayudar si alguien se anima a
aprender, pero esto **no** es un tutorial.

<center>![](/img/posts/modal-editing/vim-demonstration.gif)</center>

## La filosofía

La edición modal nace de las necesidades que tenían los programadores
allá cuando para interactuar con un ordenador tenías que hacerlo a
través de la *línea de comandos*. No existían ratones porque no
existía una interfaz por la que navegar. Aquí es donde a partir de
estas necesidades surgen los intentos de optimizar la manera en la que
editamos texto.

Y bueno "¿Cuál es la filosofía de la edición modal?" os
preguntaréis. Se podría resumir en unos puntos bastante concretos
aunque probablemente me deje algo:

- Optimizar el uso del teclado.
- Minimizar la distancia en la que movemos la mano de lo que se llama
  la *home row*, que es la línea principal donde descansan los dedos.
- Utilizar modos, de ahí *edición modal*, que cambian el
  comportamiento de cada una de las teclas para hacer uso de funciones
  específicas.
- Entender que, estés escribiendo un libro o programando, pasamos más
  tiempo editando texto que añadiéndolo, y por tanto, la optimización
  de ello deba priorizarse.
- Reducir el número de acciones repetitivas que hacemos y para ello
  hace uso de *macros* que facilitan las tareas repetitivas.

La característica principal que define todo esto serían los
modos. Digamos que los modos son maneras de separar lo que es
introducir texto con el resto de cosas relacionadas con la edición. En
*Microsoft Word* por ejemplo, podemos usar las teclas para introducir
texto, con algún que otro *atajo de teclado* para distintas funciones,
podemos seleccionar texto con el ratón, movernos con las
flechas... Todo esto resulta en una manera intuitiva de editar texto,
pero ¿es una manera eficiente de hacerlo?

### ¿Cómo se transfieren los controles que conocemos a un editor modal?

Los controles pueden resultar raros o poco intuitivos, aunque se
utiliza la mnemotécnica para facilitar el recordar los comandos. Suena
raro, pero créeme cuando digo que es cuestión de entender la lógica, a
partir de ahí, todo sigue los mismos principios.

Y como yo vengo aquí a hablar de mi libro, voy a hablar de
*Vim*. Porque es el sucesor de un editor que se creó en 1976 y sigue
teniendo relevancia a día de hoy, me parece lo suficientemente
importante para tenerlo de referencia. *Vi* no fue el primer editor
modal, pero fue el que se popularizó hasta el punto de seguirse
utilizando a día de hoy.

<center>![](/img/posts/modal-editing/vim-modes.gif)</center>

*Vim* (Vi IMproved) trata de coger *Vi* y mejorarlo. Principalmente
son muy iguales, aunque se me haría raro hablar de *Vi* ya que ha sido
eclipsado y prefiero contar cómo *Vim* traduce la filosofía modal a
los modos que utiliza:

- `Normal mode`: Este modo, que traducido sería *modo normal*, es el
  modo principal, en el que más tiempo se suele pasar normalmente. En
  el *modo normal* podemos movernos por el documento, buscar texto,
  buscar caracteres, borrar texto o decirle al editor cuál es la parte
  del texto que queremos modificar, entre muchas otras cosas. Este
  modo utiliza la mnemotécnica para asignar funciones a las teclas
  alfanuméricas, como podría ser `d` para `delete` y `p` para
  `paste`. Para moverte por el texto existen diferentes teclas, pero
  las principales serían `h` para moverse a la izquierda, `l` a la
  derecha, `j` hacia abajo y `k` hacia arriba. Suena raro, pero ahora
  podemos movernos por el texto sin mover la mano para llegar a las
  flechas.
- `Insert mode`: Este modo es el que todo el mundo conoce, el que está
  en todas partes, y es como bien indica su nombre el modo para
  insertar texto. Se podría decir que es uno de los modos en los que
  más tiempo se está. Aquí se escribe texto, las teclas alfanuméricas
  funcionan de manera normal. Siguen existiendo ciertos *atajos de
  teclado* que nos ayudan a realizar algunas acciones, pero muy
  puntuales.
- `Visual mode`: Este modo es únicamente para seleccionar texto,
  seguimos teniendo las teclas de control del *modo normal* para
  movernos por el texto y que este se seleccione. Este modo es muy
  potente, ya que podemos usar las teclas de búsqueda para mover
  nuestro cursor y así mover la selección también.
- `Visual block mode`: Este viene siendo exactamente el mismo modo que
antes, solo que el texto se selecciona en bloques. Es muy útil para
seleccionar texto que está separado en colúmnas como pueden ser las
tablas de datos.
- `Replace mode`: Este modo no lo he usado en mi vida, funciona igual
  que cuando te dejas pulsada la tecla insert en word. No ofrece
  ninguna utilidad, puesto que es más recomendable hacer uso de las
  utilidades que Vim ofrece en su **modo normal**.


Existe algún que otro modo más, como puede ser el `command mode `, `^X
mode` o el `Ex command mode`, pero no voy a entrar por ahí porque es
algo más avanzado. Y aunque todo esto parezca raro, resulta en una
edición de texto en la que se puede no mover la mano en ningún
momento.

## El lenguaje

He hablado un buen rato de la edición modal, pero no podemos
olvidarnos de la parte que hace que la edición modal sea eficiente e
intuitiva. Hablo del lenguaje que usa `vim` para sus *comandos* o
*atajos de teclado*. Como he dicho antes, el modo `insert` es el que
usamos para escribir texto, pero para hacer mágia tenemos el modo
`normal`. Cada *comando* está formado por tres partes: un *verbo*, un
*sujeto* y opcionalmente un *movimiento*. Esto facilita la
automatización y repetición de estos *comandos*, los cuales se pueden
programar, crear *macros*, etc. Vamos a ver unos ejemplos que creo que
demuestran mejor la teoría.

<center>![](/img/posts/modal-editing/vim-words.png)</center>

Cómo se haría para borrar dos palabras, cómo es posible que nos
acordemos de los millones de *comandos* que tiene Vim. Bueno, pues
queremos **borrar**, **dos**, **palabras**. Tenemos *borrar* como
verbo, *palabras* como sujeto y *dos* como movimiento. No es más
difícil que posicionar el cursor debajo de la palabra que queremos
borrar y darle a `d2w`. Pero vamos a ver, cómo que `d2w`, ¿qué
significa eso? Literalmente, *delete two words*. También podemos
añadir un multiplicador al principio para repetir el comando. Por
ejemplo, ¿qué haríamos en caso de querer borrar dos veces dos
palabras?  `2d2w`. ¿Cambiar una palabra? `cw` (*Change Word*), ¿borrar
un párrafo? `dip` (*Delete Inside Paragraph*), ¿cambiar el contenido
de un texto entre comillas? `ci"` (*Change Inside "*). Y así podría
seguir hasta el infinito, hay verbos para todo y sujetos de todo tipo.

## ¿Por qué usar la edición modal?

Aunque tras la filosofía no haya una preocupación por la salud, y
aunque no haya un estudio real que lo pruebe, se dice que usar un
editor modal puede ayudar a reducir dolores de muñeca derivados de
tener que hacer tantos movimientos para llegar a las flechas del
teclado o a coger el ratón.

La rapidez es una de las ventajas principales por las que aprender a
usar la edición modal. Una vez aprendidos los movimientos básicos y
los propósitos de los distintos modos, todas las acciones que queramos
realizar sobre nuestro texto están como mucho a dos teclas de
distancia de nuestros dedos.

Aprender a usar la edición modal es tedioso, hay que cambiar la manera
de pensar, un poco como cuando se aprende a programar, pero cuando
llegas a tener un poco de soltura es fácil ver los beneficios. En mi
caso, el interés por aprender vino de querer ser más rápida con el
teclado, cada vez que tengo que usar el ratón para hacer algo que se
puede hacer con el teclado me siento lenta.

Si os soy sincera, no creo que sea difícil como tal, no va de
memorizarse un libro, una vez entiendes los conceptos principales es
cuestión de lógica ir entendiendo los controles.

## ¿Cómo no aprender a usar la edición modal?

He dicho que *Vim* no es difícil, sí, pero requiere un periodo de
aprendizaje. No recomiendo obligarse a usarlo en el trabajo o en otras
situaciones en las que necesites ser eficiente hasta que tengas cierta
soltura.

<center>![Learning
curves](https://proxy.duckduckgo.com/iu/?u=http%3A%2F%2Fergoemacs.org%2Femacs%2Fi%2Femacs_learning_curves.png&f=1)</center>

No tienes por qué usar `vim` para aprenderlo, todo editor decente
dispone de algún tipo de plugin, que aunque algunos peores que otros,
todos llegan a ofrecer la funcionalidad principal de un editor
modal. Si tienes soltura usando *Visual Studio Code*, prueba a usar su
plugin de Vim para cosas sencillas.

## ¿Cómo sí aprender a usar la edición modal?

- Si estás dispuesta a usar *Vim* como editor para aprender, puedes
hacer uso de `vimtutor`, que es un muy buen recurso que te guía a
través del mismo de programa *Vim* sobre un documento de texto que
progresivamente te enseña los controles. Como apunte, `vimtutor` viene
instalado con Vim y lo más probable es que si tienes instalado *linux*
o *macOS* venga preinstalado.

- Si te decides por usar `emacs`, que por defecto no es un editor
modal, con sus paquetes *evil* que implementan la funcionalidad modal
puedes hacer uso de *evil-tutor*, que es una traducción a *Emacs* del
`vimtutor` hablado anteriormente.

- Como he dicho antes, cualquier editor conocido dispone de un plugin
que implementa la funcionalidad modal en el mismo. Haz uso de ese
modo, no conozco de tutoriales para cada uno de ellos, pero puedes
intentar escribir textos básicos, tuits, correos, lo que sea que te
anime a aprender.

- También puedes jugar. Sí, jugar. Existen juegos simples que haciendo
uso de los controles de Vim intentan transmitirte los mismos controles
que puedes utilizar en el editor de texto. Sé que hay varios, pero yo
recomiendo [este](https://vim-adventures.com/).

- Uno de los recursos que más me ayudó a mí fue el canal de youtube de
[ThoughtBot](https://www.youtube.com/user/ThoughtbotVideo/), donde
suelen subir videos de las charlas que acogen, entre ellas algunas de
*Vim* y *Emacs**. Las que más recomendaría son [*"aprendiendo Vim en
una semana"*](https://www.youtube.com/watch?v=_NUO4JEtkDw) y [*"cómo
dejé de preocuparme y acepté
emacs"*](https://www.youtube.com/watch?v=JWD1Fpdd4Pc). Ambas en inglés
pero muy interesantes.

- Este [otro
texto](https://stackoverflow.com/questions/1218390/what-is-your-most-productive-shortcut-with-vim/1220118#1220118)
entra en detalle en cómo poder usar `vim` más allá de los controles
básicos, fijándose en cómo incorpora funcionalidades de `ed` y demás
utilidades.

- Afróntalo progresivamente. Si acabas usando *Vim* o *Emacs*, las
posibilidades que ofrecen estos editores son infinitas, ya que
incorporan un lenguaje de programación para ampliar la funcionalidad
de estos editores. Y **todo** lo que se nos pueda ocurrir hacer, se
puede hacer. Es por ello que cuando empezamos a aprender nos podemos
sentir sobrecogidos por la cantidad de información, y lo recomendable
es aprender lo básico e ir investigando poco a poco cómo hacer uso de
las funcionalidades que necesitemos.

## Conclusión

Y hasta aquí este texto, si lo que venías a buscar era cómo salir de
*Vim* era con `:q`. Con este texto quería abstraerme de las cuestiones
técnicas, es posible que en un futuro escriba algo más técnico pero ya
existen un monton de videos y textos que se enfocan en aprender *Vim*,
así que esperad sentadas.

## Links de interés

- [Popularidad de editores de texto en la encuesta de 2019 en
  Stackoverflow.](https://insights.stackoverflow.com/survey/2019#development-environments-and-tools)
- [Página de wikipedia de Vi, predecesor de
  Vim.](https://en.wikipedia.org/wiki/Vi)
- [Vim, el editor modal por excelencia.](https://www.vim.org/)
- [Link a mi configuración de emacs, adaptada para usar edición
  modal.](https://github.com/eli-rodriguezperez/dotfiles/blob/master/init.el)
- [Link a mi configuración de
  vim.](https://github.com/eli-rodriguezperez/dotfiles/blob/master/.config/nvim/init.vim)
- [Vim-adventures, juego que hace uso de controles modales para
  enseñarte.](https://vim-adventures.com/)
- [Texto que muestra hasta donde puede llegar Vim más allá de lo
  básico](https://stackoverflow.com/questions/1218390/what-is-your-most-productive-shortcut-with-vim/1220118#1220118)
