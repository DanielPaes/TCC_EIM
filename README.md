# TCC_EIM
Aqui estão os códigos usados em meu TCC do curso de Engenharia Industrial Madeireira.

---

## Introdução

O trabalho se propôs a usar técnicas da visão computacional e do aprendizado de máquina para a criação de modelos especializados na identificação de defeitos em imagens de lâminas da madeira de *Pinus*.
As imagens foram obtidas em laboratório, usando um mini estúdio para controle da iluminação. Cada imagem foi classificada em uma das seguintes classes: sem defeito, nó, casca/resina ou trinca. A rotulação das classes foi feita de maneira individual por um operador humano. Os modelos foram gerados usando o aprendizado supervisionado.
Para a extração das feautures, utilizou-se a GLCM e o Filtro de Gabor. Os modelos de classificação foram criados usando os algortimos: KNN, SVM, Árvore de Decisão e Regressão Logística.
Ao final, os desempenhos dos modelos de classificação foram calculados usando as métricas *acurracy, precision, recall* e *f1-score*.

## Extração de caractísticas

Na extração das caracteríticas, foram utilizados a GLCM e o Filtro de Gabor. 

1. **GLCM**: foi construída usando 1 distância e 4 ângulos. As features extraídas foram: *contrast, dissimilarity, homogeneity, energy, correlation* e *ASM*. Algoritmo usado: [GLCM](https://github.com/DanielPaes/TCC_EIM/blob/main/Pinus_Aplicando_%20GLCM.ipynb).


2. **Filtro de Gabor**: se variou o frequency e o theta, gerando 64 filtros. De cada filtro, se calculou o somatório, média e energia. Ao final, foram extraídas 192 features por imagem. Algoritmo usado: [Filtro de Gabor](https://github.com/DanielPaes/TCC_EIM/blob/main/Pinus_Aplicando_Gabor.ipynb).

## Modelos de Classificação

Os classificadores foram gerados usando os dados extraídos com a GLCM e o Filtro de Gabor. Abaixo são listados os algoritmos usados.

### 1. Modelos usando GLCM

1. [GLCM - KNN](https://github.com/DanielPaes/TCC_EIM/blob/main/GLCM_KNN.ipynb)
2. [GLCM - SVM](https://github.com/DanielPaes/TCC_EIM/blob/main/GLCM_SVM.ipynb)
3. [GLCM - Árvore de decisão](https://github.com/DanielPaes/TCC_EIM/blob/main/GLCM_RandomForest.ipynb)
4. [GLCM - Regressão Logística](https://github.com/DanielPaes/TCC_EIM/blob/main/GLCM_LogisticRegression.ipynb)

### 2. Modelos usando Filtro de Gabor

1. [Filtro de Gabor - KNN](https://github.com/DanielPaes/TCC_EIM/blob/main/Gabor_KNN.ipynb)
2. [Filtro de Gabor - SVM](https://github.com/DanielPaes/TCC_EIM/blob/main/Gabor_SVM.ipynb)
3. [Filtro de Gabor - Árvore de decisão](https://github.com/DanielPaes/TCC_EIM/blob/main/Gabor_RandomForest.ipynb)
4. [Filtro de Gabor- Regressão Logística](https://github.com/DanielPaes/TCC_EIM/blob/main/Gabor_LogisticRegression.ipynb)


## Conclusão

Os algoritmos utilizados possibilitaram estudar e avaliar a aplicação das técnicas de visão computacional e aprendizado de máquina no problema proposto.
Houve algumas diferenças entre os modelos de classificação, mostrando que as diferentes técnicas computacionais possuem particularidades que devem ser consideradas.
