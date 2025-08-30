
# Comando `grep`

El comando `grep` (global regular expression print) se utiliza para buscar patrones de texto dentro de archivos. Es una de las herramientas más poderosas y utilizadas en la línea de comandos.

## Ejemplos de Uso

### Búsqueda básica
Busca una palabra o patrón específico en un archivo de texto.

```bash
grep 'palabra' archivo.txt
```

### Búsqueda ignorando mayúsculas y minúsculas
La opción `-i` permite realizar una búsqueda sin diferenciar entre mayúsculas y minúsculas.

```bash
grep -i 'palabra' archivo.txt
```

### Contar el número de coincidencias
La opción `-c` (count) muestra el número de líneas que contienen el patrón buscado, en lugar de las líneas en sí.

```bash
grep -c 'palabra' archivo.txt
```

### Filtrar la salida de otro comando
`grep` se combina frecuentemente con otros comandos mediante una tubería (`|`) para filtrar sus resultados.

```bash
cat /proc/cpuinfo | grep -i 'core id'
```

### Guardar la salida en un archivo
Puedes redirigir el resultado de `grep` a un nuevo archivo utilizando el operador `>`.

```bash
grep -i 'core id' /proc/cpuinfo > nucleos.txt
```

## Opciones Adicionales Populares

*   `-r`: Realiza una búsqueda recursiva dentro de un directorio.
*   `-v`: Invierte la búsqueda, mostrando las líneas que **no** coinciden con el patrón.
*   `-n`: Muestra el número de línea junto a la salida.
*   `-l`: Muestra únicamente los nombres de los archivos que contienen el patrón.
