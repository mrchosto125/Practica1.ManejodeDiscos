# Practica1.ManejodeDiscois

1. **Identificar y describir las diferencias entre hda, sda y vda, además explicar qué significa la letra y el número al final de los identificadores (no requiere captura de pantalla).**





2. **¿Cómo montar y desmontar un usb en el sistema por terminal?**

sudo mount [dispositivo] [destino]
sudo unmount [direccion]

![alt-text](https://raw.github.com/daerksun/Practica1.ManejodeDiscos/Imagenes/10.jpeg "Imagen 1")

3. **Enlistar la información de los dispositivos de bloque conectados aunque no estén montados en terminal.**

lsblk

4. **Mostrar la tabla de particiones del disco donde está instalado el sistema operativo en terminal.**

sudo fdisk -l

5. **Conectar una memoria usb (“usb”) y mostrar su tabla de particiones en terminal (hacer respaldo antes porque se va a borrar toda la información dentro del usb en pasos posteriores).**

sudo fdisk -l /dev/sdc

6. **Borrar todas las particiones del “usb” en terminal.**

unmount
fdiks /dev/sdc
d - delete
w - write
fdisk -l /dev/sdc



7.** Crear en el “usb” tres particiones físicas y una extendida en terminal.**

fdisk /dev/sdc
n - nueva particion
p - tipo de particion (primaria)
Primer Sector
Ultimo sector
se repite 3 veces
n
e - particion extendida
Primer Sector
Ultimo Sector
w

8. **Crear una partición dentro de la partición extendida del “usb” en terminal.**

fdisk /dev/sdc
l - particion lógica
w

9. **En la interfaz gráfica de la aplicación disks, borrar las particiones para que sólo exista una
partición que abarque toda la “usb”.**


10. **Copiar un archivo .iso de distribución live de linux a la usb por medio del comando "dd".**


