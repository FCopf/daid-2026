# Auditoria da integração do MEAD nas Leituras prévias

## Critério

Esta matriz registra os 96 arquivos `.qmd`, `.r` e `.R` examinados em `mead-main-EXAMPLE`.
`COMPLETO` significa que todos os elementos pertinentes ao escopo conceitual da unidade curricular
têm destino explícito nas Leituras prévias. `FORA DO ESCOPO` significa que o arquivo ou o elemento é
operacional, pertence a outro paradigma ou técnica, é infraestrutura, está vazio ou não acrescenta
conteúdo aos temas das quinze semanas.

Adaptação não significa transcrição literal. Exemplos foram transportados para os problemas marinhos
das leituras, código foi reescrito em R autocontido, gráficos estatísticos foram recriados no próprio
`.qmd` e elementos decorativos foram excluídos. Os arquivos de referência não foram modificados.

## Fontes pertinentes

| Fonte MEAD | Seção ou elementos | Leitura de destino | Texto | Exemplos | Equações | Código R | Figuras e gráficos | Tabelas, callouts e ressalvas | Justificativa | Status |
|---|---|---|---|---|---|---|---|---|---|---|
| `content/amostragem/pop-amostra.qmd` | população, amostra, unidade, distribuições, parâmetros, estimadores, reposição e inferência | 2 e 3 | integrado | adaptados para estações e mexilhões | integradas | reescrito | amostragem e distribuições recriadas | definições e cuidados integrados | - | COMPLETO |
| `content/amostragem/tipos-amostragem.qmd` | AAS, estratificada, sistemática, erro, acurácia, precisão e erro padrão | 2 | integrado | adaptados para cadastro costeiro | integradas | reescrito | quatro desenhos e acurácia/precisão recriados | ressalvas de periodicidade, viés e pesos integradas | - | COMPLETO |
| `content/anova/anova-simples.qmd` | modelo, hipóteses, partição, QM, F, exemplo, Tukey e pressupostos | 9 e 10 | integrado | cálculo manual e experimento de metais adaptados | integradas | reescrito sem semente | cenários, F e diagnósticos recriados | tabela ANOVA e cuidados integrados | - | COMPLETO |
| `content/anova/scripts/anova-sim.r` | gerador de dados de ANOVA | 10 e 11 | não havia | mecanismo adaptado | não havia | reescrito sem `set.seed()` | saídas recriadas | não havia | - | COMPLETO |
| `content/distribuicao-normal/distr-norm.qmd` | forma normal, parâmetros, densidade, áreas, padronização e exercícios | 3, 4 e 7 | integrado | exemplos adaptados | equações e áreas integradas | reescrito em R simples | normal, t e caudas recriadas | notas de interpretação integradas | - | COMPLETO |
| `content/distribuicao-normal/distribuicao-normal-modelo.qmd` | construção escalar da função normal e papel de mu e sigma | 3 e 4 | integrado | efeito dos parâmetros adaptado | parte escalar integrada | código Python substituído por R | curvas recriadas | ressalvas integradas | geometria e operação em Python não eram pertinentes | COMPLETO |
| `content/distribuicao-normal/distribuicao-normal-probabilidade.qmd` | probabilidades abaixo, acima, entre limites e em unidades z | 3, 4 e 7 | integrado | cálculos adaptados | integradas | reescrito com `pnorm()` | áreas recriadas | leitura de áreas integrada | código Python original não era pertinente | COMPLETO |
| `content/distribuicao-normal/scripts/normal-empirica-gg.r` | função visual da normal empírica | 1, 3 e 4 | não havia | mecanismo adaptado | não havia | incorporado diretamente nos QMD | gráficos recriados | não havia | - | COMPLETO |
| `content/estatistica-descritiva/escorez.qmd` | transformação, interpretação, retorno à escala e regra empírica | 1 | integrado | poças e medidas em escalas distintas | integrada | reescrito | posição padronizada integrada às figuras | limitações de raridade integradas | - | COMPLETO |
| `content/estatistica-descritiva/quartis.qmd` | posições, quartis, AIQ, boxplot e atípicos | 1 | integrado | comprimentos ordenados | integradas | reescrito | boxplot e cercas recriados | cuidados com atípicos integrados | - | COMPLETO |
| `content/estatistica-descritiva/scripts/assimetria-ggplot.r` | média, mediana e quartis sob assimetria | 1 | não havia | mecanismo adaptado | não havia | incorporado diretamente | histogramas e boxplot recriados | não havia | - | COMPLETO |
| `content/estatistica-descritiva/scripts/getmode.r` | cálculo da moda | 1 | não havia | valores contínuos e categorias | não havia | função autocontida reescrita | não se aplicava | ressalva sobre multimodalidade integrada | - | COMPLETO |
| `content/estatistica-descritiva/scripts/normal-empirica-gg.r` | distribuição padronizada e regra empírica | 1 | não havia | mecanismo adaptado | não havia | incorporado diretamente | representação adaptada | não havia | - | COMPLETO |
| `content/estatistica-descritiva/tendcentral.qmd` | média, mediana, moda, ponto médio e assimetria | 1 | integrado | medidas de poças | integradas | reescrito | efeitos da forma recriados | comparações e cuidados integrados | - | COMPLETO |
| `content/estatistica-descritiva/variacao.qmd` | variância, desvio-padrão, CV e amplitude | 1 | integrado | cálculo completo em graus Celsius | integradas | reescrito | distribuição e dispersão recriadas | unidades e limitações do CV integradas | - | COMPLETO |
| `content/estatistica-descritiva/varqualit.qmd` | frequências absolutas, relativas, ordinais e barras | 1 | integrado | sombreamento de poças | integrada | reescrito | barras recriadas | tabela de frequências integrada | pré-processamento operacional excluído | COMPLETO |
| `content/estatistica-descritiva/varquant.qmd` | classes, largura, frequência acumulada e histogramas | 1 | integrado | comprimentos | integrada | reescrito | histogramas e ECDF recriados | efeito da largura integrado | - | COMPLETO |
| `content/estrutura-dados/estrutura-tipo.qmd` | unidades, descritores, ausência, tipos e níveis de mensuração | 1, 5 e 12 | integrado | tabela de poças e hierarquia experimental | não se aplicava | reescrito | tabela de escalas e hierarquia adaptadas | NA, zero e operações válidas integrados | imputação avançada era fora do nível da disciplina | COMPLETO |
| `content/funcoes-modelos/funcoes-potencia.qmd` | funções potência, espécie-área, linearização e previsão | 13 | integrado | espécie-área preservado | integradas | Python reescrito em R | escalas original e logarítmica recriadas | retransformação e limites integrados | - | COMPLETO |
| `content/fundamentos-probabilidade/combina-probabilidades.qmd` | união, interseção, complemento e combinação de eventos | 9 | integrado | família de testes | integradas | simulação reescrita | mínimo de p e FWER recriados | dependência entre comparações integrada | - | COMPLETO |
| `content/fundamentos-probabilidade/espaco-amostral.qmd` | experimento, espaço, evento, probabilidade e LGN | 3 e 7 | integrado | comprimentos e eventos | integradas | reescrito | convergência da frequência recriada | limites da LGN integrados | - | COMPLETO |
| `content/fundamentos-probabilidade/probabilidade-condicional.qmd` | condicional, independência e distinção de exclusão mútua | 3, 5 e 9 | integrado | dependência amostral e testes | integradas | adaptado | representação conceitual recriada | distinções integradas | seção de Bayes excluída por escopo | COMPLETO |
| `content/fundamentos-probabilidade/scripts/conditional-tree.r` | árvore de eventos condicionais | 3 e 9 | não havia | lógica incorporada | não havia | simplificado em cálculos R | árvore substituída por visualizações diretas | não havia | - | COMPLETO |
| `content/fundamentos-probabilidade/scripts/tree-diagram.r` | árvore e produtos de probabilidades | 3 e 9 | não havia | lógica incorporada | não havia | simplificado em R base | diagrama pouco legível substituído | não havia | - | COMPLETO |
| `content/inferencia-estatistica/int-conf.qmd` | estimação, IC, t, suficiência e tamanho amostral | 4 e 8 | integrado | mexilhões e planejamento | integradas | reescrito | t, cobertura e margem recriadas | interpretação frequentista e validade integradas | - | COMPLETO |
| `content/inferencia-estatistica/scripts/normal-empirica-gg.r` | áreas centrais e valores críticos | 4 e 7 | não havia | mecanismo adaptado | não havia | incorporado nos QMD | áreas recriadas | não havia | - | COMPLETO |
| `content/inferencia-estatistica/scripts/tcl-simetry.r` | TCL sob assimetria | 3 | não havia | população exponencial preservada | não havia | reescrito sem semente | quatro distribuições recriadas | não havia | - | COMPLETO |
| `content/inferencia-estatistica/teorema-central-limite.qmd` | médias amostrais, probabilidades, assimetria e exercícios | 3 e 4 | integrado | exemplos adaptados para mexilhões | integradas | reescrito | indivíduos, médias e efeito de n recriados | condições e alertas integrados | fotos contextuais não eram estatísticas | COMPLETO |
| `content/medidas-associacao/biquanti.qmd` | covariância, correlação, escalas e interpretação | 13 | integrado | exemplo marinho adaptado para riqueza e exposição | integradas | reescrito | dispersões recriadas | causalidade e série comum integradas como ressalva | - | COMPLETO |
| `content/medidas-associacao/biquantquali.qmd` | boxplots, médias, erros, partição e R2 | 9, 10, 12 e 15 | integrado | grupos e covariáveis adaptados | integradas | reescrito | grupos, intervalos e partições recriados | notação e característica aditiva integradas | - | COMPLETO |
| `content/medidas-associacao/scripts/anova-sim.r` | gerador quanti-quali | 10 e 11 | não havia | mecanismo adaptado | não havia | reescrito sem semente | saídas recriadas | não havia | - | COMPLETO |
| `content/regressao-linear/metodo-minimos-quadrados-apresentacao.qmd` | resíduos, MMQ, ajustados, SQ e R2 | 13 | parte escalar integrada | cálculo RIKZ adaptado | parte escalar integrada | reescrito em R | resíduos e partição recriados | resumo de passos integrado | geometria vetorial e matricial excluída | COMPLETO |
| `content/regressao-linear/mmq-regressao-linear-simples.qmd` | MMQ passo a passo, ajustados, resíduos e R2 | 13 | integrado | exemplo de dez estações | parte escalar integrada | Python reescrito em R | ajuste e partição recriados | passos e interpretação integrados | álgebra matricial operacional excluída | COMPLETO |
| `content/regressao-linear/particao-soma-quadrados-r2.qmd` | desvios total, explicado e residual, R2 e limitações | 10 e 13 | integrado | subconjunto RIKZ preservado | integradas | reescrito | segmentos da partição recriados | tabela de componentes integrada | - | COMPLETO |
| `content/regressao-linear/regressao-linear-multipla.qmd` | coeficientes parciais, multicolinearidade, pressupostos e diagnósticos | 12, 13 e 15 | integrado | temperatura, peso e crescimento adaptados | integradas | reescrito | resíduos parciais, suporte e influência recriados | limitações e transformações integradas | seleção automática de variáveis excluída | COMPLETO |
| `content/regressao-linear/regressao-linear-simples.qmd` | processo, MMQ, inferência, ANOVA, R2, intervalos e diagnósticos | 13 e 14 | integrado | RIKZ e processos simulados | integradas | reescrito | reta, resíduos, bandas e influência recriados | todos os pressupostos e cuidados integrados | - | COMPLETO |
| `content/teste-hipoteses/intro-testehipot.qmd` | H0, HA, distribuição nula, alfa, p, erros e caudas | 7 e 8 | integrado | teste simulado e Z | integradas | reescrito | distribuição nula e caudas recriadas | tabela de decisões e alertas integrados | - | COMPLETO |
| `content/teste-hipoteses/teste-t.qmd` | uma amostra, pareado, independentes, graus de liberdade e variâncias | 8 | integrado | substratos e antes/depois | integradas | reescrito | normal/t e diagnósticos recriados | pressupostos e Welch integrados | - | COMPLETO |
| `content/teste-hipoteses/teste-variancia.qmd` | razão de variâncias, distribuição F e robustez | 8 e 10 | integrado | duas dispersões adaptadas | integradas | `var.test()` incorporado | F e dispersões recriadas | sensibilidade à normalidade e Levene integrados | - | COMPLETO |
| `content/visualizacao-dados/grafico-ggplot2.qmd` | camadas, histogramas, boxplots, dispersão e barras | 1 a 15 conforme o gráfico | conceitos integrados | exemplos adaptados | não se aplicava | código reescrito | geometrias pertinentes recriadas | legendas e interpretação integradas | temas e exportação operacionais excluídos | COMPLETO |
| `content/visualizacao-dados/graficos-r.qmd` | escolha de barras, histogramas, boxplots e dispersão | 1 e 13 | conceitos integrados | exemplos adaptados | não se aplicava | reescrito em ggplot2 | gráficos pertinentes recriados | critérios de escolha integrados | base R, pacote ade4 e exportação excluídos | COMPLETO |
| `topics/amostragem.qmd` | descrição e mapa do tema | 2 | escopo coberto | não havia | não havia | não havia | capa decorativa excluída | links substituídos por conteúdo local | - | COMPLETO |
| `topics/anova.qmd` | ANOVA simples, blocos e fatorial | 10 e 11 | escopo coberto | não havia | não havia | não havia | capas decorativas excluídas | links substituídos por conteúdo local | - | COMPLETO |
| `topics/distribuicao-normal.qmd` | modelo e usos da normal | 3, 4 e 7 | escopo coberto | não havia | não havia | não havia | capa decorativa excluída | links substituídos por conteúdo local | - | COMPLETO |
| `topics/estatistica-descritiva.qmd` | representação, centro e dispersão | 1 | escopo coberto | não havia | não havia | não havia | capa decorativa excluída | links substituídos por conteúdo local | - | COMPLETO |
| `topics/estrutura-dados.qmd` | tipos, unidades e mensuração | 1 e 5 | escopo coberto | não havia | não havia | não havia | capa decorativa excluída | links substituídos por conteúdo local | - | COMPLETO |
| `topics/funcoes-modelos.qmd` | funções determinísticas e potência | 13 | escopo pertinente coberto | não havia | não havia | não havia | capa decorativa excluída | links substituídos por conteúdo local | - | COMPLETO |
| `topics/fundamentos-probabilidade.qmd` | eventos, combinação, condicional e independência | 3, 5 e 9 | escopo pertinente coberto | não havia | não havia | não havia | capa decorativa excluída | Bayes explicitamente fora do escopo | - | COMPLETO |
| `topics/inferencia-estatistica.qmd` | TCL e intervalos | 3 e 4 | escopo coberto | não havia | não havia | não havia | capa decorativa excluída | links substituídos por conteúdo local | - | COMPLETO |
| `topics/medidas-associacao.qmd` | associações quanti-quanti e quanti-quali | 10, 12 e 13 | escopo pertinente coberto | não havia | não havia | não havia | capa decorativa excluída | associação só qualitativa excluída | - | COMPLETO |
| `topics/regressao-linear.qmd` | regressão simples e múltipla | 12 a 15 | escopo coberto | não havia | não havia | não havia | capa decorativa excluída | links substituídos por conteúdo local | - | COMPLETO |
| `topics/teste-hipoteses.qmd` | hipóteses, erros e p | 7 a 9 | escopo coberto | não havia | não havia | não havia | capa decorativa excluída | links substituídos por conteúdo local | - | COMPLETO |
| `topics/visualizacao-dados.qmd` | princípios e gráficos | todas conforme a necessidade | escopo estático coberto | não havia | não havia | não havia | gráficos locais substituem a capa | interatividade operacional excluída | - | COMPLETO |

