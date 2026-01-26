![[Pasted image 20240810152637.png]]

Claro, a diferença entre os métodos de treinamento de redes neurais supervisionadas e não supervisionadas está na forma como os dados são usados durante o treinamento. Aqui está uma explicação simples de cada um:
![[Pasted image 20240810153018.png]]

### **Supervised Learning (Aprendizado Supervisionado)**

1. **Definição**: No aprendizado supervisionado, o modelo é treinado com um conjunto de dados que contém exemplos de entrada e suas respectivas saídas (rótulos). O objetivo é fazer previsões ou classificações baseadas nesses dados.

2. **Exemplo de Dados**: Suponha que você tenha um conjunto de imagens de gatos e cachorros, e cada imagem já foi rotulada como "gato" ou "cachorro". O modelo aprende a identificar características das imagens para classificar novas imagens corretamente.

3. **Objetivo**: O objetivo é minimizar a diferença entre a previsão do modelo e a saída real conhecida, ajustando os parâmetros da rede para melhorar a precisão das previsões.

4. **Aplicações**: Classificação de e-mails como spam ou não spam, reconhecimento de voz, e previsão de preços de imóveis.

### **Unsupervised Learning (Aprendizado Não Supervisionado)**

1. **Definição**: No aprendizado não supervisionado, o modelo é treinado com dados que não têm rótulos ou saídas conhecidas. O objetivo é identificar padrões, estruturas ou agrupamentos nos dados.

2. **Exemplo de Dados**: Suponha que você tenha um conjunto de dados de imagens sem rótulos. O modelo pode agrupar as imagens em clusters baseados em semelhança, sem saber se as imagens são de gatos ou cachorros.

3. **Objetivo**: O objetivo é explorar e entender a estrutura dos dados, identificar padrões, ou reduzir a dimensionalidade dos dados, sem um "alvo" específico para prever.

4. **Aplicações**: Agrupamento de clientes em segmentos de mercado, redução de dimensionalidade para visualização, e detecção de anomalias.

### **Resumindo**

- **Aprendizado Supervisionado** usa dados rotulados e visa prever ou classificar dados com base nesses rótulos.
- **Aprendizado Não Supervisionado** usa dados não rotulados e visa explorar e encontrar padrões ou estruturas ocultas nos dados.

Cada método é útil em diferentes situações, dependendo dos objetivos e da disponibilidade de rótulos para os dados.

Vamos ver exemplos básicos de aprendizado supervisionado e não supervisionado usando Python e bibliotecas populares como `scikit-learn` e `numpy`.

### Exemplo 1: Aprendizado Supervisionado

Vamos usar um classificador de exemplo com o algoritmo K-Nearest Neighbors (KNN) para classificar flores Iris. 

```python
import numpy as np
from sklearn.datasets import load_iris
from sklearn.model_selection import train_test_split
from sklearn.neighbors import KNeighborsClassifier
from sklearn.metrics import accuracy_score

# Carregar o conjunto de dados Iris
iris = load_iris()
X = iris.data  # Características das flores
y = iris.target  # Rótulos das flores

# Dividir os dados em conjuntos de treino e teste
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.3, random_state=42)

# Criar o classificador KNN
model = KNeighborsClassifier(n_neighbors=3)

# Treinar o modelo
model.fit(X_train, y_train)

# Fazer previsões
y_pred = model.predict(X_test)

# Avaliar a precisão
accuracy = accuracy_score(y_test, y_pred)
print(f'Precisão do classificador KNN: {accuracy:.2f}')
```

### Exemplo 2: Aprendizado Não Supervisionado

Vamos usar o algoritmo de agrupamento K-Means para agrupar dados de flores Iris em clusters.

```python
import numpy as np
from sklearn.datasets import load_iris
from sklearn.cluster import KMeans
from sklearn.preprocessing import StandardScaler
import matplotlib.pyplot as plt

# Carregar o conjunto de dados Iris
iris = load_iris()
X = iris.data  # Características das flores

# Normalizar os dados
scaler = StandardScaler()
X_scaled = scaler.fit_transform(X)

# Criar o modelo KMeans
kmeans = KMeans(n_clusters=3, random_state=42)

# Ajustar o modelo aos dados
kmeans.fit(X_scaled)

# Obter os rótulos dos clusters
labels = kmeans.labels_

# Plotar os resultados
plt.scatter(X_scaled[:, 0], X_scaled[:, 1], c=labels, cmap='viridis')
plt.xlabel('Feature 1')
plt.ylabel('Feature 2')
plt.title('Agrupamento K-Means dos dados Iris')
plt.colorbar(label='Cluster')
plt.show()
```

### Resumo dos Exemplos:

1. **Aprendizado Supervisionado**: O primeiro exemplo usa o classificador KNN para prever a classe das flores Iris com base em características rotuladas. Ele é treinado com dados conhecidos e avalia a precisão de suas previsões.

2. **Aprendizado Não Supervisionado**: O segundo exemplo usa o K-Means para agrupar os dados de flores Iris em clusters baseados em características não rotuladas. Ele explora a estrutura dos dados sem conhecimento prévio sobre os rótulos dos clusters.

Esses exemplos fornecem uma base para entender como os algoritmos de aprendizado supervisionado e não supervisionado funcionam na prática.