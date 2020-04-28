# Clustering

**Atividade 06 (Clustering)**: Stock Returns baseado em Dividend Yields.

**k-Means**:

- Carregue a base `sample_stocks.csv`
- Visualize suas informações
- Plote a dispersão de returns vs. dividendyield
- Normalize os dados
- Plote novamente a dispersão
- Crie e treine o KMeans com um valor de k que achar válido
- Plote a dispersão juntamente com os `kmeans.cluster_centers_`
- Analise o valor de `K` utilizando o método `Elbow` baseado na inércia (`kmeans.inertia_`)

**Clustering Hierárquico**:

- Implemente Clustering Hierárquico
  - Caso seja lento, altere a distância utilizada (linkage) ou faça amostragem nos dados
- Plote o dendograma

**Implementação Livre**:

Implemente pelo menos mais uma forma de clustering a seu critério e compare as três formas de visualização.

- Sugestão: DBSCAN, Mean-Shift, ...
