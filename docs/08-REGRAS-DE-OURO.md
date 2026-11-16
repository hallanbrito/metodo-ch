# Regras de Ouro da Programação Híbrida Humano–IA

> **Construa com IA, decida com responsabilidade, aceite com evidência.**

Este guia reúne práticas operacionais do **Método C.H. — Colaboração Híbrida**. Foi inspirado por dificuldades reais de trabalho entre pessoas e agentes de inteligência artificial, mas é **independente de marcas, modelos e fornecedores**: as funções podem ser exercidas por qualquer pessoa ou sistema competente e autorizado.

É um complemento aos [Fundamentos](01-FUNDAMENTOS.md), ao [ciclo CHAVE](02-CICLO-CHAVE.md), às [Fatias W](03-FATIAS-W.md), aos [Papéis e autonomia](04-PAPEIS-E-AUTONOMIA.md) e às [Evidências e gates](05-EVIDENCIAS-E-GATES.md). Não altera retroativamente o manifesto histórico 0.1. São práticas abertas a revisão e experimentação.

## 1. A conversa nunca é a fonte da verdade

**Erro:** depender da memória do chat para saber o que está pronto, aprovado ou bloqueado.

**Prática:** o estado do projeto vive em **artefatos verificáveis e versionados**: código, testes, contratos, decisões, Issues, PRs e, quando necessário, um documento de estado (por exemplo, docs/STATUS.md). Ao começar uma sessão, identifique repositório, branch/commit e registros relevantes. Se o resumo do chat divergir do repositório, verifique antes de agir.

**Máxima:** contexto se reconstrói; histórico se versiona.

## 2. Inspecione antes de prescrever

**Erro:** inventar pré-requisitos, pedir testes já concluídos ou propor infraestrutura sem conhecer o ambiente.

**Prática:** investigue primeiro o que existe, o que funciona, quais tentativas falharam e o que já foi homologado. Não confunda hipótese com fato. Se algo não puder ser verificado, **declare a incerteza** em vez de preenchê-la com suposições.

## 3. Entregue a menor Fatia W que cria valor verificável

**Erro:** transformar uma pequena correção em um projeto paralelo.

**Prática:** delegue um objetivo por vez, com escopo, exclusões, critérios de aceite e condição de parada. Prefira diffs pequenos, compreensíveis e reversíveis. **Um arquivo ou poucas linhas são heurísticas, não limites absolutos:** código, testes e documentação podem exigir mais de um arquivo. A medida certa é a capacidade de revisar a mudança com segurança.

**Pergunta:** uma pessoa consegue explicar, testar e reverter esta W?

## 4. Imponha um orçamento de complexidade

**Erro:** adicionar framework, contêiner, serviço, camada, dependência ou processo só porque a solução parece mais profissional.

**Prática:** comece por **KISS** (simplicidade) e **YAGNI** (não construir o que ainda não é necessário). Reutilize recursos existentes. Qualquer complexidade nova deve resolver um problema demonstrável, justificar custo e manutenção e receber a autorização cabível. Exigências reais de segurança, confiabilidade, desempenho e acessibilidade podem justificar mais estrutura — simplicidade não é negligência.

## 5. Distribua papéis, não marcas

**Erro:** transformar uma ferramenta específica em coordenador obrigatório, outra em executor exclusivo e outra em único auditor possível.

**Prática:** escolha ferramentas pela capacidade, custo, risco, acesso e adequação à tarefa. Os papéis são responsabilidades intercambiáveis:

| Papel | Responsabilidade |
| --- | --- |
| **Owner humano** | Define prioridades, limites de risco e aceite final. |
| **Orquestrador** | Lê a fonte da verdade, esclarece decisões e especifica a W. |
| **Executor** | Implementa apenas o autorizado e produz evidências. |
| **Revisor / guardião** | Questiona premissas, examina diffs, testes e riscos. |
| **Mantenedor da memória** | Preserva decisões, resultados e próximos passos no repositório. |

Uma pessoa ou agente pode exercer múltiplas funções, mas **riscos maiores pedem revisão mais independente**. A eloquência de uma IA não lhe concede autoridade.

## 6. Evidência vale mais que declaração de sucesso