## Fontes fora do escopo

| Fonte MEAD | Seção ou elementos | Leitura de destino | Texto | Exemplos | Equações | Código R | Figuras e gráficos | Tabelas, callouts e ressalvas | Justificativa | Status |
|---|---|---|---|---|---|---|---|---|---|---|
| `content/fundamentos-probabilidade/scripts/bayes-diagram.r` | diagrama de Bayes | nenhum | n/a | n/a | n/a | n/a | n/a | n/a | Bayes foi excluído do programa destas leituras | FORA DO ESCOPO |
| `content/fundamentos-probabilidade/teorema-bayes.qmd` | teorema de Bayes | nenhum | n/a | n/a | n/a | n/a | n/a | n/a | paradigma/conteúdo deliberadamente excluído | FORA DO ESCOPO |
| `content/glms/intro.qmd` | GLMs, logística e Poisson | nenhum | n/a | n/a | n/a | n/a | n/a | n/a | respostas não normais não pertencem às quinze leituras | FORA DO ESCOPO |
| `content/intro-bayes/intro-bayes-binomial-grid.qmd` | aproximação por grade | nenhum | n/a | n/a | n/a | n/a | n/a | n/a | inferência bayesiana excluída | FORA DO ESCOPO |
| `content/intro-bayes/intro-bayes-binomial-pymc.qmd` | binomial em PyMC | nenhum | n/a | n/a | n/a | n/a | n/a | n/a | Bayes e operação em Python excluídos | FORA DO ESCOPO |
| `content/intro-bayes/intro-bayes-counting.qmd` | contagem bayesiana | nenhum | n/a | n/a | n/a | n/a | n/a | n/a | inferência bayesiana excluída | FORA DO ESCOPO |
| `content/intro-bayes/intro-bayes-distr-prob.qmd` | probabilidades sob perspectiva bayesiana | nenhum | n/a | n/a | n/a | n/a | n/a | n/a | conteúdo bayesiano; probabilidade frequentista foi coberta por fonte direta | FORA DO ESCOPO |
| `content/intro-bayes/intro-bayes-modelo-bayesiano.qmd` | prior, verossimilhança e posterior | nenhum | n/a | n/a | n/a | n/a | n/a | n/a | inferência bayesiana excluída | FORA DO ESCOPO |
| `content/intro-bayes/intro-bayes-modelo-normal-bayesiano-priori.qmd` | modelo normal bayesiano | nenhum | n/a | n/a | n/a | n/a | n/a | n/a | modelo bayesiano excluído; normal frequentista coberta por fonte direta | FORA DO ESCOPO |
| `content/introducao-r/data-frames.qmd` | importação e manipulação básica | nenhum | n/a | n/a | n/a | n/a | n/a | n/a | treinamento operacional de R pertence às práticas | FORA DO ESCOPO |
| `content/introducao-r/estrutura-linguagem.qmd` | linguagem e objetos R | nenhum | n/a | n/a | n/a | n/a | n/a | n/a | treinamento operacional de R pertence às práticas | FORA DO ESCOPO |
| `content/manipulacao-dados-R/import-export.qmd` | importação/exportação | nenhum | n/a | n/a | n/a | n/a | n/a | n/a | operação de software, não conceito estatístico da leitura | FORA DO ESCOPO |
| `content/manipulacao-dados-R/pipe.qmd` | operadores pipe | nenhum | n/a | n/a | n/a | n/a | n/a | n/a | operação de software, não conceito estatístico | FORA DO ESCOPO |
| `content/manipulacao-dados-R/tidyverse.qmd` | catálogo de pacotes | nenhum | n/a | n/a | n/a | n/a | n/a | n/a | operação de software; funções necessárias aparecem localmente | FORA DO ESCOPO |
| `content/manipulacao-dados-R/transform.qmd` | transformação de tabelas | nenhum | n/a | n/a | n/a | n/a | n/a | n/a | treinamento operacional pertence às práticas | FORA DO ESCOPO |
| `content/manipulacao-dados-python/01-estrutura-linguagem-python.qmd` | linguagem Python | nenhum | n/a | n/a | n/a | n/a | n/a | n/a | Python excluído | FORA DO ESCOPO |
| `content/manipulacao-dados-python/02-estrutura-tipo-python.qmd` | pandas e tipos | nenhum | n/a | n/a | n/a | n/a | n/a | n/a | Python operacional; conceitos duplicados cobertos por fonte R direta | FORA DO ESCOPO |
| `content/manipulacao-dados-python/03-estatistica-descrtitiva-python.qmd` | descritiva em Python | nenhum | n/a | n/a | n/a | n/a | n/a | n/a | duplicata operacional; conceitos cobertos nas fontes descritivas diretas | FORA DO ESCOPO |
| `content/manipulacao-dados-python/04-medidas-associacao-python.qmd` | associações em Python | nenhum | n/a | n/a | n/a | n/a | n/a | n/a | duplicata operacional; conceitos cobertos nas fontes diretas | FORA DO ESCOPO |
| `content/manipulacao-dados-python/importa-dados-python.qmd` | importação CSV | nenhum | n/a | n/a | n/a | n/a | n/a | n/a | Python operacional | FORA DO ESCOPO |
| `content/medidas-associacao/biquali.qmd` | associação entre duas qualitativas e qui-quadrado | nenhum | n/a | n/a | n/a | n/a | n/a | n/a | associação exclusivamente qualitativa foi excluída | FORA DO ESCOPO |
| `content/medidas-associacao/scripts/assoc-municipies.r` | associação qualitativa | nenhum | n/a | n/a | n/a | n/a | n/a | n/a | suporte a conteúdo exclusivamente qualitativo | FORA DO ESCOPO |
| `content/medidas-associacao/scripts/entrevista-municipes.r` | dados qualitativos simulados | nenhum | n/a | n/a | n/a | n/a | n/a | n/a | suporte a conteúdo exclusivamente qualitativo | FORA DO ESCOPO |
| `content/medidas-associacao/series.qmd` | arquivo vazio de séries | nenhum | n/a | n/a | n/a | n/a | n/a | n/a | arquivo vazio e séries fora do escopo | FORA DO ESCOPO |
| `content/modelos-regressao-bayes/regressao-glm-hierarquico-apresentacao.qmd` | regressão bayesiana e GLM hierárquico | nenhum | n/a | n/a | n/a | n/a | n/a | n/a | Bayes, GLM e hierarquia avançada excluídos | FORA DO ESCOPO |
| `content/modelos-regressao-bayes/regressao-linear-bayesiana-bambi.qmd` | fluxo bayesiano com Bambi | nenhum | n/a | n/a | n/a | n/a | n/a | n/a | Bayes e Python excluídos | FORA DO ESCOPO |
| `content/modelos-regressao-bayes/regressao-linear-bayesiana.qmd` | regressão linear bayesiana | nenhum | n/a | n/a | n/a | n/a | n/a | n/a | regressão bayesiana excluída; parte linear coberta por fonte direta | FORA DO ESCOPO |
| `content/modelos-regressao-bayes/regressao-poisson.qmd` | modelo Poisson e modelos científicos | nenhum | n/a | n/a | n/a | n/a | n/a | n/a | Poisson e fluxo bayesiano excluídos | FORA DO ESCOPO |
| `content/multivariada-numerica/clustering.qmd` | agrupamento | nenhum | n/a | n/a | n/a | n/a | n/a | n/a | análise multivariada excluída | FORA DO ESCOPO |
| `content/multivariada-numerica/cossine-similarity.qmd` | similaridade por cosseno | nenhum | n/a | n/a | n/a | n/a | n/a | n/a | análise multivariada e álgebra matricial excluídas | FORA DO ESCOPO |
| `content/multivariada-numerica/intro-matrizes.qmd` | álgebra de matrizes | nenhum | n/a | n/a | n/a | n/a | n/a | n/a | geometria e álgebra matricial avançadas excluídas | FORA DO ESCOPO |
| `content/multivariada-numerica/introducao-PCA-2d.qmd` | PCA em Python | nenhum | n/a | n/a | n/a | n/a | n/a | n/a | multivariada e Python excluídos | FORA DO ESCOPO |
| `content/multivariada-numerica/ordination.qmd` | ordenação | nenhum | n/a | n/a | n/a | n/a | n/a | n/a | análise multivariada excluída | FORA DO ESCOPO |
| `content/regressao-linear/mmq-regressao-polinomial.qmd` | MMQ polinomial em Python | nenhum | n/a | n/a | n/a | n/a | n/a | n/a | regressão polinomial e implementação matricial excluídas | FORA DO ESCOPO |
| `topics/glms.qmd` | índice de GLMs | nenhum | n/a | n/a | n/a | n/a | n/a | n/a | GLMs fora do programa | FORA DO ESCOPO |
| `topics/intro-bayes.qmd` | índice de Bayes | nenhum | n/a | n/a | n/a | n/a | n/a | n/a | Bayes fora do programa | FORA DO ESCOPO |
| `topics/introducao-r.qmd` | índice de introdução ao R | nenhum | n/a | n/a | n/a | n/a | n/a | n/a | operação de software pertence às práticas | FORA DO ESCOPO |
| `topics/manipulacao-dados-R.qmd` | índice de manipulação em R | nenhum | n/a | n/a | n/a | n/a | n/a | n/a | operação de software pertence às práticas | FORA DO ESCOPO |
| `topics/manipulacao-dados-python.qmd` | índice de Python | nenhum | n/a | n/a | n/a | n/a | n/a | n/a | Python excluído | FORA DO ESCOPO |
| `topics/modelos-regressao-bayes.qmd` | índice de regressão bayesiana | nenhum | n/a | n/a | n/a | n/a | n/a | n/a | regressão bayesiana excluída | FORA DO ESCOPO |
| `topics/multivariada-numerica.qmd` | índice multivariado | nenhum | n/a | n/a | n/a | n/a | n/a | n/a | métodos multivariados excluídos | FORA DO ESCOPO |
| `index.qmd` | página inicial e navegação do MEAD | nenhum | n/a | n/a | n/a | n/a | n/a | n/a | infraestrutura editorial, sem conteúdo estatístico independente | FORA DO ESCOPO |
| `renv/activate.R` | ativação do ambiente do MEAD | nenhum | n/a | n/a | n/a | n/a | n/a | n/a | infraestrutura e dependência externa proibida | FORA DO ESCOPO |

