---
tags:
  - RedesNeurais
---

**1. Redes Neurais Perceptron ([[RNP]])**

* A primeira arquitetura de RNN, introduzida em 1958.
* Composta por um único camada de processamento com pesos ajustáveis.

**2. Multilayer Perceptron ([[MLP]])**

* Uma extensão da RNP com múltiplas camadas de processamento.
* Cada camada aplica uma função de ativação aos resultados do caminho anterior.

**3. Redes Neurais Convolucionais ([[CNNs]])**

* Desenvolvidas para processar dados espaciais, como imagens.
* Utilizam convoluções e poolings para extrair características.

**4. Redes Neurais Recursivas ([[RNNs]])**

* Desenvolvidas para processar sequências de dados, como séries temporais ou linguagem natural.
* Utilizam recursividade para capturar dependências entre os elementos da sequência.

**5. Long Short-Term Memory ([[LSTM]])**

* Uma variação de RNNs que adiciona células de memória para manter informações durante períodos longos.
* Utiliza gates de esquecimento, lembrança e atenção para controlar a fluxo de informação.

**6. Gated Recurrent Units ([[GRUs]])**

* Uma variação de RNNs que simplifica LSTMs removendo as células de memória.
* Utilizam gates de atenção e esquecimento para controlar o fluxo de informação.

**7. [[U-Net]]**

* Desenvolvido para processamento de imagens, especialmente em segurança de fronteira e detecção de anomalias.
* Utiliza uma estrutura de "U" para combinar informações da camada de entrada com as características extraídas pela rede.

**8. [[ResNets]]**

* Desenvolvidos para processamento de imagens e sequências de dados.
* Utilizam uma estrutura em cascata para reduzir o ruído e aumentar a capacidade da rede.

**9. [[Transformer]]**

* Desenvolvido originalmente para processamento de linguagem natural, especialmente em LLMs.
* Utiliza atenção mútua e aprendizado de representações de contexto para capturar dependências entre os elementos da sequência
sem utilização de recursividade.

**10. [[BERT]] (Bidirectional Encoder Representations from Transformers)**

* Um modelo de processamento de linguagem natural que utiliza a arquitetura Transformer.
* Desenvolvido originalmente para tarefas de classificação e análise de sentimento.

**11. [[RoBERTa]] (Robustly Optimized BERT Pretraining Approach)**

* Uma variação do modelo BERT com ajustes para melhorar o desempenho em tarefas de processamento de linguagem natural.
* Utiliza uma abordagem mais robusta para treinar o modelo.

**12. [[DistilBERT]] (Distilled BERT)**

* Um modelo de processamento de linguagem natural que utiliza a arquitetura Transformer, mas com uma estrutura mais leve e
eficiente.
* Desenvolvido originalmente para tarefas de classificação e análise de sentimento.

**13. Graph Neural Networks ([[GNNs]])**

* Desenvolvidos para processamento de dados estruturais, como grafos e redes sociais.
* Utilizam operações em grafos para aprender características da rede.

**14. Graph Attention Network ([[GAN]])**

* Uma variação do modelo GNN que utiliza atenção mútua entre os nodos da rede para capturar dependências entre eles.
* Desenvolvido originalmente para tarefas de classificação e análise de redes sociais.

**15. Graph Transformer ([[GT]])**

* Um modelo que combina a arquitetura GNN com a arquitetura Transformer para processamento de dados estruturais.
* Utiliza atenção mútua e aprendizado de representações de contexto para capturar dependências entre os nodos da rede.

**15. Neural Algorithmic Reasoner ([[NAR]])**

* NAR (Neural Algorithmic Reasoner) é uma arquitetura de processamento de linguagem natural projetada para melhorar o raciocínio fora do domínio em tarefas algorítmicas. Ela combina elementos de redes neurais e algoritmos para criar um modelo que pode realizar raciocínios inferenciais sobre problemas complexos.

**16. Neural Algorithmic Reasoner ([[TransNAR]])**

* [[Transformer]] + [[NAR]]