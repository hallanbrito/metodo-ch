**WHITE PAPER EXPERIMENTAL | VERSÃO 0.1**

# Método Ágil C.H.

Engenharia de software humano-IA orientada por decisão,  
delegação limitada e evidência

> *Um método para acelerar a construção de software com agentes de IA sem terceirizar o julgamento, a responsabilidade ou a qualidade.*

**Criado por Hallan de Sousa Brito e ChatGPT (OpenAI)**

Concepção e responsabilidade humana: Hallan de Sousa Brito

Colaboração conceitual e redação assistida: ChatGPT

**Nascido da experiência de construção do Maestro Router**

Teresina, Brasil | 27 de agosto de 2026

## Resumo

O Método Ágil C.H. é uma proposta experimental para organizar o desenvolvimento de software realizado por equipes híbridas formadas por pessoas e agentes de inteligência artificial. A sigla registra sua origem - ChatGPT-Hallan - e também expressa seu princípio geral: Colaboração Híbrida. O método nasceu durante a construção incremental do Maestro Router, em 2026, quando a geração de código deixou de ser o principal gargalo e o trabalho passou a se concentrar em definir decisões, limitar o escopo delegado, verificar resultados e preservar a coerência do produto.

A proposta não substitui o Manifesto Ágil, Scrum, Kanban ou Extreme Programming. Ela herda desses referenciais a entrega incremental, o feedback frequente, a simplicidade, a qualidade técnica e a adaptação. Sua contribuição está em tornar explícitos problemas que se tornaram centrais na engenharia de software agêntica: quem responde pela decisão, qual autonomia é concedida à IA, como o contexto é preservado, quais evidências permitem aceitar uma entrega e quanto paralelismo a capacidade humana de verificação suporta.

O C.H. estrutura o trabalho em Fatias W verificáveis e utiliza o ciclo CHAVE: Contextualizar, Harmonizar, Agir, Verificar e Evoluir. A responsabilidade final permanece humana. Agentes podem planejar, implementar, testar, documentar e revisar, mas nenhum resultado é aceito apenas porque foi produzido com confiança ou velocidade. O método é apresentado como hipótese operacional aberta a experimentação, medição e revisão pública.

> **Tese central.** Na engenharia assistida por IA, produtividade sustentável não é a quantidade de código gerado. É a quantidade de valor aceito com evidência, compreensão e responsabilidade.

**Palavras-chave:** métodos ágeis; engenharia de software agêntica; colaboração humano-IA; agentes de código; governança; verificação; desenvolvimento incremental.

## 1. Introdução: o código ficou mais rápido, a responsabilidade não

O Manifesto Ágil de 2001 foi uma resposta ao excesso de processos pesados e à distância entre planejamento e entrega. Seus valores continuam atuais: pessoas, software útil, colaboração e adaptação ainda importam [1]. O Scrum consolidou ciclos empíricos de transparência, inspeção e adaptação [2], enquanto práticas do XP reforçaram pequenas entregas, testes, integração e melhoria contínua. O C.H. não nasce da rejeição dessa história. Nasce da constatação de que um novo participante entrou no sistema de produção: o agente de IA capaz de ler repositórios, editar vários arquivos, executar ferramentas, criar testes e propor pull requests.

Em 2026, esse agente não é apenas uma ferramenta de autocompletar. Ele pode receber uma tarefa, explorar o código, alterar a implementação e devolver um conjunto de mudanças para revisão. Relatos de engenharia da OpenAI descrevem fluxos nos quais agentes trabalham por prompts, abrem pull requests, respondem a revisões e executam tarefas de longa duração; o mesmo relato identifica a capacidade humana de garantia da qualidade como um novo gargalo [5]. A mudança é organizacional: quando escrever código se torna barato, produzir código demais também se torna barato.

A adoção, porém, não elimina o risco. Na pesquisa Stack Overflow de 2025, 84% dos respondentes usavam ou planejavam usar IA no desenvolvimento, mas 46% declaravam desconfiar da precisão das ferramentas, contra 33% que confiavam. Entre as frustrações, 66% citaram soluções quase corretas e 45% relataram que depurar código gerado por IA consumia mais tempo [4]. A pesquisa DORA de 2025 resume a IA como um amplificador das forças e fraquezas já presentes no sistema organizacional [3].

