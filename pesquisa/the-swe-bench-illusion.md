# LIANG ET AL. (2025) — The SWE-Bench Illusion

> **Referência:** LIANG, S.; GARG, S.; MOGHADDAM, R. Z. *The SWE-Bench Illusion: When State-of-the-Art LLMs Remember Instead of Reason*. ACM Conference / Preprint, 2025[cite: 4].
>
> **Papel no trabalho:** artigo empírico de contraponto que questiona a validade dos benchmarks de avaliação de código (como o SWE-Bench Verified), demonstrando que o alto desempenho dos modelos de linguagem decorre em grande parte da memorização de dados e contaminação de treino, e não de capacidade genuína de raciocínio em engenharia de software[cite: 4].

---

## 1. Que tipo de texto é este

É um **estudo diagnóstico e empírico controlado**, publicado no âmbito da ACM / preprint científico, e não um relato de opinião ou ensaio teórico[cite: 4]. Os autores deixam claro que o objetivo é avaliar rigorosamente se os modelos de linguagem de grande porte (LLMs) realmente raciocinam sobre código ou se apenas memorizam soluções presentes em seus dados de treinamento[cite: 4].

Os autores apresentam uma **avaliação comparativa entre múltiplos benchmarks** utilizando tarefas diagnósticas específicas (como identificação de arquivos com bugs, reprodução de funções e conclusão de prefixo)[cite: 4]. A análise abrange modelos de ponta das famílias Claude (Anthropic) e GPT (OpenAI), incluindo modelos de raciocínio como o3[cite: 4].

**Sobre os autores:** Shanchao Liang é pesquisador da Purdue University; Spandan Garg e Roshanak Zilouchian Moghaddam são pesquisadores da Microsoft[cite: 4].

---

## 2. A tese

A tese central de Liang et al. é que **os ganhos expressivos de desempenho relatados pelos LLMs no SWE-Bench Verified são inflacionados por memorização e contaminação dos dados de treinamento, mascarando a real limitação dos modelos em resolver problemas inéditos de software**[cite: 4].

Os autores fazem uma distinção importante:

| Situação | O que os autores afirmam | Avaliação |
| --- | --- | --- |
| **A — Resolver tarefas no SWE-Bench Verified** | Os modelos atingem métricas elevadas (ex.: até 76% na localização de arquivos e alta sobreposição de código)[cite: 4]. | Os autores demonstram que isso é impulsionado por memorização prévia e contaminação[cite: 4]. |
| **B — Resolver tarefas fora do benchmark (pós-cutoff / novos repositórios)** | O desempenho dos modelos sofre quedas severas de acurácia (quedas de até 47 pontos percentuais)[cite: 4]. | É o alvo principal da crítica: revela a falta de raciocínio generalizável[cite: 4]. |
| **C — Avaliar capacidade real de engenharia de software** | Benchmarks estáticos expostos publicamente não servem como métrica confiável para capacidade autônoma de codificação[cite: 4]. | É a principal limitação apontada pelos autores em relação aos testes atuais[cite: 4]. |

Os autores reconhecem que os LLMs conseguem reproduzir trechos complexos de código quando já foram expostos a eles durante o treinamento[cite: 4]. Porém, afirmam que isso é diferente de um **modelo que possui capacidade de raciocínio lógico e resolução de problemas em bases de código inéditas**[cite: 4].

### Consequências que os autores tiram da tese

- **Ilusão de raciocínio:** o alto desempenho em benchmarks públicos cria uma falsa impressão de que a IA compreende a estrutura e a lógica do software[cite: 4].
- **Viés de repositório (*Repository-Bias*):** os modelos sofrem sobreajuste (*overfitting*) nos 12 repositórios específicos do SWE-Bench, falhando em generalizar para outros projetos de popularidade equivalente[cite: 4].
- **Contaminação de dados:** a inclusão de repositórios do GitHub nos dados de pré-treinamento faz com que o modelo decore os arquivos com bug e os patches de solução[cite: 4].
- **Invalidação de benchmarks estáticos:** para avaliar a IA de forma confiável, a engenharia de software precisa de benchmarks dinâmicos, privados e imunes à contaminação[cite: 4].

---

## 3. As evidências e argumentos apresentados

