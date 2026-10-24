---
title: "Lección 12 - Publica el sitio con GitHub Pages"
description: "Usa la aplicación GitHub Copilot para configurar un flujo de trabajo de Pages, revisar su solicitud de incorporación de cambios y comprobar el Space Quiz publicado."
authors:
  - jamesmontemagno
lastUpdated: 2026-10-12
---

Publica el Space Quiz en GitHub Pages para que cualquiera pueda acceder a él. Copilot puede preparar el flujo de trabajo y guiarte durante la publicación, pero sigues siendo responsable de revisar los cambios y confirmar que el sitio está disponible.

En esta lección:

- pide a Copilot que configure la publicación en GitHub Pages.
- revisa el flujo de trabajo y la solicitud de incorporación de cambios antes de combinarla.
- sigue la publicación y comprueba el sitio publicado.

## Escenario

El Space Quiz ya está en un repositorio de GitHub, pero aún hace falta una forma sencilla de probarlo. Publicar el sitio de un solo archivo con GitHub Pages lo hace accesible desde una URL pública sin añadir un servidor ni dependencias de ejecución.

## Pide a Copilot que publique el sitio

En la sesión de la aplicación Copilot para `space-quiz`, envía este prompt:

```plaintext
Enable GitHub Pages for this repository. Create a GitHub Actions workflow that builds the website if needed and deploys it to GitHub Pages. Add a README describing the app and how to run it locally if one does not already exist. Create a pull request with these changes and merge it after required checks pass. Monitor the deployment until it succeeds, then report the final URL of the live website. If you lack permission to enable Pages or merge, tell me exactly what I need to approve or do; do not report success until the site is live.
```

![Diagrama de tres etapas: una solicitud de incorporación de cambios de space-quiz combinada; una ejecución correcta de GitHub Actions Deploy website con los pasos Build website, Upload artifact y Deploy to Pages; y el Space Quiz publicado en yourname.github.io/space-quiz/.](../../../_images/first-steps-app-pages-deploy.svg)

> [!WARNING]
> Este prompt pide al agente que cree y combine una solicitud de incorporación de cambios y cambie la configuración de Pages del repositorio. Antes de continuar, revisa el diff, los permisos de publicación y cualquier solicitud de aprobación de GitHub.

## Revisa el flujo de trabajo y comprueba la publicación

1. Confirma que el README solo se añade si el repositorio aún no tiene uno.
2. Revisa los cambios de la solicitud de incorporación de cambios, incluidos los pasos de compilación y publicación del flujo de trabajo.
3. Combina los cambios únicamente después de que se superen las comprobaciones obligatorias de la solicitud de incorporación de cambios.
4. Sigue la ejecución de publicación de GitHub Actions hasta que termine correctamente.
5. Abre la URL indicada y confirma que se carga el Space Quiz.

Si el agente no puede habilitar Pages o combinar la solicitud de incorporación de cambios, sigue las instrucciones concretas que te proporcione. No des la tarea por terminada hasta que la publicación finalice correctamente y el sitio esté disponible.

## Resumen y siguientes pasos

El Space Quiz ya está disponible como sitio publicado y has comprobado la publicación en lugar de confiar únicamente en el informe del agente. Continúa con la [Lección 13: Repaso y siguientes pasos][next-lesson].

[next-lesson]: ../13-review/
