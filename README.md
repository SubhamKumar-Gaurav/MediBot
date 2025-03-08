# MediBot - Medical ChatBot

Access the Chatbot here: https://medibot-subhamkumar-h.streamlit.app/

<img src="https://github.com/SubhamKumar-Gaurav/MediBot/blob/main/Heart_attack.png>

<img src="https://github.com/SubhamKumar-Gaurav/MediBot/blob/main/Ronaldo.png>
A **Medical Question Answering System** that utilizes **Mistral-7B** with **FAISS vector search** for retrieving relevant medical information from "The Gale Encyclopedia of Medicine Second Edition." The system is deployed using **Streamlit** for an interactive user experience. 


---

## Table of Contents

1. [Project Overview](#project-overview)
2. [Features](#features)
3. [Technologies Used](#technologies-used)
4. [Dataset](#dataset)
5. [Model and Retrieval Pipeline](#model-and-retrieval-pipeline)
6. [Web App](#web-app)
7. [Installation](#installation)
8. [How to Use](#how-to-use)
9. [Future Enhancements](#future-enhancements)
10. [Contacts](#contacts)

---

## Project Overview

This system is designed to answer **medical-related questions** based on information retrieved from "The Gale Encyclopedia of Medicine Second Edition." It employs **FAISS** for efficient vector-based retrieval and **Mistral-7B** to generate responses based on the retrieved context.

---

## Features

- **Retrieves relevant medical content** using FAISS vector search.
- **Uses Mistral-7B** to generate context-based responses.
- **Streamlit-based Web Interface** for easy interaction.
- **Ensures factual accuracy** by only responding based on provided medical texts.
- **Prevents hallucinations** by restricting responses to known context.

---

## Technologies Used

- **Python** (Core programming language)
- **Streamlit** (Web application framework)
- **LangChain** (LLM integration and retrieval pipeline)
- **FAISS** (Efficient similarity search)
- **HuggingFace Transformers** (Mistral-7B model endpoint)
- **Sentence-Transformers** (Embedding model: `all-MiniLM-L6-v2`)
- **OS and dotenv** (Environment variable management)

---

## Dataset

The knowledge base is built using **"The Gale Encyclopedia of Medicine Second Edition."** The text is indexed into a **FAISS vector store** for efficient retrieval.

---

## Model and Retrieval Pipeline

1. **Data Processing**:
   - Text is chunked and embedded using `all-MiniLM-L6-v2`.
   - FAISS is used for vector storage and similarity search.

2. **Query Handling**:
   - User query is converted into an embedding.
   - FAISS retrieves the top relevant context chunks.
   - Mistral-7B processes the retrieved context and generates an answer.

3. **Response Generation**:
   - The model **only** responds using retrieved data to ensure accuracy.
   - If no relevant information is found, it simply states "I don't know."

---

## Web App

The project includes a **Streamlit-based web application** that allows users to ask medical questions and receive AI-generated responses.

---

## Installation

Follow these steps to set up the project locally:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/SubhamKumar-Gaurav/Medical-QA-System.git
   cd Medical-QA-System
   ```

2. **Create a Virtual Environment** (optional but recommended):
   ```bash
   python -m venv env
   source env/bin/activate   # On Windows: env\Scripts\activate
   ```

3. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Set Up Streamlit Secrets** (Replace with your Hugging Face token):
   ```bash
   streamlit secrets set HF_TOKEN "your_huggingface_api_key"
   ```

5. **Run the Web Application**:
   ```bash
   streamlit run app.py
   ```

---

## How to Use

1. Open the running Streamlit web app (usually at `http://localhost:8501`).
2. Enter your medical question in the input field.
3. Click on the "Submit" button.
4. The system retrieves relevant medical information and generates an answer.

---

## Future Enhancements

1. **Expand the Knowledge Base**:
   - Include more medical resources and journals.
2. **Improve Search Capabilities**:
   - Implement hybrid search (vector + keyword-based search).
3. **Advanced LLMs**:
   - Upgrade to more powerful models like Llama or GPT-4 Turbo.
4. **Deployment**:
   - Deploy on cloud platforms (AWS, Hugging Face Spaces, or Streamlit Cloud).

---


## Contact
For any questions or feedback, please reach out to:

Subham Kumar Gaurav: subhamgaurav2001@gmail.com  
GitHub: [SubhamKumar-Gaurav](https://github.com/SubhamKumar-Gaurav)
LinkedIn: ([Subham Kumar H](https://www.linkedin.com/in/subham-kumar-h-158395216/))

---
