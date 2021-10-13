# TCC_EIM
Aqui estão os códigos usados em meu TCC do curso de Engenharia Industrial Madeireira

---

## Introdução

O trabalho se propôs a usar técnicas da visão computacional e do aprendizado de máquina para a criação de modelos especializados na identificação de defeitos em imagens de lâminas da madeira de *Pinus*.
As imagens foram obtidas em laboratório, usando um mini estúdio para controle da iluminação. Cada imagem foi classificada em uma das seguintes classes: sem defeito, nó, casca/resina ou trinca. A rotulação das classes foi feita de maneira individual por um operador humano. Os modelos foram gerados usando o aprendizado supervisionado.
Para a extração das feautures, utilizou-se a GLCM e o Filtro de Gabor. Os modelos de classificação foram criados usando os algortimos: KNN, Decision Tree, SVM e regressão logística.
Ao final, os desempenhos dos classificadores foram calculados usando as métricas *acurracy, precision, recall* e *f1-score*.

## Extração de caracetísticas

Na extração das caracteríticas, foram utilizados a GLCM e o Filtro de Gabor. 

1. **GLCM**: foi construída usando 1 distância e 4 ângulos. As features extraídas foram: *contrast, dissimilarity, homogeneity, energy, correlation* e *ASM*

2. **Filtro de Gabor**: se variou o frequency e o theta, gerando 64 filtros. De cada filtro, se calculou o somatório, média e energia. Ao final, foram extraídas 192 features por imagem.