O problema que motiva o Método C.H. é, portanto, simples de formular: os métodos existentes orientam bem a entrega iterativa por equipes humanas, mas normalmente não especificam como delegar trabalho a agentes probabilísticos, limitar sua autonomia, preservar memória entre sessões, comparar modelos, comprovar resultados e controlar uma velocidade de geração que pode ultrapassar a capacidade de revisão.

## 2. Origem e posição da proposta

### 2.1 Um nome com duas camadas

C.H. significa originalmente ChatGPT-Hallan, registrando a parceria que deu origem ao método: Hallan de Sousa Brito como Product Owner, praticante e responsável humano; ChatGPT como parceiro de arquitetura, análise e redação; e agentes de código, especialmente Codex, como executores delimitados. Para que a proposta possa ser aplicada por outras equipes, a mesma sigla também representa Colaboração Híbrida: pessoas definem propósito e assumem responsabilidade; agentes ampliam capacidade de análise e execução.

A dupla leitura preserva a origem sem transformar o método em uma receita dependente de um fornecedor. C.H. é explicitamente neutro em relação a modelos. Uma equipe pode utilizar ChatGPT, Codex, Claude, Gemini, modelos locais ou ferramentas futuras, desde que cada executor opere dentro de limites verificáveis.

### 2.2 O que o C.H. não reivindica

O C.H. não afirma ser a primeira proposta de integração entre agilidade e IA. O AgileGen, publicado em 2025, já explorou desenvolvimento generativo baseado em colaboração humano-IA e requisitos testáveis, com foco na consistência entre requisitos e código [7]. Em 2026, pesquisas também passaram a tratar a engenharia de software agêntica como área própria e a estudar formas concretas de supervisão humana [8].

A contribuição específica do C.H. é operacional: integrar decisão, delegação limitada, memória de projeto, isolamento de execução, evidência, custo, autonomia e capacidade de revisão em um único fluxo leve. Sua unidade básica não é a história de usuário, o Sprint nem o prompt. É a Fatia W: uma mudança pequena, justificável, reversível e verificável.

> **Status da proposta.** Esta versão 0.1 é um white paper conceitual baseado em um estudo de caso inicial. O método ainda precisa ser aplicado por outras equipes e comparado experimentalmente com fluxos alternativos.

## 3. A mudança de gargalo na engenharia de software

A engenharia tradicional tratava a implementação como recurso escasso: pessoas precisavam traduzir requisitos em código linha por linha. Ferramentas generativas e agentes reduzem parte desse custo, mas criam uma assimetria. Um agente pode produzir mais mudanças do que uma pessoa consegue compreender, testar e integrar com segurança.

Estudos internos da Anthropic relataram maior volume de trabalho, ampliação da atuação técnica e aceleração do aprendizado, mas também preocupações com perda de competência profunda, dificuldade de supervisão e redução da colaboração entre colegas [6]. Pesquisas com desenvolvedores experientes identificaram quatro tipos de supervisão sobre agentes: controle prévio, coplanejamento, monitoramento durante a execução e revisão posterior [8]. O fluxo real do Maestro Router apresentou as mesmas necessidades antes que elas recebessem esses nomes formais.

O C.H. parte de três deslocamentos:

- De escrever cada linha para definir intenção, arquitetura e critérios de aceitação.
- De acompanhar esforço humano para controlar autonomia, contexto, custo e risco de agentes.
- De confiar na habilidade de quem implementou para exigir evidências reproduzíveis daquilo que foi entregue.

> **Lei da capacidade de verificação.** O fluxo sustentável de uma equipe humano-IA é limitado pelo menor valor entre capacidade de execução, capacidade de verificação e capacidade de integração. Adicionar agentes não aumenta o resultado quando revisão ou integração já são o gargalo.

## 4. Os seis valores do Método C.H.

Os itens à direita continuam úteis; o C.H. apenas estabelece prioridade quando houver conflito.

