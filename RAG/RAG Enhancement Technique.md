![[rag_enhancement.png]]

1. [[Transformation from Single Query to Multi Query]]:  
Multi-Query is an advanced approach in the Query Transformation stage of retrieval. Unlike traditional methods where only one query is used, Multi-Query generates multiple queries and retrieves similar documents for each one. Builders utilize Multi-Query primarily for two reasons: enhancing suboptimal queries and expanding result sets. It addresses users’ imperfect queries by filling in gaps and retrieves more diverse results, leading to an expanded results set that can provide better answers than single-query documents.  
  
2. [[Improving Indexed Data Quality]]:  
Unfortunately, data cleaning is often overlooked during the development of RAGs, with a tendency to ingest all available documents without verifying their quality. We need to ensure that the data fed into the RAG system is of high quality for obtaining accurate answers. The principle of “garbage in, garbage out” is especially relevant here.  
  
3. [[Chunking]] strategy and size matters to optimize index structure:  
When setting up your Retrieval Augmented Generation (RAG) system, the size of the chunks and chunking technique plays a crucial role. It determines how much information is retrieved from the document store for processing. Choosing a small chunk size may lead to missing important details, while opting for a larger size could introduce irrelevant information.  
  
4. Incorporation of [[metadata with indexed vectors]]:  
Adding metadata alongside indexed vectors in the vector database offers significant benefits in organizing and enhancing search relevance.  
  
5. [[Improving search]] relevance with question-based indexing:  
LLMs and RAGs offer incredible power by allowing users to express queries in natural language, simplifying data exploration and complex tasks. However, a common challenge arises when there’s a disconnect between the concise queries, users input and the longer, more detailed documents stored in the system.  
  
6. Improving Search Precision with Mixed Retrieval — [[Hybrid Search]]  
While vector search excels in retrieving semantically relevant chunks for queries, it sometimes lacks precision in matching specific keywords. To get the best of both the worlds, (vector search + full-text search) you need hybrid search.