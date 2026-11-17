---
title: "Lição 12 - Implante o site com o GitHub Pages"
description: "Use o aplicativo GitHub Copilot para configurar um fluxo de trabalho do Pages, revisar a pull request e verificar o Space Quiz publicado."
authors:
  - jamesmontemagno
lastUpdated: 2026-10-12
---

Dê ao Space Quiz um endereço público implantando-o com o GitHub Pages. O Copilot pode preparar o fluxo de trabalho e orientar a implantação, mas você continua responsável por revisar as alterações e confirmar que o site está no ar.

Nesta lição, você vai:

- pedir ao Copilot para configurar uma implantação no GitHub Pages.
- revisar o fluxo de trabalho e a pull request antes de fazer o merge.
- acompanhar a implantação e verificar o site publicado.

## Cenário

O Space Quiz já está em um repositório do GitHub, mas as pessoas ainda precisam de uma maneira simples de experimentá-lo. Publicar o site de arquivo único com o GitHub Pages o disponibiliza em uma URL pública, sem adicionar um servidor ou dependência de runtime.

## Peça ao Copilot para preparar a implantação

> [!WARNING]
> Criar uma pull request pode fazer commit e push de código. Revise as configurações de aprovação e o repositório de destino antes de enviar este prompt. Com **Approve all** selecionado, não espere uma solicitação de confirmação separada.

Na sessão do aplicativo Copilot para `space-quiz`, envie este prompt:

```plaintext
Prepare a GitHub Pages deployment for this repository. Create a GitHub Actions workflow that builds the website if needed and deploys it to GitHub Pages after changes reach the default branch. Add a README describing the app and how to run it locally if one does not already exist. Create a pull request with these changes and report its link and any required Pages settings or permissions. Do not merge, enable auto-merge, change Pages settings, or deploy. Stop and wait for my review.
```

## Revise o fluxo de trabalho e a pull request

1. Confirme se o README foi adicionado somente quando ainda não existia no repositório.
2. Revise as alterações da pull request, incluindo as etapas de build e implantação do fluxo de trabalho, os gatilhos e as permissões.
3. Confirme que o fluxo de trabalho implanta a partir da branch padrão, e não de uma pull request ainda não mesclada.
4. Peça as correções necessárias e revise o diff atualizado. Aguarde a aprovação nas verificações obrigatórias da pull request antes de autorizar o merge.

## Autorize o merge e a implantação

> [!WARNING]
> O prompt a seguir autoriza o agente a mesclar a pull request revisada, alterar as configurações do Pages do repositório e publicar o site. Envie-o somente depois de concluir a revisão e confirmar o repositório e a pull request. Dependendo das configurações de aprovação, essas ações podem ocorrer sem outra solicitação de confirmação.

Substitua `<PR_NUMBER>` pelo número da pull request revisada e envie este prompt separadamente:

```plaintext
I have reviewed pull request <PR_NUMBER> in this repository and authorize its merge and deployment. Enable GitHub Pages using GitHub Actions, merge that pull request only after required checks pass, and monitor the deployment until it succeeds. Report the final URL of the live website. If you lack permission to enable Pages or merge, tell me exactly what I need to approve or do; do not report success until the site is live.
```

![Diagrama em três etapas: uma pull request do space-quiz mesclada; uma execução bem-sucedida do GitHub Actions Deploy website com as etapas Build website, Upload artifact e Deploy to Pages; e o Space Quiz publicado em yourname.github.io/space-quiz/.](../../../_images/first-steps-app-pages-deploy.svg)

## Verifique a implantação

1. Acompanhe a execução de implantação do GitHub Actions até ela ser concluída com sucesso.
2. Abra a URL informada e confirme que o Space Quiz carrega.

Se o agente não puder habilitar o Pages ou mesclar a pull request, siga as instruções específicas fornecidas por ele. Não considere a tarefa concluída até que a implantação seja bem-sucedida e o site esteja no ar.

## Resumo e próximas etapas

O Space Quiz agora está disponível como um site publicado, e você verificou a implantação em vez de confiar no relato do agente. Continue para a [Lição 13: Revisão e próximos passos][next-lesson].

[next-lesson]: ../13-review/
