# Práctico: Git + Docker

Estas son las pruebas que hice para contenerizar una pequeña app desarrolla en .NET 8

## Cree el repositorio en GitHub
- Lo cree desde GitHub.com
- lo clone

```bash
git clone https://github.com/leoparolo/IngSoftwareISTEA.git
```

## Con la aplicación ya creada, cree el archivo Dockerfile (sin extensión)
- Aproveche e investigue un poco más, haciendo un Dockerfile que solamente copia los dll para ejecutar la app
- y también hice otro archivo Dockerfile que publica y ejecuta la app, evitando tener que descargar las herramientas de Microsoft .NET para compilarlo

## Finalmente, para conteneizar la app hice lo siguiente:

```bash
docker build -t helloworld .
```

- lo cree con el tag helloworld y le indico que el proyecto esta en la carpeta donde se encuentra actualmente

```bash
docker run --rm helloworld
```

- Con este comando ejecuto la app, para este caso (aplicación de consola) utilice --rm para que se elimine el contenedor luego de su ejecución, evitando que queden contenedores parados