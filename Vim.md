# Notas para orientar en el uso del editor de textos Vim

**NOTA**: Más información sobre Vim se encuentra en las páginas 9 a 11 de la [guía rápida de Linux](https://github.com/grobiglio/DevOps/blob/main/Linux%2BQuickstart%2BV5.pdf).

El editor de textos Vim posee tres modos:
- Command mode (es el modo por defecto cuando se abre Vim)
- Insert mode (modo de edición)
- Extended command mode

## Cambio de modos

Estando en *command mode*, presionando `i` se pasa a *insert mode*, presionando `o` se pasa a *insert mode* listo para insertar texto en la última línea.

Estando en *insert mode*, presionando `Esc` se pasa a *command mode*.

Estando en *command mode*, presionando `:` se pasa a *extended command mode*.

## Principales comando en cada modo

### Command mode

|Comando|Descripción|
|:-----:|-----------|
|`gg`|Ir al principio de la página|
|`G`|Ir al final de la página|
|`w`|Mueve el cursor hacia adelante, palabra por palabra|
|`b`|Mueve el cursor hacia atrás, palabra por palabra|
|`nw`|Mueve el cursor hacia adelante `n` palabras|
|`nb`|Mueve l cursor hacia atrás `n` palabras|
|`u`|Deshace el último cambio (palabra)|
|`U`|Deshace el último cambio (línea entera)|
|`Ctrl + R`|Rehace los cambios|
|`yy`|Copia la línea donde se encuentra el cursor|
|`nyy`|Copia `n` líneas. La línea donde se encuentra el cursor mas las `n-1` líneas debajo del cursor|
|`p`|Pega la o las líneas copiadas debajo de la línea donde se encuentra el cursor|
|`P`|Pega la o las líneas copiadas encima de la línea donde se encuentra el cursor|
|`dw`|Borra una palabra letra por letra al estilo `Backspace`|
|`x`|Borra una palabra letra por letra al estilo `DEL`|
|`dd`|Corta (o elimina) la línea donde se encuentra el cursor|
|`ndd`|Corta (o elimina) `n` líneas. La línea donde se encuentra el cursor mas las `n-1` líneas debajo del cursor|
|`/`|Busca una palabra en el archivo de texto. Con `n` se navega entre búsquedas. Tener en cuenta que la búsqueda es sensible a mayúsculas.|

### Extended command mode

|Comando|Descripción|
|:-----:|-----------|
|`:q`|Sale de Vim|
|`:w`|Guarda el archivo|
|`:wq`|Guarda el archivo y salde de Vim al mismo tiempo|
|`:q!`|Sale a la fuerza de Vim sin guardar los cambios|
|`:se nu`|Enumera las líneas del archivo de texto|