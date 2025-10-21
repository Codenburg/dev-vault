---
title: Docker Volúmenes
date: 20251020
tags: [concept, docker, devops]
status: evergreen
related: [Docker Compose]
---
# Docker Volúmenes

## Explicación
Los volúmenes en Docker permiten persistir datos fuera del ciclo de vida del contenedor.  
Evitan la pérdida de información al reiniciar o reconstruir imágenes.  
Existen dos tipos principales: **bind mounts** (rutas locales) y **named volumes** (gestionados por Docker).

## Ejemplo
```yaml
services:
  db:
    image: postgres
    volumes:
      - db_data:/var/lib/postgresql/data

volumes:
  db_data:
  ```
## Aplicación
Usados para bases de datos, configuraciones persistentes y almacenamiento temporal entre servicios.

## Referencias
Documentación oficial de Docker Volumes

[Docker Compose Basics](https://docs.docker.com/compose/gettingstarted/)
