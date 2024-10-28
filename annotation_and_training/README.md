# Processo de anotação e treinamento

## Anotação
Anotar dados para localização de objetos significa marcar as regiões de interesse em uma imagem onde os objetos aparecem e associá-los com uma classe específica. Esse processo é essencial para criar um dataset de treino confiável para o modelo.

## Etapas do processo de anotação:
1 - Escolha do Dataset: O dataset pode ser coletado manualmente ou obtido de fontes públicas. Ele deve conter uma variedade de imagens com os objetos de interesse visíveis de diferentes ângulos, tamanhos e iluminações.

2 - Definição das Classes: Antes de iniciar a anotação, é necessário definir as categorias ou classes de objetos que serão localizados (por exemplo, "cachorro", "carro", "pessoa").

3 - Anotação de Caixas Delimitadoras (Bounding Boxes): A anotação envolve desenhar caixas ao redor dos objetos de interesse. Isso é feito marcando as coordenadas do canto superior esquerdo e do canto inferior direito para criar uma caixa que delimita o objeto.

4 - Ferramentas de Anotação: Existem várias ferramentas disponíveis para anotação de imagens, como:
LabelImg: uma ferramenta de anotação manual popular para desenhar bounding boxes.
CVAT: uma plataforma de anotação para tarefas mais complexas, como segmentação semântica.

5 - Formato de Saída dos Dados: A anotação resulta em um arquivo de saída (geralmente um arquivo XML, JSON ou TXT) que contém as classes de cada objeto e as coordenadas de suas caixas delimitadoras.

## Treinamento do Modelo (Object Localization):
O treinamento de um modelo para localização de objetos usa os dados anotados para aprender a prever a presença e a localização dos objetos em imagens. Para isso, utilizam-se arquiteturas de deep learning especializadas.

## Principais Componentes do Processo de Treinamento:
Modelo Base: O modelo mais comum para object localization é uma rede neural convolucional (CNN), uma arquitetura excelente para extrair características espaciais de imagens. Exemplos de arquiteturas usadas incluem:
YOLO (You Only Look Once): Este é um modelo famoso para detecção de objetos em tempo real, que divide a imagem em uma grade e faz previsões das caixas delimitadoras e classes para cada célula da grade.

Input (Entradas): As imagens de entrada são passadas para a rede junto com as anotações das caixas delimitadoras e suas respectivas classes. A rede precisa aprender tanto a localizar (prever as coordenadas corretas das caixas) quanto a classificar (prever corretamente a classe do objeto dentro de cada caixa).

Função de Custo: O treinamento é guiado por uma função de custo que leva em consideração:

Erro de Localização: Medido como a diferença entre as caixas preditas e as caixas anotadas no dataset. Uma métrica comum é o IoU (Intersection over Union), que calcula a interseção entre a caixa predita e a anotada, dividida pela união das duas caixas.

Erro de Classificação: Refere-se à previsão incorreta da classe do objeto dentro da caixa. O erro é minimizado usando uma função de perda, como Cross-Entropy Loss.

Data Augmentation: Para aumentar a robustez do modelo e melhorar a generalização, técnicas de data augmentation são aplicadas ao dataset de treinamento. Isso pode incluir:

Rotação ou espelhamento das imagens.

Ajuste no brilho ou contraste.

Zoom ou corte para criar mais variação nas caixas delimitadoras.


Treinamento: O treinamento consiste em passar as imagens e suas anotações para o modelo durante várias iterações (épocas). Em cada iteração, o modelo ajusta seus pesos para minimizar a função de custo.
