Nos tenemos que ir al apartado de vpc dentro del aws y crear una vpc, seleccionamos la opcion de una vpc y mas, le damos un nombre, le asignaos una ip principal, que despues se va a dividir en 4 subredes, 2 de ambito privado y 2 de ambito publico.
![image](https://github.com/user-attachments/assets/68528a84-2339-4146-a26f-57a3a67566ce)

Vamos a darle las direcciones ip publicas y privadas, una vez que este configurado como esta en la foto, le vamos a dar a crear vpc, se nos va a cargar y se nos va a mostrar toda la informacion de esa nueva vpc.

![image](https://github.com/user-attachments/assets/caadff9a-2032-4db7-8a5c-c33157d09b30)

Ahora vamos a crear la instancia para hacer el proyecto, dentro de aws tenemos que buscar el apartado de ec2, una vez la hemos encontrado vamos a darle y hay un boton que pone lanzar instancia le damos y se nos habre lo que esta en la foto para configurar la instancia, le damos un nombre y seleccionamos un sistema operativo para esa maquina, que en mi caso va a ser ubuntu que se adapta mejor a mi proyecto

![image](https://github.com/user-attachments/assets/03934846-3b87-4ce0-a056-c0e4babf995c)

Despues hay que asociarle la vpc a la instancia para poder trabajr con las subredes que hemos creado antes, seleccionamos las claves vockey para poder conectarnos con ssh si fuera necesario, y editamos la configuracion de red donde vamos a trabajar con la vpc, y en la red vamos a poner la vpc que se a creado antes y en la subred vamos a poner la subred publica 2, vamos a configurar el grupo de seguridad de la instancia y le vamos a añadir reglas de entradas para conectarnos a apache y a wordpress en un futuro como pide la practica, una vez tengamos echo eso vamos a darle a crear instancia.
![image](https://github.com/user-attachments/assets/cfff8a8c-83d6-4274-99f2-70b5992cfbe8)


Se nos crea la instancia y si le damos al nombre podemos ver toda la informacion de la instancia, despues en un apartado arriba tiene que haber un boton que pone conectarse, le damos y se nos habre el menu de la imagen con la ip publica que nos va a hacer falta mas adelante para el apache y el wordpress, le damos a conectarse y se nos tiene que iniciar la instancia en modo comandos.

![image](https://github.com/user-attachments/assets/a2d1d1e4-1630-472c-be51-bac7a054f2fc)


Aqui ya tenemos la instancia funcionando bien, ya aqui vamos a hacer las distintas operaciones para instalar apache, wordpress y todo lo necesario.

![image](https://github.com/user-attachments/assets/6ba9b593-eaa6-4629-be5b-234534d69fef)


Vamos a comenzar por instalar apache, para eso siempre hay que poner al dia los paquetes de la instancia para que esten actualizados a la ultima version con este comando sudo apt update && sudo apt upgrade -y

![image](https://github.com/user-attachments/assets/8d480562-bbd8-4f1d-82d1-8c463399cae5)

Una vez que tengamos esto echo, vamos a instalar el apache, para eso vamos a utilizar el siguiente comando sudo apt install apache2
![image](https://github.com/user-attachments/assets/b04abec0-ce48-45bf-8105-14ade7b8b279)

Si no hay ningun error, en el propio navegar utilizaremos nuestra ip de la instancia y nos debera llevar a la pagina inicial de apache como muestra en la imagen, como en las reglas de entrada hemso habilitado http y https solo con la ip nos vale si esta bien configurado la instancia y los pasos de los comandos en la instancia.
![image](https://github.com/user-attachments/assets/4aac11c2-b3b6-4941-ba9d-8e8c2bfc4da7)

Ahora para ir preparando la base de datos vamos a instalar el php con el siguinete comando sudo apt install php libapache2-mod-php php-cli
![image](https://github.com/user-attachments/assets/78315f8e-17e3-41f5-bc99-6ed4c40d7b54)

Una vez que tengamos eso echo vamos a instalar el mysql para comunicarnos con la base de datos con el siguinete comando sudo apt install php-mysql
![image](https://github.com/user-attachments/assets/2427e4b3-62e9-4b24-acb5-eecfc8259c27)

Ahora vamos a buscar en aws una opcion que se llama rds para crear la base de datos y trabajar con ella para poder crear wordpress, como vez en la imagen hay que darle a la opcion de crear base de datos, despues se nos abre la configuracion de esa base de daatos
![image](https://github.com/user-attachments/assets/a811038b-2900-4282-aeb7-6c2261077ba1)

Ya aqui vamos a configuarar la base de datos con un nombre, vamos a escoger el paquete MySQL que es la version mas conocida y con la que mas comodo se trabaja
![image](https://github.com/user-attachments/assets/6bd8e5dc-24c4-4e6f-b11a-7ce0e2bf3a0d)

Escogemos la capa gratuita que nos va a funcionar para las pruebas basicas y el paquete por defecto que nos da opcion.
![image](https://github.com/user-attachments/assets/39e9ff00-2694-4ebb-8e60-711e8b0de77f)

Aqui ya si le damos un nombre a la base de datos, vanos a administrar nosotros mismos los usuarios y las contraseñas asi que seleccionamos la opcion de autoadministrado, una vez echo eso le vamos a dar un nombre de usuario y una contraseña
![image](https://github.com/user-attachments/assets/ae3eb798-657e-4a86-8453-301d16ac9649)

Ahora en la parte de conectividad vamos a asociar la vpc que hemos creado a esta base de datos para que nos podamos comunicar, tambien creamos un nuevo grupo de seguridad donde le daremos las reglas de entrada mas adelante
![image](https://github.com/user-attachments/assets/46a70e07-7179-445b-9382-40643b794b47)

![image](https://github.com/user-attachments/assets/3ccc3611-77b5-49f0-a847-f19917ad4ea5)

Si le queremos dar mas detalles a la base de datos en configuracion adicional le podemos dar otros nombres tambien, pero ahi no he tocado mucho, casi todo se deja por defecto, una vez echo eso le damos a crear base de datos y listo ya la tenemos creada
![image](https://github.com/user-attachments/assets/c915487a-2176-4f0f-8981-f0270ccdce6e)

Cuando se haya creado la base de datos se nos actualiza la pagina y nos sale la base de datos, la selecionamos y en acciones le vamos a dar a configurar la conexion de ec2 y se nos habre la siguinete ventana
![image](https://github.com/user-attachments/assets/3fc57c5f-e045-4bee-8bdb-25ebe1b8a1bb)

En esta parte donde pone instancia ec2 le vamos a asociar la isntancia con la que estamos trabajando y le damos a continuar, en la siguinete parte se nos abre una ventana con la informacion de configuracion y le damos a continuar o a finalizar.
![image](https://github.com/user-attachments/assets/4699ab6f-cdd4-41cd-8419-e51c98bee80c)

A continuación, deberemos crear el sistema de almacenamiento externo que vamos a conectar a la instancia y que más tarde conectaremos a wordpress, para ello en el buscador de AWS buscamos EFS y le daremos al primer resultado, en el submenu le daremos a sistema de archivos, se nos pone esta ventana que esta en la imagen le damos a crear un sistema de archivos
![image](https://github.com/user-attachments/assets/4f9d60f0-2d65-49e6-9881-f8b398ecce32)

Ahora se nos toca configurar ese sistema de archivos, le damos un nombre y le asociamos nuestra vpc.
![image](https://github.com/user-attachments/assets/d4da6774-6c76-411d-81bf-7af2935fb713)

Se nos crea el sistema de archivos, cuando lo tenemos lo seleccionamos y en le damos a detalles para que se nos habra toda la informacion, debajo del recuadro de la informacion hay un apartado con distintamos opciones y buscamos red y le damos a administrar se nos abre esta ventana y ahi le vamosa agregar el grupo de seguridad que hemos creado antes y le damos a guardar.
![image](https://github.com/user-attachments/assets/891ff086-57a2-4f1b-b5a6-2c9513ff87a9)

A ese grupo de seguridad que hemos creado antes y le hemos asignado al sistema de archivos que hemos creado antes, para llegar al grupo de seguridad hay que ir a ec2-grupo de seguridad-seleccionamos el que hemos creado al principio y le editamos las reglas de entrada.
![image](https://github.com/user-attachments/assets/4595aea7-3057-4c08-b155-d17f929c5b5d)

Estos dos pasos estan para poder copiar direcciones que se van a utilizar mas adelante en linea de comandos
![image](https://github.com/user-attachments/assets/91dda7bc-ac13-466c-868a-a4d8292ccd26)

Ahora vamos a instalar el paquete nfs con el siguiente comando sudo apt-get install nfs-common
![image](https://github.com/user-attachments/assets/b5319224-d99b-4ae9-8a63-4bcd7a564173)

Una vez que tengamos el paquete bien instalado vamos a crear una carpeta que va a ser el directorio principal y seguidamente pegamos el comando que copiamos antes en el apartado de efs para conectar la instancia EC2 con la EFS.
![image](https://github.com/user-attachments/assets/d9275226-3f2d-4e81-886c-be2751a52b6e)

Nos movemos al directorio principal con cd /var/www/html
![image](https://github.com/user-attachments/assets/e96f3991-a9bd-4977-a898-be2e8bebd506)

Una vez dentro descargamos el archivo comprimido de wordpress con el comando sudo wget http://wordpress.org/latest.tar.gz
![image](https://github.com/user-attachments/assets/76e10449-84e3-425d-b09d-a1848253fc89)

Descomprimimos el archivo de wordpres que hemos descargado antes con el comando sudo tar -xf latest.tar.gz
![image](https://github.com/user-attachments/assets/805fa734-c10b-428b-a5d8-360b3db7f1fe)

Una vez tenemos echo eso vamos a instalar el cliente MySQL con el siguinete comando sudo apt install default-mysql-client
![image](https://github.com/user-attachments/assets/b9a93b87-28d3-4152-9180-6c94db401f51)

Ahora nos dirigiremos al menú de RDS para copiar el punto de enlace y conectarnos a la base de datos EFS que creamos anteriormente. En esta sección, buscaremos nuestra base de datos y accederemos para copiar el punto de enlace, una vez heccho ejecutaremos el siguiente comando para conectarnos a la base de datos. 
con este comado mysql -u admin -h (enlace) -p nos vamos a conectar a la base de datos.
![image](https://github.com/user-attachments/assets/f820fb83-4898-4ea0-9b01-e43dfc04debc)

Ahora ejecutaremos las siguientes líneas de MySQL para crear nuestra base de datos Wordpress:
![image](https://github.com/user-attachments/assets/89b6632f-675b-465d-a5dd-7ada9641bb92)

Salimos de la linea de comandos y vamos al navegador y con la ip de la instancia otra vez per esta vez le añadimos ip/wordpress y se nos va a la pagina de configuracion de wordpress 
![image](https://github.com/user-attachments/assets/f9ed340b-72f8-4201-babb-fe61674ac545)

Cuando le demos a login en la otra pagina se nos abre la configuracion, le vamos a dar un nombre a la base de datos, una conraseña y el enlace de la base de datos que hemos creado antes.
![image](https://github.com/user-attachments/assets/85220a83-7dd9-4fa7-b5a3-292af7243672)

Ejecutamos los siguientes compandos para crear un fichero en el que pgar los datos que nos ha proporcionado el WordPress
cd /var/www/html sudo nano wp-config.php
![image](https://github.com/user-attachments/assets/44fc2325-0860-463d-822e-ffeb518ef7ef)

Ya que tenemso esta parte echa vamos al na vegador otra vez y vamos a darle un titulo, un usuario, una contraseña y un correo y al terminar le daremos a install WordPress
![image](https://github.com/user-attachments/assets/d0c8eb2e-9ca7-4b19-a430-86eefd8456e2)

Recargamos la pagina y nos saldra las credenciales, ponemos las credenciales que hemos creado enates con nuestro usuario y nuestra contraseña y estamos dentro.
![image](https://github.com/user-attachments/assets/a9848e68-cbbb-4e15-8361-e00d63e3c80c)

