| # | Valorizamos | Mais que |
|---|---|---|
| 1 | Intenção verificável | prompts extensos ou sofisticados |
| 2 | Evidência reproduzível | respostas confiantes |
| 3 | Fatias pequenas e reversíveis | grandes entregas autônomas |
| 4 | Memória explícita do projeto | contexto presumido da conversa |
| 5 | Responsabilidade humana | conveniência da autonomia |
| 6 | Orquestração adequada ao problema | fidelidade a um modelo ou ferramenta |

## 5. Os doze princípios

1. Toda entrega possui um responsável humano identificável, inclusive quando toda a implementação foi realizada por agentes.
2. O trabalho começa pela compreensão do valor esperado, não pela escolha da ferramenta ou pela escrita do prompt.
3. Antes de agir, o agente deve consultar a fonte de verdade atual: código, testes, contratos, decisões e instruções do repositório.
4. Mudanças arquiteturais, contratuais, econômicas ou de segurança exigem decisão explícita antes da implementação.
5. Cada delegação deve ter objetivo, escopo autorizado, restrições, critérios de aceitação e condição clara de parada.
6. A execução deve ocorrer em ambiente isolado e produzir uma mudança reversível, preferencialmente em branch ou worktree própria.
7. Nenhuma afirmação de sucesso substitui evidência: diff, testes, análise estática, demonstração funcional e limitações conhecidas.
8. A profundidade da revisão e o nível de autonomia devem crescer ou diminuir de acordo com risco, impacto e reversibilidade.
9. O paralelismo deve ser limitado pela capacidade de verificar e integrar, não pela quantidade de agentes disponíveis.
10. Modelos, ferramentas e provedores devem ser escolhidos pela adequação à tarefa, considerando capacidade, custo, privacidade e risco.
11. Decisões, correções e aprendizados relevantes devem retornar ao repositório para reduzir dependência de memória conversacional.
12. A equipe deve eliminar continuamente dívida técnica, desvio de padrões e entropia produzidos pelo aumento de velocidade.

## 6. Papéis e responsabilidades

C.H. define responsabilidades, não cargos fixos. Em uma equipe pequena, uma pessoa ou agente pode acumular funções, mas responsabilidade humana e execução agêntica não devem ser confundidas.

| Responsabilidade | Função no método |
|---|---|
| **Owner Humano** | Define valor, prioridade, risco aceitável e aprovação final. Responde pelo produto e não pode transferir essa responsabilidade à IA. |
| **Orquestrador Cognitivo** | Transforma intenção em decisões e Fatias W, seleciona agentes, fecha escopo, identifica conflitos e coordena revisões. Pode ser uma pessoa ou IA supervisionada. |
| **Executor Agêntico** | Executa a Fatia W no ambiente autorizado, altera apenas o escopo permitido, produz testes, diff, documentação e relatório de execução. |
| **Guardião de Evidências** | Verifica se os critérios foram realmente atendidos, desafia suposições, avalia segurança e coerência. Deve ter independência suficiente em relação à execução. |
| **Mantenedor da Memória** | Preserva instruções, mapas, ADRs, contratos, padrões e aprendizados como fonte de verdade versionada. |

No Maestro Router, Hallan exerce o papel de Owner Humano; ChatGPT atua principalmente como Orquestrador Cognitivo e revisor arquitetural; Codex atua como Executor Agêntico; e a combinação de testes, revisão por ChatGPT e aprovação de Hallan forma o Guardião de Evidências. O próprio repositório, por meio de documentos e decisões versionadas, sustenta a memória.

## 7. Artefatos essenciais

