# Segmentação Estratégica de Talentos com K-means

**Autora:** Mikaela Garcia Fernandes  
**Orientadora:** Ana Julia Righetto  
**Curso:** MBA em Data Science and Analytics - USP/Esalq (2025)

---

## 1. Visão Geral

Este repositório contém o código-fonte e a análise de dados desenvolvidos para o Trabalho de Conclusão de Curso (TCC) intitulado **"Segmentação Estratégica de Talentos: Uma Aplicação de *K-means* na Gestão de Desempenho Orientada a Dados"**.

O estudo aborda o desafio da subjetividade nos processos de avaliação de desempenho e propõe um *framework* de apoio à decisão, baseado em aprendizado não supervisionado, para segmentar colaboradores de forma objetiva. A aplicação do algoritmo de clusterização *K-means* permite a identificação de perfis profissionais distintos, possibilitando que as estratégias de gestão de talentos (desenvolvimento, retenção, sucessão, etc.) sejam personalizadas e mais eficazes.

## 2. Análise e Resultados

A metodologia completa e a discussão dos resultados encontram-se no [documento TCC](TCC_MBA_em_Data%20Science_and_Analytics_Mikaela%20Garcia%20Fernandes_2025.docx). Os principais achados foram:

* **Determinação de K=4:** Após uma análise comparativa de três métodos de validação distintos (*Elbow*, *Silhouette* e *Calinski-Harabasz*), o número de quatro *clusters* foi definido como a solução ótima por oferecer o melhor balanço entre rigor estatístico e interpretabilidade gerencial.
* **Criação de 4 Personas:** A análise permitiu a caracterização de quatro perfis profissionais distintos:
    * **Cluster 0: Profissionais Juniores Sólidos**
    * **Cluster 1: Profissionais Plenos/Sênior Estáveis**
    * **Cluster 2: Líderes e Especialistas Seniores**
    * **Cluster 3: Novos Talentos / Início de Carreira**
* **Principal *Insight***: A validação estatística via ANOVA revelou que a principal distinção entre os grupos não reside no desempenho ou na satisfação — que se mostraram homogêneos —, mas sim no **estágio da jornada de carreira** de cada colaborador.

### Visualização dos Clusters (PCA)
![Visualização dos Clusters com PCA](figura_5_visualizacao_pca.png)

## 3. Reprodutibilidade do Estudo

Para garantir a total reprodutibilidade desta análise, seguem as informações técnicas.

* **Notebook:** O código completo está disponível no arquivo [`TCC_K_means.ipynb`](TCC_K_means.ipynb).
* **Dataset:** Foi utilizado o *dataset* público "IBM HR Analytics Employee Attrition & Performance", disponível no Kaggle. O código lê os dados diretamente de um repositório para garantir a execução.
* **Ambiente:** Python 3.10
* **Bibliotecas Principais:** `pandas`, `numpy`, `matplotlib`, `seaborn`, `plotly`, `scikit-learn`, `scipy`.
* **Instalação:** Para instalar todas as dependências, execute o seguinte comando:
    ```bash
    pip install -r requirements.txt
    ```
    *(Nota: O arquivo `requirements.txt` deve ser gerado a partir do seu ambiente)*
* **Seed Aleatória:** Para garantir a consistência dos resultados do *K-means*, a `random_state` (ou `np.random.seed`) foi fixada em `42`.

## 4. Contato

Para mais informações, entre em contato:

* **Mikaela Garcia Fernandes:** mikaelagarciaf@gmail.com
