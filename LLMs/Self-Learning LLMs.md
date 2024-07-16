![[20240715215838.png]]

Self-learning LLM framework enables an LLM to independently learn previously unknown knowledge through self-assessment of their own hallucinations.  
  
Why Self-Learning is needed?  
Hallucination is a serious problem that hinders many LLM applications.  
One of its main reasons is the model’s lack of knowledge on a given topic.  
This problem is typically overcome by finetuning, i.e., additional learning using new data.  
  
Simultaneously, determining what the model already knows and what it does not know yet is very difficult, especially if there is limited information on the model’s past training data. Because of this, finetuning is often a very inefficient process & this is where we need self-learning approach.  
  
Using the hallucination score, this research paper authors have introduce a new concept of Points in The Unknown (PiUs), along with one extrinsic and three intrinsic methods for automatic PiUs identification. [Read more about PiUs in the research paper, link shared at the end]  
  
It facilitates the creation of a self-learning loop that focuses exclusively on the knowledge gap in Points in The Unknown, resulting in a reduced hallucination score.  
  
They also developed evaluation metrics for gauging an LLM's self-learning capability.  
  
Their experiments revealed that 7B-Mistral models that have been finetuned or aligned are capable of self-learning considerably well.  
  
Their self-learning concept allows more efficient LLM updates and opens new perspectives for knowledge exchange. It may also increase public trust in AI.