| Artefato | Finalidade |
|---|---|
| **Mapa do Produto** | Visão, problemas, capacidades presentes, limites e evolução pretendida. |
| **Backlog de Ws** | Fila priorizada de Fatias W; ideias futuras não são tratadas como funcionalidades existentes. |
| **Registro de Decisão** | ADR ou nota equivalente para escolhas que alteram contratos, arquitetura, política econômica ou segurança. |
| **Contrato de Execução** | Prompt fechado ou especificação com baseline, escopo permitido, proibições, critérios e saídas esperadas. |
| **Pacote de Evidências** | Diff, testes, checagens, demonstrações, hipóteses, limitações, custo e relatório de desvios. |
| **Pedido de Integração** | Draft PR ou unidade equivalente que permita revisão antes da incorporação. |
| **Registro de Aceitação** | Aprovação, rejeição ou solicitação de correção pelo responsável humano. |
| **Memória Versionada** | Instruções para agentes, documentação, mapas, padrões e histórico técnico dentro da fonte de verdade. |

## 8. A unidade de trabalho: Fatia W

A Fatia W, ou Work Slice, é a menor mudança capaz de produzir aprendizado ou valor verificável sem romper a coerência do produto. Ela pode ser documental, arquitetural, funcional, corretiva ou experimental. Seu tamanho é determinado pela capacidade de revisão, não pela capacidade máxima do agente.

Uma W pronta para execução deve registrar:

- identificador, objetivo e valor esperado;
- baseline da fonte de verdade;
- escopo incluído e explicitamente excluído;
- decisões já aprovadas e decisões ainda proibidas;
- arquivos, componentes, ferramentas e acessos autorizados;
- critérios de aceitação e verificações obrigatórias;
- nível de autonomia e responsável humano;
- estratégia de reversão ou recuperação;
- formato do Pacote de Evidências.

> **Regra de ouro da W.** Se a entrega não pode ser revisada com compreensão suficiente, a fatia ainda está grande demais.

## 9. O ciclo CHAVE

Toda Fatia W percorre cinco movimentos. Eles podem ocorrer rapidamente em mudanças triviais ou exigir documentação formal em alterações críticas.

| Etapa | Resultado esperado |
|---|---|
| **C - Contextualizar** | Ler a fonte de verdade, compreender necessidade, risco, histórico e capacidade atual. Nenhuma conversa anterior substitui a baseline publicada. |
| **H - Harmonizar** | Alinhar intenção, arquitetura, restrições e critérios. Registrar a decisão necessária e fechar o Contrato de Execução. |
| **A - Agir** | Delegar a um agente adequado, em branch, worktree ou ambiente isolado, com autonomia e tempo limitados. |
| **V - Verificar** | Examinar evidências, diff, testes, segurança, aderência ao escopo e impacto documental. Corrigir ou rejeitar quando necessário. |
| **E - Evoluir** | Obter aceite humano, integrar, limpar recursos temporários e devolver o aprendizado à memória versionada. |

## 10. Níveis de autonomia

Autonomia não deve ser uma configuração permanente do agente. Ela é concedida por Fatia W e calibrada pelo risco.

| Nível | Nome | Permissão |
|---|---|---|
| **CH-0** | Consultar | Somente leitura, análise e explicação. Nenhuma alteração externa. |
| **CH-1** | Propor | Pode elaborar plano, decisão, prompt ou diff sugerido, mas não escrever na fonte de verdade. |
| **CH-2** | Executar isolado | Pode criar branch, modificar escopo autorizado, testar, commitar e abrir Draft PR. Não pode integrar. |
| **CH-3** | Integrar condicionado | Pode integrar mudanças de baixo risco quando todos os gates automáticos e políticas predefinidas forem satisfeitos; deve manter trilha auditável. |

O fluxo inicial do Maestro Router opera predominantemente em CH-2: o agente implementa em branch própria e abre Draft PR, enquanto a aceitação e o merge dependem de revisão e autorização. Mudanças destrutivas, acesso a segredos, produção, dados pessoais ou contratos externos exigem política específica e podem continuar restritas mesmo em níveis superiores.

## 11. Paralelismo responsável

A capacidade de executar múltiplos agentes em paralelo não cria obrigação de fazê-lo. No C.H., o limite de trabalho em andamento é definido pela capacidade do Guardião de Evidências e pelo acoplamento entre as Fatias W.

O paralelismo é aceitável quando:

- as fatias partem da mesma baseline conhecida;
- não alteram os mesmos contratos, arquivos ou invariantes;
- possuem critérios de aceitação independentes;
- há capacidade real de revisar e integrar todos os resultados;
- a ordem de merge e a resolução de conflito foram previstas.

