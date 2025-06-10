# Imagen base: SDK completo
FROM mcr.microsoft.com/dotnet/sdk:8.0 AS build

# Directorio de trabajo
WORKDIR /src

# Copiar todo el proyecto
COPY . .

# Restaurar dependencias (opcional)
RUN dotnet restore

# Publicar la app
RUN dotnet publish -c Release -o /app/out

# Imagen final, Runtime solamente (para achicar la imagen):
FROM mcr.microsoft.com/dotnet/runtime:8.0 AS runtime

WORKDIR /app

COPY --from=build /app/out ./

ENTRYPOINT ["dotnet", "HelloWorld.dll"]