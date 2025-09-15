# RAG Experiment with Synthetic Educational Data

This project demonstrates a Retrieval-Augmented Generation (RAG) experiment using synthetic markdown data from **Horizon International Institute (HII)**.  
The experiment explores building a chat application by embedding the knowledge base into vector databases and comparing retrieval performance.

---

## Dataset
A synthetic dataset of markdown files was created to represent different aspects of an educational institute:

- About (Institute details, mission, vision, accreditations)  
- Careers (job postings and work culture)  
- Profiles (faculty and alumni profiles)  
- Student Life (clubs, events, sports, facilities)  
- Programs and Courses (undergraduate, postgraduate, short courses)  

---

## Methodology

### 1. Data Preparation
- Converted markdown files into structured text data.  
- Focused on the **About** section as the knowledge base for the experiment.  

### 2. Vectorization
- Embedded text chunks using sentence-transformers.  
- Created two separate vector databases for comparison:  
  - **ChromaDB**  
  - **FAISS**  

### 3. RAG Pipeline
- Built a retrieval-augmented generation pipeline with the following steps:  
  1. Query → Convert into embedding.  
  2. Retrieve top-k similar chunks from the vector database.  
  3. Pass retrieved context + query into a GPT model.  
  4. Generate final response in conversational format.  

### 4. Chat Application
- Developed a simple chat interface to interact with the system.  
- Users can ask questions about Horizon International Institute (HII).  
- The system retrieves and generates answers grounded in the **About** knowledge base.  

---

## Experiments

### ChromaDB
- Indexed embeddings into **Chroma**.  
- Queries retrieved accurate responses with smooth integration.  
- Good performance for small-scale experimentation.  

### FAISS
- Implemented **FAISS** as an alternative vector store.  
- Showed faster retrieval on larger embeddings.  
- Better suited for scaling experiments.  

Some of the screenshots are attached below.

<img width="1490" height="462" alt="image" src="https://github.com/user-attachments/assets/eeb2312c-93d6-4274-9954-c7d331b502cb" />

<img width="1447" height="532" alt="image" src="https://github.com/user-attachments/assets/39983b92-e95d-43f1-8b96-41262ae13faf" />

<img width="1467" height="213" alt="image" src="https://github.com/user-attachments/assets/6888ff2e-d48f-4aa9-bdb0-efd578e0a37f" />


---

## Comparison

| Feature              | ChromaDB                        | FAISS                        |
|----------------------|---------------------------------|------------------------------|
| Ease of Setup        | Simple, minimal configuration  | Requires setup for indexing |
| Speed (Retrieval)    | Good for small datasets        | Faster on larger datasets   |
| Scalability          | Moderate                       | High                        |
| Integration          | Python-first, user-friendly    | Widely used in industry     |

---


