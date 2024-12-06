# Pharma Knowledge Assistant

## **Overview**
Pharma Knowledge Assistant is an AI-driven solution designed to facilitate user interaction with pharmaceutical knowledge. It provides natural language processing (NLP) capabilities for answering queries, generating summaries, and offering recommendations based on pharmaceutical product data. 

This system integrates:
- **Qwen Model** for natural language understanding.
- **BERT** for embedding generation.
- **HDBSCAN** for clustering embeddings and efficient data retrieval.

Developed as part of a hackathon challenge, this project demonstrates advanced concepts like Retrieval-Augmented Generation (RAG), agent-based design, and embedding-based search.

---

## **Features**
- Answer natural language queries about pharmaceutical products.
- Generate recommendations or warnings based on user symptoms or conditions.
- Summarize product details into concise and user-friendly explanations.
- Provide alternative medication suggestions when needed.
  - Example: Alternatives to Ibuprofen for pain relief.
- Utilize agent-based design for dynamic and interactive problem-solving.
- Include a GUI chatbot built with Streamlit for user interaction.

---

## **Architecture**
The architecture comprises:
- **Qwen Model**: Acts as the primary LLM for generating responses.
- **BERT**: Used to create dense embeddings for efficient search.
- **HDBSCAN**: Clustering for storing and retrieving embeddings.
- **LangChain**: For orchestrating Retrieval-Augmented Generation (RAG) and agent-based workflows.
- **Streamlit**: Provides the GUI for interacting with the system.

The system uses an agent-based design where features like RAG, summarization, and recommendations are represented as nodes in a graph. This modular architecture allows dynamic query handling and context sharing between nodes.

---

## **Implementation Steps**
1. **Dataset Preparation**
   - Used `web_scrapper.py` to collect data and expanded the dataset from the starter set of 10 JSON files.
   - Ensured consistency across all JSON files by defining a uniform schema.

2. **RAG Application for Question Answering**
   - Implemented using LangChain to provide accurate responses to user queries.
   - Integrated with agent nodes for seamless interaction.

3. **Recommendation System**
   - Developed to provide warnings and safe medication recommendations based on user input.

4. **Alternatives Generator**
   - Suggested alternatives to medications using RAG or specialized agents.

5. **Summarizer**
   - Implemented product detail summarization for easier understanding by end users.

6. **Agent Framework**
   - Designed a graph-based agentic application where nodes perform tasks like query answering, summarization, and search.

7. **GUI Development**
   - Built a chatbot interface using Streamlit to allow user interaction with the assistant.

---

## **How to Run**
### Prerequisites
- **Environment Setup**
  - Python 3.8 or higher.
  - Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```
- **Dataset**
  - Place the expanded dataset in JSON format in the `data/` directory.
- **LLM Configuration**
  - Install and configure the Qwen model (using Ollama or LMStudio as needed).

### Steps
1. Start the Streamlit application:
   ```bash
   streamlit run app.py


