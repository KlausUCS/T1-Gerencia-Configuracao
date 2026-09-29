# CAO (2026) — *Agentic Software: How AI Agents Are Restructuring the Software Paradigm*

> **Referência:** CAO, Z. *Agentic Software: How AI Agents Are Restructuring the Software Paradigm*. arXiv, 2026.
>
> **Papel no trabalho:** artigo utilizado para discutir a transformação da engenharia de software a partir do uso de agentes baseados em LLMs.

---

## 1. Que tipo de texto é este

O artigo apresenta uma discussão **teórica e prospectiva** sobre como agentes de IA podem modificar a engenharia de software. Cao não realiza um experimento próprio; sua argumentação é construída a partir de conceitos, trabalhos anteriores e benchmarks como SWE-bench e EvoClaw.

A tese central é que agentes de IA podem representar mais do que uma ferramenta de auxílio à programação: eles podem alterar a forma como o software é construído. Enquanto no modelo tradicional o desenvolvedor define previamente grande parte da lógica, sistemas agentivos podem tomar parte das decisões durante a execução, utilizando LLMs, ferramentas e mecanismos de avaliação.

É importante destacar que essa é uma **proposta de evolução**, e não uma transformação já comprovada empiricamente.

---

## 2. A tese

Cao argumenta que a engenharia de software pode caminhar em direção a um novo paradigma denominado **Agentic Engineering**.

| Modelo                              | Característica principal                                                             |
| ----------------------------------- | ------------------------------------------------------------------------------------ |
| **Software tradicional**            | O desenvolvedor define previamente a lógica por meio do código.                      |
| **IA auxiliando o desenvolvimento** | A IA produz ou modifica código sob orientação humana.                                |
| **Software agentivo**               | O agente recebe objetivos, planeja ações, utiliza ferramentas e adapta sua execução. |

A principal mudança está no papel do código: parte das decisões necessárias para alcançar um objetivo pode ser tomada pelo agente durante a execução.

Wang et al. (2024) reforçam essa interpretação ao descrever agentes de engenharia de software por meio de **percepção, memória e ação**, mostrando que eles não devem ser entendidos apenas como geradores de código.

Cao também prevê uma mudança no papel do desenvolvedor, que pode assumir maior responsabilidade por **objetivos, arquitetura, avaliação, coordenação e supervisão**.

---

## 3. As evidências apresentadas

O artigo utiliza diferentes tipos de evidência, que não possuem o mesmo peso científico:

| Evidência             | Natureza                  | O que demonstra                                                                  |
| --------------------- | ------------------------- | -------------------------------------------------------------------------------- |
| **SWE-bench**         | Benchmark acadêmico       | Avalia agentes na resolução de problemas reais de repositórios GitHub.           |
| **EvoClaw**           | Benchmark acadêmico       | Avalia agentes durante evolução contínua de software.                            |
| **Wang et al.**       | Revisão acadêmica         | Sistematiza pesquisas sobre agentes em engenharia de software.                   |
| **Becker et al.**     | Experimento controlado    | Avalia impacto de IA na produtividade de desenvolvedores em contexto específico. |
| **Kumar e Ramagopal** | Relato técnico/industrial | Apresenta resultados de um piloto multiagente específico.                        |

O **SWE-bench** possui originalmente 2.294 problemas provenientes de 12 repositórios Python. Seu diferencial é avaliar tarefas próximas de manutenção de software, e não apenas geração de pequenos trechos de código.

Entretanto, resolver uma tarefa isolada não significa conseguir manter um sistema durante sua evolução. Essa limitação é justamente explorada pelo **EvoClaw**.

---

## 4. Análise crítica

### 4.1 Mudança de paradigma não significa desaparecimento do código

Os agentes podem alterar o nível de abstração do desenvolvimento, mas isso não significa que o código deixe de ser importante.

Mesmo em sistemas agentivos continuam existindo **ferramentas, memória, permissões, infraestrutura, interfaces, testes e mecanismos de avaliação**.

Assim, uma interpretação mais cautelosa é considerar uma possível mudança de **"código como centro do sistema" para "agente como novo nível de abstração"**, e não o desaparecimento da engenharia de software.

---

### 4.2 Resolver uma tarefa não é o mesmo que manter um software

O SWE-bench avalia problemas delimitados. O EvoClaw procura avaliar uma situação diferente: o agente precisa continuar modificando o sistema sem comprometer alterações anteriores.

No EvoClaw, foram avaliados **12 modelos em quatro frameworks**. A pontuação passou de valores superiores a **80% em tarefas isoladas para, no máximo, 38% em cenários de evolução contínua**.

Esse número deve ser entendido como uma **métrica específica do benchmark**, e não como uma taxa geral de capacidade dos agentes.

O resultado, porém, evidencia uma diferença importante entre resolver uma tarefa individual e preservar a integridade de um sistema durante sua evolução.

---

### 4.3 Mais autonomia aumenta a importância da avaliação

Quanto maior a autonomia do agente, maior a importância de definir corretamente objetivos, restrições e critérios de avaliação.