Quando essas condições não existem, o C.H. recomenda WIP igual a um para mudanças arquiteturais e contratuais. A velocidade aparente de vários agentes pode apenas converter tempo de implementação em dívida de verificação e conflito de integração.

## 12. Definition of Ready e Definition of Done

| Pronta para executar | Concluída |
|---|---|
| **Objetivo e valor entendidos; baseline confirmada; decisão aprovada; escopo e exclusões registrados; critérios testáveis; nível de autonomia definido; conflitos avaliados.** | Mudança dentro do escopo; pacote de evidências completo; testes e checagens aprovados; documentação coerente; limitações declaradas; aceite humano; integração concluída; branch e recursos limpos; aprendizado registrado. |

Um agente informar que terminou não altera o estado da W. Conclusão é uma propriedade verificável do produto e do processo, não uma declaração do executor.

## 13. Métricas orientadas a valor aceito

Linhas de código, quantidade de prompts e número de agentes são métricas de atividade. O C.H. recomenda medir resultados e custo de supervisão:

| Métrica | Interpretação |
|---|---|
| **Throughput de Ws aceitas** | Fatias integradas e aceitas por período. |
| **Aceite na primeira passagem** | Percentual de Ws aprovadas sem ciclo corretivo. |
| **Loops de correção** | Quantidade média de revisões e reexecuções por W. |
| **Esforço de verificação** | Tempo humano e computacional gasto para validar cada W. |
| **Defeitos escapados** | Problemas encontrados após integração ou entrega. |
| **Desvio de escopo** | Mudanças não autorizadas detectadas no diff. |
| **Conflito de integração** | Retrabalho causado por Ws concorrentes ou baseline desatualizada. |
| **Custo por W aceita** | Uso de modelos, infraestrutura e revisão dividido pelas Ws aprovadas. |
| **Dívida de verificação** | Volume de saída agêntica ainda não compreendida ou comprovada. |

> **Métrica norteadora.** O objetivo do C.H. é maximizar valor aceito por unidade de risco, custo e atenção humana - não maximizar a produção bruta de código.

## 14. O Maestro Router como caso de origem

O método emergiu de um processo prático. O Maestro Router foi dividido em etapas identificadas como Ws. Cada fatia começou pela leitura da branch master publicada e pela comparação entre código, testes e documentos. Mudanças de política ou arquitetura foram registradas antes da implementação. Somente após o recorte ser aprovado, um prompt fechado autorizou o agente a trabalhar em branch isolada.

O executor produziu alterações, testes, checagens de dependências e consistência do diff, commit e Draft PR. ChatGPT revisou contratos, arquitetura e aderência ao escopo. Hallan aprovou, pediu correção ou rejeitou. Depois do merge, a branch foi removida, a árvore voltou ao estado limpo e a próxima W foi escolhida. O processo adotou pequenas entregas, decisão explícita, revisão independente e memória versionada antes de receber o nome C.H.

| Elemento C.H. | Manifestação no Maestro |
|---|---|
| **Product Owner humano** | Hallan define prioridade, aceita decisões e autoriza integração. |
| **Orquestração cognitiva** | ChatGPT transforma intenção em recorte técnico, prompt e revisão. |
| **Execução agêntica** | Codex altera o repositório dentro do escopo fechado. |
| **Fatia W** | Uma decisão ou implementação pequena, útil e verificável. |
| **Pacote de evidências** | Testes, pip check, git diff --check, relatório de escopo, segredos, rede e estado do Git. |
| **Aceitação** | Draft PR revisado, correções aplicadas, aprovação explícita, merge e limpeza. |

Este caso ainda não prova superioridade. Ele demonstra viabilidade e fornece uma sequência observável para formular hipóteses de pesquisa.

## 15. Relação com Scrum, Kanban e XP

