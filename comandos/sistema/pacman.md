
# Comando `pacman`

`pacman` es el gestor de paquetes para distribuciones de Linux basadas en Arch, como Arch Linux, Manjaro, etc.

## Instalación de Paquetes

### Instalar un paquete
Descarga e instala un paquete desde los repositorios.

```bash
pacman -S nombre_del_paquete
```

### Sincronizar e instalar
Actualiza la base de datos de paquetes y luego instala.

```bash
pacman -Sy nombre_del_paquete
```

## Actualización del Sistema

### Sincronizar y actualizar todo
Es el comando recomendado para actualizar el sistema.

```bash
pacman -Syu
```

### Forzar la sincronización
Descarga una copia nueva de la base de datos de paquetes, incluso si se considera actualizada.

```bash
pacman -Syy
```

## Búsqueda de Paquetes

### Buscar en los repositorios
Busca un paquete en los repositorios remotos.

```bash
pacman -Ss palabra_clave
```

### Buscar en paquetes instalados
Busca un paquete que ya está instalado en el sistema.

```bash
pacman -Qs palabra_clave
```

### Mostrar información detallada
Muestra toda la información de un paquete. `-i` para paquetes instalados, `-Si` para paquetes en el repositorio.

```bash
# Paquete instalado
pacman -Qi nombre_del_paquete

# Paquete en el repositorio
pacman -Si nombre_del_paquete
```

## Eliminación de Paquetes

### Eliminar un paquete
Elimina un paquete, pero deja sus dependencias.

```bash
pacman -R nombre_del_paquete
```

### Eliminar un paquete y sus dependencias
Elimina un paquete junto con las dependencias que no son utilizadas por ningún otro paquete. (Recomendado).

```bash
pacman -Rs nombre_del_paquete
```
