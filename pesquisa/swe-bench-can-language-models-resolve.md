# SWE-bench: Can Language Models Resolve Real-World GitHub Issues?

O artigo **SWE-bench: Can Language Models Resolve Real-World GitHub Issues?** apresenta uma nova estrutura de avaliação (*benchmark*) projetada para testar a capacidade dos modelos de linguagem em resolver problemas reais de engenharia de software extraídos do GitHub[cite: 3].

---

## 1. Visão Geral e Motivação
* **Limitação dos Benchmarks Anteriores**: Benchmarks tradicionais (como o HumanEval) avaliam a geração de código em tarefas isoladas e curtas, que não refletem a complexidade do desenvolvimento de software no mundo real[cite: 3].
* **Objetivo do SWE-bench**: Avaliar se os modelos conseguem receber a descrição em linguagem natural de um problema (*issue*) e a base de código de um repositório, gerando uma modificação (*patch* ou *diff*) que resolva a *issue* e passe nos testes unitários e de integração[cite: 3].

---

## 2. Construção do Dataset
* **Escala**: É composto por **2 294 problemas** extraídos de *pull requests* (PRs) e *issues* de 12 repositórios populares em Python (como Django, SymPy, Matplotlib, Scikit-learn, Pytest e Sphinx)[cite: 3].
* **Processo de Filtragem em 3 Etapas**:
  1. **Coleta de PRs**: Raspagem de cerca de 90 000 PRs de repositórios Python com mais de 90% de código na linguagem[cite: 3].
  2. **Filtragem por Atributos**: Seleção de PRs fundidos (*merged*) que estejam associados a uma *issue* e que contenham novos testes[cite: 3].
  3. **Filtragem por Execução**: Verificação num ambiente virtual de execução para garantir que a instalação é bem-sucedida e que existe pelo menos um teste cuja situação muda de falha para sucesso (*fail-to-pass*) após a aplicação da solução[cite: 3].
* **SWE-bench Lite**: Uma versão reduzida constituída por 300 instâncias, otimizada para permitir avaliações mais rápidas e de menor custo computacional[cite: 3].

---

## 3. Treino do Modelo SWE-Llama
* **SWE-bench-train**: Criado um dataset de treino com 19 000 pares de *issue-PR* provenientes de 37 repositórios totalmente distintos dos usados na avaliação[cite: 3].
* **Modelos SWE-Llama**: Os autores realizaram ajuste fino supervisionado (*fine-tuning* via LoRA) dos modelos CodeLlama-Python de 7B e 13B parâmetros, especializando-os na edição e resolução de problemas em bases de código[cite: 3].

---

## 4. Principais Resultados e Desempenho

| Configuração de Contexto | Modelo | Taxa de Resolução (% Resolved) |
| :--- | :--- | :--- |
| **Recuperação BM25** | Claude 3 Opus | **3,79%**[cite: 3] |
| **Recuperação BM25** | Claude 2 | **1,96%**[cite: 3] |
| **Recuperação BM25** | GPT-4-turbo | **1,31%**[cite: 3] |
| **Recuperação BM25** | SWE-Llama 13b | **0,70%**[cite: 3] |
| **Recuperação BM25** | ChatGPT-3.5 | **0,17%**[cite: 3] |
| **Recuperação "Oracle"** | Claude 2 | **4,80%**[cite: 3] |
| **Recuperação "Oracle"** | SWE-Llama 13b | **3,97%**[cite: 3] |
| **Recuperação "Oracle"** | GPT-4 (amostra 25%) | **1,74%**[cite: 3] |

*(Nota: Na recuperação "Oracle", o modelo recebe exatamente os ficheiros modificados no PR de referência[cite: 3]. Na recuperação BM25, os ficheiros são selecionados via pesquisa esparsa de texto[cite: 3]).*

---

## 5. Principais Conclusões e Desafios Identificados
* **Efeito da Extensão do Contexto**: O desempenho dos modelos diminui drasticamente à medida que o tamanho do contexto aumenta, evidenciando dificuldade em localizar o trecho de código exato a modificar em bases de código grandes[cite: 3].
* **Dificuldade na Geração de Patches**: Os modelos frequentemente têm dificuldades em formatar corretamente os ficheiros de *diff/patch* ou geram soluções demasiado "gananciosas" e simplistas, que não respeitam o estilo do projeto nem prevêm dependências cruzadas entre ficheiros[cite: 3].
* **Edições de Ficheiro Completo vs. Patch**: Forçar o modelo a regerar o ficheiro inteiro em vez de produzir um *patch* reduz ainda mais a taxa de sucesso[cite: 3].
* **Ausência de Mapeamento de Dependências**: Modificações que corrigem o erro imediato frequentemente falham por causarem regressões em outros módulos do projeto[cite: 3].