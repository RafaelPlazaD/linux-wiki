
# Gestión de WiFi con `nmcli` y `nmtui`

`nmcli` es la herramienta de línea de comandos para controlar NetworkManager, mientras que `nmtui` proporciona una interfaz de usuario de texto (TUI) más sencilla.

## Usando `nmcli` (Línea de Comandos)

### 1. Listar redes WiFi disponibles
Escanea y muestra las redes WiFi a tu alcance.

```bash
nmcli device wifi list
```
**Salida de ejemplo:**
```
IN-USE  SSID                           MODE   CHAN  RATE        SIGNAL  BARS  SECURITY
        1st Network                    Infra  1     54 Mbit/s   65      ▂▄▆_  --
        2nd Network                    Infra  1     130 Mbit/s  52      ▂▄__  --
*       3rd Network                    Infra  10    195 Mbit/s  29      ▂___  WPA2
```

### 2. Conectarse a una red
Usa el SSID (nombre de la red) y la contraseña para conectar.

```bash
nmcli device wifi connect "SSID_DE_LA_RED" password "CONTRASEÑA"
```

## Comandos Adicionales de `nmcli`

### Ver conexiones guardadas
Muestra un listado de las redes que has guardado previamente.

```bash
nmcli con show
```

### Desconectarse de una red
Usa el nombre de la conexión para desconectarte.

```bash
nmcli con down "SSID_DE_LA_RED"
```

### Conectarse a una red guardada
Si ya te has conectado antes, puedes levantar la conexión por su nombre.

```bash
nmcli con up "SSID_DE_LA_RED"
```

## Usando `nmtui` (Interfaz de Texto)
Para una experiencia más visual en la terminal, simplemente ejecuta `nmtui`.

```bash
nmtui
```
Esto abrirá un menú interactivo para activar, desactivar y editar conexiones de red.
