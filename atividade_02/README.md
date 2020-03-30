# 👋🛳️ Titanic: Machine Learning from Disaster

> Kaggle Competition [link](https://www.kaggle.com/c/titanic)

**Atividade 02 (kNN)**: vamos aplicar kNN para predizer os sobreviventes do Titanic.

Instruções gerais:

1. Volte ao notebook da prática anterior e divida a base em treinamento e testes
2. Crie um classificador kNN escolhendo um `k` que você deseje
3. Treine com todas as características numéricas 'escalonadas'
4. Faça a predição na base de testes
5. Avalie a qualidade do seu modelo de acordo com a quantidade de acertos e erros da predição quando comparada ao valor real - dê este valor como um percentual
6. Descubra o melhor valor de `k` executando várias vezes os passos `3` a `6` com diferentes valores possíveis de `k` e optando pela melhor avaliação.

## The Challenge

The sinking of the Titanic is one of the most infamous shipwrecks in history.

On April 15, 1912, during her maiden voyage, the widely considered “unsinkable” RMS Titanic sank after colliding with an iceberg. Unfortunately, there weren’t enough lifeboats for everyone onboard, resulting in the death of 1502 out of 2224 passengers and crew.

While there was some element of luck involved in surviving, it seems some groups of people were more likely to survive than others.

In this challenge, we ask you to build a predictive model that answers the question: “what sorts of people were more likely to survive?” using passenger data (ie name, age, gender, socio-economic class, etc).

## Data Description

The training set should be used to build your machine learning models. For the training set, we provide the outcome (also known as the “ground truth”) for each passenger. Your model will be based on “features” like passengers’ gender and class. You can also use feature engineering to create new features.

The test set should be used to see how well your model performs on unseen data. For the test set, we do not provide the ground truth for each passenger. It is your job to predict these outcomes. For each passenger in the test set, use the model you trained to predict whether or not they survived the sinking of the Titanic.

We also include gender_submission.csv, a set of predictions that assume all and only female passengers survive, as an example of what a submission file should look like.

## Data Dictionary

**Variable**|**Definition**|**Key**
:-----:|:-----:|:-----:
survival|Survival|0 = No, 1 = Yes
pclass|Ticket class|1 = 1st, 2 = 2nd, 3 = 3rd
sex|Sex|
Age|Age in years|
sibsp|# of siblings / spouses aboard the Titanic|
parch|# of parents / children aboard the Titanic|
ticket|Ticket number|
fare|Passenger fare|
cabin|Cabin number|
embarked|Port of Embarkation|C = Cherbourg, Q = Queenstown, S = Southampton

## Variable Notes

**pclass**: A proxy for socio-economic status (SES)

- 1st = Upper
- 2nd = Middle
- 3rd = Lower

**age**: Age is fractional if less than 1. If the age is estimated, is it in the form of xx.5

**sibsp** The dataset defines family relations in this way...

- Sibling = brother, sister, stepbrother, stepsister
- Spouse = husband, wife (mistresses and fiancés were ignored)

**parch** The dataset defines family relations in this way...

- Parent = mother, father
- Child = daughter, son, stepdaughter, stepson
- Some children travelled only with a nanny, therefore parch=0 for them
