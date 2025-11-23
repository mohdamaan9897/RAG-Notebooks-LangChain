- I explored Retrieval-Augmented Generation (RAG) using different file types such as PDF, DOCX, Excel, CSV, and more. I understood how raw files are converted into a Document structure containing metadata and text content, then chunked for processing.
Using embedding models, I converted text/images into vector embeddings and stored them in vector databases such as:

- FAISS – local vector storage

- ChromaDB – open-source, embedded vector DB

- Pinecone – fully managed, scalable cloud vector DB

This formed the first pipeline.

- I then built the second pipeline, where the user query first goes to the vector database, performs similarity search / cosine similarity, retrieves the top-k relevant chunks, and sends both query + retrieved content to the LLM.
The LLM then generates answers strictly based on the retrieved context.

- I learned why RAG is important:
    - LLMs hallucinate when asked about topics  after their training cutoff date.
    - LLMs cannot accurately answer questions about private or proprietary company data.
    - RAG solves this by injecting the exact relevant content into the model, ensuring accuracy and reducing hallucinations.