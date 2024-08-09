![[rag_reranking.png]]

LLMs can acquire new information in at least two ways:  
1. [[Fine-tuning ]] 
2. [[RAG/RAG]] (retrieval augmented generation)  
  
Retrieval-augmented generation (RAG) is the practice of extending the “memory” or knowledge of LLM by providing access to information from an external data source.  
  
Traditional semantic search consists of a two-part process.  
First, an initial retrieval mechanism does an approximate sweep over a collection of documents and creates a document list.  
  
Then, a re-ranker mechanism will take this candidate document list and re-rank the elements. With [[Rerank]], we can improve your models by re-organizing your results based on certain parameters.  
  
Why is Re-Ranking Required ?  
⮕ The recall performance for LLMs decreases as we add more context resulting in increased context window(context stuffing)  
  
⮕ Basic Idea behind reranking is to filter down the total number of documents into a fixed number .  
  
⮕ The re-ranker will re-rank the records and get the most relevant items at the top and they can be sent to the LLM  
  
⮕ The Reranking offers a solution by finding those records that may not be within the top 3 results and put them into a smaller set of results that can be further fed into the LLM  
  
Reranking basically enhance the relevance and precision of retrieved results.