# Variables de Entorno
### ¿Qué son las variables de entorno
las variables de entorno son variables disponibles para tu programa/aplicación de forma dinámica durante el tiempo de ejecución. El valor de estas variables puede proceder de diversas fuentes: archivos de texto, gestores secretos de terceros, scripts de llamada, etc.

# COMPLETAR

### Para crear un contenedor con variables de entorno?

```
docker run -d --name <nombre contenedor> -e <nombre variable1>=<valor1> -e <nombre variable2>=<valor2>
```

### Crear un contenedor a partir de la imagen de nginx:alpine con las siguientes variables de entorno: username y role. Para la variable de entorno rol asignar el valor admin.

# COMPLETAR
![image](https://github.com/user-attachments/assets/52d48169-8770-4c95-858b-cf08dc738b64)


# CAPTURA CON LA COMPROBACIÓN DE LA CREACIÓN DE LAS VARIABLES DE ENTORNO DEL CONTENEDOR ANTERIOR
![image](https://github.com/user-attachments/assets/ab39c757-cf09-443d-b41a-bafc91fc7444)

### Crear un contenedor con mysql:8 , mapear todos los puertos
# COMPLETAR
![image](https://github.com/user-attachments/assets/853a24b9-97ef-4860-8ec9-01fd605e2450)


### ¿El contenedor se está ejecutando?
SI
![image](https://github.com/user-attachments/assets/d8d92404-ce7e-4781-8ce5-0a27734e72a8)

# COMPLETAR

### Identificar el problema
# COMPLETAR

### Eliminar el contenedor creado con mysql:8 
# COMPLETAR
![image](https://github.com/user-attachments/assets/5f73788a-8b86-462f-a9c5-c7deecb8cbb0)


### Para crear un contenedor con variables de entorno especificadas
- Portabilidad: Las aplicaciones se vuelven más portátiles y pueden ser desplegadas en diferentes entornos (desarrollo, pruebas, producción) simplemente cambiando el archivo de variables de entorno.
- Centralización: Todas las configuraciones importantes se centralizan en un solo lugar, lo que facilita la gestión y auditoría de las configuraciones.
- Consistencia: Asegura que todos los miembros del equipo de desarrollo o los entornos de despliegue utilicen las mismas configuraciones.
- Evitar Exposición en el Código: Mantener variables sensibles como contraseñas, claves API, y tokens fuera del código fuente reduce el riesgo de exposición accidental a través del control de versiones.
- Control de Acceso: Los archivos de variables de entorno pueden ser gestionados con permisos específicos, limitando quién puede ver o modificar la configuración sensible.

Previo a esto es necesario crear el archivo y colocar las variables en un archivo, **.env** se ha convertido en una convención estándar, pero también es posible usar cualquier extensión como **.txt**.
```
docker run -d --name <nombre contenedor> --env-file=<nombreArchivo>.<extensión> <nombre imagen>
```
**Considerar**
Es necesario especificar la ruta absoluta del archivo si este se encuentra en una ubicación diferente a la que estás ejecutando el comando docker run.

### Crear un contenedor con mysql:8 , mapear todos los puertos y configurar las variables de entorno mediante un archivo
# COMPLETAR
![image](https://github.com/user-attachments/assets/d4d7eb91-7e64-4901-9aea-15191f4794ad)

# CAPTURA CON LA COMPROBACIÓN DE LA CREACIÓN DE LAS VARIABLES DE ENTORNO DEL CONTENEDOR ANTERIOR 
![image](https://github.com/user-attachments/assets/d5c9b838-4619-4169-8155-46effe03c32a)


### ¿Qué bases de datos existen en el contenedor creado?
![image](https://github.com/user-attachments/assets/363dd257-01b0-4607-8a8a-7f6e581375fe)

# COMPLETAR
