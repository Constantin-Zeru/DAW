Vamos a actualizar los paquetes de apache antes de instalarlo para tenerlos todos actualizados

![image](https://github.com/user-attachments/assets/e2f5c111-34c9-46eb-a918-04f7f25aa68e)

Una vez echo eso vamos a instalar apache con el siguiente comando

![image](https://github.com/user-attachments/assets/c5b4d794-c2cc-4515-8a88-5b343ea04e59)

cuando se a instalado apache y no a dado ningun problema la descarga vamos a iniciar apache y 
lo vamos a se utilizar para configurar el servicio de Apache para que se inicie automáticamente cada vez que el sistema arranque.

![image](https://github.com/user-attachments/assets/51b35c8d-d1af-413d-b79f-b20e1e16aeee)

Vamos a instalar la base de datos de mysql, con este comando

![image](https://github.com/user-attachments/assets/18465fc7-255f-4cea-ab5f-12229fd1c1f0)

Una vez que se a instalado bien vamos a iniciar y establer el mysql como con apache 

![image](https://github.com/user-attachments/assets/a8f3255c-eff8-4140-a456-6412ccafa7e2)

Vamos a abirir la base de datos con el siguiente comando

![image](https://github.com/user-attachments/assets/7534cab8-9b6f-4b5c-86d1-6e262ac59e8e)

Una vez que la tenemos abierta vamos a crear la base de datos de los usuarios, el admin
y las diferentes tablas 

![image](https://github.com/user-attachments/assets/f69a3404-4dd3-4bea-ac00-9c25865637fc)

instalar el paquete libaprutil1-dbd-mysql, que es una biblioteca necesaria para que el servidor Apache pueda conectarse y autenticarse usando una base de datos MySQL.

![image](https://github.com/user-attachments/assets/518c3f26-5484-4864-9043-254f93f3e76a)

Vamos a configurar el archivo de configuracion de apache 
![image](https://github.com/user-attachments/assets/c1fa1443-1aa1-4203-a807-52e81b5524ab)

Cuando se abra vamos a añadir al final del archivo las siguientes lineas donde le vamos a pasar la nombre de la base de datos,
el usuario y la contraseña, y un select para que coja el usuario y la contraseña

![image](https://github.com/user-attachments/assets/2fb70d0c-2938-4e9a-b9c9-b83d75102332)

Vamos a editar el archivo del sitio predeterminado:

![image](https://github.com/user-attachments/assets/0a550c31-b5dc-42cd-84f3-231a52d8b050)

Vamos a agregar en el bloque del Virtual Host las siguientes lineas

![image](https://github.com/user-attachments/assets/d1fd4afa-479f-40f7-b291-b229708cc97e)

Una vez hemos echo eso, vamos a craer con mkdir el directorio donde va a estar el index.html

![image](https://github.com/user-attachments/assets/85d1096d-a6e9-4c32-a555-dcc424c65b73)

Por temas de permisos vamos a utilizar la funcionalidad touch para darle permisos elevados al directorio,

![image](https://github.com/user-attachments/assets/fd8e76ff-6be6-4400-a3fd-fdf9c3cd0cd2)

Abrimos el archivo index.html 
![image](https://github.com/user-attachments/assets/a7ed77a9-5b91-4cb6-849f-3e5ef5e4d626)

![image](https://github.com/user-attachments/assets/6e11fc62-706c-4432-adf9-b2e282a66975)

Y le damos un mensaje de bienvenida o informativo

![image](https://github.com/user-attachments/assets/3e028f38-d0e6-43dd-948b-0cd096e0d306)

Reiniciamos el apache para aplicar los cambios 
![image](https://github.com/user-attachments/assets/b5263d96-7ee8-4efd-96ab-6893c7c6cbf4)

Habilitamos el modulo ssl con el siguiente comando

![image](https://github.com/user-attachments/assets/9c633b7d-d4e2-46cb-8776-26700577d956)

Y reiniciamos el apache para guardar los cambios

![image](https://github.com/user-attachments/assets/417233ac-0a6b-4acd-8880-ebd43b517cc4)

Una vez que eso esta echo, vamos a crear el certificado SSL autofirmado

![image](https://github.com/user-attachments/assets/9f135a78-69d6-4046-bcf9-83273de0c7fa)

Completamos los campos que hagan falta o algunos los podemos dejar en blanco que no nos va a dar error

![image](https://github.com/user-attachments/assets/cabc3bb3-f98c-4d27-be65-253dd64f5e7f)

Editamos el archivo SSL

![image](https://github.com/user-attachments/assets/2f0ffaef-0da3-4334-bf08-a7ccb4853282)

Incluimos las rutas de los certificados

![image](https://github.com/user-attachments/assets/9c735e8e-2d4d-4089-b720-98d43ddb2c7a)

Habilitamos el sitio SSL

![image](https://github.com/user-attachments/assets/bacccf7f-d4b9-414b-bda5-6fb5ead6ab8b)

![image](https://github.com/user-attachments/assets/19897122-8676-4dc4-8e8f-1e8ad0727619)

Utilizamos el siguiente comando sudo systemctl reload apache2 para recargar la configuración de Apache sin detener el servicio completamente.

![image](https://github.com/user-attachments/assets/43269691-27c6-4d99-befb-e57999bf0f39)

Con la ip de nuestra instancia/protegido que es la carpeta que hemos creado antes en la barra de busqueda si todo lo hemos echi bien nos va a pedir autentificarnos con el usuario y la contraseña
![image](https://github.com/user-attachments/assets/b37d6bc7-6f17-42d5-974d-be8e0bba6197)

![image](https://github.com/user-attachments/assets/b7aa660b-8549-42b3-ba9a-5861707626e8)




























