# Avaliação de Modelo com Métricas de Classificação
Este script implementa uma função para avaliar modelos de classificação, calculando e exibindo métricas como precisão, revocação e F1-Score, além de exibir a matriz de confusão. Essas métricas ajudam a avaliar o desempenho do modelo em diferentes classes de uma forma ponderada.

Funcionalidades
Precisão (Precision): Mede a exatidão das previsões positivas do modelo.
Revocação (Recall): Mede a capacidade do modelo em recuperar verdadeiros positivos.
F1-Score: Calcula a média harmônica entre precisão e revocação.
Matriz de Confusão: Mostra a relação entre previsões corretas e incorretas para cada classe.
Essas métricas são calculadas com ponderação (average='weighted'), garantindo uma análise equilibrada mesmo para classes desbalanceadas.

Requisitos
Certifique-se de instalar as dependências antes de executar o código:

bash
Copiar código
pip install numpy pandas scikit-learn
Uso
A função evaluate_model recebe três parâmetros:

predictions: Lista com as previsões do modelo.
ground_truth: Lista com os valores reais para comparação.
class_labels: Lista opcional contendo o nome das classes.


# Avaliação de Modelo com Métricas de Classificação e IoU
Este projeto implementa funções para avaliar modelos de classificação, calculando e exibindo métricas como precisão, revocação, F1-Score, matriz de confusão e visualização de IoU por classe. Essas métricas são essenciais para compreender o desempenho do modelo em diferentes classes, permitindo ajustes e melhorias.

Funcionalidades
Função evaluate_model
Calcula e exibe as seguintes métricas:

Precisão (Precision): Exatidão das previsões positivas do modelo.
Revocação (Recall): Capacidade do modelo em identificar verdadeiros positivos.
F1-Score: Média harmônica entre precisão e revocação.
Matriz de Confusão: Relação entre previsões corretas e incorretas para cada classe.
Essas métricas são calculadas com ponderação (average='weighted') para considerar as classes desbalanceadas.

Função plot_iou_map:
Plota um gráfico de barras do IoU (Intersection over Union) por classe, permitindo uma visualização clara do desempenho em cada classe específica.

IoU (Intersection over Union): Métrica de avaliação para problemas de segmentação e detecção, que mede a sobreposição entre as previsões e os valores reais.

Requisitos:
pip install numpy pandas scikit-learn matplotlib

Uso:
Função evaluate_model
A função evaluate_model recebe três parâmetros:

predictions: Lista com as previsões do modelo.
ground_truth: Lista com os valores reais para comparação.
class_labels: Lista opcional com os nomes das classes.

Para calcular o IoU (Intersection over Union) usando a matriz de confusão, precisamos calcular o IoU individual para cada classe com base nos verdadeiros positivos (TP), falsos positivos (FP) e falsos negativos (FN) obtidos da matriz de confusão.


# Resultados:

![image](https://github.com/user-attachments/assets/f913a4a2-356a-4f31-a0a8-e9de4c911d2d)

![image](https://github.com/user-attachments/assets/004f1cf0-a192-4ecf-82c1-7619afd8bb28)

​![image](https://github.com/user-attachments/assets/e7f335d4-791c-4d5b-b162-fc70048859c4)

![image](https://github.com/user-attachments/assets/5187cc02-5dea-4c72-8377-080656ed4729)

![image](https://github.com/user-attachments/assets/f6824dc9-2454-44e6-a434-3a8319f79b60)

​![image](https://github.com/user-attachments/assets/339ec9d8-bfcd-4942-81e0-034f5dd5e6bd)

