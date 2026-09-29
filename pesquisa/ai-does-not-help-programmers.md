# MEYER (2023) — AI Does Not Help Programmers

> **Referência:** MEYER, B. *AI Does Not Help Programmers*. Communications of the ACM, Blog@CACM, Artificial Intelligence and Machine Learning. Publicado em 3 jun. 2023.

>

> **Papel no trabalho:** artigo de contraponto ao texto de Matt Welsh, utilizado para questionar a ideia de que a IA está tornando a programação obsoleta.

>
---

## 1. Que tipo de texto é este

É um **artigo de opinião/argumentação**, publicado no **Blog@CACM**, e não um relato de experimento controlado. O próprio Meyer deixa claro que o título deve ser entendido como uma **proposição a ser debatida**, e não como uma conclusão definitiva. Ele afirma que seu objetivo é estimular uma discussão que vá além do efeito de entusiasmo causado pelas novas ferramentas de IA.

O autor apresenta principalmente sua **experiência pessoal utilizando ChatGPT 4 para programação**. Ele ressalta algumas limitações da análise:

* a tecnologia ainda estava nos primeiros estágios;
* outros assistentes poderiam apresentar resultados melhores;
* o teste foi realizado especificamente com ChatGPT 4;
* seu objetivo não era tentar "enganar" a IA, mas verificar honestamente se ela poderia ajudá-lo em programação profissional.

**Sobre o autor:** Bertrand Meyer é apresentado ao final do artigo como professor e *Provost* do Constructor Institute, na Suíça, e CTO da Eiffel Software, nos Estados Unidos.

---

## 2. A tese

A tese central de Meyer é que **as ferramentas de IA generativa disponíveis naquele momento não ajudam suficientemente o programador profissional a produzir software correto**.

O autor faz uma distinção importante:

| Situação                                   | O que Meyer afirma                                                                                                                | Avaliação                                    |
| ------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------- |
| **A — Criar um programa do zero**          | A IA pode ser bastante útil para criar protótipos e programas simples a partir de especificações gerais.                          | O autor reconhece essa capacidade.           |
| **B — Ajudar um programador profissional** | A IA não consegue atuar como um bom parceiro de programação porque produz respostas que parecem corretas, mas podem conter erros. | É o alvo principal da crítica.               |
| **C — Produzir software correto**          | Para software profissional, a correção é fundamental, e a IA não oferece garantia de que o programa produzido esteja correto.     | É a principal limitação apontada pelo autor. |

Meyer reconhece que pessoas com pouco conhecimento de programação conseguem produzir protótipos úteis usando IA e cita o caso de desenvolvimento a partir de telas do Figma e especificações. Porém, afirma que isso é diferente da utilização da IA por um **programador profissional que busca melhorar seu trabalho**.

### Consequências que o autor tira da tese

* **Correção:** programas precisam fazer exatamente aquilo que deveriam fazer. Um resultado que apenas "parece correto" não é suficiente.

* **Assistente de programação:** Meyer gostaria de uma espécie de parceiro que identificasse seus erros e o alertasse sobre problemas, mas afirma que o ChatGPT não cumpre esse papel de maneira confiável.

* **IA generativa:** o autor caracteriza os modelos atuais como sistemas baseados em **inferência estatística**, capazes de produzir textos e programas que parecem corretos, mas sem garantia lógica de correção.

* **Engenharia de software:** mesmo que a IA escreva o programa, ainda serão necessárias **especificações e verificação**.

---

## 3. As evidências apresentadas