## Fontes mistas: decisão por elemento

- `estrutura-tipo.qmd`: unidades, descritores, tipos, mensuração e ausência foram integrados;
  técnicas avançadas de imputação foram excluídas por exigirem um módulo próprio de dados ausentes.
- `probabilidade-condicional.qmd`: probabilidade condicional, independência e exclusão mútua foram
  integradas; Teorema de Bayes foi excluído conforme o escopo confirmado.
- Os dois tutoriais complementares da normal tiveram suas sequências escalares e probabilísticas
  integradas; implementação em Python foi substituída por R.
- `anova-simples.qmd`: modelo, derivação, exemplo, Tukey e pressupostos têm destinos nas semanas 9 e
  10; a semente do gerador original foi removida.
- `metodo-minimos-quadrados-apresentacao.qmd` e `mmq-regressao-linear-simples.qmd`: resíduos,
  minimização, coeficientes, ajustados, somas de quadrados e R2 foram integrados; geometria vetorial,
  solução matricial e Python foram excluídos.
- `regressao-linear-multipla.qmd`: coeficientes parciais, multicolinearidade, suporte, resíduos,
  alavancagem, Cook e transformações foram integrados; seleção automática não foi transportada.
- `funcoes-potencia.qmd`: relação espécie-área, linearização, interpretação e previsão foram
  integradas em R; a apresentação operacional em Python não foi preservada.
