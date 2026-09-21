# Fundamentos do Método C.H.

O C.H. organiza engenharia de software humano-IA em torno de decisão explícita, delegação limitada, evidência e memória versionada.

## Valores

O método prioriza:

1. intenção verificável sobre prompts extensos ou sofisticados;
2. evidência reproduzível sobre respostas confiantes;
3. fatias pequenas e reversíveis sobre grandes entregas autônomas;
4. memória explícita do projeto sobre contexto presumido da conversa;
5. responsabilidade humana sobre conveniência da autonomia;
6. orquestração adequada ao problema sobre fidelidade a um modelo ou ferramenta.

## Doze princípios

1. Toda entrega possui um responsável humano identificável, inclusive quando toda a implementação foi realizada por agentes.
2. O trabalho começa pela compreensão do valor esperado, não pela escolha da ferramenta ou pela escrita do prompt.
3. Antes de agir, o agente deve consultar a fonte de verdade atual: código, testes, contratos, decisões e instruções do repositório.
4. Mudanças arquiteturais, contratuais, econômicas ou de segurança exigem decisão explícita antes da implementação.
5. Cada delegação deve ter objetivo, escopo autorizado, restrições, critérios de aceitação e condição clara de parada.
6. A execução deve ocorrer em ambiente isolado e produzir mudança reversível, preferencialmente em branch ou worktree própria.
7. Nenhuma afirmação de sucesso substitui evidência: diff, testes, análise estática, demonstração funcional e limitações conhecidas.
8. A profundidade da revisão e o nível de autonomia devem variar conforme risco, impacto e reversibilidade.
9. O paralelismo deve ser limitado pela capacidade de verificar e integrar, não pela quantidade de agentes disponíveis.
10. Modelos, ferramentas e provedores devem ser escolhidos pela adequação à tarefa, considerando capacidade, custo, privacidade e risco.
11. Decisões, correções e aprendizados relevantes devem retornar ao repositório para reduzir dependência de memória conversacional.
12. A equipe deve eliminar continuamente dívida técnica, desvio de padrões e entropia produzidos pelo aumento de velocidade.

## Status

O C.H. é uma proposta experimental. Seus princípios devem ser aplicáveis, mensuráveis, criticáveis e evolutivos.
