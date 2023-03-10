# Notas para orientar en el uso del editor de textos Vim

**NOTA 1**: Más información sobre Vim se encuentra en las páginas 9 a 11 de la [guía rápida de Linux](https://github.com/grobiglio/DevOps/blob/main/Linux%2BQuickstart%2BV5.pdf).

**NOTA 2**: Se puede aprender más de Vim en este curso gratuito de Udemy 👉 [Vim, aumenta tu velocidad de desarrollo](https://www.udemy.com/course/vim-aumenta-tu-velocidad-de-desarrollo/).

# Instalación de Vim

Acceder 👉 [aquí](https://www.vim.org/download.php) 👈 para decargar e instalar.

# Modos de Vim

El editor de textos Vim posee tres modos:
- *Command mode* o modo normal (es el modo por defecto cuando se abre Vim)
- *Insert mode* o modo de edición
- *Extended command mode*

## Cambio de modos

- Desde *command mode* se pasa a *insert mode* presionando `i`, `o`, `a` o `A`. Ver la descripción de los comandos de *command mode* para mayor detalle.
- Desde *command mode* se pasa a *extended command mode* presionando `:`.
- Desde *insert mode* se pasa a *command mode* presionando `Esc` una o dos veces.

## Principales comandos en *command mode*

|Comando|Descripción|
|:-----:|-----------|
|`a`|Accede al *insert mode* inmediatamente después del caracter sobre el que se encuentra el cursor|
|`A`|Accede al *insert mode* al final de la línea en la que se encuentra el cursor|
|`i`|Accede al *insert mode* en el caracter sobre el que se encuentra el cursor|
|`o`|Accede al *insert mode* insertando una línea debajo de aquella en la que se encuentra el cursor|
|`O`|Accede al *insert mode* insertando una línea encima de aquella en la que se encuentra el cursor|
|`gg`|Ir al principio de la página|
|`G`|Ir al final de la página|
|`nG`|Ir a la línea `n`|
|`l`|Mueve el cursor un caracter hacia la derecha. Equivale a presionar la flecha derecha ➡ del cursor.|
|`h`|Mueve el cursor un caracter hacia la izquierda. Equivale a presionar la flecha izquierda ⬅ del cursor.|
|`j`|Mueve el cursor un caracter hacia abajo. Equivale a presionar la flecha abajo ⬇ del cursor.|
|`k`|Mueve el cursor un caracter hacia arriba. Equivale a presionar la flecha arriba ⬆ del cursor.|
|`w`|Mueve el cursor hacia adelante, palabra por palabra. Posiciona el cursor en el primer caracter de la palabra|
|`e`|Mueve el cursor hacia adelante, palabra por palabra. Posiciona el cursor en el último caracter de la palabra|
|`b`|Mueve el cursor hacia atrás, palabra por palabra|
|`nw`|Mueve el cursor hacia adelante `n` palabras (2️⃣)|
|`ne`|Mueve el cursor hacia adelante `n` palabras (2️⃣)|
|`nb`|Mueve l cursor hacia atrás `n` palabras (2️⃣)|
|`u`|Deshace el último cambio (palabra)|
|`U`|Deshace el último cambio (línea entera)|
|`Ctrl + R`|Rehace los cambios|
|`yy`|Copia la línea donde se encuentra el cursor|
|`nyy`|Copia `n` líneas. La línea donde se encuentra el cursor mas las `n-1` líneas debajo del cursor|
|`p`|Pega la o las líneas copiadas debajo de la línea donde se encuentra el cursor|
|`P`|Pega la o las líneas copiadas encima de la línea donde se encuentra el cursor|
|`dw`|Borra completamente la palabra sobre la que se encuentre el cursor (1️⃣)|
|`dnw`|Borra completamente la palabra sobre la que se encuentre el cursor más las `n-1` palabras que se encuentran a la derecha (3️⃣)|
|`x`|Borra un caracter al estilo `DEL`|
|`dd`|Corta (o elimina) la línea donde se encuentra el cursor|
|`ndd`|Corta (o elimina) `n` líneas. La línea donde se encuentra el cursor mas las `n-1` líneas debajo del cursor|
|`d$`|Corta (o elimina) desde donde se encuentra el cursor hasta el final de la línea|
|`/`|Busca una palabra en el archivo de texto. La búsqueda se realiza desde la posición del cursor hacia adelante. Con `n` (después de presionar `Intro`) se navega entre búsquedas. Tener en cuenta que la búsqueda es sensible a mayúsculas. Con `N` se regresa a la búsqueda.|
|`?`|Busca una palabra en el archivo de texto. La búsqueda se realiza desde la posición del cursor hacia atrás. Con `n` (después de presionar `Intro`) se navega entre búsquedas. Con `N` se regresa a la búsqueda.|
|`gd`|Lleva el cursor a la definición de una función, variable, constante u objeto|
|`gf`|Accede al archivo que se está citando en el texto|
|`Ctrl + o`|Vuelve al archivo desde el que se llegó usando `gf`|
|`Ctrl + i`|Para navegar hacia adelante entre archivos. Es lo inverso a `Ctrl + o` en la navegación entre archivos|
|`r`|Reemplaza el caracter sobre el que se encuentra el cursor por el que se indique inmediatamente depués|
|`R`|Habilita *modo de reemplazo* hasta que se presiona `Esc`. En *modo de reemplazo*, todo lo que se tipee reemplaza al texto existente.|
|`cw`|Elimina los caracteres de la palabra que se encuentran por delante del cursor y pasa a *insert mode* (para que se tipee nuevo texto)|
|`ciw`|Elimina la palabra sobre la que se encuentra el cursor y pasa a *insert mode* (para que se tipee nuevo texto)|
|`%`|Salta desde el paréntesis, corchete o llave donde se encuentra el cursor hasta su opuesto. Si está en el de apertura salta al de cierre y viceversa.|
|`$`|Lleva el cursor al final de la línea|
|`0`|Lleva el cursor al inicio de la línea|
|`v`|Pasa a modo visual. En *modo visual*, todo movimiento que se haga selecciona el texto. Con `y` se copia y se sale del modo visual.|

(1️⃣) El operador `d` (eliminar o cortar) se puede combinar con los comando de movimiento `l`, `h`, `j`, `k`, `w`, `e`, `b` para que la eliminación o corte lo haga en el sentido del movimiento.

(2️⃣) El operador `n` (candidad de veces) se puede combinar con los comando de movimiento `l`, `h`, `j`, `k`, `w`, `e`, `b` para que dicho movimiento se multiplique por la cantidad de veces `n`.

(3️⃣) `dnw` equivale a ejecutar hacer `n` veces `dw`. En un sentido general la operación se puede aplicar a las combinaciones explicadas en (1️⃣).

## Principales comandos en *extended command mode*

|Comando|Descripción|
|:-----:|-----------|
|`:q`|Sale de Vim|
|`:w`|Guarda el archivo|
|`:wq`|Guarda el archivo y salde de Vim al mismo tiempo|
|`:q!`|Sale a la fuerza de Vim sin guardar los cambios|
|`:se nu`|Enumera las líneas del archivo de texto|
|`:s/<cadena 1>/<cadena 2>/g`|Reemplaza todas las ocurrencias de la `cadena 1` por la `cadena 2` en la línea donde se encuentra el cursor. Si se ominte `/g` solamente se reeplazará la primera ocurrencia.|
|`:%s/<cadena 1>/<cadena 2>/g`|Reemplaza todas las ocurrencias de la `cadena 1` por la `cadena 2` en el archivo.|
|`:%s/<cadena 1>/<cadena 2>/gc`|Para todas las ocurrencias de la `cadena 1` en el archivo pregunta si se quiere reemplazar por la `cadena 2`.|