**Erro:** aceitar “concluído”, “funcionando” ou “testes passaram” sem execução demonstrável.

**Prática:** exija o diff, o ambiente, os comandos realmente executados, os resultados observados, os testes que **não** foram rodados, riscos e limitações. Separe fatos, inferências e pendências. Um PR aberto ou um relatório bonito não substitui o funcionamento do produto, a revisão nem o aceite humano.

## 7. Corte ciclos de complexidade sem valor

**Erro:** criar fases, siglas, gates, relatórios e scripts para validar outros relatórios e scripts, sem risco novo nem avanço no produto.

**Prática:** todo controle precisa reduzir risco, preservar decisão ou diminuir retrabalho. Se não consegue mostrar esse benefício, simplifique. Testes automatizados são valiosos quando validam comportamento; burocracia repetitiva não é qualidade. Ao identificar um ciclo improdutivo, use o comando de interrupção ao final deste documento.

## 8. Autonomia deve ter fronteiras explícitas

**Erro:** delegar “resolva tudo” sem delimitar arquivos, permissões, custos e integração.

**Prática:** defina o que o agente pode ler, modificar, testar, publicar e integrar. Prefira branches ou ambientes isolados, mudanças reversíveis e decisões humanas para escolhas fora do contrato. Produção, segredos, dados pessoais, despesas e operações destrutivas exigem controles adicionais. Utilize os [níveis CH-0 a CH-3](04-PAPEIS-E-AUTONOMIA.md).

## 9. Registre o aprendizado; não repita o mesmo trabalho

**Erro:** reabrir discussões decididas, reconstruir contexto e executar novamente testes já válidos, sem motivo técnico.

**Prática:** após cada W, registre **estado final, evidências, falhas conhecidas, decisões, pendências e próximo passo**. Atualize documentação existente antes de criar arquivos novos. Referencie logs completos em vez de copiá-los por toda parte. A próxima conversa precisa conseguir continuar a partir do repositório.

## 10. Meça valor entregue, não atividade gerada

**Erro:** tratar quantidade de prompts, linhas, commits, agentes, fases ou horas como medida automática de produtividade.

**Prática:** avalie entregas aceitas, defeitos, ciclos de correção, esforço de revisão, tempo e custo por W aceita, quando mensuráveis. Mais automação só é avanço se melhorar qualidade, custo ou capacidade de entrega.

---

## Comando de interrupção — PARE / KISS

Quando a coordenação começar a produzir mais processo que resultado, qualquer participante pode dizer:

> **PARE — KISS.** Consulte o estado versionado e o que já foi validado. Não invente infraestrutura, não repita verificações sem causa e não crie fases sem risco identificado. Proponha **uma única Fatia W mínima**, contendo objetivo, mudanças necessárias, critério de aceite e próxima ação executável. Se houver decisão humana pendente, solicite-a; não escolha silenciosamente.

## Contrato mínimo para começar uma tarefa

~~~text
Repositório e referência: <repo + branch/commit>
Fonte da verdade: <documentos, Issue/PR, decisões, testes>
Objetivo da W: <resultado observável>
Escopo permitido: <o que pode mudar>
Fora do escopo: <o que não pode mudar>
Restrições: reutilizar o existente; nenhuma dependência,
serviço ou arquitetura nova sem justificativa e aprovação.
Critérios de aceite: <como demonstrar que funciona>
Evidências: <diff, comandos, testes, limitações>
Autonomia: <CH-0, CH-1, CH-2 ou CH-3>
Parada: <quando escalar uma decisão ao humano>
~~~

**Antes de coordenar:** confirme a referência. **Antes de executar:** confirme limites. **Antes de concluir:** demonstre a evidência. **Antes de encerrar:** devolva o aprendizado à fonte da verdade.

## Princípio final

> **A inteligência artificial pode acelerar a construção do software; não deve acelerar a perda de contexto, a burocracia ou a transferência silenciosa de responsabilidade.**

Estas regras constituem **orientações operacionais evolutivas**, não uma promessa de superioridade universal. Adapte-as ao contexto, ao risco e à capacidade da equipe, preservando simplicidade, rastreabilidade e responsabilidade humana.
