# O Futuro da Engenharia de Software na Era da Inteligência Artificial: Entre a Automação do Código e a Essência da Resolução de Problemas

## 1. Introdução: A Transformação da Profissão de Desenvolvedor

A disseminação da Inteligência Artificial (IA) generativa tem provocado discussões sobre o futuro da programação e da profissão de desenvolvedor. Ferramentas capazes de gerar, explicar, corrigir e modificar código levantam a possibilidade de que parte significativa das atividades tradicionalmente realizadas por programadores possa ser automatizada.

Entretanto, a Engenharia de Software não se limita à escrita de código. A partir da distinção apresentada por Fred Brooks (1986) entre dificuldades **essenciais** e **acidentais**, é possível observar que ferramentas de IA atuam principalmente sobre aspectos relacionados à representação e implementação do software, como sintaxe, código repetitivo e *boilerplate*. Isso não significa que problemas relacionados à definição dos requisitos, arquitetura, modelagem do domínio, validação e tomada de decisões sejam automaticamente eliminados.

Os estudos analisados neste trabalho apresentam resultados diferentes conforme o contexto. Experimentos controlados identificam ganhos de produtividade em determinadas tarefas, enquanto outras pesquisas apontam limitações relacionadas à qualidade, generalização, aprendizagem, manutenção e capacidade dos modelos de resolver problemas novos. Dessa forma, a literatura não sustenta uma conclusão simples de que a programação será eliminada, mas aponta para uma possível transformação das atividades e competências associadas à Engenharia de Software.

Nesse contexto, torna-se necessário analisar não apenas a capacidade da IA de produzir código, mas também sua capacidade de contribuir para a resolução de problemas complexos de Engenharia de Software.

---

# 2. Análise das Perguntas Norteadoras

## 2.1 O que a Engenharia de Software resolve de verdade?

A Engenharia de Software transcende a implementação técnica. Ela envolve a transformação de necessidades humanas e organizacionais em sistemas que precisam atender requisitos funcionais e não funcionais, manter qualidade, segurança, confiabilidade e capacidade de evolução.

Brooks (1986) argumenta que parte significativa da dificuldade do desenvolvimento de software está relacionada à sua **complexidade essencial**. Essa complexidade surge da necessidade de compreender o problema, definir abstrações, estabelecer relações entre componentes e atender às características específicas do domínio.

A IA generativa pode reduzir parte do esforço relacionado à implementação. Ferramentas como assistentes de programação conseguem gerar trechos de código, sugerir soluções e automatizar tarefas repetitivas. Entretanto, a geração de código não elimina automaticamente a necessidade de determinar se a solução atende corretamente ao problema.

Meyer (2023) chama atenção justamente para essa limitação. Sistemas baseados em modelos de linguagem produzem respostas estatisticamente plausíveis, mas isso não significa que exista uma garantia lógica de correção. Consequentemente, atividades de verificação e validação continuam sendo relevantes.

A perspectiva de Karpathy (2017), apresentada em *Software 2.0*, também mostra que a automação pode deslocar o trabalho para outros níveis. Quando parte da lógica deixa de ser expressa diretamente por código e passa a ser aprendida por modelos, tornam-se importantes questões relacionadas a dados, objetivos, treinamento e avaliação.

Assim, a Engenharia de Software não desaparece simplesmente quando a escrita de código é parcialmente automatizada. Parte da atividade pode ser deslocada para a definição do problema, seleção das estratégias, avaliação das soluções e supervisão dos sistemas produzidos.

---

## 2.2 Perspectiva Histórica: A Recorrência das "Soluções Milagrosas"

A expectativa de que uma nova tecnologia possa eliminar grande parte das dificuldades da programação não é recente.

Brooks (1986) já discutia a busca recorrente por uma tecnologia capaz de produzir grandes aumentos de produtividade. Sua argumentação é que determinadas dificuldades do desenvolvimento são inerentes à própria natureza do software e, portanto, não podem ser eliminadas simplesmente por uma nova ferramenta.