| Evidência                                                             | Tipo                           | Observação                                                                                                                   |
| --------------------------------------------------------------------- | ------------------------------ | ---------------------------------------------------------------------------------------------------------------------------- |
| Experiência pessoal de Meyer utilizando ChatGPT 4                     | Experimento pessoal            | O autor tentou utilizar a ferramenta para programação e concluiu que ela não era confiável para seu objetivo.                |
| Exemplo de desenvolvimento de um MVP com Copilot                      | Relato/anecdota                | O autor reconhece que iniciantes podem conseguir bons resultados em programas desenvolvidos do zero.                         |
| Teste com algoritmo de busca binária                                  | Exemplo prático                | ChatGPT identificou alguns aspectos corretamente, mas a tentativa de corrigir o código introduziu outro erro.                |
| Respostas sobre invariantes de laço                                   | Exemplo de comportamento da IA | O sistema apresenta conhecimento técnico, mas Meyer considera que isso não resolve o problema fundamental da confiabilidade. |
| Diferença entre programas "que parecem corretos" e programas corretos | Argumentação conceitual        | Para Meyer, essa diferença é fundamental na programação profissional.                                                        |

**Síntese:** as principais evidências do artigo são **experiências e exemplos apresentados pelo próprio autor**, e não um estudo estatístico amplo sobre produtividade de programadores.

---

## 4. Análise crítica

### 4.1 A principal crítica: parecer correto não significa estar correto

O ponto central de Meyer é que a programação possui uma exigência diferente de muitas outras atividades.

Uma tradução pode ser boa mesmo que pequenas imperfeições permaneçam. Um texto de marketing pode ser convincente mesmo sem precisão absoluta. Entretanto, um programa precisa executar corretamente suas funções.

O autor utiliza um exemplo de operações financeiras: se o cliente determina comprar 100 ações da Microsoft e vender 50 da Amazon, o programa não pode simplesmente inverter as operações porque algum objeto foi compartilhado em vez de replicado.

Assim, **"parecer correto" não é suficiente para software**.

---

### 4.2 O exemplo da busca binária

O exemplo mais importante do artigo é o algoritmo de **busca binária**.

Meyer apresenta a um ChatGPT uma implementação que continha um erro e pergunta se o programa estava correto.

O sistema apresenta uma análise inicialmente útil, mas posteriormente propõe uma correção que contém **um novo erro**. O autor compara esse comportamento com uma sequência anterior de seus próprios textos sobre busca binária, nos quais uma tentativa de corrigir um problema acabava revelando outro.

O problema, segundo Meyer, é que o ChatGPT apresenta a nova solução com segurança, mesmo sem conseguir garantir sua correção.

---

### 4.3 O problema não é falta de conhecimento técnico

Um ponto interessante é que Meyer reconhece que o ChatGPT possui bastante conhecimento.

O sistema consegue falar sobre conceitos como **invariantes de laço**, fazer análises e produzir explicações tecnicamente sofisticadas. O problema é que possuir conhecimento sobre programação não significa necessariamente conseguir **garantir que um programa está correto**.

Portanto, a crítica não é simplesmente:

> "A IA não sabe programar."

É mais precisamente:

> **A IA consegue gerar e explicar código, mas não consegue garantir sua correção.**

---

### 4.4 O problema da verificação

Para Meyer, a consequência mais importante para a engenharia de software é que **qualquer programa, seja produzido por uma pessoa ou por uma máquina, precisa ser verificado**.

O autor afirma que programadores humanos ou automáticos precisam de:

* **especificações**, para determinar o que o sistema deve fazer;
* **verificação**, para determinar se o programa realmente faz aquilo que deveria;
* requisitos claros, para evitar que um programa tecnicamente impressionante faça a coisa errada.

Essa conclusão é importante para o Tema 6 porque desloca a discussão de:

**"Quem escreve o código?"**

para:

**"Como sabemos que o software produzido está correto?"**

---

### 4.5 Meyer não afirma que a IA seja inútil

É importante não interpretar o artigo de maneira exagerada.

O próprio autor reconhece que existe um mercado para ferramentas capazes de produzir um **programa básico que "mais ou menos" funciona**, inclusive em uma linguagem que o usuário não conhece bem.

Portanto, a posição de Meyer é mais específica:

**A IA pode ser útil para prototipagem e geração inicial de código, mas, segundo sua avaliação de 2023, não é confiável o suficiente para substituir a necessidade de engenharia, especificação e verificação em software profissional.**

---

## 5. Relação com as perguntas norteadoras

