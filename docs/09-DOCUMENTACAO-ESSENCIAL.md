# Documentação essencial — só o necessário

> **Um novo desenvolvedor ou agente deve conseguir continuar o trabalho sem depender de um chat antigo.**

Este guia operacional do [Método C.H.](../README.md) não exige arquivos por obrigação. **Use o que já funciona.** Código, testes, Git, Issues e PRs são fontes verificáveis; não crie uma segunda versão contraditória do mesmo estado.

## A receita mínima

| Registro | Para quê? | Quando usar? |
|---|---|---|
| `README.md` | O que é e como instalar, executar e testar | Todo repositório compartilhado |
| `docs/STATUS.md` **ou** Issue/Project | O que funciona, está bloqueado e vem depois | Projetos longos ou com vários agentes |
| `AGENTS.md` **ou** instruções equivalentes | Como agentes devem operar, testar e parar | Uso recorrente de IA |
| Issue **ou** [Fatia W](../templates/FATIA-W.md) | Uma tarefa, limites e critérios de aceite | Antes de delegar mudanças |
| PR **ou** [Pacote de Evidências](../templates/PACOTE-DE-EVIDENCIAS.md) | Diff, testes e revisão | Antes de aceitar uma entrega |

**Só quando necessário:** `ARCHITECTURE.md` (arquitetura difícil de entender), ADR/Issue (decisão duradoura), `SECURITY.md` (política de reporte) e changelog (releases). Simplicidade não dispensa controles exigidos pelo risco.

## `STATUS.md` em poucas linhas

~~~markdown
# Estado do projeto
- Atualizado: <data, responsável, branch e commit>
- Funciona: <resultado + teste ou PR>
- Em andamento: <Issue + responsável>
- Bloqueado: <problema + evidência>
- Decisão vigente: <link>
- Próxima tarefa autorizada: <uma W + autonomia>
- Não verificado: <limitação>
~~~

**Importante:** o STATUS é um **resumo com links**, não um segundo Kanban. Atualize somente quando o estado mudar. Se o Project/Issues já resolve, não crie o arquivo.

## `AGENTS.md` em poucas linhas

~~~markdown
# Instruções para agentes
- Antes: leia README, estado e Issue delegada; confira HEAD.
- Escopo: só altere o autorizado; decisões extras voltam ao humano.
- Comandos: <instalação, testes e build realmente verificados>
- Limites: sem merge, deploy, gasto ou destruição sem permissão.
- Entrega: diff, testes executados, limitações e PR.
- Parada: <condição acordada com o responsável humano>
~~~

Nem toda IA lê `AGENTS.md` automaticamente. Forneça essas regras pelo canal apropriado. **Nunca versionar segredos.**

## Ciclo diário — sem cerimônia extra

1. **Começar:** confirme README, fonte de estado, Issue e commit.
2. **Executar:** uma W pequena, com limites e aceitação definidos.
3. **Verificar:** mostre o que mudou, rodou e falhou.
4. **Encerrar:** registre decisão, evidência e próxima ação **onde isso já é controlado**.

**Antipadrões:** copiar logs para vários arquivos, criar STATUS concorrentes, registrar testes nunca feitos e atualizar documentos sem mudança real.

**Princípio final:** **a melhor documentação é a menor que permite continuar com segurança.**

*Prática operacional evolutiva. Preserva o manifesto e o white paper histórico v0.1.*
