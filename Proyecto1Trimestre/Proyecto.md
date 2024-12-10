- 1º trimestre

### Instalación del servidor web apache. Usaremos dos dominios mediante el archivo hosts: centro.intranet y departamentos.centro.intranet. El primero servirá el contenido mediante wordpress y el segundo una aplicación en python

Instalamos Apache desde el terminal con el comando que aparece en la imagen:

![image](https://github.com/user-attachments/assets/15969bb1-bf2a-444d-adda-ea103f0f8ed6)

Lo habilitamos con sudo systemctl enable apache2

![image](https://github.com/user-attachments/assets/0f8fc95c-0fd6-421a-9939-84c6e4b9900e)

Comprobamos que esta instalado con el localhost

![](https://github.com/user-attachments/assets/e888712a-8742-4515-91a9-44b097c3c1f6)

abrimos el archivo hosts con nano para configurar los hosts virtuales
![image](https://github.com/user-attachments/assets/3a85612e-ea0b-4c2b-af4d-368ab4f97dbf)

Le asignamos la ip por la que va a entrar y el nombre del dominio
![image](https://github.com/user-attachments/assets/cd600df1-14ac-4161-a2df-7079e793d799)

abrimos la configuracion de los sitios virtuales de apache con nano para configurar los hosts virtuales.
![image](https://github.com/user-attachments/assets/d331d171-4c06-4de0-9922-5f5d9bb384e0)

Le asignamos el servidor, el puerto de entrada y el root por el cual acceder
![image](https://github.com/user-attachments/assets/0b7e38da-0007-4114-ae45-3520623b67ad)

### Activar los módulos necesarios para ejecutar php y acceder a mysql

instalamos el las librerias de apache y las de sql para trabajar con apache y las bases de datos con el comando de la imagen y esperamos que se instale
![image](https://github.com/user-attachments/assets/2cde851b-b9b0-40f9-8106-0f188a95541c)

### Instala y configura wordpress

vamos a descargar wordpress
![image](https://github.com/user-attachments/assets/8b5565a8-0d11-495f-99cb-00db38829fc1)

Ejecutamos esto y se nos abre para craer una base de datos le damos los parametros y listo
![image](https://github.com/user-attachments/assets/81fe76e2-0bdb-49b6-bd56-8c5c8ca28576)

### Crea y despliega una pequeña aplicación python para comprobar que funciona correctamente.

creamos unas carpetas donde va a estar el programa python
![image](https://github.com/user-attachments/assets/77eeac32-465f-4b7e-99d6-e345318cf1af)

le damos las instrucciones necesarias 
![image](https://github.com/user-attachments/assets/06e94e09-921d-44e6-b4a6-42fcaf6aa18c)

### Adicionalmente protegeremos el acceso a la aplicación python mediante autenticación

Despues de eso vamos a hacer el proceso de autenticacion
![image](https://github.com/user-attachments/assets/bb00d0ae-b8f9-4f95-b6c7-629dd2c8a73f)

### Instala y configura awstat.

vamos a configurar awstats
![image](https://github.com/user-attachments/assets/6bf8046f-676f-4c01-b799-317e8cc59992)

### Instala un segundo servidor de tu elección (nginx, lighttpd) bajo el dominio “servidor2.centro.intranet”. Debes configurarlo para que sirva en el puerto 8080 y haz los cambios necesarios para ejecutar php. Instala phpmyadmin.

instalamos el nginx
![image](https://github.com/user-attachments/assets/dc8135ba-dff9-4e6f-aeb5-313de2750a80)

editamos los archivos para copnfigurar el puerto de escucha y el noimbre del servidor al que va a ir
![image](https://github.com/user-attachments/assets/75ba2302-a0ed-44f6-84b7-aae34a379f9e)

![image](https://github.com/user-attachments/assets/dd52359f-cf5f-4918-9278-89dbdae0eefb)

con sudo apt install phpmyadmin -y instalamos phpmyadmin, se nos va a empezar a decargar y despues nos aparecera opciones de configuracion 
![image](https://github.com/user-attachments/assets/16c9a02e-7a98-4298-9b0d-372ee2086047)
![image](https://github.com/user-attachments/assets/c32f6e85-addb-4fd3-b431-5d84d9f468eb)
![image](https://github.com/user-attachments/assets/37cff844-087a-447b-bb84-35d1dfc030f7)


















