# Teste

Este repositório contém o link para a notebook [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1-fR_0jtT4mf2DNUy14ARGk1kHYTMZ1PP?usp=sharing) com os modelos de machine learning para fazer a predição do Price. O arquivo não encontra-se no repositório devido à limitação de tamanho de arquivos no github.



### Como foi a definição da sua estratégia de modelagem? 
A estratégica utilizada foi, em primeiro lugar, criar um modelo para servir como baseline para as futuras comparações.

Em seguida foi feita uma análise exploratória para conhecer melhor as features. 

Depois foi analisado a correlação linear entre as features, e com base nisso, foram removidas as features que possuiam pouca correlação. Os modelos foram retreinados para verificar se houve melhora na performance. Por isso a importância de ter um baseline logo no início.

Após a análise exploratória foi aplicado uma técnica de GridSearch nos dois melhores modelos para obter um conjunto de hyper-parametros que otimizem a performance do modelo.

Também foi implementado uma rede neural profunda usando as mesmas features numéricas. O resultado não foi melhor.

Por fim foi implementada uma rede neural profunda com adição das features textuais contidas na coluna Amenities.


### Como foi definida a função de custo utilizada?
Por ser um problema de regressão, a função custo é a MSE (Mean Squared Error)

### Qual foi o critério utilizado na seleção do modelo final? 
O modelo que possui maior fator R^2.

### Qual foi o critério utilizado para validação do modelo? Por que escolheu utilizar este método?
Para validação o dataset foi splitado em train/test/validation, usando 80%-10%-10%

### Quais evidências você possui de que seu modelo é suficientemente bom?
O modelo apresentou um Rˆ2 de ~ 0.6 que é regular considerando os preços com média de 701,00 e desvio padrão 5611,00.


### Algumas propostas para possíveis melhorias
- Treinar modelos em subconjunto de dados agregados por categoria de quarto, obtendo modelos menores e mais específicos.
- Criar algumas features compostas, como por exemplo, distância da localidade até o centro da cidade e também de algum ponto turístico importante. Isso seria possível pois há a localização GPS do local no dataset.