- 1º trimestre

### Instalación del servidor web apache. Usaremos dos dominios mediante el archivo hosts: centro.intranet y departamentos.centro.intranet. El primero servirá el contenido mediante wordpress y el segundo una aplicación en python

Instalamos Apache desde el terminal con el comando que aparece en la imagen:

![](https://github.com/user-attachments/assets/8a8dba05-47c7-4485-8ba9-c5382c5b5e4b)

Lo habilitamos con sudo systemctl enable apache2

![](https://github.com/user-attachments/assets/ca10f7fb-bd15-4ff1-a969-fffa0786bd5e)

Comprobamos que esta instalado con el localhost

![](https://github.com/user-attachments/assets/e888712a-8742-4515-91a9-44b097c3c1f6)

abrimos el archivo hosts con nano para configurar los hosts virtuales
![](https://github.com/user-attachments/assets/ebcb2414-7a73-483e-9591-c9c34c46c04a)





