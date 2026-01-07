# 🚢 Titanic: Previsão de Sobreviventes com Pipelines

![Status](https://img.shields.io/badge/status-conclu%C3%ADdo-brightgreen)

## 📄 Descrição do Projeto

Este projeto aborda o clássico desafio de Machine Learning de prever a sobrevivência dos passageiros do Titanic. O objetivo principal foi construir um pipeline de classificação robusto, demonstrando as melhores práticas de pré-processamento de dados e modelagem para um dataset com desafios do mundo real, como valores ausentes e múltiplos tipos de dados.

## 📊 Dataset

O dataset utilizado foi o "Titanic - Machine Learning from Disaster" do Kaggle. Ele contém informações demográficas e de viagem de 891 passageiros, incluindo a variável alvo `Survived` (0 = Não, 1 = Sim).

*   **Link para o Dataset:** [Titanic Dataset](https://www.kaggle.com/c/titanic/data)
*   **Desafios do Dataset:** O principal desafio foi lidar com valores ausentes em colunas importantes, especialmente `Age` (Idade).

## 🛠️ Ferramentas e Técnicas Utilizadas

*   **Linguagem:** Python 3
*   **Bibliotecas:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn
*   **Pré-processamento com Pipelines:** O coração deste projeto foi a utilização de `Pipelines` e `ColumnTransformer` do Scikit-learn para criar um fluxo de pré-processamento robusto e livre de *data leakage*. O pipeline executou as seguintes etapas:
    1.  **Imputação Numérica:** Valores ausentes na coluna `Age` foram preenchidos com a **mediana**.
    2.  **Imputação Categórica:** Valores ausentes na coluna `Embarked` foram preenchidos com a **moda** (valor mais frequente).
    3.  **One-Hot Encoding:** Variáveis categóricas (`Sex`, `Embarked`) foram transformadas em formato numérico.
    4.  **Scaling:** Todas as features numéricas foram padronizadas com `StandardScaler`.
*   **Modelo de Machine Learning:**
    *   **`RandomForestClassifier`**: Um modelo de Floresta Aleatória foi treinado como o classificador final, devido à sua alta performance e robustez.

## 📈 Resultados do Modelo

O pipeline completo, quando treinado e avaliado, alcançou um desempenho sólido no conjunto de teste:

*   **Acurácia Geral:** **80%**
*   **Performance na Detecção de Sobreviventes (Classe `1`):**
    *   🎯 **Precisão (Precision): 83%** - Quando o modelo prevê que um passageiro sobreviveu, ele está correto 83% das vezes.
    *   🎣 **Recall (Revocação): 66%** - O modelo conseguiu identificar com sucesso 66% de todos os passageiros que realmente sobreviveram.

**Conclusão Final:** O uso de pipelines do Scikit-learn permitiu a criação de um modelo de classificação eficaz e robusto, com um processo de pré-processamento limpo e profissional. O resultado de 80% de acurácia é um excelente *baseline* para este problema clássico.

## 🚀 Como Executar o Projeto

1.  **Clone o repositório.**
2.  **Instale as dependências.**
3.  **Execute o Notebook:** Abra e execute o arquivo `analise_titanic.ipynb` em um ambiente Jupyter.