Ao longo da história da computação, diferentes tecnologias aumentaram o nível de abstração utilizado pelos desenvolvedores:

* **Linguagens de alto nível:** reduziram a necessidade de trabalhar diretamente com detalhes do hardware e da linguagem de máquina, tornando a programação mais acessível e produtiva.
* **Programação Orientada a Objetos:** introduziu mecanismos de encapsulamento, abstração e reutilização, facilitando a construção de sistemas complexos, mas sem eliminar a necessidade de decisões arquiteturais.
* **Ferramentas CASE e abordagens de baixo código:** procuraram reduzir a quantidade de programação manual por meio de abstrações, modelos e componentes reutilizáveis.
* **Software 2.0:** conforme Karpathy (2017), desloca parte da definição do comportamento do software para modelos treinados com dados.
* **IA generativa e agentes:** ampliam essa tendência ao permitir que sistemas produzam código, executem ferramentas e participem de várias etapas do desenvolvimento.

Essas transformações mostram um padrão importante: a redução do esforço necessário para uma determinada atividade pode permitir que sistemas mais complexos sejam construídos. Com isso, novas dificuldades e responsabilidades podem surgir em níveis superiores de abstração.

Portanto, a evolução das ferramentas de programação não deve ser analisada apenas pela quantidade de código que elas conseguem produzir, mas também pelo tipo de problema que os desenvolvedores passam a enfrentar.

---

## 2.3 Critérios de Validação: Como Avaliar Previsões sobre o Futuro

A análise das previsões sobre o futuro da programação exige diferenciação entre resultados experimentais, interpretações dos autores e previsões sobre o futuro.

Para isso, podem ser utilizados alguns critérios.

### 1. Critério de Brooks

É necessário verificar se uma tecnologia está reduzindo principalmente dificuldades de implementação e representação ou se também consegue lidar com a definição e compreensão do problema.

A distinção entre **complexidade acidental** e **complexidade essencial** continua sendo útil para analisar até que ponto uma nova ferramenta realmente reduz a dificuldade do desenvolvimento de software.

### 2. Desempenho em benchmarks

Benchmarks como o SWE-Bench são importantes porque permitem comparar diferentes sistemas de IA em tarefas relacionadas a problemas reais de software.

Jimenez et al. (2024) propuseram o SWE-Bench para avaliar a capacidade de modelos de linguagem de resolver problemas reais registrados em repositórios do GitHub. Entretanto, o desempenho em um benchmark não deve ser automaticamente interpretado como prova de capacidade geral de Engenharia de Software.

Liang et al. (2025), no trabalho *The SWE-Bench Illusion*, apresentam evidências de que parte do desempenho observado em determinados cenários pode estar relacionada à exposição prévia dos modelos aos dados utilizados nos testes. O estudo levanta, portanto, questionamentos sobre generalização e contaminação de benchmarks.

Dessa forma, resultados de benchmarks devem ser interpretados considerando a origem dos dados, a possibilidade de memorização e a diferença entre tarefas conhecidas e problemas realmente novos.

### 3. Evidência empírica versus generalização

Peng et al. (2023) encontraram um ganho de **55,8% no tempo de conclusão** de uma tarefa específica em um experimento controlado envolvendo o GitHub Copilot. Esse resultado fornece evidência de aumento de produtividade naquele contexto.

Entretanto, o resultado não deve ser interpretado como uma medida geral de que a IA torna qualquer atividade de desenvolvimento 55,8% mais rápida. A tarefa analisada, o ambiente experimental e o perfil dos participantes precisam ser considerados.

A meta-análise de Maier et al. (2026) amplia essa discussão ao reunir resultados de diferentes estudos. Os autores encontraram um efeito positivo moderado da IA generativa sobre a produtividade em programação, mas também observaram variações importantes entre diferentes contextos.

### 4. Contexto e generalização

Os resultados obtidos em tarefas simples e controladas não necessariamente se repetem em sistemas grandes, proprietários ou legados.

Projetos reais podem envolver requisitos incompletos, código antigo, dependências externas, regras de negócio específicas, restrições de segurança e conhecimento que não está disponível publicamente.

