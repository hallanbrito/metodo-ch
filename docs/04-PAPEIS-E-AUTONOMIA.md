# Papéis e autonomia

O C.H. define **responsabilidades**, não cargos fixos. Pessoas e agentes podem acumular funções, mas responsabilidade humana e execução agêntica não devem ser confundidas.

## Papéis

| Responsabilidade | Função |
|---|---|
| **Owner Humano** | Define valor, prioridade, risco aceitável e aprovação final. Responde pelo produto e não transfere essa responsabilidade à IA. |
| **Orquestrador Cognitivo** | Transforma intenção em decisões e Fatias W, seleciona agentes, fecha escopo, identifica conflitos e coordena revisões. |
| **Executor Agêntico** | Executa a W no ambiente autorizado, altera apenas o escopo permitido e produz evidências. |
| **Guardião de Evidências** | Verifica critérios, desafia suposições e avalia segurança e coerência com independência suficiente da execução. |
| **Mantenedor da Memória** | Preserva instruções, mapas, decisões, contratos, padrões e aprendizados na fonte de verdade versionada. |

## Níveis de autonomia

Autonomia é concedida **por Fatia W** e calibrada pelo risco.

| Nível | Nome | Permissão |
|---|---|---|
| **CH-0** | Consultar | Somente leitura, análise e explicação. Nenhuma alteração externa. |
| **CH-1** | Propor | Pode elaborar plano, decisão, prompt ou diff sugerido, sem escrever na fonte de verdade. |
| **CH-2** | Executar isolado | Pode criar branch, modificar escopo autorizado, testar, commitar e abrir Draft PR. Não pode integrar. |
| **CH-3** | Integrar condicionado | Pode integrar mudanças de baixo risco quando gates e políticas predefinidas forem satisfeitos, mantendo trilha auditável. |

Níveis superiores não anulam políticas específicas para operações destrutivas, segredos, produção, dados pessoais ou contratos externos.

## Paralelismo responsável

A disponibilidade de vários agentes não obriga execução paralela. O limite de trabalho em andamento é definido pela capacidade de revisão e pelo acoplamento entre as Fatias W.
