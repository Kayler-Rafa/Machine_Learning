# 📊 Projeto de Aprendizado de Máquina: Classificação e Regressão

Este repositório contém três projetos distintos aplicando técnicas de aprendizado de máquina supervisionado em diferentes conjuntos de dados. Cada projeto aborda tarefas específicas utilizando modelos adequados e análises detalhadas.

---

## 📁 Dataset A: Taiwanese Bankruptcy Prediction

### 🔍 Descrição do Dataset

- **Instâncias**: 6819
- **Variáveis**: 96
- **Variável Alvo**: `Bankrupt?` — variável binária indicando falência ou não.
- **Variáveis Preditivas**: Indicadores financeiros diversos (rentabilidade, margem de lucro, ativos, passivos etc.)

### 📊 Análise Exploratória

- Remoção de colunas com mais de 30% de valores ausentes.
- Seleção das variáveis com maior correlação com a variável alvo.
- Correlações analisadas com heatmaps e estatísticas.

### 🛠️ Engenharia de Características

- Remoção de valores ausentes.
- Padronização com StandardScaler.
- Normalização com MinMaxScaler.
- Seleção de variáveis relevantes com base na correlação.

### 🤖 Modelos de Classificação

- **Regressão Logística**  
  - Acurácia: 0.9694  
  - Precisão: 0.6876  
  - Revocação: 0.1045  
  - F1-Score: 0.1789  

- **KNN**  
  - Acurácia: 0.9689  
  - Precisão: 0.5456  
  - Revocação: 0.2000  
  - F1-Score: 0.2921  

- **Árvore de Decisão**  
  - Acurácia: 0.9680  
  - Precisão: 0.5914  
  - Revocação: 0.1091  
  - F1-Score: 0.1741  

- **Naive Bayes**  
  - Acurácia: 0.9529  
  - Precisão: 0.3231  
  - Revocação: 0.4045  
  - F1-Score: 0.3582  

- **Neural Network**  
  - Acurácia: 0.9689  
  - Precisão: 0.5759  
  - Revocação: 0.1500  
  - F1-Score: 0.2360  

### 📝 Discussão

- Modelos com alta acurácia, porém com baixo recall, indicando dificuldade em detectar casos de falência.
- Desequilíbrio na variável alvo impactou o desempenho.
- Possíveis extensões: uso de técnicas de balanceamento como SMOTE.

---

## 📁 Dataset B: MiniBooNE Particle Identification

### 🔍 Descrição do Dataset

- **Instâncias**: 130065
- **Variáveis**: 50
- **Variável Alvo**: Classe — 1 (sinal) e 0 (background).
- **Variáveis Preditivas**: Medições numéricas associadas a partículas físicas.

### 📊 Análise Exploratória

- Nenhum valor ausente.
- Padronização realizada.
- PCA aplicada para visualização bidimensional dos clusters.
- Correlações baixas entre as variáveis.

### 🛠️ Engenharia de Características

- Padronização com StandardScaler.
- PCA para redução de dimensionalidade e visualização.
- Divisão entre sinal e background conforme instruções do dataset.

### 🤖 Modelos de Classificação

- **Regressão Logística**  
  - Acurácia: 0.8560  
  - Precisão: 0.8136  
  - Revocação: 0.6316  
  - F1-Score: 0.7111  

- **KNN**  
  - Acurácia: 0.8829  
  - Precisão: 0.7830  
  - Revocação: 0.8063  
  - F1-Score: 0.7945  

- **Árvore de Decisão**  
  - Acurácia: 0.9105  
  - Precisão: 0.8368  
  - Revocação: 0.8461  
  - F1-Score: 0.8414  

- **Naive Bayes**  
  - Acurácia: 0.2841  
  - Precisão: 0.2815  
  - Revocação: 0.9995  
  - F1-Score: 0.4393  

- **Neural Network**  
  - Execução incompleta devido ao tempo de processamento elevado.

### 📝 Discussão

- Árvore de Decisão apresentou o melhor desempenho.
- Naive Bayes teve desempenho inadequado para esse tipo de dado.
- Neural Network não concluída por limitações de tempo.
- Extensão futura: concluir execução do MLP e realizar ajustes finos.

---

## 📁 Dataset C: Room Occupancy Estimation

### 🔍 Descrição do Dataset

- **Instâncias**: Aproximadamente 22650
- **Variáveis**: 18 (após remoção de `Date` e `Time`)
- **Variável Alvo**: `Room_Occupancy_Count` — número de ocupantes na sala (0 a 3).
- **Variáveis Preditivas**: Temperatura, Luminosidade, Som, CO₂, Inclinação de CO₂, sensores de movimento PIR.

### 📊 Análise Exploratória

- Sem valores ausentes.
- Correlações observadas entre sensores ambientais e ocupação.
- Distribuições analisadas com histogramas.

### 🛠️ Engenharia de Características

- Remoção de colunas de data e hora.
- Normalização com StandardScaler.
- Seleção de variáveis com base na relevância.

### 🤖 Modelos de Regressão

- **Regressão Linear**  
  - R²: 0.8878  
  - RMSE: 0.3034  
  - MAE: 0.1637  
  - MAPE: inf%  

- **MLP Regressor**  
  - R²: 0.9825  
  - RMSE: 0.1199  
  - MAE: 0.0358  
  - MAPE: inf%  

### 📝 Discussão

- MLP apresentou desempenho superior.
- O valor infinito do MAPE ocorreu devido à divisão por zero com valores reais igual a zero.
- Possíveis melhorias: utilizar métricas robustas a zero ou ajustar o cálculo do MAPE.

---

## 🧰 Tecnologias Utilizadas

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn

---

## 👥 Autores

- [Rafael "A lenda" Diniz](https://github.com/Kayler-Rafa)
- Amigos da lenda 

---

## 📬 Contato

Para dúvidas ou sugestões, entre em contato: [rafaeldinizcruz@gmail.com]