Portanto, a avaliação da IA na Engenharia de Software deve considerar não apenas sua capacidade de produzir código, mas também sua capacidade de trabalhar dentro das restrições e necessidades de sistemas reais.

---

# 3. Resumo Analítico dos 10 Artigos do Caderno

## 1. Brooks (1986) — *No Silver Bullet*

* **Tese:** Nenhuma tecnologia isolada provavelmente produzirá ganhos de produtividade de uma ordem de grandeza, pois parte significativa das dificuldades do software está relacionada à sua complexidade essencial.
* **Insight:** O desenvolvimento de software envolve problemas que não desaparecem simplesmente com melhorias nas ferramentas de implementação. A distinção entre dificuldades essenciais e acidentais fornece uma base para analisar as promessas atuais da IA.

## 2. Welsh (2023) — *The End of Programming*

* **Tese:** O avanço de modelos generativos pode modificar profundamente a forma tradicional de programar, reduzindo a necessidade de escrever manualmente grande parte do código.
* **Insight:** O trabalho desloca a atenção da escrita direta de código para a especificação de objetivos, dados e instruções para sistemas de IA. A proposta é provocativa e deve ser interpretada como uma previsão sobre a evolução da programação, e não como evidência de que a profissão será necessariamente eliminada.

## 3. Meyer (2023) — *AI Does Not Help Programmers*

* **Tese:** Modelos de linguagem podem produzir código plausível sem garantir sua correção lógica.
* **Insight:** O artigo destaca a necessidade de revisão e validação humana. A capacidade de gerar uma solução aparentemente correta não é equivalente à capacidade de demonstrar que essa solução está correta.

## 4. Karpathy (2017) — *Software 2.0*

* **Tese:** Parte do desenvolvimento de software pode migrar da escrita explícita de código para a definição de modelos e processos de treinamento orientados por dados.
* **Insight:** A mudança de paradigma não elimina a Engenharia de Software, mas desloca parte de suas atividades para dados, objetivos, treinamento, avaliação e arquitetura dos sistemas.

## 5. Cao (2026) — *Agentic Software*

* **Tese:** Sistemas agentivos ampliam a capacidade da IA de planejar e executar sequências de tarefas relacionadas ao desenvolvimento de software.
* **Insight:** A utilização de agentes pode deslocar parte do trabalho do desenvolvedor para atividades de especificação, coordenação, avaliação e supervisão. Os resultados e limitações apresentados no artigo devem ser analisados considerando os cenários específicos dos experimentos e benchmarks utilizados.

## 6. Jimenez et al. (2024) — *SWE-bench*

* **Tese:** O SWE-Bench foi criado para avaliar a capacidade de modelos de linguagem de resolver problemas reais encontrados em repositórios de software.
* **Insight:** O benchmark representa uma tentativa de aproximar a avaliação de IA de problemas reais de desenvolvimento, indo além de tarefas isoladas de geração de código. Seus resultados também mostram que resolver problemas em grandes bases de código envolve localizar alterações relevantes, compreender o contexto e lidar com dependências.

## 7. Liang et al. (2025) — *The SWE-Bench Illusion*

* **Tese:** O desempenho de modelos em determinados benchmarks pode ser influenciado pela exposição prévia aos dados utilizados na avaliação.
* **Insight:** O estudo apresenta evidências relacionadas à memorização e levanta questionamentos sobre a capacidade de generalização dos modelos. Isso reforça a necessidade de utilizar avaliações com dados novos e metodologias que reduzam o risco de contaminação.

## 8. Peng et al. (2023) — *The Impact of AI on Developer Productivity*

* **Tese:** Ferramentas de IA podem aumentar significativamente a velocidade de execução de determinadas tarefas de programação.
* **Insight:** Em um experimento controlado, participantes utilizando GitHub Copilot concluíram uma tarefa específica 55,8% mais rapidamente que o grupo de controle. O resultado demonstra potencial de ganho de produtividade, mas não deve ser generalizado automaticamente para todos os tipos de desenvolvimento.

