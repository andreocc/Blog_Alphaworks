---
title: "Não é vazamento, é design — o caso Claude que todo CTO deveria estudar"
date: 2026-08-08T15:34:03-03:00
draft: false
tags:

summary: ""
---

## Âncora Externa
Centenas de conversas privadas com o Claude (Anthropic) ficaram acessíveis publicamente no Google. Usuários usaram a opção "compartilhar", os links foram indexados por buscadores. Dados corporativos confidenciais, currículos e pesquisas pessoais expostos. A Anthropic respondeu que "os links não eram previsíveis ou detectáveis a menos que as pessoas optassem por compartilhar". Fonte: G1 (28/07/2026).

## Ângulo
Não é sobre o usuário que clicou "compartilhar" sem ler. É sobre o design que trata "compartilhar" como ação trivial — mesma lógica de "curtir" — quando na prática é "tornar público e indexável no Google". O problema é de **arquitetura de decisão**: se o usuário precisa entender indexação de buscadores para não expor dados da empresa, o design falhou.

## Lição de Board
"Confiança não é virtude — é consequência de design." (Simon Sinek)

## Assinatura
Menos fumaça, mais governança.

## Esboço de corpo
Hook: "Não é um vazamento de dados. É um vazamento de design."

Setup: Centenas de conversas privadas do Claude apareceram no Google. A Anthropic disse que o usuário optou por compartilhar.

Conflito: O problema é que "compartilhar" num chat de IA não tem o mesmo peso que "publicar na web". O design trata como ação reversível, quando não é. Seu currículo, seu plano estratégico, sua pesquisa de mercado — tudo indexado porque um botão estava no lugar errado.

Resolução: Empresas que adotam IA precisam de uma camada de governança entre o usuário e a ferramenta. Não dá para delegar segurança pra UX de terceiros.

Lição: "Confiança não é virtude — é consequência de design." Cada botão de compartilhar no seu ecossistema precisa ser auditado como se fosse uma porta de dados.

Assinatura: Menos fumaça, mais governança.
