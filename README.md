🎯 Objective
Design and implement a context-aware chatbot that uses Retrieval-Augmented Generation (RAG) principles via LangChain — allowing the bot to answer questions grounded in a custom knowledge base rather than relying solely on a base language model.

🛠️ Methodology / Approach
Leveraged LangChain as the orchestration framework to chain together retrieval and generation steps.
Built a document ingestion pipeline: text documents are split into chunks, converted to vector embeddings, and stored in a vector store.
On each user query, the most relevant document chunks are retrieved and injected into the prompt context (RAG pattern).
The language model then generates a response grounded in those retrieved passages — reducing hallucinations and enabling domain-specific Q&A.
Maintained conversation memory across turns so the chatbot is context-aware throughout a session.
📊 Key Results / Observations
The RAG approach significantly improves answer accuracy compared to a plain LLM with no retrieval.
Context window management (chunking strategy, overlap) proved critical for coherent multi-turn conversations.
The architecture is modular: the vector store, LLM, and retriever can each be swapped independently (e.g., FAISS → Pinecone, OpenAI → local model).
🗂️ Repository Structure
├── Task_2_End_to_End_ML_Pipeline_for_Customer_Churn_Prediction.ipynb
├── Task_3_Multimodal_Housing_Price_Prediction__Images___Tabular_.ipynb
├── Task_4_Context_Aware_Chatbot_Using_LangChain_RAG.ipynb
└── README.md
🧰 Tech Stack
Python · scikit-learn · TensorFlow / Keras · LangChain · OpenCV · pandas · NumPy · joblib
