
# Notas Varias del Sistema

Esta sección contiene apuntes diversos sobre comandos y conceptos del sistema.

## Mapa de Memoria Virtual de un Proceso

Puedes inspeccionar el mapa de memoria que el kernel asigna a un proceso leyendo el archivo `maps` dentro del directorio `/proc/<PID>/`.

Donde `<PID>` es el ID del proceso.

```bash
# Ejemplo para el proceso con PID 1217
cat /proc/1217/maps
```

## Variable de Entorno del Prompt (`PS1`)

La variable `$PS1` define cómo se ve el prompt de tu shell. Puedes ver su contenido con `echo`.

```bash
echo $PS1
```
Modificar esta variable te permite personalizar la información que se muestra en tu prompt (usuario, host, directorio actual, etc.).
