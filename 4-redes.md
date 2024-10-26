# Redes
Las redes son un componente fundamental que permite la comunicación entre contenedores, así como la comunicación de los contenedores con el mundo exterior. 
![Imagen](img/redes.PNG)
- Bridge: Esta es la red por defecto en Docker. Permite la comunicación entre contenedores en el mismo host. Cada contenedor conectado a la red bridge tiene una IP propia en la subred de la red bridge.
    -  Brige por default: Cuando se ejecuta un contenedor, Docker crea automáticamente una red de tipo bridge por default. Esta red se utiliza para permitir la comunicación entre contenedores en el mismo host. Cada contenedor conectado a esta red obtiene su propia dirección IP en la subred de la red bridge.
    - Bridge creada por nosotros: Un usuario también puede crear sus propias redes de tipo bridge en Docker. Esto puede ser útil para organizar y segmentar los contenedores de una aplicación de manera más controlada. Al crear una red bridge personalizada, se puede especificar un rango de direcciones IP y otras configuraciones de red específicas. Los contenedores conectados a esta red utilizarán las direcciones IP de la subred definida por el usuario.
- Host: Con esta red, los contenedores comparten la red del host en lugar de tener su propia interfaz de red. Esto puede mejorar el rendimiento de red, pero los contenedores pueden entrar en conflicto con los puertos del host si intentan utilizar los mismos puertos.
- None: Con esta red, se deshabilita la configuración de red. Los contenedores que usan esta red tienen su propia red de bucle invertido y no pueden comunicarse con otros contenedores a menos que se conecten explícitamente a una red.

### Crear una red de tipo bridge

```
docker network create <nombre red> -d bridge
```
![image](https://github.com/user-attachments/assets/271a5743-6c31-437c-808f-2c7500fd59fb)

### Crear un contenedor vinculado a una red

```
docker run -d --name <nombre contenedor> --network <nombre red> <nombre imagen>
```
![image](https://github.com/user-attachments/assets/9ba3f5d9-f3c4-4303-95c4-833775304f6a)

### Para saber a qué red está conectado un contenedor

```
docker inspect <nombre contenedor>
```
ó
```
docker network inspect <nombre red> 
```
![image](https://github.com/user-attachments/assets/6d2b2738-93b8-458b-b154-6e19af2b83a9)

### Vincular contenedor a una red
```
docker network connect <nombre red> <nombre contenedor>
```
![image](https://github.com/user-attachments/assets/ef8b4864-895b-403b-a268-d1308de4ab8b)


### Para desvincular un contenedor de una red
```
docker network disconnect <nombre red> <nombre contenedor>
```

### Para listar las redes existentes
```
docker network ls
```
![image](https://github.com/user-attachments/assets/f88e67be-4428-4bcf-9856-80d19245b34a)

### Crear los contenedores y las redes que se presentan en el esquema. Usar para todos los contenedores la imagen de nginx:alpine

![Imagen](img/esquema-ejercicio-redes.PNG)


![image](https://github.com/user-attachments/assets/c69951a2-1e93-43f1-b85d-3b33184b1a67)

# COLOCAR UNA CAPTURA DE LAS REDES EXISTENTES CREADAS
![image](https://github.com/user-attachments/assets/5b4bcec8-b288-4cf7-9913-0982f5e3f5a0)


# COLOCAR UNA(S) CAPTURAS(S) DE LOS CONTENEDORES CREADOS EN DONDE SE EVIDENCIE A QUÉ RED ESTÁN VINCULADOS
![image](https://github.com/user-attachments/assets/97b30bc2-e46f-488e-b672-0ff621f39dbb)

![image](https://github.com/user-attachments/assets/f218f679-7579-4dfd-b250-7d4bbe82e1db)


### Para eliminar las redes creadas
```
docker network rm <nombre de la red>
```
![image](https://github.com/user-attachments/assets/9d813894-23d9-4ec0-93a4-8fbbc986f0f9)

