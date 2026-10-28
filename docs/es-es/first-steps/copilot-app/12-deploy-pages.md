---
title: "Lección 12 - Publica el sitio con GitHub Pages"
description: "Usa la aplicación GitHub Copilot para configurar un flujo de trabajo de Pages, revisar su solicitud de incorporación de cambios y comprobar el Space Quiz publicado."
authors:
  - jamesmontemagno
lastUpdated: 2026-10-12
---

Ofrece al Space Quiz un hogar público con GitHub Pages. Copilot puede preparar el flujo de trabajo y guiarte durante la publicación, pero debes revisar los cambios y confirmar que el sitio está disponible.

En esta lección vas a:

- pedir a Copilot que configure la publicación en GitHub Pages;
- revisar el flujo de trabajo y la solicitud de incorporación de cambios antes de fusionarla;
- seguir la publicación y comprobar el sitio publicado.

## Escenario

El Space Quiz ya está en un repositorio de GitHub, pero la gente todavía necesita una forma sencilla de probarlo. Publicar el sitio de un solo archivo con GitHub Pages lo hace accesible desde una URL pública sin añadir un servidor ni una dependencia del entorno de ejecución.

## Pide a Copilot que publique el sitio

En la sesión de la aplicación Copilot para `space-quiz`, envía este prompt:

```plaintext
Activa GitHub Pages para este repositorio. Crea un flujo de trabajo de GitHub Actions que compile el sitio web si es necesario y lo publique en GitHub Pages. Añade un README que describa la aplicación y cómo ejecutarla localmente si todavía no existe. Crea una solicitud de incorporación de cambios con estos cambios y fusiónala cuando se superen las comprobaciones obligatorias. Supervisa la publicación hasta que finalice correctamente y, después, indica la URL final del sitio web activo. Si no tienes permiso para activar Pages o fusionar la solicitud, dime exactamente qué debo aprobar o hacer; no informes de que la publicación se ha completado hasta que el sitio esté disponible.
```

![Diagrama de tres fases: una solicitud de incorporación de cambios de space-quiz fusionada; una ejecución correcta de GitHub Actions Deploy website con los pasos Build website, Upload artifact y Deploy to Pages; y el Space Quiz activo en yourname.github.io/space-quiz/.](../../../_images/first-steps-app-pages-deploy.svg)

> [!WARNING]
> Este prompt pide al agente que cree y fusione una solicitud de incorporación de cambios y cambie la configuración de Pages del repositorio. Revisa las diferencias, los permisos de publicación y cualquier solicitud de aprobación de GitHub antes de continuar.

## Revisa el flujo de trabajo y comprueba la publicación

1. Confirma que el README solo se añade si el repositorio todavía no tiene uno.
2. Revisa los cambios de la solicitud de incorporación de cambios, incluidos los pasos de compilación y publicación del flujo de trabajo.
3. Fusiona los cambios solo después de que se superen las comprobaciones obligatorias de la solicitud.
4. Sigue la ejecución de publicación de GitHub Actions hasta que finalice correctamente.
5. Abre la URL indicada y confirma que se carga el Space Quiz.

Si el agente no puede activar Pages o fusionar la solicitud de incorporación de cambios, sigue las instrucciones concretas que te proporcione. No des la tarea por terminada hasta que la publicación finalice correctamente y el sitio activo se cargue.

## Resumen y siguientes pasos

El Space Quiz ya está disponible como sitio activo y has comprobado la publicación en lugar de confiar únicamente en el informe del agente. Continúa con la [Lección 13: Revisión y siguientes pasos][next-lesson].

[next-lesson]: ../13-review/
