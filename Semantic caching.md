![[semantic_caching.png]]


1. Enhancing Speed and Responsiveness  
2. Optimizing Resource Utilization  
3. Preserving Contextual Information  
  
Semantic caching workflow in LLM applications:  
1. User Query: A user submits a query to the system.  
2. LLM Wrappers: The query first goes through LLM wrappers, which integrate and support different LLMs (e.g., Llama, OpenAI).  
3. Generate Embeddings: The query is then converted into an embedding using an embedding algorithm (e.g., SBERT).  
4. Vector Store: The generated embedding is stored in a vector store, which is optimized for fast retrieval of embeddings.  
5. Similarity Evaluation: The system performs a similarity evaluation, comparing the new query's embedding with stored embeddings to determine if there is a cache hit.  
6. Cache Hit Check: If a similar query is found in the cache store, the cached response is returned, bypassing the need for the LLM to generate a new response.  
7. LLM Generation: If no similar query is found (cache miss), the LLM generates a new response, which is then stored in the cache store for future use