❑ [[QnA Maker Service]] Is used for authoring and query prediction. 
❑ It provides access to the authoring and publishing APIs of the [[QnA Maker Service]] 
❑ It also uses natural language processing ([[NLP]]) capabilities to learn about specifics of questions in the knowledge base and predict at runtime which QnA pair matches as the best answer. 
❑ [[Cognitive Search]] is used for data storage and search. 
❑ Cognitive Search stores the QnA pairs and maintains indexes for all published knowledge bases. ❑ When a new query is raised by [[QnA Maker resource]], [[Cognitive Services]] handles its execution to provide rich search experience. 
❑ App Service enables access to the published knowledge bases of [[QnA Maker Service]] via runtime query prediction endpoints. 
❑ Application Insights is used for query prediction telemetry. 
❑ Application Insights can collect [[Chatbot]]’s logs and telemetry. 
❑ It also includes powerful analytics tool to diagnose potential issues and process telemetry data with [[KQL]] (Kusto Query Language).