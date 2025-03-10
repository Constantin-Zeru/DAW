Tarea 1:

Vamos a instalar docker en ubunto que es lo que pide la primera tarea

![image](https://github.com/user-attachments/assets/e600e726-ab0f-4f53-a616-e5216e143ab1)

Para instaalr docker lo pripero que tenemso que hacer es actualizar los paquetes de ubuntu con el comando sudo apt-get update

![image](https://github.com/user-attachments/assets/d50fc144-b132-420e-9fec-06fad133afe4)

Despues un sudo apt-get upgrade para instalar esos paquetes actualizados

![image](https://github.com/user-attachments/assets/41d3e059-f35c-44aa-9bd7-3c2f508296c2)

Hacemos un sudo apt-get remove docker docker-engine docker.io conatinerd runc para desisnstalar los rastos de docker mas antiguos y no nos de conflicto

![image](https://github.com/user-attachments/assets/b7c6eea1-8ebd-4593-9e74-9c7a0f4fefd7)


![image](https://github.com/user-attachments/assets/26a32b2f-c86e-48f2-85d5-3b58bd83999e)

Ahora en este comando ponemos la web de docker y le añadimos las claves para descargarla

![image](https://github.com/user-attachments/assets/cb86cdb6-1514-44e0-80bf-1b9c37447c5b)

añadimos el repositorio para trabajar con el en el futuro.

![image](https://github.com/user-attachments/assets/d21e9d97-77f1-4938-9b42-918bc1bbcab0)

y por ultimo instalamos el cliente docker con ese comando que hay en la foto.

![image](https://github.com/user-attachments/assets/5fa2637f-831f-4f48-ae2d-07b1dcf09a10)


Tarea 2:
Ahora nos vamos a preparar para la segunda actividad
![image](https://github.com/user-attachments/assets/c1c81c45-911d-4a6a-94b1-a1664f045991)


![image](https://github.com/user-attachments/assets/45906787-655b-4cb0-85c8-7b5ff440fa50)

1. Ejecutar hello-world
   
Como en la primera parte ya tenemos docker descargado, nos va a traer la imagen de hello-world echa, asi que con el comando sudo docker run hello-world

![image](https://github.com/user-attachments/assets/4bd174ce-5c91-49a1-a73f-8c1432276e79)

2. Imagenes docker instaladas

Con el comando sudo docker images nos mostrara directamente las imagenes que tenemos en el ordenador  

![image](https://github.com/user-attachments/assets/f0eb083a-ac05-4271-a590-3fc39d0edd5e)

3. Mostarar contenedores

Con el comando sudo docker ps nos va a salir todos los conenedores que tenemos en el sistema

![image](https://github.com/user-attachments/assets/8c6b6eca-c2c3-4c24-b879-1e4cfbeac245)

Segunda parte:

1. Editar fichero

vamos a crear una carpeta para trabajar sobre ella con el comando mkdir

![image](https://github.com/user-attachments/assets/ad55bd82-d30f-4668-9160-9d9b165f6991)

Añadimos las lineas que estan en la imagen, impportante en el apartado de actualizar los paquetes escribir bien la palabra curl para que no de fallos.

![image](https://github.com/user-attachments/assets/8506f59b-9ab7-4dc0-9d08-84913aad0b32)

2. Construir contenedor

Para construir el contenedor, vamos a poner el siguiente comando en el terminal, en mi caso le e puesto el nombre de usuario/el nombre de la imagen con la ultima version

![image](https://github.com/user-attachments/assets/b2cdc0c3-7fb0-4eee-a47f-5eedbda64694)

3. Ejecutar contenedor

Ahora para ejecutarlo lo que tenemos que hacer poner el comando sudo docker run y el nombre completo del contenedor que hemos creado antes

![image](https://github.com/user-attachments/assets/bff3468e-43be-4b91-8a81-1cdb34134d90)

4. Cuenta hub.docker.com

Primero tenemos que hacer el login en docker con el comando que sale en la imagen, le vamos a dar al enlace de docker de la imagen, nos va a llevar a una pagina web, tambien necesitamos copiar el codigo de confirmacion que sale en el terminal 

![image](https://github.com/user-attachments/assets/fb2ec756-738b-4e8b-bf1e-ec466c724712)

Cuando estemos en la pagina web del enlace del terminal, como se explica en el anterior paso vamos a pegar el codigo de confirmacion y vamos a entrar con nuestros credenciales de docker. 

![image](https://github.com/user-attachments/assets/570479e8-4e06-443c-8491-04d7f7b2c3fa)

Después, es importante que la imagen tenga la etiqueta que incluya mi usuario de Docker Hub. Para ello con el comando que viene abajo le ponemos a la imagenes que hicimos el usuario nuestro y el nombre de la imagen que creamos al principio:

docker tag proyecto costel452/proyectodocker:1.0

![image](https://github.com/user-attachments/assets/5ea2e282-67f4-45bf-b220-e15e9dca1e95)

Ahora tocaria subirlo con el comando push que sale en la imagen

![image](https://github.com/user-attachments/assets/5105cc20-5750-4fa0-b48c-042f0c774809)

En la cuenta de hub.docker.com donde hemos creado nuestro proyecto si nos vamos a el y miramos los tag veremos como se a modificado

![image](https://github.com/user-attachments/assets/5f6c9945-5f30-4930-a3fb-b18c53a5209a)

cuenta de dockerhub
Nos saldra la pagina principal para registrarnos o iniciar sesion ya

![image](https://github.com/user-attachments/assets/aa375746-77a0-41a5-af8a-2b7348f3b9c0)

Este seria mi usuario

![image](https://github.com/user-attachments/assets/2eac31f8-2857-421c-af0f-b3c1602f40e1)

Ahora dentro de repositorios le vamos a dar a crear repositorio y le damos un nombre, lo dejamos en publico y listo

![image](https://github.com/user-attachments/assets/ff0a5ff8-30d0-4d57-a422-79881fd2d527)

Tarea 3:
Vamos con la siguiente tarea
![image](https://github.com/user-attachments/assets/0c76abdb-a0c6-4489-bf19-b20ef77bc810)

1. Descargar imagen Ubuntu

Para descargar ubuntu ponemso el comando de la imagen y listo, no deberia dar ningun error 

![image](https://github.com/user-attachments/assets/28eab7d7-37c6-4308-8d04-2af7653d05ef)

2. Descargar imagen hello-world

Repetimos el proceso pero cambiamos ubuntu por hello-world

![image](https://github.com/user-attachments/assets/b5b21acc-9348-4ee4-b26f-61dc1aef58fb)

3. Descargar imagen nginx

El mismo proceso pero con el nombre de nginx

![image](https://github.com/user-attachments/assets/4e420f14-1169-4fba-a9c7-a8d356fb704b)

4. Listado de imagenes

Con el comando que esta en la imagen nos va a salir toda la infomacion.

![image](https://github.com/user-attachments/assets/7f95d001-dab2-463d-9adf-0ee5fc7387d5)

5. Ejecutar y dar nombre a myhello1

Con el comando de la imagen lo vamos a ejecutar y dar nombre por los argumentos que le hemos metido, run para ejecutarlo y --name para darle nmbre y llamamos a la imagen que hemos descargado antes

![image](https://github.com/user-attachments/assets/c3f4a44b-6f3b-43f8-9950-530ec8f9ba4e)

6.  Ejecutar y dar nombre a myhello2

Mismo proceso que antes pero le cambiamos el nombre al que corresponde 

![image](https://github.com/user-attachments/assets/a36bec16-3976-48aa-8c53-c5a10b61e1ff)

7. Ejecutar y dar nombre a myhello3

Mismo proceso que antes pero le cambiamos el nombre al que corresponde 

![image](https://github.com/user-attachments/assets/c785f4a4-9498-49fa-b8a4-d75d87f924b8)

8. Contenedores en ejecucion

Con el comando que sale en la imagen se nos va a mostrar toda la lista

![image](https://github.com/user-attachments/assets/ee414c9a-a85f-4272-ad5d-4f632f5d56d2)

9. Parar contenedor myhello1 y 10. Parar contenedor myhello2

Para parar los contenedores vamos a poner stop y el nombre del comando

![image](https://github.com/user-attachments/assets/04384b30-8818-4cd3-96c8-42ab21cb9c53)

11. Borrar contenedor myhello1

Para borrar el contenedor vamos a poner la opcion rm mas el nombre del contenedor

![image](https://github.com/user-attachments/assets/333a8371-6dc2-4506-8309-5480ee8ebcfe)

12. Mostrar contenedores en ejecucion

Repetimos el comando del punto 8.

![image](https://github.com/user-attachments/assets/488add18-c631-4043-8b68-b3fabf11516e)

13. Borrar todos los contenedores

Ponemso el siguiente comando y si no hay equivocacion en pasos anteriores deberia bastar con eso
![image](https://github.com/user-attachments/assets/0e89267d-e591-4242-b218-67527ed6c8a8)

Tarea 4:

![image](https://github.com/user-attachments/assets/0117967c-3e97-4e0c-bffe-37d383e61dc7)

Ejemplo 1:
![image](https://github.com/user-attachments/assets/0cc2cebf-5234-4080-94ea-04743e9c6a32)
![image](https://github.com/user-attachments/assets/4f4bd287-c1b0-4eea-9b07-7c3a9822e45a)
![image](https://github.com/user-attachments/assets/d298ce44-3b1f-471a-9ba0-acfb255671d8)

Ejemplo 2:
![image](https://github.com/user-attachments/assets/ebfa9d59-681d-459d-985d-0d39c8db7133)
![image](https://github.com/user-attachments/assets/fd61b4ca-1997-4b4f-a9d3-cee26fc2b63d)

Tarea 5:

![image](https://github.com/user-attachments/assets/3ee09c0b-9313-43fd-854f-efff73866800)





