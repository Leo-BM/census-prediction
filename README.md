# 📊 Classificação de Renda - Censo Americano

> *Um estudo prático sobre Algoritmos de Classificação (Árvores de Decisão e Random Forest) aplicados a dados demográficos.*

##  Sobre Mim e o Projeto
Olá! Sou um desenvolvedor Front-end em transição de carreira para a área de **Data Science e Machine Learning**. 

Este repositório documenta meus estudos iniciais com algoritmos de classificação supervisionada. O objetivo deste projeto não é apenas obter a maior acurácia possível, mas sim consolidar os fundamentos de pré-processamento de dados, análise exploratória e a diferença prática entre modelos de árvore única e florestas de decisão.

##  O Dataset
Utilizei a base de dados clássica **"Census Income"** (também conhecida como *Adult Data Set*).
* **Fonte:**  https://archive.ics.uci.edu/dataset/20/census+income   -> Extraída do censo de 1994 dos EUA.
* **Objetivo:** Prever se a renda anual de uma pessoa excede **$50.000 (<=50K ou >50K)**.
* **Atributos:** Idade, classe de trabalho, educação, estado civil, ocupação, relacionamento, raça, sexo, horas trabalhadas por semana, país nativo, etc.

##  Tecnologias Utilizadas
* **Linguagem:** Python
* **Manipulação de Dados:** Pandas, NumPy
* **Visualização:** Matplotlib, Seaborn
* **Machine Learning:** Scikit-Learn (Decision Tree, Random Forest)
* **Ferramenta:** Google Colab / Jupyter Notebook

##  Etapas do Projeto

### 1. Análise Exploratória de Dados (EDA)
Realizei uma análise visual para entender a distribuição dos dados, identificando padrões como:
* Distribuição de idade e horas de trabalho.
* Desbalanceamento das classes (há muito mais pessoas ganhando <=50K do que >50K).
* Visualização de *Outliers* através de Boxplots.

### 2. Pré-processamento
Esta foi a etapa mais crítica do aprendizado. Tratei os dados brutos para que pudessem ser lidos pelos algoritmos:
* **Tratamento de dados faltantes.**
* **Separação de variáveis:** Divisão entre previsores (X) e classe (y).
* **Encoding:** Transformação de variáveis categóricas (texto) em numéricas. Estudei o uso de `LabelEncoder` e as vantagens do `OneHotEncoder` via `ColumnTransformer`.
* **Escalonamento:** Padronização de escalas (StandardScaler) para variáveis numéricas (embora árvores sofram menos com isso, é uma boa prática).
* **Divisão Treino/Teste:** Separação clássica para validar o modelo.

### 3. Modelagem e Comparativo
Treinei e comparei dois algoritmos populares:

| Modelo | Acurácia (Teste) | Observações |
| :--- | :--- | :--- |
| **Árvore de Decisão** (Decision Tree) | *~81.0%* | Modelo mais simples, rápido, porém tende a sofrer overfitting facilmente se não podado. |
| **Random Forest** (Floresta Aleatória) | *~85.0%* | Modelo de *Ensemble*. Mais robusto e estável, pois combina o voto de múltiplas árvores (neste teste, usamos 40 árvores). |

> *Nota: Os valores de acurácia podem variar ligeiramente dependendo da semente aleatória (random_state) utilizada na separação dos dados.*

## 🚀 Próximos Passos (Melhorias Futuras)
Como parte do meu aprendizado contínuo, pretendo revisitar este projeto para aplicar:
- [ ] **Cross-Validation (Validação Cruzada)** para ter uma métrica de acurácia mais confiável.
- [ ] **GridSearchCV** para encontrar os melhores parâmetros automaticamente (tuning).
- [ ] Testar algoritmos mais avançados como **XGBoost** ou **LightGBM**.
- [ ] Melhorar o tratamento do desbalanceamento de classes (SMOTE).

##  Contato
Se você tiver dicas ou sugestões de melhoria para o código, sinta-se à vontade para abrir uma *issue* ou entrar em contato! Estou sempre aberto a aprender.

---
*Desenvolvido por Leonardo Bento Maria durante estudos de Machine Learning.*