- Tutoriais de visualização: a escolha das geometrias e a leitura dos gráficos foram integradas;
  instalação de pacotes, formatação extensa, exportação e interatividade pertencem às práticas.

## Autonomia

As Leituras prévias não leem scripts, dados, imagens nem páginas de `mead-main-EXAMPLE`. Todos os
exemplos pequenos criam seus dados no próprio bloco; as figuras estatísticas são produzidas durante
a renderização. Não foi necessário copiar assets ou conjuntos externos. As referências já presentes
em `references.bib` cobrem as citações mantidas.

## Validação final

- A matriz contém 96 linhas de fontes: 53 com status `COMPLETO` e 43 com status
  `FORA DO ESCOPO`. A comparação automatizada com o inventário de arquivos não encontrou fonte
  ausente.
- Os 67 blocos de código recolhíveis foram executados separadamente em processos `R --vanilla`.
  Todos terminaram com código de saída zero, sem depender do ambiente criado por outro bloco.
- As leituras contêm 46 figuras e quatro tabelas com identificadores globais. Todas as figuras têm
  legenda e texto alternativo; todas as tabelas têm legenda. Não há identificadores duplicados.
- Duas passagens executaram individualmente as 15 leituras com `--execute --no-cache`; depois de
  cada passagem, uma renderização integral concluiu os 36 documentos do projeto. As quatro etapas
  terminaram com código de saída zero.
- A comparação das passagens confirmou nova execução das simulações. Entre os resultados que
  mudaram, a taxa simulada de falso alarme com três grupos passou de 12% para 11%, o desvio-padrão
  amostral das estações soltas passou de 0,70 para 0,67 e o número de intervalos sem cobertura em
  cem repetições passou de 1 para 5. Texto, gráficos e tabelas de cada passagem foram produzidos pelo
  mesmo objeto daquela execução.
- Uma cópia temporária sem o diretório `mead-main-EXAMPLE` renderizou integralmente os mesmos 36
  documentos. Isso confirma a autonomia de código, dados, figuras e referências.
- Capturas das 15 páginas foram inspecionadas em larguras de 1440 e 390 pixels. Equações, tabelas,
  código recolhível, figuras, legendas, callouts e navegação permaneceram legíveis, sem sobreposição
  ou corte visual observado.
- As verificações estáticas não encontraram `set.seed()`, travessões Unicode, links ou caminhos do
  MEAD fora desta auditoria, blocos `r` estáticos, `eval: false`, rótulos duplicados nem referências a
  assets inexistentes nas leituras.