## 9. Maier et al. (2026) — *A Meta-analysis of the Effect of Generative AI on Productivity and Learning in Programming*

* **Tese:** A IA generativa apresenta efeito positivo moderado sobre a produtividade em programação, mas os resultados variam conforme o contexto.
* **Insight:** A análise de 23 estudos e 27 tamanhos de efeito indica que produtividade e aprendizagem são dimensões diferentes. O estudo encontrou efeito positivo sobre produtividade, mas não encontrou efeito estatisticamente significativo sobre aprendizagem.

## 10. Abrahão et al. (2025) — *Software Engineering by and for Humans in an AI Era*

* **Tese:** A evolução da IA na Engenharia de Software deve ser analisada considerando a interação entre tecnologia, desenvolvedores, equipes e usuários.
* **Insight:** A produtividade não deve ser reduzida à quantidade de código produzido. Comunicação, requisitos, colaboração, qualidade, experiência dos desenvolvedores e tomada de decisões continuam sendo componentes importantes da Engenharia de Software.

---

# 4. Síntese dos Resultados

A análise conjunta dos dez artigos permite identificar alguns pontos de convergência e também diferenças importantes.

Primeiramente, existe evidência de que ferramentas de IA podem aumentar a produtividade em determinadas tarefas. O experimento de Peng et al. (2023) apresenta um ganho expressivo em uma tarefa específica, enquanto a meta-análise de Maier et al. (2026) identifica um efeito positivo moderado quando diferentes estudos são considerados em conjunto.

Entretanto, esses resultados não significam que a IA produza os mesmos ganhos em qualquer situação. A diferença entre experimentos controlados, projetos reais e diferentes tipos de tarefas mostra que o contexto é fundamental.

Outro ponto importante é a diferença entre **gerar código e resolver problemas de Engenharia de Software**. A geração automática de código pode reduzir o esforço de implementação, mas problemas relacionados à definição de requisitos, arquitetura, integração, segurança, manutenção e validação continuam exigindo avaliação.

Os trabalhos de Meyer (2023), Jimenez et al. (2024) e Liang et al. (2025) contribuem para essa discussão ao apresentar diferentes limitações relacionadas à correção, resolução de problemas reais e avaliação de modelos.

Além disso, os artigos de Karpathy (2017), Welsh (2023), Cao (2026) e Abrahão et al. (2025) apontam para uma transformação no papel do desenvolvedor. Em diferentes níveis, esses trabalhos discutem uma mudança de atividades de implementação direta para atividades de especificação, configuração, supervisão, avaliação e integração de sistemas baseados em IA.

Essa mudança não significa necessariamente que todas as tarefas tradicionalmente realizadas por desenvolvedores desaparecerão. Ela indica que a distribuição das responsabilidades dentro do processo de desenvolvimento pode ser modificada.

---

## 5. Quadro Comparativo: Evolução das Responsabilidades

### 5.1 Atividade principal

**Desenvolvimento tradicional**

Implementação manual, testes, depuração e manutenção do código.

**Desenvolvimento com IA generativa e agentes**

Definição de objetivos, especificação, implementação assistida, avaliação dos resultados e supervisão dos sistemas de IA.

---

### 5.2 Produção de código

**Desenvolvimento tradicional**

A maior parte do código é escrita diretamente pelo desenvolvedor.

**Desenvolvimento com IA generativa e agentes**

Parte significativa do código pode ser gerada ou modificada automaticamente a partir de instruções e contexto fornecidos pelo desenvolvedor.

---

### 5.3 Principais gargalos

**Desenvolvimento tradicional**

Tempo de implementação, compreensão do código, depuração e correção de erros.

**Desenvolvimento com IA generativa e agentes**

Definição precisa do problema, validação das soluções geradas, integração com sistemas existentes e controle dos resultados produzidos pela IA.

---

### 5.4 Ferramentas

**Desenvolvimento tradicional**

IDEs, compiladores, sistemas de controle de versão, ferramentas de testes e depuradores.

**Desenvolvimento com IA generativa e agentes**

