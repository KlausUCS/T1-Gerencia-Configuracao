# WELSH (2023) — The End of Programming

> **Referência:** WELSH, M. The End of Programming. *Communications of the ACM*, v. 66, n. 1, p. 34–35, jan. 2023. DOI: [10.1145/3570220](https://doi.org/10.1145/3570220)
>
> **Papel no trabalho:** artigo-âncora do Tema 6 (leitura obrigatória de todos os integrantes).
>
> **Responsável pelo resumo:** Gianluca Debastiani Gonçalves

---

## 1. Que tipo de texto é este

É um *Viewpoint*, ou seja, um **artigo de opinião** de duas páginas. Não apresenta experimento, amostra nem dados coletados. É uma **previsão** feita por um profissional da área, e deve ser lido e avaliado como tal.

**Sobre o autor** (conforme a bio do próprio artigo):

- era CEO e cofundador da Fixie.ai, startup que desenvolvia IA para apoiar times de desenvolvimento de software;
- foi professor de Ciência da Computação em Harvard;
- teve cargos de engenharia no Google, na Apple e na OctoML.

---

## 2. A tese

O autor afirma que **programar, no sentido de escrever programas, vai se tornar obsoleto**. Ele sustenta isso em duas afirmações diferentes, que convém separar:

| Afirmação | O que diz | Força |
|---|---|---|
| **A — IA gera o código** | Programas "simples" passarão a ser gerados por IA; o humano fica, no máximo, num papel de supervisão. | Mais fraca, mais próxima do que já se observa com assistentes como o Copilot. |
| **B — Treinar substitui programar** | A maior parte do software, fora aplicações muito específicas, será substituída por sistemas de IA **treinados** em vez de programados. | Mais forte. É a ideia de *Software 2.0* (Karpathy, 2017) levada ao extremo. |

**Consequências que o autor tira da tese:**

- **Ensino:** estudantes não precisarão aprender a inserir um nó em uma árvore binária nem a programar em C++. Ele compara esse ensino ao da régua de cálculo.
- **O trabalho do engenheiro:** passa a ser escolher bons exemplos, bons dados de treino e boas formas de avaliar o resultado. A área deixaria de parecer engenharia e passaria a parecer **educação da máquina**.
- **A unidade de computação:** deixa de ser a máquina de von Neumann e passa a ser um grande modelo pré-treinado. Esse modelo já não se presta a análise estática nem a prova formal, e ninguém entende completamente como funciona.
- **Aplicações:** esses sistemas pilotariam aviões, operariam redes elétricas e talvez até governassem países.

**Prazo declarado:** o autor diz que ficaria surpreso se, em **10 ou 30 anos** a partir de 2023, a Ciência da Computação ainda fosse ensinada com estruturas de dados, algoritmos e programação no centro.

---

## 3. As evidências apresentadas

| Evidência | Tipo | Observação |
|---|---|---|
| Diferença de qualidade entre DALL-E v1 e v2, anunciados com **15 meses** de intervalo | Progresso em outro domínio | Trata de geração de **imagem**, não de software. É extrapolação entre domínios. |
| Aposta de que **99%** de quem escreve software não sabe como uma CPU funciona | Opinião | O próprio autor apresenta como aposta. Não há fonte, então não pode ser usado como dado. |
| O paper do GPT-3 (75 páginas) descreve o software do modelo em **três frases** | Anedota | Mostra que a arquitetura ficou mais abstrata, não que a engenharia desapareceu. |
| Os pioneiros achavam que todo cientista da computação precisaria entender semicondutores, e a abstração venceu | Analogia histórica | Argumento plausível, mas a abstração **mudou** a profissão sem **eliminá-la**. |
| Modelo de "quatro quintilhões de parâmetros" que conteria todo o conhecimento humano | Cenário hipotético | Não é evidência; é ilustração retórica. |

**Síntese:** nenhuma das evidências mede diretamente o trabalho de desenvolvimento de software.

---

## 4. Análise crítica

### 4.1 O autor descreve a engenharia de software com outras palavras

O engenheiro do futuro, segundo o próprio Welsh, vai escolher exemplos, dados e critérios de avaliação. Isso é **especificação e validação**.

Brooks (1987) separa as dificuldades do software em dois tipos:

- **Essência:** definir, especificar e testar o que o sistema deve fazer.
- **Acidente:** as dificuldades de representar isso numa linguagem e numa máquina.

Brooks defende que a essência é a parte difícil. O que o Welsh descreve como "o fim da programação" é o fim do **acidente**; a **essência** reaparece no próprio texto com outro nome.

Brooks também registra, citando Parnas, que "programação automática" sempre foi, na prática, um nome para programar numa linguagem de nível mais alto do que a disponível na época.

### 4.2 Contradição interna: sistemas inverificáveis em funções críticas

No mesmo texto, o autor afirma que:

1. ninguém entende de fato como os grandes modelos funcionam;
2. não há forma de determinar seus limites a não ser por estudo empírico;
3. esses modelos vão pilotar aviões e operar redes elétricas.

Quanto mais crítico e menos verificável um componente, **mais** trabalho de engenharia é preciso ao redor dele: testes, monitoramento, redundância e responsabilização. O argumento aponta contra a conclusão do próprio autor.

### 4.3 Linguagem natural não elimina a ambiguidade

Dijkstra (1978), no EWD667, argumenta que a precisão das linguagens formais não é um obstáculo a superar: é o que permite dizer exatamente o que se quer. Substituir código por exemplos e instruções em linguagem natural transfere a ambiguidade para outro lugar, mas não a remove.

### 4.4 Conflito de interesse

Na época, o autor dirigia uma empresa que vendia IA para desenvolvimento de software. Isso **não invalida** o argumento, mas é um critério legítimo para avaliar uma previsão: o autor ganha algo se ela for acreditada?

---

## 5. Relação com as perguntas norteadoras

**O que a engenharia de software resolve de verdade: escrever código ou outra coisa?**
O texto do Welsh serve de evidência para "outra coisa". Mesmo no cenário dele, a parte que sobra para o humano (especificar, escolher dados, avaliar) é a essência do problema, segundo Brooks.

**Outras tecnologias já prometeram acabar com a programação antes? O que aconteceu?**
O Welsh usa uma analogia histórica a favor da tese: a abstração do hardware. Há promessas anteriores que podem ser comparadas:

- COBOL, que se apresentava como programação próxima do inglês;
- linguagens de 4ª geração (4GL) e ferramentas CASE;
- plataformas no-code e low-code.

*(Pesquisa com fontes a ser feita pelo grupo.)*

**Como avaliar se uma previsão sobre o futuro de uma profissão merece ser levada a sério?**
Critérios que o próprio texto permite aplicar:

1. As evidências vêm do mesmo domínio da previsão? (Aqui, não: vêm de geração de imagem.)
2. Os números têm fonte? (Os principais, não.)
3. O autor tem interesse no resultado? (Sim.)
4. A previsão tem prazo e pode ser testada? (Sim: 10 anos a partir de 2023. Já é possível confrontá-la com dados de 2023 a 2026.)

---

## 6. Como testar a previsão com dados atuais

O artigo é de janeiro de 2023, então quase 4 dos 10 anos do prazo já se passaram. Possíveis confrontos:

- **METR (2025)**, estudo randomizado com desenvolvedores experientes de projetos open source: com ferramentas de IA, eles levaram **19% mais tempo** para concluir as tarefas, embora acreditassem ter ficado cerca de 20% mais rápidos (BECKER et al., 2025).
- **SWE-bench** e ***The SWE-Bench Illusion***: discutir se os benchmarks que sustentam o otimismo medem raciocínio ou memorização.
- **Mercado e ensino:** o que mudou na demanda por desenvolvedores e nos currículos de computação desde 2023. *(Pesquisa com fonte atual a ser feita.)*

---

## 7. Posicionamento sugerido para o grupo

> A IA está eliminando a programação como **digitação de código**, não a engenharia de software como **resolução de problemas**. Ao descrever o engenheiro do futuro, o próprio Welsh descreve especificação, dados e avaliação, que são a essência que Brooks já apontava em 1987.

---

## Referências

- BECKER, J.; RUSH, N.; BARNES, E.; REIN, D. Measuring the Impact of Early-2025 AI on Experienced Open-Source Developer Productivity. METR, 2025. [arxiv.org/abs/2507.09089](https://arxiv.org/abs/2507.09089)
- BROOKS, F. P. No Silver Bullet: Essence and Accidents of Software Engineering. *IEEE Computer*, v. 20, n. 4, 1987. [doi.org/10.1109/MC.1987.1663532](https://doi.org/10.1109/MC.1987.1663532)
- DIJKSTRA, E. W. On the foolishness of "natural language programming". EWD667, 1978. [cs.utexas.edu/users/EWD/transcriptions/EWD06xx/EWD667.html](https://www.cs.utexas.edu/users/EWD/transcriptions/EWD06xx/EWD667.html)
- KARPATHY, A. Software 2.0. Medium, 2017. [karpathy.medium.com/software-2-0-a64152b37c35](https://karpathy.medium.com/software-2-0-a64152b37c35)
- WELSH, M. The End of Programming. *Communications of the ACM*, v. 66, n. 1, 2023. [doi.org/10.1145/3570220](https://doi.org/10.1145/3570220)