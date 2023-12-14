#1.Modifica el nombre de los virtualhost dados de ejemplo para que sean:
www.local -> nombre-apellidos-www.local
intranet.local -> nombre-apellidos-intranet.local

Accedemos al Archivo de Hosts
Abrir el archivo de hosts en el sistema. Este archivo generalmente se encuentra en:

Windows: C:\Windows\System32\drivers\etc\hosts

![rutahosts](docs/images/1.png)

Editar el Archivo de Hosts y añadimos al final del texto lo siguiente
127.0.0.1    alvaro-perez-infante-www.local
127.0.0.1    alvaro-perez-infante-intranet.local
127.0.0.1    alvaro-perez-infante-phpmyadmin.local

![txt](docs/images/2.png)

Ahora nos vamos a nuestro proyecto que clonamos del profesor:

![miproy](docs/images/3.png)

Y editamos el archivo de configuración:

![confienlaces](docs/images/4.png)

Primero lo buildeamos y lo subimos:

![build](docs/images/5.png)

Probamos que todo funcione correctamente:
http://alvaro-perez-infante-www.local/

![funciona](docs/images/6.png)

http://alvaro-perez-infante-intranet.local:8060/

![funciona2](docs/images/7.png)

###1. Creación de Virtual Host para PhpMyAdmin

Se debe crear un nuevo archivo de configuración del virtual host que se llame nombre-apellidos-phpmyadmin.conf

![ruta](docs/images/8.png)

Miramos que la página nos mande a donde corresponde:

![ruta2](docs/images/9.png)

###3. Modificación del Index.html de Intranet
   
![ruta3](docs/images/10.png)

###4. Añadir Nuevo Usuario

![nuevousuario](docs/images/11.png)

Realizamos un restart para que se actualize la información:

![restart](docs/images/12.png)
![pruebanuevousuario](docs/images/13.png)
![pruebanuevousuario](docs/images/14.png)
![pruebanuevousuarioruta](docs/images/15.png)

###5. Instalación de CMS Wordpress
![pruebanuevousuarioruta](docs/images/16.png)
![pruebanuevousuarioruta](docs/images/17.png)
![pruebanuevousuarioruta](docs/images/18.png)
![pruebanuevousuarioruta](docs/images/19.png)
![pruebanuevousuarioruta](docs/images/20.png)
![pruebanuevousuarioruta](docs/images/21.png)
Instalamos wordpress y lo metemos en la carpeta www del proyecto una vez realizado esto,entramos en el archivo wp-config-php y realizamos los siguientes cambios
![confiwordpress](docs/images/23.png)
![confiwordpress](docs/images/22.png)
Entramos en la ruta para ver que todo funciona
http://alvaro-perez-infante-intranet.local/wordpress/wp-admin/install.php
![a](docs/images/24.png)
![b](docs/images/25.png)
![c](docs/images/26.png)


#PARTE 2: Instalación de Certificados SSL
###1. Generación de Certificados
![certificados1](docs/images/27.png)
![certificados2](docs/images/28.png)
![certificados3](docs/images/29.png)

###2. Configurar para el protocolo HTTPS
![nuevasrutas](docs/images/30.png)
![nuevasrutas2](docs/images/31.png)
![nuevasrutas3](docs/images/33.png)

###3. Habilitar Módulo mod_ssl

![modulo](docs/images/32.png)
