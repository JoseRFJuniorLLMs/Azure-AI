![[RAG_Retrieval_Sources.png]]

⮕ [[Unstructured Data]] (Text): This includes plain text documents, web pages, and other free-form textual sources.  
  
⮕ [[Semi_Structured_Data]] (PDF): PDF documents, such as research papers, reports, and manuals, contain a mix of textual and structural information.  
  
⮕ [[Structured_Data]] (Knowledge Graphs): Knowledge graphs, such as Wikipedia and Freebase, represent information in a structured and interconnected format.  
  
⮕ [[LLM_Generated_Content]]: Recent advancements have shown that LLMs themselves can generate high-quality content that can be used as a retrieval source. This approach leverages the knowledge captured within the LLM's parameters to generate relevant information.  
  
All this data gets converted into embeddings and gets stored in a vector database. When a user query comes in, it also gets converted into an embedding (query embedding) and the most relevant answer will be retrieved using semantic search. The vector database becomes knowledge base to search for the contextually relevant answer.