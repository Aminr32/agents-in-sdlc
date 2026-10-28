---
title: "Lição 12 - Implante o site com o GitHub Pages"
description: "Use o aplicativo GitHub Copilot para configurar um fluxo de trabalho do Pages, revisar o pull request e verificar o Space Quiz publicado."
authors:
  - jamesmontemagno
lastUpdated: 2026-10-12
---

Publique o Space Quiz para que todos possam acessá-lo usando o GitHub Pages. O Copilot pode preparar o fluxo de trabalho e orientar a implantação, mas você continua responsável por revisar as alterações e confirmar se o site está no ar.

Nesta lição, você vai:

- pedir ao Copilot para configurar a implantação no GitHub Pages;
- revisar o fluxo de trabalho e o pull request antes da mesclagem;
- acompanhar a implantação e verificar o site publicado.

## Cenário

O Space Quiz já está em um repositório do GitHub, mas as pessoas ainda precisam de uma forma simples de experimentá-lo. Publicar o site de arquivo único com o GitHub Pages o disponibiliza em uma URL pública, sem adicionar um servidor ou uma dependência de runtime.

## Peça ao Copilot para implantar o site

Na sessão do aplicativo Copilot para `space-quiz`, envie este prompt:

```plaintext
Habilite o GitHub Pages para este repositório. Crie um fluxo de trabalho do GitHub Actions que compile o site, se necessário, e o implante no GitHub Pages. Adicione um README descrevendo o aplicativo e como executá-lo localmente, caso ainda não exista. Crie um pull request com essas alterações e faça a mesclagem depois que as verificações obrigatórias forem aprovadas. Monitore a implantação até que ela seja concluída com sucesso e, em seguida, informe a URL final do site publicado. Se você não tiver permissão para habilitar o Pages ou mesclar, diga exatamente o que preciso aprovar ou fazer; não informe que a implantação foi bem-sucedida até que o site esteja no ar.
```

![Diagrama em três etapas: um pull request do space-quiz mesclado; uma execução bem-sucedida do GitHub Actions Deploy website com as etapas Build website, Upload artifact e Deploy to Pages; e o Space Quiz publicado em yourname.github.io/space-quiz/.](../../../_images/first-steps-app-pages-deploy.svg)

> [!WARNING]
> Este prompt pede ao agente que crie e mescle um pull request e altere as configurações do Pages no repositório. Antes de continuar, revise o diff, as permissões de implantação e quaisquer solicitações de aprovação do GitHub.

## Revise o fluxo de trabalho e verifique a implantação

1. Confirme se o README foi adicionado somente quando o repositório ainda não tinha um.
2. Revise as alterações do pull request, incluindo as etapas de compilação e implantação do fluxo de trabalho.
3. Faça a mesclagem somente depois que as verificações obrigatórias do pull request forem aprovadas.
4. Acompanhe a execução de implantação do GitHub Actions até que ela seja concluída com sucesso.
5. Abra a URL informada e confirme se o Space Quiz carrega.

Se o agente não puder habilitar o Pages ou mesclar o pull request, siga as instruções específicas que ele fornecer. Não considere a tarefa concluída até que a implantação seja bem-sucedida e o site publicado carregue.

## Resumo e próximos passos

O Space Quiz agora está disponível em um site publicado, e você verificou a implantação em vez de confiar somente no relatório do agente. Continue para a [Lição 13: Revisão e próximos passos][next-lesson].

[next-lesson]: ../13-review/
