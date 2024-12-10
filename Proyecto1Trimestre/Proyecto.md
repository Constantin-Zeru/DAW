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





