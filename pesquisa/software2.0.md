# KARPATHY (2017) — Software 2.0

> **Referência:** KARPATHY, A. *Software 2.0*. Medium, 11 nov. 2017[cite: 2].
>
> **Papel no trabalho:** artigo-base para discutir a transição paradigmática da escrita explícita de código (Software 1.0) para a otimização baseada em dados e redes neurais (Software 2.0), redefinindo a atuação do engenheiro de software[cite: 2].

---

## 1. Que tipo de texto é este

É um **artigo de análise e reflexão sobre a evolução do desenvolvimento de software**[cite: 2]. Karpathy questiona a visão de que redes neurais são apenas "mais uma ferramenta" no arsenal do aprendizado de máquina, defendendo que elas representam uma mudança fundamental na forma como o software é construído[cite: 2].

A metáfora do **"Software 2.0"** contrapõe a programação tradicional (na qual desenvolvedores escrevem instruções explícitas linha por linha em linguagens como C++ ou Python) a um paradigma abstrato no qual o código é representado pelos pesos numéricos de uma rede neural[cite: 2]. Nesse novo modelo, os seres humanos especificam objetivos e a arquitetura base, enquanto algoritmos de otimização (como a retropropagação e o gradiente descendente) buscam e encontram o programa ideal no espaço de programas[cite: 2].

---

## 2. A tese

Karpathy divide a engenharia de software em dois paradigmas principais[cite: 2]:

| Tipo | O que significa | Exemplos / Componentes |
| --- | --- | --- |
| **Software 1.0** | Código clássico escrito manualmente por humanos, identificando pontos específicos no espaço de programas[cite: 2]. | Linguagens como C++ e Python; instruções lógicas explícitas, regras condicionais e algoritmos manuais[cite: 2]. |
| **Software 2.0** | Código escrito em pesos numéricos abstratos, gerado por algoritmos de otimização no espaço de programas[cite: 2]. | Redes neurais profundas (CNNs, WaveNet), pesos treinados via *backpropagation* e gradiente descendente[cite: 2]. |

A tese central é que **o Software 2.0 está engolindo o Software 1.0** em um amplo espectro de problemas onde é substancialmente mais fácil coletar e rotular dados (ou definir comportamentos desejados) do que escrever o algoritmo de forma explícita[cite: 2].

Karpathy identifica características estruturais marcantes do paradigma 2.0:

- **Homogeneidade computacional:** o código é composto primariamente por poucas operações matemáticas simples, como multiplicação de matrizes e limiares a zero (ReLU)[cite: 2].
- **Constância e previsibilidade:** tempo de execução e uso de memória são constantes por *forward pass*, eliminando a alocação dinâmica e reduzindo riscos de *loops* infinitos e *memory leaks*[cite: 2].
- **Agilidade e portabilidade:** facilidade de ajustar o *trade-off* entre desempenho e velocidade (por exemplo, reduzindo canais e retreinando) e facilidade de execução em hardwares arbitrários[cite: 2].
- **Centralidade nos dados:** a atividade principal do programador passa a ser a curadoria, limpeza, expansão e rotulagem de conjuntos de dados[cite: 2].

---

## 3. As evidências e argumentos apresentados

| Argumento / Evidência | Tipo | O que sustenta |
| --- | --- | --- |
| Reconhecimento Visual | Exemplo histórico / técnico | A transição de filtros manuais e classificadores (como SVMs) para redes convolucionais (CNNs) superou a capacidade humana de projetar extratores de características[cite: 2]. |
| Reconhecimento e Síntese de Voz | Exemplo histórico / técnico | Substituição de modelos estatísticos complexos (GMM/HMM) e montagem de trechos de áudio por arquiteturas neurais ponta a ponta (como WaveNet)[cite: 2]. |
| Tradução Automática | Exemplo técnico | Transição de métodos estatísticos baseados em frases para modelos neurais multilíngues e pouco supervisionados[cite: 2]. |
| Jogos de Estratégia | Exemplo prático | O AlphaGo Zero aprendeu a jogar Go em nível super-humano avaliando o tabuleiro diretamente, sem heurísticas manuais escritas por humanos[cite: 2]. |
| Estruturas e Bancos de Dados | Exemplo emergente | Substituição de componentes tradicionais como árvores B por modelos neurais (*Learned Index Structures*), superando a velocidade e economizando memória[cite: 2]. |
| Eficiência em Hardware | Análise de arquitetura | A simplicidade do conjunto de instruções do Software 2.0 facilita a integração direta em silício (ASICs dedicados e chips neuromórficos)[cite: 2]. |

**Síntese:** Karpathy evidencia que o Software 2.0 não é uma hipótese distante, mas uma transição já em curso em gigantes da tecnologia (como o Google)[cite: 2]. Onde a avaliação repetível do desempenho é viável, o gradiente descendente encontra códigos melhores do que qualquer programador humano conseguiria escrever[cite: 2].

---

## 4. Análise crítica

### 4.1 O ponto forte: redefinição do fluxo de trabalho e do papel do desenvolvedor

A contribuição central do artigo é redefinir o que constitui o "código" e a "compilação" no paradigma moderno[cite: 2].

