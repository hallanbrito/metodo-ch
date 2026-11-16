# 10 Regras de Ouro — Humano + IA

> **Construa com IA. Decida como humano. Aceite com evidência.**

Este é um guia prático do [Método C.H.](../README.md). Não depende de marca, agente ou modelo. Para aprofundar, veja [Fundamentos](01-FUNDAMENTOS.md), [Fatias W](03-FATIAS-W.md) e [Autonomia](04-PAPEIS-E-AUTONOMIA.md).

## A receita

1. **Conversa não é fonte da verdade.** Consulte código, testes, Issues, PRs e decisões versionadas. Use `STATUS.md` quando isso ajudar a retomar o trabalho.
2. **Olhe antes de propor.** Descubra o que já funciona e foi testado. Não invente pré-requisitos.
3. **Faça uma Fatia W pequena.** Um objetivo, limites e critério de aceite. O tamanho é o que uma pessoa consegue revisar; não existe regra universal de 20 linhas ou um arquivo.
4. **Use KISS e YAGNI.** Sem serviço, framework ou dependência nova sem necessidade demonstrada. Segurança necessária não é excesso.
5. **Distribua papéis, não marcas.** Humano responsável decide; orquestrador organiza; executor implementa; revisor verifica. Ferramentas são substituíveis.
6. **Peça prova, não promessa.** Diff, teste realmente executado, comportamento observado e limitações. Diga quando não testou.
7. **Corte burocracia circular.** Uma etapa, gate ou script só existe se reduz risco ou retrabalho.
8. **Delegue com limites.** Defina o que pode mudar, acesso, custo, autonomia e quando parar. Produção e operações destrutivas exigem controle.
9. **Aprenda uma vez.** Registre decisões, falhas e próximo passo no repositório; não refaça a descoberta em cada chat.
10. **Meça valor aceito.** Qualidade, retrabalho e esforço de revisão importam mais que prompts, linhas ou quantidade de agentes.

## Comando de resgate

> **PARE — KISS.** Consulte o estado versionado. Não repita testes sem motivo nem crie etapas sem risco real. Mostre uma única Fatia W mínima: objetivo, limites, teste de aceite e próxima ação. Se faltar autorização, pergunte ao humano.

## Prompt mínimo

~~~text
Projeto e baseline: <repositório, branch e commit>
Objetivo: <uma entrega observável>
Fonte da verdade: <código, Issue, decisões, testes>
Pode alterar: <escopo>
Não pode alterar: <exclusões>
Aceite: <como comprovar>
Autonomia: <CH-0 a CH-3>
Parada: <quando devolver ao humano>
~~~

**Regra final:** o método deve reduzir a carga mental de quem desenvolve, não criar trabalho para parecer profissional.

*Prática operacional evolutiva. O manifesto histórico v0.1 permanece preservado.*