IDEs, assistentes de programação, modelos de linguagem, agentes de IA, ferramentas de automação e sistemas de avaliação.

---

### 5.5 Responsabilidade humana

**Desenvolvimento tradicional**

Projeto, implementação, testes, depuração e manutenção do sistema.

**Desenvolvimento com IA generativa e agentes**

Definição dos objetivos, arquitetura, especificação dos requisitos, avaliação das soluções, supervisão da IA e decisões técnicas.

---

### 5.6 Principais riscos

**Desenvolvimento tradicional**

Erros de implementação, falhas de projeto, problemas de integração e dificuldades de manutenção.

**Desenvolvimento com IA generativa e agentes**

Código incorreto ou inadequado, respostas plausíveis mas incorretas, problemas de segurança, dependência excessiva das ferramentas e dificuldades de validação.

---

### 5.7 Critérios de avaliação

**Desenvolvimento tradicional**

Testes automatizados, revisão de código, análise de requisitos e validação do sistema.

**Desenvolvimento com IA generativa e agentes**

Testes, revisão de código, validação das respostas da IA, avaliação do comportamento dos agentes e verificação da adequação das soluções aos requisitos.

---

### 5.8 Competências relevantes

**Desenvolvimento tradicional**

Programação, algoritmos, arquitetura, testes e depuração.

**Desenvolvimento com IA generativa e agentes**

Programação, arquitetura, especificação de problemas, avaliação de soluções, validação, supervisão de IA e tomada de decisões de engenharia.

---

# 6. Conclusão: Uma Engenharia de Software em Transformação

Os dez artigos analisados não apresentam uma resposta única sobre o futuro da Engenharia de Software. Em conjunto, entretanto, fornecem evidências de que a Inteligência Artificial já está modificando algumas atividades relacionadas ao desenvolvimento de software.

As pesquisas sobre produtividade mostram que ferramentas de IA podem acelerar determinadas tarefas. O experimento de Peng et al. (2023) apresenta um resultado expressivo em um cenário controlado, enquanto a meta-análise de Maier et al. (2026) indica um efeito positivo moderado quando diferentes estudos são analisados conjuntamente.

Ao mesmo tempo, os estudos sobre correção, benchmarks e problemas reais mostram que produzir código rapidamente não é equivalente a resolver todos os problemas da Engenharia de Software. A necessidade de compreender requisitos, avaliar soluções, verificar resultados e manter sistemas complexos permanece relevante.

A perspectiva apresentada por Brooks (1986) continua sendo útil nesse cenário. A automação pode reduzir algumas dificuldades relacionadas à implementação e representação, mas não elimina automaticamente a complexidade associada à definição do problema e à construção de sistemas que atendam corretamente às necessidades de seus usuários e organizações.

Os artigos analisados também indicam uma possível mudança na distribuição das responsabilidades dos profissionais. À medida que ferramentas de IA assumem parte das atividades de implementação, podem ganhar importância competências relacionadas à especificação, arquitetura, validação, integração, supervisão e tomada de decisões.

Portanto, os resultados analisados sugerem que a questão central não é simplesmente saber se a IA irá substituir a programação, mas compreender **como a relação entre seres humanos, código e sistemas inteligentes está modificando a Engenharia de Software**.

Nesse cenário, a programação pode deixar de ser predominantemente uma atividade de escrita manual de código e passar a envolver uma combinação maior de definição de problemas, orientação de sistemas de IA, avaliação de resultados e tomada de decisões de engenharia. A extensão dessa transformação, porém, dependerá da evolução das ferramentas, da capacidade de generalização dos modelos e da forma como essas tecnologias serão incorporadas aos processos reais de desenvolvimento.

A Engenharia de Software, portanto, encontra-se diante de uma transformação significativa, mas os estudos analisados não sustentam a conclusão de que seus fundamentos tenham deixado de ser necessários. Ao contrário, aspectos como compreensão do problema, arquitetura, validação, qualidade e tomada de decisões continuam presentes mesmo quando parte da implementação é automatizada.
