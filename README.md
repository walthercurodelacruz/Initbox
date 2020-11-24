### PROYECTO INITBOX | MAQUINA VIRTUAL

_Initbox es una Maquina Virtual con Ubuntu Server 20.04.1 LTS que puedes ejecutar desde tu propio computador._

Un sistema linux virtualizado y actualizado con todos los servicios instalados nativamente para entornos de desarrollo web y motores de base de datos mysql y postgresql.

Initbox es una Maquina Virtual (MV) con sistema operativo Ubuntu Server, instalado desde cero y con los servicios actualizados y preparados para ejecutarse desde el primer arranque

Con la robustez de Ubuntu Server 20.04.1 en la versión LTS se garantiza un soporte extendido y por ende la estabilidad que se espera de un buen servidor derivado de Debian.

![](http://www.walthercuro.com/wp-content/uploads/2020/11/ubuntu-20-04-1.png)

Entre los servicios y librerías instaladas están:

* Apache 2.4.41
* PHP 7.4.3
* MySql 8.0.22
* Postgresql 12.5
* Python 2.7.18
* Python 3.8.5
* SSH 8.2
* Webmin 1.9.62
* PhpMysql
* PhpMailer
* Próximamente Samba y FTP.

# Descargar 

[Descargar Initbox](https://mega.nz/folder/ZfplmIgJ#FMvy0ycTeKJ_ogmzsJNxdA)

Importar Maquina Virtual
El proceso de instalación y puesta en marcha es muy sencillo e intuitivo, pero debes tener en cuenta los siguientes requisitos mínimos:

La memoria Ram y espacio en disco que consume tu Maquina Virtual será tomada de tu computador directamente como recurso de hardware virtualizado, por ello se recomienda un mínimo de 6BG de Ram y un espacio en disco libre de 10 GB. Mas adelante cuando empieces a explorar el mundo de la virtualización notaras lo sencillo que es optimizar recursos y podras tunear o customizar tu MV a tu gusto. Dicho todo esto iniciemos…

Instalar la última versión de Virtual Box e instalar su Oracle VM VirtualBox Extensión Pack (importante) desde su pagina oficial https://www.virtualbox.org/

![](http://www.walthercuro.com/wp-content/uploads/2020/11/virtualbox-logo-1.jpg)

Descargar la maquina virtual en paquete ova (.ova) e importarla en Virtual Box.

**Clic en Importar**

![](http://www.walthercuro.com/wp-content/uploads/2020/11/Importar_mv_1.png)

**Clic en Archivo**

![](http://www.walthercuro.com/wp-content/uploads/2020/11/Importar_mv_2.png)

**Seleccionar Maquina Virtual en formato OVA, previamente descargado.**

![](http://www.walthercuro.com/wp-content/uploads/2020/11/Importar_mv_3.png)

**Clic Next**

![](http://www.walthercuro.com/wp-content/uploads/2020/11/Importar_mv_4.png)

**Revisar datos de la Maquina Virtual e importar**

![](http://www.walthercuro.com/wp-content/uploads/2020/11/Importar_mv_5.png)

![](http://www.walthercuro.com/wp-content/uploads/2020/11/Importar_mv_6.png)

Listo… Ya tienes tu Maquina Virtual.

![](http://www.walthercuro.com/wp-content/uploads/2020/11/Importar_mv_7.png)


## Usuarios, Contraseñas y configuraciones adicionales.
A continuación detallo los usuarios y contraseñas que tienen los diferentes servicios que ejecuta InitBox:

* Usuario Dios (Linux) : root / Contraseña: s5st6m8s
* Usuario Principal (Linux): init / Contraseña: s5st6m8s
* Usuario Postgres (Postgresql) : postgres / Contraseña: s5st6m8s
* Usuario Mysql (BD) : initmysql / Contraseña: s5st6m8s
* Usuario Postgresql (BD) : initpostgresql / Contraseña: s5st6m8s
* Usuario Phpmyadmin: initmysql / Contraseña: s5st6m8s
* Usuario Webmin: root / Contraseña: s5st6m8s
* Puerto Webmin: 10000
* Puerto Mysql: 3306
* Puerto Postgresql: 5432
* Puerto SSH: 22
* Puerto Apache: 80

Initbox cuenta con dos tarjetas de red virtuales, una de ellas en configuración NAT para permitirle salida a Internet y la otra se encuentra en DHCP mediante la configuración «adaptador solo-anfitrión» lo cual permite que puedas acceder a la maquina virtual mediante el segmento de red 192.168.56.0/24 [Por defecto tomará la IP:192.168.56.102]. Para confirmar la IP usar el comando ifconfig.

Se podrá acceder a la Maquina virtual mediante SSH [[Putty](https://www.putty.org/)] o mediante [WinSCP](https://winscp.net/eng/download.php) a través del puerto 22 para que puedas cargar tus proyectos, la ruta de la carpeta web es: **/var/www**

Asi mismo se puede acceder mediante Webmin bajo la IP: https://192.168.56.102:10000/ o mediante: https://initserver:10000/

PhpMyAdmin también esta habilitado mediante: http://192.168.56.102/phpmyadmin/

Importante: No olvidar que la IP podría variar en cada equipo, por ello utilizar el comando ifconfig para validar la dirección asignada mediante DHCP.

## Capturas de Pantalla

![](http://www.walthercuro.com/wp-content/uploads/2020/11/Captura1.png)

![](http://www.walthercuro.com/wp-content/uploads/2020/11/Captura4.png)

![](http://www.walthercuro.com/wp-content/uploads/2020/11/Captura2.png)

![](http://www.walthercuro.com/wp-content/uploads/2020/11/Captura3-1024x483.png)

### Nota Importante

**Use esta herramienta solamente bajo su propia responsabilidad.**

## Próximas Mejoras…

* Implementar Samba
* Habilitar Carpeta WWW mediante Samba (Actualmente se accede mediante SSH)
* Implementar servicio FTP
* Colocar formulario de contacto como ejemplo en el servidor web para probar la librería phpmailer.

