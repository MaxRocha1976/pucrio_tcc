# Predição de Demandas de Estoque com o uso de Recurrent Neural Network LSTM (Long Short Term Memory)

## Trabalho de Conclusão de Curso

### Pontifícia Universidade Católica do Rio de Janeiro – Puc-Rio

### Curso:  	Pós Graduação em Business Intelligence - BI MASTER (https://ica.puc-rio.ai/bi-master)

### Aluno: 	    Maximiliano Augusto Rocha Júnior.

### Matrícula: 	181.477.003

### Orientador:	Leonardo Forero Mendonza


## Introdução

No Brasil, o setor Atacadista é responsável pela distribuição de produtos industrializados para empresas Varejistas, que por sua vez, comercializam estes produtos com à população de modo geral.  
Neste cenário, as distribuidoras atacadistas, tem papel fundamental no abastecimento de produtos, de diversas categorias, onde podemos destacar os produtos de primeira necessidade dos segmentos alimentícios, higiene e limpeza.
Para que este processo aconteça com excelência, é necessário conhecer bem o comportamento de consumo em cada região, de forma a fazer com que o produto colocado na ponta de gôndola do grande supermercado ou na prateleira da pequena mercearia, seja visualizado, apreciado e adquirido pelo consumidor. 
O conhecimento do comportamento de consumo de cada região, já não pode ser analisado de forma empírica, mas necessita de indicadores precisos de hábitos de consumidores para direcionar a cadeia de abastecimento, evitando assim prejuízos pelo vencimento dos produtos em excesso nas gôndolas, bem como o desabastecimento da população pela falta do mesmo.


## Objetivo

O intuito deste trabalho é aplicar técnicas e conceitos modernos de Machine Learning para apoio à tomada de decisões pelos gestores e ou colaboradores no processo da cadeia de distribuição.
Demonstrar o uso de Redes Neurais Recorrentes com LSTM para predição de quantidades em caixas da venda de um produto comum de mercado. 
O "comprador" de posse desta informação com antecedência pode garantir o abastecimento, evitando a falta de estoque e o excesso de produtos no armazém WMS da empresa e melhorando o fluxo de caixa financeiro, otimizando a recepção, armazenamento e distribuição do produto.
Por fim, utilizaremos uma compilação de técnicas aprendidas no decorrer do curso com algoritmos de Machine Learning, Deep Learning, análise exploratória e preditiva dos dados.

## Motivação

Este trabalho foi desenvolvido, para uma empresa distribuidora de produtos alimentícios, higiene e limpeza, (aqui preservada sua a identidade), que atua no mercado de distribuição atacadista desde 2009, com equipe de vendas de aproximadamente 350 funcionários, presente em mais de 400 cidades, abastecendo cerca de 8 milhões de consumidores no estado de Minas Gerais.  
Seu time operacional é composto por uma equipe de aproximadamente 130 vendedores e 15 coordenadores, além de seus colaboradores internos, que consomem informações de acompanhamento da distribuição de aproximadamente 1500 produtos ativos de 30 diferentes fabricantes.
O acompanhamento destes dados, oriundos de sistemas de SFA, ERP, WMS e BI geram um grande esforço para catalogar e analisar milhares de registros de dados, em diversas bases gerenciadas por SGDBs distintos.
Para este trabalho foi utilizado o banco de dados Oracle para a extração dos dados históricos e máquinas virtuais na Google Cloud, onde podemos aplicar as técnicas necessárias com a linguagem Python, organizando de maneira didática os códigos utilizados através de Notebooks Python para explorar, inferir, analisar e consumir as informações processadas.

## Metodologia

1.	Seleção: Nesta etapa foi escolhido um produto de exemplo, Lamen Nissin Galinha Caipira, e extraído os dados de vendas mensais a no período entre 2011 e 2021  através de comandos SQL no banco de dados Oracle, transformando o resultado da Query em um arquivo de saída texto separado por vírgulas, este arquivo por sua vez foi salvo no Google Drive.
2.	Utilizado um Notebook Python na ferramenta Google Colaboratory para codificação na linguagem Python.
3.	Montado o Drive Google através do biblioteca google.colab e definido um diretório de trabalho.
4.	Para desenvolvimento do código, foram usadas as bibliotecas, Pandas, Sklearn, Keras, Math, Matplotlib, Numpy.
5.	Os dados CSV do arquivo ‘lamen_mes.csv’ foram alocados em um dataset.
6.	Os dados foram normalizados e escalados para números entre 0 e 1.
7.	A partir desta etapa, foram utilizados os algoritmos de Redes Neurais Recorrentes com LSTM, onde utilizamos quatro camadas com 150, 100 e 50 neurônios de entrada e uma camada de saída com 1 neurônio.
8.	A Rede Neural foi compilada com otimizador ‘adam’ e o erro foi mensurado com ‘mean_squared_error’ e métricas de acurácia ‘acc’.
9.	O treinamento da rede, foi executado diversas vezes com quantidades de épocas diferentes, até que o melhor resultado de configuração com 300 épocas fosse alcançado, para isto foram usados dados dos últimos 9 anos para treino.
10.	Foi separado um período do último ano para Teste na rede neural.
11.	Os resultados reais e de predição foram plotados em um gráfico e sobrepostos para avaliação da acurácia alcançada.
12.	Para métricas de avaliação foram usadas as técnicas de RMSE (Root mean Squared Error), MAE (Mean Absolute Error) e MAPE (Mean Absolute Percentage Error) sendo este último usado como norte para os testes e alcançando resultados de erros na predição próximos à 15% e acertos na casa de 85% de acurácia.


## Codificação

Link para o código no GitHub: 


## Conclusão

Dadas a dimensão da movimentação de produtos na empresa, podemos considerar que a cada 1% melhorado na acurácia final da Rede Neural Recorrente LSTM, implementamos consideravelmente a economia de recursos financeiros na etapa de Compra, bem como a otimização e economia de espaço físico no Armazém da empresa, ainda mais importante, o aumento de vendas devido o correto abastecimento dos produtos e a eliminação de rupturas de mercado.
É possível ainda mensurar os erros médios, através da escolha de uma métrica simplificada como o índice MAPE, e aprimorar o modelo de algoritmo proposto através do aprendizado de máquinas e parametrização simplificada do modelo.