| Argumento / Evidência | Tipo | O que sustenta |
| --- | --- | --- |
| Identificação de caminho de arquivo sem acesso à árvore do repositório | Experimento diagnóstico | Modelos como o OpenAI o3 acertam 76% no SWE-Bench Verified, mas caem para 53% em repositórios fora do benchmark[cite: 4]. |
| Teste de acurácia filtrada (sem nomes de arquivo na descrição) | Controle estatístico | Mesmo removendo referências explícitas na issue, a acurácia permanece desproporcionalmente alta no SWE-Bench Verified (70% vs 47%)[cite: 4]. |
| Reprodução de funções sem assinatura ou especificação | Exemplo prático / Medição | O Claude 4 Opus atinge 34,9% de sobreposição de 5-grams no SWE-Bench Verified, contra apenas 13,9% em repositórios externos[cite: 4]. |
| Conclusão de prefixo sem descrição de bug | Teste de memorização verbatim | Modelos reproduzem o patch exato de correção em até 31,6% das vezes sem receber qualquer explicação sobre o problema[cite: 4]. |
| Análise do diferencial de sobreposição ($\Delta_5$) | Comparação estatística (Pre vs. Post-patch) | Em tarefas recentes (SWE-Bench Extra), o $\Delta_5$ torna-se negativo, provando que sem a solução memorizada o modelo tende a replicar o código com bug[cite: 4]. |

**Síntese:** Liang et al. evidenciam que o progresso reportado em benchmarks públicos é parcialmente ilusório[cite: 4]. Onde a exposição prévia aos dados do GitHub ocorre durante o treinamento, o modelo simula capacidade técnica recuperando respostas da memória em vez de raciocinar sobre o problema[cite: 4].

---

## 4. Análise crítica

### 4.1 A principal crítica: memorizar um repositório não é o mesmo que raciocinar sobre ele

O ponto central de Liang et al. é que a engenharia de software possui uma exigência diferente de tarefas baseadas em reconhecimento de padrões[cite: 4].

Uma busca ou edição de código pode parecer eficiente quando a IA reutiliza um caminho memorizado[cite: 4]. Entretanto, a resolução de problemas em software exige navegação real pela arquitetura e pelas dependências do sistema[cite: 4].

Os autores demonstram que os LLMs de ponta não estão analisando a lógica do projeto para localizar e corrigir bugs; estão simplesmente recuperando da memória de treinamento onde as alterações foram feitas no GitHub[cite: 4].

Assim, **"alta pontuação no benchmark" não é suficiente para comprovar raciocínio em engenharia de software**[cite: 4].

---

### 4.2 O exemplo da identificação do caminho do arquivo

O teste mais revelador do artigo é a **tarefa de identificação do caminho do arquivo (*File Path Identification*)**[cite: 4].

Os autores apresentam ao modelo apenas a descrição da *issue* e o nome do repositório, **sem fornecer a árvore de diretórios ou os arquivos do projeto**[cite: 4].

Modelos como o OpenAI o3 alcançam até 76% de acurácia no SWE-Bench Verified[cite: 4]. No entanto, quando testados com o mesmo método em repositórios populares fora do benchmark, a acurácia cai para 53%[cite: 4].

A razão para essa queda, segundo os autores, é que o modelo não está "deduzindo" onde o bug está localizado com base no problema, mas sim **lembrando** do caminho exato memorizado durante o treino[cite: 4].

---

### 4.3 O problema da memorização verbatim e a taxa de 5-grams

Outro ponto fundamental é a medição da memorização direta através da **reprodução de funções** e da **conclusão de prefixos**[cite: 4].

Na tarefa de reprodução de funções — onde a assinatura e o corpo da função são completamente apagados —, os modelos conseguem reconstruir a implementação com até **34,9% de sobreposição consecutiva de 5-grams** em relação à solução original[cite: 4].

Na conclusão de prefixo, onde o modelo recebe apenas as linhas anteriores ao bug sem qualquer descrição da *issue*, modelos como o Claude 4 Opus reproduzem a solução exata em **31,6% dos casos**[cite: 4].

Isso evidencia que os modelos não estão programando uma solução lógica, mas executando uma geração *verbatim* baseada em sequências decoradas[cite: 4].

---

### 4.4 O comportamento da métrica $\Delta_5$ em dados inéditos

Para comprovar se o código gerado é fruto de raciocínio ou cópia, os autores introduzem a métrica diferencial $\Delta_5$, que compara a sobreposição de 5-grams do código gerado com a solução corrigida ($f_{\text{GT}}$) e com o código defeituoso original ($f_{\text{buggy}}$)[cite: 4]:

$$\Delta_5 = \text{overlap}_5(\hat{f}, f_{\text{GT}}) - \text{overlap}_5(\hat{f}, f_{\text{buggy}})$$

Os resultados mostram uma inversão de comportamento:
- No **SWE-Bench Verified** (dados vistos), o $\Delta_5$ é fortemente **positivo**, pois o modelo reproduz a solução memorizada[cite: 4].
- No **SWE-Bench Extra** (tarefas recentes pós-cutoff, não vistas no treino), o $\Delta_5$ torna-se **negativo** para a maioria dos modelos[cite: 4].

Essa inversão prova que, na ausência do patch memorizado, a IA falha em raciocinar sobre a correção e tende a apenas duplicar a estrutura com bug presente no contexto[cite: 4].

---

