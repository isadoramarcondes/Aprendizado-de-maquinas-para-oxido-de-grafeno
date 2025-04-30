# Aprendizado de maquinas para óxido de grafeno
Aplicação de Modelos de Aprendizado de Máquina na Predição de Propriedades de Óxido de Grafeno

Com os dados em mãos, precisávamos selecionar quais eram mais úteis para nossos targets numéricos, que são a energia de fermi¹ e energia por átomo. Para isso calculamos quão relacionados estavam cada uma das features dos dados (tínhamos aproximadamente 800 delas) com as informações que queríamos (nosso target). Relacionamos eles usando o coeficiente de correlação de Pearson.

Conseguimos juntar essa informação na tabela abaixo, nela podemos observar que as fatures que mais se relacionam com a energia de fermi estão próximos de 1 ou –1 (caso exista uma relação de proporção inversa).

Atributos para calcular a energia de Fermi:

![Texto alternativo](https://github.com/Karl-Marcos/ML-2022-DIMP/blob/main/imagens/atributos_energia_fermi.png)

Atributos para calcular a energia por átomo:

