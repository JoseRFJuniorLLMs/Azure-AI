![[semantic_entropy.png]]


𝐃𝐞𝐭𝐞𝐜𝐭𝐢𝐧𝐠 𝐡𝐚𝐥𝐥𝐮𝐜𝐢𝐧𝐚𝐭𝐢𝐨𝐧𝐬 𝐢𝐧 𝐥𝐚𝐫𝐠𝐞 𝐥𝐚𝐧𝐠𝐮𝐚𝐠𝐞 𝐦𝐨𝐝𝐞𝐥𝐬 𝐮𝐬𝐢𝐧𝐠 𝐬𝐞𝐦𝐚𝐧𝐭𝐢𝐜 𝐞𝐧𝐭𝐫𝐨𝐩𝐲: The paper discusses the effectiveness of semantic entropy in detecting confabulations, which are a significant type of error in model generations. It compares semantic entropy with other methods, highlighting that while some methods can identify various errors, semantic entropy is superior in detecting confabulations specifically. The study emphasizes the importance of context in evaluating model responses, noting that fixed reference answers may not adequately capture the flexibility needed in conversational AI. Overall, the findings suggest that semantic entropy provides a reliable measure for assessing the correctness of model outputs in various contexts.
#### Como a Semântica Entropia é Usada na Prática?

1. **Medir Consistência**: Analisar se as respostas do modelo mantêm consistência semântica em relação às perguntas ou informações fornecidas.
2. **Detectar Incertezas**: Identificar respostas com alta entropia semântica, que podem indicar respostas fabricadas ou menos confiáveis.
3. **Ajuste de Modelos**: Refine os modelos para minimizar a geração de respostas com alta entropia, melhorando a precisão e confiabilidade.

Para demonstrar a ideia de entropia semântica em um exemplo em Python, podemos usar técnicas de Processamento de Linguagem Natural (NLP) para comparar a semântica de diferentes respostas geradas por um modelo de linguagem, como o GPT, em relação a uma pergunta ou contexto dado. 

Neste exemplo, utilizaremos a similaridade de cosseno entre embeddings de sentenças para avaliar a consistência semântica. Vamos calcular a similaridade entre a resposta gerada e uma referência esperada, e usar isso como uma forma de "entropia semântica".

Para isso, utilizaremos a biblioteca `transformers` da Hugging Face e a `sentence-transformers` para calcular as embeddings de sentenças.

Primeiro, instale as bibliotecas necessárias:

```bash
pip install transformers sentence-transformers
```

Agora, crie um script Python para calcular a entropia semântica:

```python
from sentence_transformers import SentenceTransformer, util
import numpy as np

# Carrega o modelo para gerar embeddings das sentenças
model = SentenceTransformer('all-MiniLM-L6-v2')

# Função para calcular a entropia semântica (similaridade)
def semantic_entropy(reference, response):
    # Calcula as embeddings para as sentenças de referência e resposta
    ref_embedding = model.encode(reference, convert_to_tensor=True)
    res_embedding = model.encode(response, convert_to_tensor=True)

    # Calcula a similaridade de cosseno entre as embeddings
    similarity = util.cos_sim(ref_embedding, res_embedding)

    # Converte a similaridade para um valor escalar
    similarity_score = similarity.item()

    # Calcular a entropia semântica como a diferença da similaridade
    entropy = 1 - similarity_score

    return entropy

# Exemplos de perguntas e respostas
reference_answer = "O sol é uma estrela que fica no centro do Sistema Solar."
response_1 = "O sol é uma estrela central em nosso sistema."
response_2 = "Os gatos são animais domésticos comuns."
response_3 = "O sistema solar é composto por planetas que orbitam o sol."

# Calcula a entropia semântica para as respostas
entropy_1 = semantic_entropy(reference_answer, response_1)
entropy_2 = semantic_entropy(reference_answer, response_2)
entropy_3 = semantic_entropy(reference_answer, response_3)

# Mostra os resultados
print(f"Entropia semântica para resposta 1: {entropy_1:.4f}")
print(f"Entropia semântica para resposta 2: {entropy_2:.4f}")
print(f"Entropia semântica para resposta 3: {entropy_3:.4f}")
```

### Explicação do Código:
- **Modelo de Embeddings:** Usamos `SentenceTransformer` para gerar embeddings das sentenças. Essas embeddings são vetores numéricos que capturam o significado semântico das sentenças.
- **Similaridade de Cosseno:** Calculamos a similaridade de cosseno entre as embeddings da resposta e da referência. Valores próximos de 1 indicam alta similaridade (baixa entropia semântica), enquanto valores próximos de 0 indicam baixa similaridade (alta entropia semântica).
- **Entropia Semântica:** Definimos a entropia semântica como \( 1 - \text{similaridade} \). Assim, quanto maior for a entropia, menor a similaridade entre a resposta e a referência.

### Resultados:
Ao rodar o script, você verá que respostas mais próximas da referência terão menor entropia semântica, enquanto respostas menos relevantes ou incorretas terão entropia maior.

Esse exemplo é uma forma simples de demonstrar como a entropia semântica pode ser usada para avaliar a qualidade e a consistência das respostas geradas por um modelo de linguagem.