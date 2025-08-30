
# Comando `ps`

El comando `ps` (process status) muestra información sobre los procesos que se están ejecutando en el sistema.

## Ejemplos de Uso

### Listar procesos de la terminal actual
Sin opciones, `ps` solo muestra los procesos asociados a la terminal actual.

```bash
ps
```

### Listar todos los procesos
La opción `-e` (every) selecciona todos los procesos del sistema.

```bash
ps -e
```

### Mostrar formato completo
La opción `-f` (full format) muestra una lista detallada que incluye el UID, PID, PPID, C, STIME, TTY, TIME y CMD.

```bash
ps -f
```

### Combinación más común
La combinación `ps -ef` es una de las más utilizadas para ver todos los procesos del sistema en formato completo.

```bash
ps -ef
```

### Filtrar por usuario
La opción `-u` permite ver los procesos de un usuario específico.

```bash
ps -u nombre_de_usuario
```
