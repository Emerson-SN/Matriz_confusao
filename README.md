 Cálculo de Métricas com Matriz de Confusão

Este notebook demonstra, de forma prática, como avaliar um modelo de Machine Learning utilizando métricas clássicas de classificação. O modelo é treinado com o dataset MNIST e avaliado a partir de sua matriz de confusão.

O objetivo principal é compreender como as métricas funcionam internamente, calculando-as manualmente a partir dos dados do modelo.

Etapas do Código

1. Treinamento do modelo

O código inicia com o treinamento de uma Rede Neural Convolucional (CNN) para classificar imagens de dígitos manuscritos (0 a 9). Após o treinamento, o modelo gera previsões para o conjunto de teste.

2. Geração da matriz de confusão

Com os rótulos reais (`y_true`) e as previsões do modelo (`y_pred`), é criada uma matriz de confusão.  
Essa matriz organiza os acertos e erros do modelo, onde a diagonal principal representa as classificações corretas.

3. Conversão para classificação binária
4. 
Para o cálculo das métricas solicitadas no desafio, o problema multiclasse é convertido em binário:

- Classe positiva: dígito 0  
- Classe negativa: dígitos 1 a 9  

Essa conversão permite aplicar corretamente métricas como precisão, sensibilidade e especificidade.

4. Extração de VP, FP, FN e VN

A partir da matriz de confusão são extraídos:

- VP (Verdadeiro Positivo): quando o modelo acerta a classe positiva  
- FN (Falso Negativo): quando o modelo erra a classe positiva  
- FP (Falso Positivo): quando o modelo indica positivo incorretamente  
- VN (Verdadeiro Negativo): quando o modelo acerta a classe negativa  

Esses valores são a base para o cálculo das métricas de avaliação.

5. Cálculo das métricas

As métricas são implementadas manualmente utilizando suas fórmulas matemáticas:

- Acurácia: desempenho geral do modelo  
- Precisão: confiabilidade das previsões positivas  
- Sensibilidade (Recall): capacidade de identificar corretamente os positivos  
- Especificidade: capacidade de identificar corretamente os negativos  
- F1-score: equilíbrio entre precisão e sensibilidade  

Nenhuma biblioteca pronta de métricas é utilizada.

### 6. Apresentação dos resultados

Os resultados finais são organizados em uma tabela, facilitando a visualização e interpretação do desempenho do modelo.

Conclusão

Este projeto reforça os fundamentos da avaliação de modelos de Machine Learning, mostrando de forma clara a relação entre matriz de confusão e métricas de desempenho, promovendo um aprendizado sólido e prático.

