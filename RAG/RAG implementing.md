![[Retrieval_Augmente_Generation.png]]

Retrieval component, Augmentation component, Generation component.  
  
⮕ [[Retrieval]]: This component helps you fetch the relevant information from the external knowledge base like a vector database for any given user query. This component is very crucial as this is the first step in curating the meaningful and contextually correct responses.  
  
⮕ [[Augmentation]]: This part involves enhancing and adding more relevant context to the retrieved response for the user query.  
  
⮕ [[Generation]]: Finally, a final output is presented to the user with the help of a large language model ([[RedeNeural/LLMs|LLMs]]). The LLM uses its own knowledge and the provided context and comes up with an apt response to the user’s query.  
  
These three components are the basis of a RAG pipeline to help users to get the contextually-rich and accurate responses they are looking for. That is the reason why RAG is so special when it comes to building chatbots, question-answering systems, etc.  
  
Along with RAG, AI frameworks like [[LangChain]] and [[LlamaIndex]] make the LLM-applications more efficient by providing the required toolkit.  
  
Let’s build a simple AI application that can fetch the contextually relevant information from our own data for any given user query.