### **O que a engenharia de software resolve de verdade: escrever código ou outra coisa?**

O artigo de Meyer é uma evidência forte para a ideia de que engenharia de software não se resume a escrever código.

Mesmo que uma IA consiga produzir o código automaticamente, ainda é necessário determinar:

* o que o sistema deve fazer;
* quais são os requisitos;
* como verificar o comportamento;
* se o resultado realmente atende ao que o cliente solicitou.

Meyer afirma explicitamente que qualquer programa, humano ou automático, precisa de **especificações e verificação**.

---

### **A IA realmente elimina a necessidade do programador?**

O artigo apresenta uma resposta contrária à previsão mais radical de Welsh.

Para Meyer, eliminar a escrita manual do código não significa eliminar a necessidade de engenharia. O código pode ser produzido automaticamente, mas alguém ainda precisa garantir que ele está correto.

Assim, a IA poderia **mudar o trabalho do programador**, mas isso não significa automaticamente que a profissão desapareça.

---

### **O que diferencia um protótipo de um software profissional?**

Essa é uma das contribuições mais importantes do artigo.

Um protótipo pode ser considerado útil mesmo apresentando limitações, desde que demonstre uma ideia ou ajude a iniciar um projeto.

Software profissional, entretanto, precisa funcionar corretamente. O autor aceita que a IA possa ajudar na criação de programas básicos, mas rejeita a ideia de que isso seja suficiente para substituir o trabalho de desenvolvimento profissional.

---

### **Como avaliar uma previsão sobre o futuro da programação?**

O artigo fornece alguns critérios:

1. **A ferramenta realmente consegue produzir código correto?**
2. **Ela consegue detectar seus próprios erros?**
3. **Existe garantia de correção ou apenas aparência de correção?**
4. **O resultado funciona em situações reais e não apenas em exemplos simples?**
5. **Ainda são necessárias especificação e verificação?**

Para Meyer, em 2023, as respostas indicavam que a IA ainda não era confiável o suficiente para substituir essas etapas.

---

## 6. Como o artigo pode ser confrontado com outros trabalhos

O artigo é especialmente interessante quando colocado em oposição ao texto de **Matt Welsh, "The End of Programming"**.

Welsh argumenta que a programação tradicional poderá perder importância porque a IA será responsável pela produção dos programas.

Meyer concorda parcialmente com a possibilidade de a IA gerar código, mas questiona a conclusão de que isso elimina a programação profissional.

A diferença pode ser resumida assim:

| Welsh                                                        | Meyer                                                                         |
| ------------------------------------------------------------ | ----------------------------------------------------------------------------- |
| A IA poderá gerar cada vez mais código.                      | A IA já consegue gerar código, mas isso não garante correção.                 |
| A programação poderá se tornar obsoleta.                     | A engenharia continua necessária para especificação e verificação.            |
| O programador poderá atuar mais como supervisor.             | O profissional ainda precisa verificar o resultado.                           |
| O avanço da IA aponta para o fim da programação tradicional. | O avanço da IA pode aumentar a importância da verificação e da especificação. |

O próprio Meyer termina sugerindo que, para a IA se tornar realmente eficaz na programação profissional, poderá ser necessária uma **"renascença" dos estudos e ferramentas de especificação formal e verificação**.

---

## 7. Posicionamento sugerido para o grupo

> **A IA consegue reduzir a necessidade de escrever código manualmente, mas isso não significa o fim da engenharia de software. O principal problema apontado por Meyer é que gerar um programa que parece correto é diferente de garantir que ele realmente funciona. Mesmo com código produzido por IA, continuam sendo necessárias especificação, validação e verificação. Portanto, a IA pode mudar o papel do programador, mas não elimina a necessidade de profissionais capazes de definir o problema e garantir a correção da solução.**

---

## Referência

* **MEYER, B.** *AI Does Not Help Programmers*. Communications of the ACM, Blog@CACM, Artificial Intelligence and Machine Learning. Publicado em 3 jun. 2023.