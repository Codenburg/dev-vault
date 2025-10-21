---

---
---
title: Docker Compose Hot Reload  
date: 2025-10-2025  
tags: #practice #docker #node]

---
# Docker Compose Hot Reload

## Propósito

Implementar hot reload en un entorno Node.js dentro de contenedor Docker.

## Pasos

1. Crear `docker-compose.yml` con bind mount hacia el código fuente.
    
2. Añadir `nodemon` al proyecto.
    
3. Ejecutar `docker compose up` y verificar recarga automática.
    

## Resultado

El servidor Node se recarga al modificar archivos locales sin reconstruir la imagen.

## Lección

Los **bind mounts** permiten desarrollo activo, pero no deben usarse en entornos de producción.