### 4.5 A necessidade de novos padrões de avaliação

Para os autores, a consequência mais importante para a engenharia de software é que **qualquer avaliação baseada em benchmarks públicos e estáticos é suscetível à contaminação**[cite: 4].

Os autores afirmam que a comunidade científica precisa de:
- **benchmarks dinâmicos**, atualizados continuamente com novas *issues*;
- **ambientes privados e inéditos**, para evitar a memorização prévia do código;
- **controles rigorosos de corte temporal (*cutoff*)**, para separar aprendizado de padrões de mera recuperação de memória[cite: 4].

Essa conclusão desloca a discussão de "quão alta é a nota da IA no benchmark" para **"como podemos garantir que o benchmark realmente mede raciocínio?"**[cite: 4].

---

## 5. Relação com as perguntas norteadoras

### **O que a engenharia de software resolve de verdade: escrever código ou outra coisa?**

Para Liang et al., a engenharia de software envolve **raciocinar e resolver problemas em sistemas inéditos e complexos**[cite: 4]. Reproduzir sintaxe ou trechos de código previamente vistos no GitHub não equivale a fazer engenharia de software real[cite: 4].

### **A IA realmente elimina a necessidade do programador?**

O artigo indica que não[cite: 4]. Como a capacidade dos modelos cai drasticamente ao saírem dos repositórios memorizados para projetos inéditos, o desenvolvedor humano continua indispensável para navegar, arquitetar e resolver problemas em bases de código reais e proprietárias[cite: 4].

### **O que diferencia um protótipo de um software profissional?**

Um protótipo ou teste de benchmark pode ser resolvido reutilizando soluções decoradas de repositórios públicos[cite: 4]. Software profissional, no entanto, opera em bases de código privadas e exige generalização precisa para problemas inéditos[cite: 4]. O artigo mostra que os LLMs falham exatamente nessa transição[cite: 4].

### **Como avaliar uma previsão sobre o futuro da programação?**

O critério de Liang et al. baseia-se na resistência à contaminação e na capacidade de generalização[cite: 4]:

> **Se o desempenho de um modelo despenca ao ser testado em repositórios inéditos ou pós-cutoff, o resultado elevado em benchmarks públicos reflete memorização estatística e contaminação de dados, não raciocínio autônomo de engenharia[cite: 4].**

---

## 6. Como o artigo pode ser confrontado com outros trabalhos

O artigo é especialmente interessante quando colocado em oposição ao texto de **Matt Welsh ("The End of Programming")** e em diálogo direto com as análises de **Karpathy ("Software 2.0")** e **Meyer ("AI Does Not Help Programmers")**.

| Autor / Artigo | Tese Central | Papel do Programador | Conclusão sobre a IA no Código |
| --- | --- | --- | --- |
| **Welsh (2023)** | A IA substituirá a escrita manual de código[cite: 2]. | Atuará como supervisor e educador[cite: 2]. | A programação tradicional se tornará obsoleta[cite: 2]. |
| **Meyer (2023)** | A IA gera código que parece correto, mas sem garantias formais[cite: 4]. | Necessário para especificação e verificação rigorosa[cite: 4]. | A IA não substitui a engenharia profissional de software[cite: 4]. |
| **Karpathy (2017)** | Transição para Software 2.0 baseado em otimização de pesos e dados[cite: 2]. | Curador de dados e arquiteto de modelos[cite: 2]. | O código é gerado por gradiente descendente a partir de dados[cite: 2]. |
| **Liang et al. (2025)** | Altas notas em benchmarks são fruto de memorização e contaminação[cite: 4]. | Indispensável para resolver problemas em código inédito[cite: 4]. | A IA atual memoriza repositórios, mas não raciocina autonomamente[cite: 4]. |

---

## 7. Posicionamento sugerido para o grupo

> **Liang et al. (2025) demonstram que o alto desempenho divulgado dos modelos de linguagem em benchmarks de engenharia de software, como o SWE-Bench Verified, é em grande parte uma ilusão provocada pela memorização de dados de treinamento e contaminação[cite: 4]. Quando submetidos a repositórios inéditos ou tarefas pós-cutoff, os modelos sofrem quedas acentuadas de desempenho, demonstrando falta de raciocínio lógico autônomo[cite: 4]. Em diálogo com as reflexões de Brooks, Karpathy, Welsh e Meyer, esses resultados comprovam que a IA atual atua como um repositório de padrões conhecidos, mas não substitui a capacidade essencial do engenheiro de software de compreender, arquitetar e resolver problemas em sistemas inéditos e proprietários[cite: 4].**

---

## Referência

- **LIANG, S.; GARG, S.; MOGHADDAM, R. Z.** *The SWE-Bench Illusion: When State-of-the-Art LLMs Remember Instead of Reason*. ACM Conference / Preprint, 2025.