Práctico: Git + Docker

Estas son las pruebas que hice para contenerizar una pequeña app desarrolla en .NET 8

1) Cree el repositorio en GitHub
 a) Lo cree desde GitHub.com
 b) lo clone | git clone https://github.com/leoparolo/IngSoftwareISTEA.git
2) Con la aplicación ya creada, cree el archivo Dockerfile (sin extensión)
 a) Aproveche e investigue un poco más, haciendo un Dockerfile que solamente copia los dll para ejecutar la app
 b) y también hice otro archivo Dockerfile que publica y ejecuta la app, evitando tener que descargar las herramientas de Microsoft .NET para compilarlo
3) Finalmente, para conteneizar la app hice lo siguiente:
 a) docker build -t helloworld .
lo cree con el tag helloworld y le indico que el proyecto esta en la carpeta donde se encuentra actualmente
 b) docker run --rm helloworld
Con este comando ejecuto la app, para este caso (aplicación de consola) utilice --rm para que se elimine el contenedor luego de su ejecución, evitando que queden contenedores parados