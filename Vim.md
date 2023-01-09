# Notas para orientar en el uso del editor de textos Vim

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

### Extended command mode

|Comando|Descripción|
|:-----:|-----------|
|`:q`|Sale de Vim|
|`:w`|Guarda el archivo|