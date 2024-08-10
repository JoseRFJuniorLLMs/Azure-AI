![[TransNAR.png]] TransNAR: Augmenting Transformers with a pre-trained GNN-based NAR

**Augmenting [[RedeNeural/LLMs]] com algoritmo de razão**: A ideia é aumentar as capacidades de um grande modelo de linguagem ([[RedeNeural/LLMs]])
adicionando uma camada de raciocínio algorítmico.

**Neural Algorithmic Reasoner (NAR)**: A NAR é um módulo que utiliza uma rede neural para executar cálculos algorítmicos em
grafos. Isso significa que a NAR pode processar informações estruturadas em forma de grafos e produzir saídas baseadas em
cálculos específicos.

**Pre-treinamento da [[NAR]]**: A NAR é pre-educada para executar várias operações algorítmicas em uma coleção de entradas baseadas
em grafos. Isso significa que a NAR aprendeu a processar informações estruturadas e produzir saídas baseadas em cálculos
específicos.

**Integração com o [[Transformer]]**: A NAR é integrada ao modelo de linguagem (LLM) através da atenção cruz, que permite que as
saídas da NAR sejam acessadas pelo LLM. Isso significa que o LLM pode utilizar a saída da NAR como uma forma de input adicional
para produzir sua própria saída.

Em resumo, a TransNAR é uma abordagem que combina o poder do modelo de linguagem (LLM) com as capacidades algorítmicas da NAR.
Isso permite ao LLM processar informações estruturadas e produzir saídas baseadas em cálculos específicos, aumentando suas
capacidades em geral.