Um agente pode produzir código que satisfaz determinados testes e ainda apresentar problemas não capturados por eles.

Assim, a automação não elimina necessariamente o trabalho humano: parte dele pode ser transferida da implementação para **especificação, arquitetura, validação e supervisão**.

---

### 4.4 Benchmarks não equivalem a produtividade

Resultados de benchmarks não devem ser confundidos automaticamente com produtividade profissional.

Becker et al. (2025), em um experimento da METR com **16 desenvolvedores e 246 tarefas**, encontrou aumento de aproximadamente **19% no tempo de conclusão** quando IA era permitida, utilizando ferramentas disponíveis entre fevereiro e junho de 2025.

Esse resultado é específico daquele contexto e não demonstra que IA reduz produtividade de maneira geral.

Posteriormente, a própria METR atualizou sua análise e observou que ferramentas mais recentes apresentavam sinais diferentes, mas que efeitos de seleção dificultavam estimar com segurança o tamanho do ganho.

Portanto, benchmarks medem principalmente **capacidade em determinadas tarefas**, enquanto produtividade depende também do contexto, do projeto, do desenvolvedor e das ferramentas utilizadas.

---

## 5. Relação com as perguntas norteadoras

**A IA está substituindo o programador ou mudando seu trabalho?**

As evidências fornecem maior suporte à ideia de **mudança das atividades** do que à substituição completa. O profissional pode assumir maior responsabilidade por intenção, arquitetura, coordenação e auditoria.

**O código ainda será importante?**

Sim. O próprio modelo agentivo continua utilizando código, embora parte dele possa ser gerada ou modificada dinamicamente pelo agente.

**Os agentes já conseguem desenvolver software sozinhos?**

Eles demonstram capacidade de executar determinadas tarefas, mas as evidências disponíveis ainda não demonstram autonomia confiável durante todo o ciclo de vida de sistemas complexos.

**Qual passa a ser o papel do engenheiro?**

No cenário proposto por Cao, ganham importância atividades como definição de objetivos, arquitetura, avaliação, coordenação e supervisão.

---

## 6. Como avaliar essa previsão

Cao propõe um **roadmap evolutivo**:

1. ferramentas de auxílio ao programador;
2. agentes executando tarefas completas;
3. equipes formadas por múltiplos agentes;
4. ecossistemas capazes de evoluir autonomamente.

Esses estágios representam uma **proposta de evolução**, não uma sequência empiricamente comprovada.

Para avaliar essa previsão, é mais relevante observar se os agentes conseguem passar de tarefas isoladas para **desenvolvimento contínuo**, mantendo qualidade, arquitetura e integridade do sistema.

---

## 7. Posicionamento sugerido para o grupo

> **Os agentes de IA representam uma mudança relevante na forma como software pode ser desenvolvido, pois permitem transferir parte das decisões de implementação para sistemas capazes de planejar e utilizar ferramentas. Entretanto, as evidências atuais mostram uma diferença importante entre resolver tarefas individuais e manter sistemas durante longos períodos. Assim, os estudos analisados fornecem maior suporte à interpretação de que a engenharia de software está passando por uma transformação do papel do profissional do que à conclusão de que ela será substituída. Especificação, arquitetura, avaliação, coordenação e supervisão tendem a ganhar importância, enquanto parte da implementação pode ser automatizada.**

A principal contribuição de Cao, portanto, é propor uma mudança de perspectiva: em vez de especificar detalhadamente **como** executar cada tarefa, o profissional pode cada vez mais definir **o que** precisa ser alcançado e delegar parte do "como" ao agente.

A questão em aberto é até que ponto essa autonomia poderá crescer sem comprometer **confiabilidade, manutenção e controle**. As evidências atuais indicam avanços relevantes, mas ainda não demonstram autonomia confiável durante todo o ciclo de vida de sistemas complexos.

---

## Referências

BECKER, Joel; RUSH, Nate; BARNES, Elizabeth; REIN, David. **Measuring the Impact of Early-2025 AI on Experienced Open-Source Developer Productivity**. arXiv, 2025. arXiv:2507.09089.

CAO, Zhenfeng. **Agentic Software: How AI Agents Are Restructuring the Software Paradigm**. arXiv, 2026. arXiv:2606.05608.

DENG, Gangda et al. **EvoClaw: Evaluating AI Agents on Continuous Software Evolution**. arXiv, 2026. arXiv:2603.13428.

JIMENEZ, Carlos E. et al. **SWE-bench: Can Language Models Resolve Real-World GitHub Issues?** ICLR, 2024. arXiv:2310.06770.

KUMAR, Renuka; RAMAGOPAL, Prashanth. **Agentic Engineering: How Swarms of AI Agents Are Redefining Software Engineering**. LangChain, 2026. Relato técnico/industrial.

METR. **We are Changing our Developer Productivity Experiment Design**. 2026.

WANG, Yanlin et al. **Agents in Software Engineering: Survey, Landscape, and Vision**. arXiv, 2024. arXiv:2409.09030.
