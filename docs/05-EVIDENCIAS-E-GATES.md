# Evidências e gates

No C.H., confiança não é critério de aceite. Uma entrega deve produzir evidências proporcionais ao risco.

## Pacote de Evidências mínimo

| Bloco | Evidência esperada |
|---|---|
| **Identidade** | W, executor, modelo, ambiente, branch e baseline. |
| **Mudanças** | Resumo do diff e arquivos alterados. |
| **Verificações** | Testes, análise estática, build e demonstração funcional quando aplicável. |
| **Aderência** | Confirmação de escopo; desvios devem ser declarados. |
| **Risco e segurança** | Segredos, dados, rede, dependências, permissões e operações destrutivas. |
| **Limitações** | Suposições, casos não testados, dúvidas e decisões adiadas. |
| **Economia** | Tempo, uso, custo conhecido e motivo da seleção do executor, quando mensurável. |
| **Estado final** | Commit, Draft PR, estado da árvore e estratégia de reversão. |

## Gates

A profundidade dos gates acompanha risco, impacto e reversibilidade. O fluxo típico separa:

**execução → evidência → revisão independente → aceite humano → integração**

Uma Draft PR é um pedido de integração, não prova de conclusão. Testes aprovados também não substituem revisão de requisitos, arquitetura, segurança ou escopo.

## Métricas úteis

O C.H. privilegia valor aceito e custo de supervisão, como throughput de Ws aceitas, aceite na primeira passagem, loops de correção, esforço de verificação, defeitos escapados, desvio de escopo, conflito de integração e custo por W aceita.
