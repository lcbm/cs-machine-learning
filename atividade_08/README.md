# Seatle, WA, NOAA Climate Data

**Atividade 08 (Decision Trees)**: Nesta base vamos tentar predizer a temperatura máxima do dia seguinte em Seattle-WA baseado em dados climáticos.

Instruções gerais:

1. Carregue a base temps.csv e prepare os dados
    - Visualização, tratamento de colunas, divisão de dados, etc
2. Crie e treine uma Árvore de Decisão
   - Varie alguns parâmetros e avalie por meio de validação cruzada considerando que se trata de uma série temporal
   - Obs.: por se tratar de uma série de dados temporal, existem algumas implicações na validação cruzada.
   - Favor ler este link e tentar se adaptar a este fator
3. Treine o modelo final e avalie-o na base de testes
   - Utilize os melhores parâmetros descobertos na etapa anterior, use o modelo para predizer a temperatura (actual) na base de testes e avalie o resultado
4. Exiba a árvore final em texto simples e como uma imagem
5. Extra: exiba a predição e os dados reais (eixo y) vs a data (eixo x)