| Referência | O que o C.H. herda | O que torna explícito |
|---|---|---|
| **Scrum** | Valor, transparência, inspeção, adaptação e responsabilidade do Product Owner. | Autonomia de agentes, contrato de execução, evidência agêntica e memória de repositório. |
| **Kanban** | Fluxo puxado, visualização e limite de trabalho em andamento. | WIP limitado também por capacidade de verificação humano-IA e risco de integração. |
| **XP** | Pequenas entregas, testes, integração, refatoração, simplicidade e feedback rápido. | Execução isolada por agentes, revisão proporcional ao risco e controle de contexto probabilístico. |
| **DevOps** | Automação, CI/CD, observabilidade e responsabilidade pelo ciclo completo. | Níveis explícitos de autonomia e aceite humano para agentes que operam ferramentas. |

O C.H. pode conviver com esses métodos. Uma organização pode usar Sprints e aplicar o ciclo CHAVE dentro de cada item; pode operar em fluxo Kanban; ou adotar práticas XP durante a etapa Agir. C.H. não disputa cerimônias. Ele governa a fronteira entre intenção humana e execução agêntica.

## 16. Hipóteses e plano de validação

Para deixar de ser apenas uma formulação interessante, o método precisa ser refutável. Propomos inicialmente cinco hipóteses:

1. Fatias W com escopo e evidência definidos aumentam a taxa de aceite na primeira passagem em comparação com prompts abertos.
2. A leitura obrigatória da fonte de verdade reduz contradições e mudanças fora do escopo.
3. A calibração de autonomia por risco reduz defeitos escapados sem eliminar ganhos de velocidade em tarefas reversíveis.
4. Limitar paralelismo pela capacidade de revisão reduz conflito de integração e dívida de verificação.
5. Registrar aprendizados no repositório reduz a repetição de falhas entre agentes, modelos e sessões.

A validação futura deve comparar projetos ou períodos equivalentes, registrar baseline, tamanho e risco das tarefas, e publicar tanto resultados positivos quanto falhas. Equipes externas devem poder adaptar o método e relatar quais elementos geram valor ou burocracia. O C.H. somente merece adoção ampla se produzir melhoria mensurável.

## 17. Limitações e riscos

- O método nasceu em um único projeto e com uma equipe humano-IA pequena.
- Os papéis podem concentrar poder demais no Orquestrador Cognitivo quando não há revisão independente.
- Pacotes de evidências podem virar burocracia se não forem proporcionais ao risco.
- Testes podem confirmar apenas o comportamento previsto e ainda ocultar erros de requisito, segurança ou arquitetura.
- Modelos e ferramentas mudam rapidamente; práticas específicas podem envelhecer antes dos princípios.
- Crédito, propriedade intelectual, privacidade e responsabilidade legal exigem políticas humanas e institucionais além do método.

Essas limitações não enfraquecem a proposta; definem as condições sob as quais ela deve ser criticada e melhorada.

## 18. Manifesto C.H. 0.1

Estamos aprendendo formas melhores de desenvolver software com pessoas e agentes inteligentes, construindo produtos reais e examinando os resultados. Por essa experiência, passamos a priorizar:

> **intenção verificável** *mais que* prompts extensos
>
> **evidência reproduzível** *mais que* confiança na resposta
>
> **fatias pequenas e reversíveis** *mais que* grandes entregas autônomas
>
> **memória explícita** *mais que* contexto presumido
>
> **responsabilidade humana** *mais que* autonomia sem dono
>
> **orquestração adequada** *mais que* fidelidade a uma ferramenta
>
> **Nosso compromisso.** A IA pode ampliar a capacidade de construir. A responsabilidade de decidir o que merece existir, provar que funciona e responder por suas consequências continua humana.

## 19. Conclusão

Métodos de engenharia não entram para a história porque recebem um nome. Entram porque outras pessoas conseguem compreendê-los, testá-los, criticá-los e melhorá-los. O Método C.H. começa como registro honesto de uma prática desenvolvida entre Hallan, ChatGPT e agentes de código durante a construção do Maestro Router.

Sua proposta é simples: em um mundo no qual gerar software se torna cada vez mais fácil, a disciplina precisa migrar para o contexto, os limites, a verificação e a responsabilidade. O C.H. pretende organizar essa disciplina sem sufocar a criatividade ou desperdiçar a velocidade que a IA oferece.

