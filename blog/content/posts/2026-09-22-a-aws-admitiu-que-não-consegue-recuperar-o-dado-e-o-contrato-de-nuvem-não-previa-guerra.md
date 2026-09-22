---
title: "A AWS admitiu que não consegue recuperar o dado e o contrato de nuvem não previa guerra"
date: 2026-09-22T18:45:50-03:00
draft: false
tags:
  - custos
  - cloud
  - risco
summary: ""
---

Em 15 de setembro de 2026, a AWS atualizou o painel de status e confirmou o que nenhum contrato de nuvem prevê: dados de clientes perdidos de forma permanente. Seis meses antes, em 1º de março, drones atingiram dois data centers da Amazon nos Emirados Árabes Unidos e causaram danos a uma instalação no Bahrein. A Guarda Revolucionária iraniana assumiu a autoria e declarou que a instalação do Bahrein foi escolhida por sediar operações ligadas ao apoio da Amazon às forças militares dos Estados Unidos.

O resultado, seis meses depois, não é indisponibilidade. É perda. No Bahrein (região me-south-1), a AWS informou que não consegue restaurar o acesso a recursos e dados de nenhuma das três zonas de disponibilidade. Nos Emirados (mec1), a perda mais grave ficou em uma das três zonas, a mec1-az2; as outras duas seguem em recuperação, ainda em andamento. A empresa orientou clientes a migrar operações para outras regiões e restaurar de cópias de segurança remotas, suspendeu cobranças nas regiões atingidas e concedeu cerca de US$ 150 milhões em créditos. A maior parte dos clientes conseguiu restabelecer as operações pelo caminho da migração. Nova atualização pública foi prometida apenas para o começo de 2027.

## Tolerância a falha não é sobrevivência do dado

O senso comum de arquitetura repete uma equação simples: três zonas de disponibilidade, logo o sistema resiste. Essa equação descreve tolerância a falha, não sobrevivência do dado. São promessas diferentes e você provavelmente comprou uma acreditando ter as duas.

A tolerância a falha opera sob dois pressupostos silenciosos: a região continua existindo e o provedor continua operando dentro dela. Um disco morre, uma zona cai, o balanceamento assume, alguém troca o hardware, a operação segue. Esse é o cenário que o desenho cobre, e cobre bem. Quando o risco deixa de ser técnico e passa a ser geopolítico, os dois pressupostos caem no mesmo instante, porque não dependem um do outro. Não existe plano de replicação entre zonas que sobreviva à decisão de um terceiro de atingir fisicamente o prédio.

A própria AWS escreveu a frase que encerra a discussão: o dano superou o que os sistemas regionais e de múltiplas zonas foram desenhados para suportar. A perda de uma única zona nunca deveria comprometer a região. Aqui, todas as três foram comprometidas ao mesmo tempo. A réplica existia, estava saudável e estava no mesmo endereço.

## O teste de sobrevivência regional

Trate o episódio como método. O teste de sobrevivência regional tem três perguntas, e cada uma cobre um grau diferente de exposição.

Primeira: quais dados existem em um único lugar. Não "estão replicados", mas existem em um único lugar geográfico, jurídico e elétrico. Réplica na zona ao lado não conta. Réplica na mesma região, sob o mesmo provedor, sob a mesma jurisdição e o mesmo risco físico, conta como um lugar só.

Segunda: quem assinou por esses dados. Existe um nome, um cargo e uma data no documento que declara aquele ativo crítico e o nível de proteção aceito. Se a resposta for "a equipe de infraestrutura decidiu", o risco subiu para o board sem passar por ele. O que não tem assinatura não tem dono, e o que não tem dono não tem orçamento de contingência.

Terceira: quanto tempo a operação vive sem esses dados. Não quanto tempo o sistema fica no ar, mas quanto tempo o negócio funciona: faturar, atender, entregar, cumprir obrigação regulatória. Essa é a única métrica que transforma risco técnico em decisão de investimento, porque é a única que alguém fora da tecnologia consegue dimensionar em dinheiro.

As três perguntas juntas definem o que o contrato realmente cobre. Nenhum contrato de nuvem prevê guerra. A maioria também não prevê o que acontece quando o provedor simplesmente informa que o dado não volta, e é por isso que a resposta precisa estar do seu lado da fronteira, não do lado dele.

## O que fica descoberto

O que o incidente expôs não foi uma falha de engenharia da AWS. Foi o intervalo entre o que a arquitetura promete e o que o contrato garante. A região do Golfo vinha atraindo investimento pesado em nuvem e inteligência artificial, com projetos de vários gigawatts anunciados desde 2025, e a pergunta de risco geopolítico foi tratada como custo de seguro, não como premissa de desenho. Seis meses de tentativa, créditos devolvidos e um novo comunicado apenas em 2027 formam o retrato de um prazo que ninguém no board havia orçado.

Plano de continuidade escrito para falha de disco não cobre falha de país. Backup que mora no mesmo provedor não cobre a saída do provedor. E registro de risco que não nomeia responsável não cobre nada: apenas documenta que alguém sabia.

Leve o teste de sobrevivência regional para a próxima revisão de arquitetura. Responda as três perguntas por escrito, com nome, data e valor. Onde a resposta for "não sei" ou "não temos", você acabou de encontrar o risco que ainda não foi precificado. O resto é fumaça de conformidade.

Menos fumaça, mais governança.
Do Tech ao Board.
