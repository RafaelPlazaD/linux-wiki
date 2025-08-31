## Conectarse a un servidor ftp  existente

ftp **ip_address** **port**
```bash
ftp ip_address port
```

## Habilitar un servidor ftp nuestro  host(PC)
Para poder hacer esto necesitamos tener instalado **vsftpd**

### 1. Instalación
para intalarlo en en **arch** o derivados :
```bash
sudo pacman -S vsftpd
```

### 2.Configuración
Editamos el archivo de configuracion de **vsftpd**

```bash
    sudo vim /etc/vsftpd.conf
```
Dentro del archivo tenemos que buscar estas lineas y descoméntarlas (borrando el **#**):

```
    # Deshabilitar el acceso anónimo por
      seguridad.
    anonymous_enable=NO
   
    # Permitir que los usuarios locales (con
    cuenta en tu PC) inicien sesión.
    local_enable=YES
   
    # Permitir comandos que modifican el sistema
    de archivos (ej. subir archivos).
    write_enable=YES
   
    # Enjaular a los usuarios en su directorio
    home para que no puedan navegar por todo el
    sistema.
    chroot_local_user=YES
   
       
    # (Opcional) Configurar puertos pasivos para
    mejorar la compatibilidad con firewalls/NAT.
    # Añade estas líneas al final del archivo.
    pasv_min_port=30000
    pasv_max_port=31000
```
añadimos esta linea al final del archivo:
```
# Para evitar un error común con la opción
    anterior, añade esta línea al final del
    archivo.
    allow_writeable_chroot=YES

```

## 3.Iniciar y habilitar el servicio (vsftpd)

```bash
sudo systemctl start vsftpd
sudo systemctl enable vsftpd
```

## (Opcional/IMPORTANTE) si tenemos algun Firewall (como **ufw** o **iptables**)

Para **ufw**
```bash
sudo ufw allow 21/tcp
sudo ufw allow 30000:31000/tcp
sudo ufw reload
```

## 5.Encontrar la **IP** de nuestro PC
```bash
ip addr show | grep "wlo1"
```
**wlo1**, para motrar ip que tiene mi interfaz de red, en este caso es  la interfaz de wifi, puedes remplazar **wlo1** por **wl**
si estas conectado por wifi.

la salida del anterior comando :
```
2: wlo1: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc noqueue state UP group default qlen 1000
    altname wlp1s0
    altname wlx50c2e89937f1
    inet 192.168.147.187/24 brd 192.168.147.255 scope global dynamic noprefixroute wlo1
```
***inet 192.168.147.187/24 brd 192.168.147.255 scope global dynamic noprefixroute wlo1***

**192.168.147.187** Es la IP de nuestro pc

## Conectarse al servido 
Desde otro pc/explorador de archivos de otro dispositivo podemos ahecerlo

Colocamos estos datos en nuestro cliente(otro dispositivo)

**IP** --la de nuestro servidor **192.168.147.187**

**usuario** -- el nombre del usuario de nuestro servidor(pc)

**contraseña** --contraseña de nuestro usuario(pc)

**Puerto** --por defecto es el **21**

##

**IP** :**192.168.147.187**

**Usuario** :**rafael**

**Contraseña** :**---------**

**Puerto** :**21**
