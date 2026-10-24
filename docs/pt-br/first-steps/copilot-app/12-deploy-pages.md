---
title: "Lição 12 - Publique o site com o GitHub Pages"
description: "Use o app do GitHub Copilot para configurar um fluxo de trabalho do Pages, revisar o pull request e verificar o Space Quiz publicado."
authors:
  - jamesmontemagno
lastUpdated: 2026-10-12
---

Publique o Space Quiz no GitHub Pages para que todos possam acessá-lo. O Copilot pode preparar o fluxo de trabalho e orientar a publicação, mas você continua responsável por revisar as alterações e confirmar que o site está no ar.

Nesta lição, você vai:

- pedir ao Copilot para configurar a publicação no GitHub Pages.
- revisar o fluxo de trabalho e o pull request antes de mesclá-lo.
- acompanhar a publicação e verificar o site publicado.

## Cenário

O Space Quiz já está em um repositório do GitHub, mas ainda é necessário oferecer uma maneira simples de testá-lo. Publicar o site de arquivo único com o GitHub Pages o torna acessível por uma URL pública sem adicionar um servidor ou uma dependência de runtime.

## Peça ao Copilot para publicar o site

Na sessão do app do Copilot para `space-quiz`, envie este prompt:

```plaintext
Enable GitHub Pages for this repository. Create a GitHub Actions workflow that builds the website if needed and deploys it to GitHub Pages. Add a README describing the app and how to run it locally if one does not already exist. Create a pull request with these changes and merge it after required checks pass. Monitor the deployment until it succeeds, then report the final URL of the live website. If you lack permission to enable Pages or merge, tell me exactly what I need to approve or do; do not report success until the site is live.
```

![Diagrama em três etapas: pull request do space-quiz mesclado; execução bem-sucedida do Deploy website do GitHub Actions com as etapas Build website, Upload artifact e Deploy to Pages; e Space Quiz publicado em yourname.github.io/space-quiz/.](../../../_images/first-steps-app-pages-deploy.svg)

> [!WARNING]
> Este prompt pede ao agente para criar e mesclar um pull request e alterar as configurações de Pages do repositório. Antes de continuar, revise o diff, as permissões de publicação e qualquer solicitação de aprovação do GitHub.

## Revise o fluxo de trabalho e verifique a publicação

1. Confirme se o README só foi adicionado caso ainda não existisse no repositório.
2. Revise as alterações do pull request, incluindo as etapas de build e publicação do fluxo de trabalho.
3. Faça a mesclagem somente depois que as verificações obrigatórias do pull request forem aprovadas.
4. Acompanhe a execução de publicação do GitHub Actions até que seja concluída com sucesso.
5. Abra a URL informada e confirme que o Space Quiz carrega.

Se o agente não puder habilitar o Pages ou mesclar o pull request, siga as instruções específicas que ele fornecer. Não considere a tarefa concluída até que a publicação tenha sucesso e o site esteja no ar.

## Resumo e próximas etapas

O Space Quiz agora está disponível como um site publicado, e você verificou a publicação em vez de confiar apenas no relato do agente. Continue para a [Lição 13: Revisão e próximas etapas][next-lesson].

[next-lesson]: ../13-review/
