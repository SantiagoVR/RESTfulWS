# RESTfulWS
Aplicación web de Java Enterprise Edition con Spring Framework MVC para crear RESTful Web Services basado en patrones de diseño corporativos y modelos para asegurar la escalabilidad y usabilidad de los Web Services.

**1. Instalación**
  
**Clonar el repositorio** 

   git clone https://github.com/SantiagoVR/RESTfulWS.git

   o Descargar el proyecto en archivo zip
  
**Importar a Eclipse**  

   1. Clic en `File -> Import -> Existing Projects into Workspace`.
   2. Selecciona la carpeta donde se encuentra la carpeta del proyecto si se descargo el proyecto en un archivo zip primero se tendrá que descomprimir.
   3. Correr `Run As-> Maven install`.

**Exportar .war**
   
   1. Clic derecho al proyecto en Eclipse.  
   2. Selecciona `Export -> WAR file`.

**Desplegar el archivo .war**
   
  Ya que se tenga el archivo WAR
     
   1. Tener instalado Apache Tomcat.
   2. Iniciar Tomcat e ir a la página `http://localhost:8080`.
   3. Presionar `Manager App`.
   4. Escribir el usuario y contraseña correctos.
   5. Buscar la sección **Desplegar**, Presionar `Choose File` y seleccionar el archivo WAR del proyecto.
   6. Presionar `Desplegar`.
   7. Revisar el proyecto en la sección **Aplicaciones** y buscar el nombre del archivo WAR.
   8. Observar el funcionamiento del proyecto.

**2. Uso**
  
  **Index**
  
  **api/v1/**  
   1. **GET**: Listar los recursos disponibles en el api.

  **File**
  
  **api/v1/file**  
   1. **GET**: Descarga un archivo con el path. 
        ```
        api/v1/file/?path=
        ```
   2. **POST**: Sube un archivo con name, dir y file.
        ```
        api/v1/file/ name="imagen.jpg" dir="/Files" file@/Users/User/Downloads/imagen.jpg --form
        ```
   3. **DELETE**: Elimina un archivo con path.
        ```
        api/v1/file/?path=
        ```
  **Directory**     
  
  **api/v1/directory**  
   1. **GET**: Listar archivos contenidos en un directorio con **dir**. 
        ```
        api/v1/directory/?dir=
        ```
  **Notify** 
  
  **api/v1/notify**  
   1. **GET**: Lista las notificaciones.
   2. **POST**: Crear notificación con subject, message, toAddress y ccAddress.
        ```
        api/v1/notify subject="hello" message="Hello from Spring" toAddress="ejemplo@mail.com" ccAddress="ejemplo@mail.com"
        ```
  **User**    
  
  **api/v1/user**  
   1. **GET**: Lista los usuarios.
   2. **POST**: Crear un usuario con username, password y fullName.
        ```
        api/v1/user username="user" password="pass" fullName="Emmanuel"
        ```
  **api/v1/user/{username}**  
   1. **GET**: Muestra la información del usuario.
   2. **PUT**: Actualiza la información del usuario con username, password y fullName.
        ```
        api/v1/user/user username="user" password="pass" fullName="Emmanuel"
        ```
   3. **DELETE**: Elimina al usuario.

**3. Créditos**
 Desarrollado por: Emmanuel Santiago Vilchis Reyes
 Matricula:  2742546
  
**4. Licencia** 
