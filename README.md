# Aprendizado de maquinas para óxido de grafeno
Aplicação de Modelos de Aprendizado de Máquina na Predição de Propriedades de Óxido de Grafeno
Esse repositório apresenta ferramentas úteis para o compreendimento de dados a respeito de flakes de óxido de grafeno. Grafeno é uma estrutura composta apenas por carbono, é uma monocamada de grafite. Seu óxido, portanto, é essa mesma estrutura, porém com defeitos de oxigênio e hidrogênio.

Um breve guia de onde encontrar as informações citadas no readme. Os códigos foram separados da seguinte maneira:

- pre_processamento_dados.ipynb : correlação entre as features e os targets, matriz de correlação, histograma de ambos targets.
- aprendizado_maquina_grafeno.ipynb : modelo baseline, modelo Knn, modelo linear (normalizado e não normalizado), árvore de decisão, floresta aleatória, gráfico de importância.

Selecionamos quais eram mais úteis para nossos targets numéricos, que são a energia de fermi¹ e energia por átomo. Para isso calculamos quão relacionados estavam cada uma das features dos dados (tínhamos aproximadamente 800 delas) com as informações que queríamos (nosso target). Relacionamos eles usando o coeficiente de correlação de Pearson.

Conseguimos juntar essa informação na tabela abaixo, nela podemos observar que as fatures que mais se relacionam com a energia de fermi estão próximos de 1 ou –1 (caso exista uma relação de proporção inversa).

Atributos para calcular a energia de Fermi:

![Texto alternativo]([https://github.com/Karl-Marcos/ML-2022-DIMP/blob/main/imagens/atributos_energia_fermi.png](https://github.com/isadoramarcondes/Aprendizado-de-maquinas-para-oxido-de-grafeno/blob/main/Imagens/correl_fermi.png)

Atributos para calcular a energia por átomo:

![Texto alternativo](https://github.com/isadoramarcondes/Aprendizado-de-maquinas-para-oxido-de-grafeno/blob/main/Imagens/atributos_energia_por_atomo.png)

Para o Aprendizado supervisionado utilizamos as seguintes bibliotecas:

`pandas`, `matplotlib.pyplot`, `plt.style.use('seaborn-bright')`, `numpy`, `lmfit`, `sklearn` 

Para calcular métricas de Machine Learnig, testaremos modelos:

- Baseline;
- K-NN;
- Linear Normalizado;
- Linear Não-Normalizado;
- Árvore de decisão;
- Floresta aleatória

Antes de testar os modelos e decidir qual o melhor para o nosso `dataset`, separamos os dados em dois grupos diferentes: teste e treino. Os dados de teste são usados somente na hora de testar os modelos, para não haver possibilidade do algoritimo ter decorado os dados e devolvido somente um valor que já era conhecido. Para melhorarmos os nossos modelos, nós também modificamos os hiperparâmetros para podermos ter melhores resultados das relações. 

