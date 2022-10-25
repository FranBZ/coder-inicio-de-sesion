# coder-inicio-de-sesion

## Consigna: 
Implementar sobre el entregable que venimos realizando un mecanismo de
autenticación. Para ello:
- Se incluirá una vista de registro, en donde se pidan email y contraseña. Estos datos
se persistirán usando MongoDb, en una (nueva) colección de usuarios, cuidando
que la contraseña quede encriptada (sugerencia: usar la librería bcrypt).
- Una vista de login, donde se pida email y contraseña, y que realice la autenticación
del lado del servidor a través de una estrategia de passport local.
- Cada una de las vistas (logueo - registro) deberá tener un botón para ser redirigido a
la otra.
- Una vez logueado el usuario, se lo redirigirá al inicio, el cual ahora mostrará también
su email, y un botón para desolguearse.
- Además, se activará un espacio de sesión controlado por la sesión de passport.
Esta estará activa por 10 minutos y en cada acceso se recargará este tiempo.
- Agregar también vistas de error para login (credenciales no válidas) y registro
(usuario ya registrado).
- El resto de la funciones, deben quedar tal cual estaban el proyecto original.

<sup>Formato de entrega: link a un repositorio en Github con los tres proyectos en
carpetas separadas. No incluir los node_modules.</sup>

# Como ejecutar el proyecto
### En tu pc
- Antes que nada debes tener instalado en tu pc node.js
- Debes clonar el repositorio
- Abrir una terminal y en ella dirigirte a la carpeta con el nombre del proyecto
- Ejecutar el comando ``` npm install ```
- Deves configurar un archivo ``` .env ``` con los siguientes datos
    ```
    MONGO_USER = "<usuario de mongo atlas>"
    MONGO_PASS = "<contraseña de mongo atlas>"
    ```
- Una vez finalizado el punto anterior, ejecutar el comando ``` npm run start ```
- Luego dirigite en tu navegador de preferencia a [esta ruta](http://localhost:8080/api/productos-test) 
para testear la app