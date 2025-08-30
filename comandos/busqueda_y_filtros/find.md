
# Comando `find`

El comando `find` busca archivos y directorios en una jerarquía de directorios basada en expresiones que el usuario especifica.

## Ejemplos de Uso

### Buscar por nombre
Busca archivos que coincidan con un nombre específico. Es sensible a mayúsculas.

```bash
find /ruta/de/busqueda -name "nombre_archivo.txt"
```

Para ignorar mayúsculas y minúsculas, usa `-iname`.

```bash
find /ruta/de/busqueda -iname "nombre_archivo.txt"
```

### Buscar por extensión
Es un caso particular de la búsqueda por nombre, utilizando un comodín (`*`).

```bash
# Busca todos los archivos .txt en el directorio actual y subdirectorios
find . -name "*.txt"
```

### Buscar por tipo
Puedes buscar específicamente archivos (`f`) o directorios (`d`).

```bash
# Encontrar solo directorios
find . -type d -name "fotos"

# Encontrar solo archivos
find . -type f -name "*.jpg"
```
