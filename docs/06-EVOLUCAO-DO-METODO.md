# Evolução do Método C.H.

Este documento separa o **registro histórico congelado** das práticas que continuam evoluindo.

## Regra de preservação

A versão 0.1, consolidada em 27 de agosto de 2026, não será reescrita para parecer mais madura do que era. Novas práticas entram como evolução, hipótese ou versão posterior.

## Linha histórica

### Agosto de 2026 — origem prática

Durante o desenvolvimento do Maestro Router, o fluxo humano-IA começou a estabilizar espontaneamente: decisão humana, recorte pequeno, execução agêntica delimitada, evidências, revisão e autorização antes da integração.

### 27 de agosto de 2026 — White Paper Experimental v0.1

A experiência foi formalizada como **Método Ágil C.H.**.

Foram registrados:

- a dupla leitura ChatGPT-Hallan / Colaboração Híbrida;
- seis valores;
- doze princípios;
- Fatias W;
- ciclo CHAVE;
- papéis e responsabilidades;
- níveis de autonomia CH-0 a CH-3;
- Pacote de Evidências;
- gates de integração;
- métricas e hipóteses de validação.

A v0.1 permanece disponível em [../whitepaper/WHITE-PAPER-v0.1.md](../whitepaper/WHITE-PAPER-v0.1.md).

### Setembro de 2026 — aplicação contínua no Maestro Router

O método continuou sendo exercitado em Ws reais. A prática reforçou a separação entre:

- decisão de produto;
- decisão arquitetural;
- execução;
- verificação;
- autorização de integração.

Também ficou mais explícita a necessidade de independência entre executor e revisor, de baselines exatas antes de cada W e de gates contra merge sobre um HEAD diferente daquele efetivamente revisado.

### Setembro de 2026 — hipótese do C.H. Econômico

O uso intensivo de agentes revelou outro gargalo: **o próprio custo de raciocínio, contexto e revisão pode crescer mais rápido que o valor da W**.

Da observação nasceu uma evolução operacional ainda em validação, provisoriamente chamada **C.H. Econômico**.

Ela não substitui os princípios da v0.1. Busca reduzir redundância sem reduzir controles:

1. usar capacidade/modelo proporcional à dificuldade da etapa;
2. escalar capacidade apenas quando houver evidência de necessidade;
3. evitar transportar logs extensos para o contexto do orquestrador;
4. inspecionar diffs de forma progressiva e seletiva;
5. separar revisão detalhada de implementação, revisão arquitetural e gate independente;
6. medir economia por W aceita, não por quantidade bruta de chamadas;
7. abrir nova sessão quando contexto acumulado deixa de produzir valor.

### Estado atual

**C.H. Econômico não é uma versão histórica publicada do método.** É uma hipótese operacional em experimentação. Só deverá entrar em uma versão posterior depois de uso, observação, correção e documentação suficientes.

## Como uma evolução se torna parte do método

Uma prática nova deve passar pelo próprio CHAVE:

**Contextualizar → Harmonizar → Agir → Verificar → Evoluir**

Antes de ser promovida de experimento para princípio ou prática recomendada, deve existir evidência de aplicação, limitações conhecidas e justificativa para sua inclusão.

## Compromisso

O objetivo não é preservar o C.H. exatamente como nasceu. É preservar **a verdade sobre como nasceu** e permitir que o método evolua de forma rastreável.