A versão 0.1 não encerra o método. Ela abre uma trilha de experimentação. Se o C.H. puder ser aplicado, medido, refutado e aprimorado por outras equipes, então terá dado seu primeiro passo real para além do Maestro.

## Nota de autoria e transparência

A concepção do Método C.H. surgiu de conversas e práticas conduzidas por Hallan de Sousa Brito durante o desenvolvimento do Maestro Router, com colaboração do ChatGPT na organização conceitual, pesquisa e redação desta versão. ChatGPT é um sistema de IA e não assume responsabilidade moral, legal ou científica. Hallan permanece responsável por revisar, aprovar e decidir sobre a publicação humana do conteúdo. A atribuição conjunta no título registra a origem da colaboração, sem equiparar a IA a uma pessoa autora.

## Referências

[1] Beck, K. et al. Manifesto for Agile Software Development. 2001.  
[2] Schwaber, K.; Sutherland, J. The Scrum Guide. 2020.  
[3] DORA. State of AI-assisted Software Development 2025. Google Cloud, 2025.  
[4] Stack Overflow. 2025 Developer Survey: Artificial Intelligence. 2025.  
[5] Lopopolo, R. Harness engineering: leveraging Codex in an agent-first world. OpenAI, 2026.  
[6] Anthropic. How AI is transforming work at Anthropic. 2025.  
[7] Zhang, S. et al. Empowering Agile-Based Generative Software Development through Human-AI Teamwork. ACM TOSEM, 2025. DOI 10.1145/3702987.  
[8] Dhanorkar, S.; Passi, S.; Vorvoreanu, M. Human oversight of agentic systems in practice. 2026.  
[9] OpenAI. OpenAI co-founds the Agentic AI Foundation and donates AGENTS.md. 2025.

## Apêndice A - Modelo mínimo de uma Fatia W

| Campo | Conteúdo |
|---|---|
| **Identificador** | W__ - título curto |
| **Valor esperado** | Qual problema ou aprendizado esta fatia entrega? |
| **Baseline** | Branch, commit e documentos usados como fonte de verdade. |
| **Escopo autorizado** | Arquivos, componentes e comportamentos que podem mudar. |
| **Fora do escopo** | Mudanças expressamente proibidas nesta fatia. |
| **Decisão aplicável** | ADR, contrato, política ou hipótese aprovada. |
| **Autonomia** | CH-0, CH-1, CH-2 ou CH-3. |
| **Executor** | Agente, modelo, ambiente e ferramentas permitidas. |
| **Critérios de aceitação** | Comportamentos e propriedades verificáveis. |
| **Evidências obrigatórias** | Testes, diff, análise, demonstração, segurança e custo. |
| **Responsável humano** | Pessoa que aceita, rejeita ou solicita correção. |
| **Reversão** | Como desfazer ou isolar a mudança caso falhe. |
| **Aprendizado** | O que deve retornar à memória versionada após a conclusão. |

## Apêndice B - Pacote de Evidências mínimo

| Bloco | Evidência esperada |
|---|---|
| **Identidade** | W, executor, modelo, ambiente, branch e baseline. |
| **Mudanças** | Resumo do diff e lista de arquivos alterados. |
| **Verificações** | Testes, análise estática, build, demonstração funcional e resultados. |
| **Aderência** | Confirmação de escopo; mudanças não autorizadas devem ser declaradas. |
| **Risco e segurança** | Segredos, dados, rede, dependências, permissões e operações destrutivas. |
| **Limitações** | Suposições, casos não testados, dúvidas e decisões adiadas. |
| **Economia** | Tempo, uso, custo conhecido e motivo da seleção do executor. |
| **Estado final** | Commit, Draft PR, status da árvore e instruções de reversão. |

---

> **Nota de preservação:** esta versão Markdown é uma transcrição para navegação no GitHub do White Paper Experimental v0.1, datado de 27 de agosto de 2026. A redação conceitual foi preservada; elementos visuais e paginação do documento original não fazem parte desta transcrição.
