## Esquema para el ejercicio
![Imagen](img/esquema-ejercicio5.PNG)

### Crear la red
![image](https://github.com/user-attachments/assets/d9b0097a-4c36-4887-a97f-27a0c79b9fc6)

# COMPLETAR

### Crear el contenedor mysql a partir de la imagen mysql:8, configurar las variables de entorno necesarias
![image](https://github.com/user-attachments/assets/9f369d50-f7a9-445f-83c6-bfcb016dc87a)

# COMPLETAR

### Crear el contenedor wordpress a partir de la imagen: wordpress, configurar las variables de entorno necesarias
![image](https://github.com/user-attachments/assets/96c275a5-6dbd-4d93-9a30-e83462785960)

# COMPLETAR

De acuerdo con el trabajo realizado, en la el esquema de ejercicio el puerto a es **80**

Ingresar desde el navegador al wordpress y finalizar la configuración de instalación.
![image](https://github.com/user-attachments/assets/d01865b8-030a-441a-a249-6a0301fb1d73)
![image](https://github.com/user-attachments/assets/15ec69ec-91a4-4980-a52a-cd2e40e4d738)


# COLOCAR UNA CAPTURA DE LA CONFIGURACIÓN

Desde el panel de admin: cambiar el tema y crear una nueva publicación.
Ingresar a: http://localhost:9300/ 
recordar que a es el puerto que usó para el mapeo con wordpress
# COLOCAR UNA CAPTURA DEL SITO EN DONDE SEA VISIBLE LA PUBLICACIÓN.
![image](https://github.com/user-attachments/assets/56075fab-0086-4948-ba43-87a42740ecb1)

### Eliminar el contenedor wordpress
# COMPLETAR
![image](https://github.com/user-attachments/assets/84f0540a-f9dc-4572-9ef4-5b6e3d0860c2)

### Crear nuevamente el contenedor wordpress
Ingresar a: http://localhost:9300/ 
recordar que a es el puerto que usó para el mapeo con wordpress

### ¿Qué ha sucedido, qué puede observar?
Localhost rechaza la conexion debido a que el puerto en el cual se creó *wordpress* es el 80, y al tratar de ingresar al 9300 no lo permite.
![image](https://github.com/user-attachments/assets/c08a22a6-6dc4-4ec3-aad6-eb1a2c884fc9)

# COMPLETAR





