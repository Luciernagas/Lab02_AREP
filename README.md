## DISEÑO Y ESTRUCTURACIÓN DE APLICACIONES DISTRIBUIDAS EN INTERNET

En el siguiente proyecto se realizó la construcción de un servidor web que soporta múlltiples solicitudes seguidas (no concurrentes). El servidor lee archivos del disco local y retorna todos los archivos solicitados, incluyendo páginas html, archivos java script, css e imágenes.

* * *
### Prerrequisitos
Se debe tener instalado java, maven y git.
* Descargar maven en  http://maven.apache.org/download.html
* Descargar git en https://git-scm.com/book/en/v2/Getting-Started-Installing-Git
  
* * *
### Instalando
Se debe clonar el proyecto con el comando:
~~~
git clone https://github.com/Luciernagas/Lab02_AREP.git
~~~
En la terminal se debe ingresar el siguiente comando para compilar y empaquetar el proyecto:
~~~
mvn package
~~~
Finalmente para ejecutar el programa se debe ingresar el siguiente comando:
~~~
java -cp "./target/classes" org.example.laboratorio.HttpServer
~~~
Cuando en la terminal veamos el mensaje "Listo para recibir ..." ingresamos mediante nuestro browser a la siguiente ruta:
```
localhost:35000/(el archivo o imagen que desea visualizar con su extensión correspondiente)
```

Los archivos disponibles en el disco local se encuentran en la ruta /src/main/resources, se encontrará 2 carpetas, images que contiene los archivos tipo imagen (jpg, png y gif) y www en donde se encontraran los archivos html, js y css, se tiene 2 archivos para la prueba de los html (index.html y page2.html) y por otro lado un archivo html en donde se probaban una página creada con JavaScript y css.

* * *
### Ejecutando pruebas
En la sección de pruebas se confirmará el correcto funcionamiento del servidor web:
1. Archivos .html
![image](https://github.com/Luciernagas/Lab02_AREP/assets/104604359/b48446be-2a21-4440-a84b-1d1556340e20)
![image](https://github.com/Luciernagas/Lab02_AREP/assets/104604359/c6e9893b-4f62-42a4-aef2-8ab80eba430c)

2. Imagenes .png , .jpg. , .gif
![image](https://github.com/Luciernagas/Lab02_AREP/assets/104604359/dc42d72f-afb8-4e20-ad40-dcfa5a284498)
![image](https://github.com/Luciernagas/Lab02_AREP/assets/104604359/d79e13d9-7aad-4335-9588-4936fbed0fd3)
![image](https://github.com/Luciernagas/Lab02_AREP/assets/104604359/b7491f05-d809-489a-8f05-747867d54804)

3. Archivos .js .css
![image](https://github.com/Luciernagas/Lab02_AREP/assets/104604359/a8c9b3d7-b9d0-4bf9-9214-ec76cc10a1f9)
![image](https://github.com/Luciernagas/Lab02_AREP/assets/104604359/382a5c07-4f52-407d-9692-e898945aa5b8)


* * *
### Arquitectura del prototipo
El prototipo presentado es un servidor HTTP que utiliza sockets para recibir conexiones, procesa solicitudes y genera respuestas en función de las rutas solicitadas, en mi concepto su arquitectura está dada por:
* La configuración de un ServerSocket en el puerto 35000 para que los usuarios logren una conexión con el servidor.
* El análisis las solicitudes HTTP recibidas en donde se identifica la ruta solicitada y el método HTTP utilizado.
* Basarse en la solicitud y la ruta para generar respuestas adecuadas (archivos .html, .js, .css, .jpg, .png o .gif).

* * *
### Construido con
* Maven - Gestión de dependencias

* * *
### Autores
♡ Luisa Valentina De la hoz Rocha ♡

* * *
### Licencia
Este proyecto esta autorizado bajo la licencia que se puede encontar en el archivo LICENSE.txt, en el se pueden encontrar los detalles
