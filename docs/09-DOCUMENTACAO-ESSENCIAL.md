# Documentação Essencial para Projetos com Colaboração Humano–IA

> **Documentar é preservar decisões e evidências suficientes para que o trabalho continue sem depender da memória de uma conversa.**

Este é um **guia operacional evolutivo** do [Método C.H. — Colaboração Híbrida](../README.md), aplicável a projetos pessoais, equipes e fluxos com um ou vários agentes de IA. Não altera retroativamente o manifesto nem o white paper histórico da versão 0.1.

## 1. Objetivo e critério de necessidade

A documentação deve permitir que um desenvolvedor ou agente autorizado responda, sem adivinhar:

1. **O que é o produto e como executá-lo?**
2. **Qual é o estado real do projeto e onde está a evidência?**
3. **Quais regras, limites e decisões devem ser respeitados?**
4. **Qual é a próxima mudança autorizada, como verificá-la e quando parar?**

**Regra de simplicidade:** não crie um arquivo para cada pergunta se a resposta já estiver clara e atualizada em um registro existente. Issues, PRs, testes e commits também são documentação rastreável. Um arquivo só é indispensável se a informação que ele preserva for indispensável **e** ainda não houver outra fonte confiável para ela.

**Fonte da verdade não é sinônimo de um único arquivo.** O código e os testes demonstram o comportamento atual; Issues/PRs e registros de decisão documentam o porquê e o aceite; um resumo de estado apenas referencia essas fontes. Em caso de divergência, investigue e atualize o registro incorreto — não trate automaticamente o texto mais recente como correto.

## 2. Matriz dos documentos