No Software 2.0:
- O **código-fonte** passa a ser o conjunto de dados rotulados combinado com o esqueleto da arquitetura neural[cite: 2].
- O **processo de compilação** é o treinamento da rede neural via otimização[cite: 2].
- Os **desenvolvedores** dividem-se entre programadores 2.0 (que editam e curam dados) e uma minoria de programadores 1.0 (que desenvolvem a infraestrutura de treinamento, análises e interfaces de rotulagem)[cite: 2].

---

### 4.2 As limitações e riscos do paradigma 2.0

Karpathy é transparente ao ponderar as desvantagens e desafios graves do Software 2.0[cite: 2]:

- **Opacidade e Ininterpretabilidade:** os modelos resultantes funcionam muito bem, mas é extremamente difícil entender *como* funcionam, criando o dilema entre usar um modelo 90% preciso e compreensível ou 99% preciso e opaco[cite: 2].
- **Falhas silenciosas e vieses:** os modelos podem falhar de maneiras não intuitivas ou absorver silenciosamente vieses indesejados presentes nos dados de treinamento[cite: 2].
- **Vulnerabilidades adversariais:** a existência de ataques adversariais revela a natureza contra-intuitiva desse tipo de código e representa um desafio de segurança[cite: 2].

---

### 4.3 A necessidade de uma nova infraestrutura (IDEs e ferramentas 2.0)

O artigo enfatiza que a indústria possui décadas de ferramentas consolidadas para Software 1.0 (IDEs, profilers, debuggers, Git, pip/conda), mas carece de um ecossistema equivalente para Software 2.0[cite: 2]:

- **IDEs 2.0:** ambientes para ajudar a navegar, visualizar, limpar e identificar dados mal rotulados a partir da perda (*loss*) do modelo[cite: 2].
- **GitHub 2.0:** repositórios onde os *commits* e edições são feitos nos rótulos e conjuntos de dados[cite: 2].
- **Gerenciadores de pacotes 2.0:** infraestruturas dedicadas ao compartilhamento, implantação e composição de binários neurais[cite: 2].

---

## 5. Relação com as perguntas norteadoras

### **O que a engenharia de software resolve de verdade: escrever código ou outra coisa?**

Para Karpathy, no Software 1.0 resolve-se o problema explicitando a lógica humana[cite: 2]. No Software 2.0, o papel central passa a ser **especificar o objetivo, desenhar o esqueleto da arquitetura e realizar a curadoria de dados de alta qualidade** para que a otimização encontre o programa ideal[cite: 2].

### **Outras tecnologias já prometeram acabar com a programação?**

O artigo indica que a programação não acaba, mas **se eleva de nível de abstração**[cite: 2]. A escrita manual de código (1.0) é reduzida, dando lugar a uma disciplina focada na engenharia de dados, na otimização e na manutenção de sistemas de treinamento[cite: 2].

### **Como avaliar uma nova tecnologia que promete revolucionar a programação?**

O critério de Karpathy baseia-se na viabilidade de avaliação repetível do problema[cite: 2]:

> **Se é possível avaliar repetidamente o desempenho de um programa em relação a um critério objetivo (ex: classificar dados corretamente ou vencer um jogo), a otimização por dados tende a encontrar soluções superiores às escritas por seres humanos[cite: 2].**

---

## 6. Relação com Brooks, Karpathy, Welsh e Meyer

| Brooks (1986) | Karpathy (2017)[cite: 2] | Welsh (2023) | Meyer (2023) |
| --- | --- | --- | --- |
| Não há bala de prata; a maior dificuldade é essencial (requisitos e especificação). | O Software 2.0 é um novo paradigma: a otimização por dados substitui o código explícito[cite: 2]. | A IA tornará a programação tradicional obsoleta, migrando o humano para supervisão. | A IA gera código sem garantias formais; especificação e verificação continuam cruciais. |
| Distingue complexidade essencial de acidental. | Distingue Software 1.0 (lógica manual) de Software 2.0 (pesos e dados)[cite: 2]. | Prevê o fim do papel do programador tradicional. | Alerta para riscos de confiabilidade e falta de rigor sintático/lógico. |
| Foco no projeto de sistemas complexos. | Foco na busca no espaço de programas via otimização e curadoria de dados[cite: 2]. | Foco em modelos generativos de linguagem e agentes. | Foco na validação rigorosa dos resultados gerados por IA. |

---

## 7. Posicionamento sugerido para o grupo

> **Karpathy (2017) demonstra que a ascensão da Inteligência Artificial consolida o paradigma do Software 2.0, no qual a escrita explícita de algoritmos dá lugar à otimização contínua de pesos orientada a dados[cite: 2]. Em diálogo com as reflexões de Brooks e Meyer, esse movimento não elimina os desafios da engenharia de software, mas os desloca: a complexidade essencial deixa de estar na digitação de sintaxe ou lógica procedimental e passa a residir na definição de objetivos, na garantia da qualidade e imparcialidade dos dados e na mitigação dos riscos de opacidade e falhas silenciosas dos modelos neurais[cite: 2].**

---

## Referência

- **KARPATHY, A.** *Software 2.0*. Medium, 11 nov. 2017. Disponível em: <https://medium.com/@karpathy/software-2-0-a538203f4d23>[cite: 2].