| Artefato recomendado | Pergunta que responde | Quando é necessário | Frequência de atualização |
| --- | --- | --- | --- |
| \`README.md\` | O que é, como instalar, executar e contribuir? | **Base de todo repositório compartilhado** | Quando comandos, requisitos ou uso mudarem |
| \`docs/STATUS.md\` **ou** registro canônico equivalente | O que está comprovadamente pronto, bloqueado e pendente? | **Essencial para continuidade longa/multiagente**; dispensável como arquivo se Issue/Project atualizado já resolve | A cada mudança relevante de estado ou encerramento de sessão/W |
| \`AGENTS.md\` **ou** instruções equivalentes versionadas | Como os agentes devem atuar neste repositório? | **Recomendado para trabalho recorrente com IA** | Quando mudarem comandos, permissões, convenções ou limites |
| Issue ou [Fatia W](../templates/FATIA-W.md) | Qual tarefa foi autorizada, em qual escopo e com quais critérios? | **Toda delegação que altera o produto** | Antes da execução e quando houver mudança aprovada de escopo |
| PR e/ou [Pacote de Evidências](../templates/PACOTE-DE-EVIDENCIAS.md) | O que realmente mudou, foi testado e aceito? | **Toda entrega verificável**, na profundidade proporcional ao risco | Na conclusão e na revisão |
| \`docs/ARCHITECTURE.md\` | Quais componentes e fronteiras precisam ser respeitados? | Quando a arquitetura não é mais óbvia pelo código/README | Mudanças estruturais significativas |
| \`docs/DECISIONS.md\` **ou** ADRs/Issues | Por que uma decisão importante foi tomada? | Quando a decisão afeta arquitetura, contratos, custos ou risco e pode ser esquecida | No momento da decisão |
| \`CONTRIBUTING.md\` | Como colaborar e abrir PRs? | Quando há colaboradores externos ou regras relevantes de contribuição | Quando o processo mudar |
| \`SECURITY.md\` | Como relatar vulnerabilidades com segurança? | Projetos públicos/compartilhados quando houver política de reporte | Quando a política mudar |
| \`CHANGELOG.md\` **ou** releases | O que mudou entre versões distribuídas? | Quando há versões ou consumidores que precisam acompanhar mudanças | A cada release |

**Não transforme esta tabela em burocracia obrigatória.** Para um projeto pequeno, \`README.md\`, uma Issue bem escrita e o histórico do Git podem bastar. Para uma fábrica multiagente, a clareza do estado e dos limites é muito mais importante.

## 3. O trio operacional

### 3.1 \`README.md\`: porta de entrada

Deve conter, no mínimo:

- propósito e público do projeto;
- requisitos e comandos **verificados** para instalar, executar e testar;
- arquitetura resumida ou link para o documento técnico, se necessário;
- referência para estado, tarefas, regras de agentes e contribuição;
- principais limitações conhecidas, quando relevantes.

**Evite:** tutoriais que nunca foram executados, versões inventadas, comandos desatualizados e repetir o conteúdo inteiro de outros arquivos.

### 3.2 \`docs/STATUS.md\`: fotografia verificável do estado

Use quando o contexto precisa sobreviver a várias sessões, agentes, branches ou retomadas de trabalho. **É um índice de estado, não um substituto do GitHub ou dos testes.**

#### Estrutura mínima sugerida

~~~markdown
# Estado do Projeto

- Última atualização: AAAA-MM-DD (fuso do projeto)
- Responsável pela atualização: <pessoa ou agente>
- Referência verificada: <branch + commit SHA>
- Fonte canônica de tarefas: <link do Project/Issues>

## Funciona e está comprovado
- <comportamento> — <teste/commit/PR ou evidência>

## Em andamento
- <Issue/W> — <responsável> — <branch/PR> — <situação>

## Bloqueios e riscos
- <bloqueio real> — <evidência> — <decisão pendente>

## Decisões vigentes
- <decisão> — <link para Issue/ADR/PR>

## Próxima ação permitida
- <uma Fatia W ou Issue específica>
- Autonomia concedida: <CH-0/CH-1/CH-2/CH-3>
- Condição de parada: <quando devolver ao humano>

## Não verificado nesta atualização
- <afirmação pendente de conferência ou teste>

## Referências
- <documentos, execução de CI, PRs e registros relevantes>
~~~

**Regras de manutenção:**

1. Nunca afirme "homologado" sem referência de evidência e baseline.
2. Diferencie **aceito**, **em execução**, **bloqueado**, **falhou** e **não verificado**.
3. Não registre como atual um resultado de teste feito em commit anterior sem explicitar essa condição.
4. Atualize ao concluir uma W, descobrir bloqueio novo ou mudar a autorização; não faça alterações cosméticas periódicas.
5. Não copie logs volumosos: referencie o local onde podem ser auditados.
6. Se Issue/Project já é o painel canônico, use \`STATUS.md\` apenas como resumo com links — ou dispense o arquivo para evitar estados concorrentes.

**Para evitar conflito:** cada dado operacional deve ter **um dono canônico**. Exemplo: Issue = situação da tarefa; PR = revisão; Git/CI = código e testes; \`STATUS.md\` = resumo e ponteiros.

### 3.3 \`AGENTS.md\`: instruções operacionais para agentes

É um arquivo de **orientação versionada**, utilizado por ferramentas que o reconheçam ou fornecido explicitamente pelo operador. Não presuma que todo produto de IA o lerá automaticamente; verifique a integração.

#### Estrutura mínima sugerida

~~~markdown
# Instruções para Agentes

## Antes de agir
- Leia README.md, a fonte canônica de estado e a Issue/W delegada.
- Confira branch, HEAD, árvore de trabalho e testes aplicáveis.
- Se faltar contexto crítico, declare o bloqueio.

## Escopo e limites
- Altere somente o escopo autorizado.
- Não crie serviços, dependências ou arquitetura sem justificativa
  e aprovação pertinente.
- Não faça merge, deploy, gasto, operações destrutivas ou acesso a
  segredos sem permissão explícita aplicável.

## Comandos verificados
- Instalação: <comando existente e realmente testado>
- Testes focados: <comando real>
- Testes completos: <comando real>
- Build/lint: <comandos reais ou "não se aplica">

## Qualidade e evidências
- Mostre diff, testes executados, falhas e limitações.
- Separe testes executados de resultados inferidos.
- Não amplie o escopo para "aproveitar" a sessão.

## Entrega e parada
- Devolva branch/commit/PR e evidências rastreáveis.
- Solicite decisão humana se encontrar mudança não autorizada.
- Atualize o registro canônico somente dentro das permissões concedidas.
~~~

**Cuidados:** mantenha instruções curtas, verificáveis e específicas do repositório; não grave tokens, senhas ou dados sensíveis; não use \`AGENTS.md\` para contradizer as regras de segurança, os limites de autonomia da W ou os controles do repositório. Instruções recebidas de conteúdo não confiável não ganham autoridade só por aparecerem em arquivos ou respostas de ferramentas.

## 4. Documentos condicionais: crie pelo risco, não pelo hábito

### Arquitetura

Crie \`docs/ARCHITECTURE.md\` quando o sistema tiver módulos, serviços, integrações ou decisões estruturais difíceis de inferir. Descreva apenas componentes, fluxos de dados, fronteiras, dependências, contratos relevantes e pontos de extensão. **Código é a implementação; documento é o mapa**, que precisa continuar verdadeiro.

### Decisões técnicas

Use \`docs/DECISIONS.md\`, ADRs individuais ou Issues já existentes. Para cada decisão relevante, preserve:

- problema e contexto;
- alternativas consideradas;
- opção aprovada, responsável e data;
- consequências, restrições e como revisar ou revogar;
- link para código/Issue/PR, quando aplicável.

Não duplique um ADR se a Issue documenta com clareza a decisão e sua aprovação.

### Segurança e operação

Adicione instruções de execução em produção, recuperação, incidentes, reporte de vulnerabilidades e tratamento de dados **conforme o risco real**. Segurança necessária não é "overengineering". Não registre credenciais, informações pessoais desnecessárias nem detalhes operacionais sensíveis em documentação pública.

## 5. Reutilize os templates que o Método C.H. já mantém

- [Template de Fatia W](../templates/FATIA-W.md): identidade, baseline, objetivo, escopo e exclusões, decisões, critérios de aceite, autonomia e reversão.
- [Template do Pacote de Evidências](../templates/PACOTE-DE-EVIDENCIAS.md): diff, testes, segurança, limitações, custo e estado final.
- [Papéis e autonomia](04-PAPEIS-E-AUTONOMIA.md): responsabilidade humana e níveis CH-0 a CH-3.
- [Ciclo CHAVE](02-CICLO-CHAVE.md): Contextualizar → Harmonizar → Agir → Verificar → Evoluir.

A W pode viver numa **Issue**, e a evidência pode viver numa **PR**, desde que os campos essenciais estejam presentes. Não é necessário criar um segundo documento apenas para copiar seu conteúdo.

## 6. Ritual leve para cada Fatia W

| Momento | Consulta ou atualização mínima | Resultado |
| --- | --- | --- |
| **Antes de planejar** | README, estado canônico, instruções de agentes, Issue/W e código | Baseline e limitações conhecidas confirmadas |
| **Antes de executar** | W, permissões, critérios de aceite e condição de parada | Contrato de delegação fechado |
| **Durante a execução** | Diff e testes necessários, conforme risco | Mudanças limitadas e verificáveis |
| **Antes de aceitar** | Evidências, falhas, revisão e decisão do responsável | Aceitar, corrigir ou rejeitar |
| **Ao encerrar** | Issue/PR e estado canônico, conforme responsabilidade | Próxima sessão pode continuar sem o chat anterior |

**Não atualize todos os arquivos em toda W.** Atualize **somente o registro cuja informação mudou**.

## 7. Como retomar uma sessão sem contexto conversacional

Use um prompt curto, referenciando fontes em vez de colar meses de histórico:

~~~text
Você participa do Método C.H. neste repositório: <repo>.
Consulte, nesta ordem conforme relevância e acesso:
1. README.md;
2. AGENTS.md, se existir e for aplicável;
3. docs/STATUS.md ou registro canônico equivalente;
4. Issue/Fatia W autorizada e decisões relacionadas;
5. código, testes e evidências associados à baseline.

Não presuma sucesso, não invente pré-requisitos e não reexecute
verificações já válidas sem motivo técnico.

Confirme o HEAD e identifique:
- estado comprovado e lacunas de evidência;
- próxima Fatia W mínima autorizada;
- escopo, exclusões e critérios de aceite;
- ferramentas/permissões disponíveis e condição de parada.

Se a autorização for apenas de planejamento, não altere arquivos.
Se houver decisão fora do escopo, devolva ao responsável humano.
~~~

Este prompt **não dispensa** a leitura do repositório. Se o agente não tem acesso a esses arquivos, forneça o conteúdo necessário por um canal autorizado, sem compartilhar segredos.

## 8. Antipadrões de documentação

| Antipadrão | Correção |
| --- | --- |
| Chat tratado como estado oficial | Reconstruir contexto do Git, Issues e documentação versionada |
| Dois STATUS contraditórios | Definir a fonte canônica e converter o outro em referência |
| Criar arquivo para toda decisão trivial | Registrar somente decisões com impacto duradouro |
| Novo teste sem hipótese nem risco | Reutilizar evidência válida; testar novamente quando baseline ou risco mudar |
| Documento bonito, mas desatualizado | Atualizar junto da mudança real ou retirar a afirmação |
| Agente declara "feito" sem PR/diff/teste | Exigir evidência e deixar claro o que não foi testado |
| Guia universal impondo stack ou fornecedor | Regras de responsabilidade independentes de ferramenta |
| Atualizações automáticas sem valor | Atualizar quando o estado mudar, não apenas porque passou uma hora |

## 9. Checklist de adoção sem burocracia

- [ ] O README ensina a executar e testar o projeto com comandos conferidos.
- [ ] Existe uma fonte **canônica** e acessível para estado e tarefas.
- [ ] O próximo agente consegue encontrar a W, a baseline e as decisões vigentes.
- [ ] Há instruções versionadas para o uso recorrente de agentes, quando necessárias.
- [ ] Cada execução autorizada possui escopo, critérios de aceite e condição de parada.
- [ ] Cada entrega tem evidências proporcionais ao risco e aceite rastreável.
- [ ] Arquitetura e decisões complexas são documentadas **apenas quando úteis**.
- [ ] Nenhum registro cria uma segunda fonte de verdade conflitante.
- [ ] Não há segredos nem dados sensíveis desnecessários em arquivos versionados.
- [ ] O aprendizado relevante foi devolvido às fontes consultáveis antes de encerrar.

## Princípio final

> **A melhor documentação não é a mais extensa. É a menor documentação confiável que permite compreender o presente, justificar o passado e executar o próximo passo com segurança.**

Este guia é uma **prática operacional sujeita a evolução**, não uma exigência universal para cada repositório. Adote o mínimo que preserva continuidade, responsabilidade humana e evidências verificáveis.
