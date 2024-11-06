# Conversational AI for Finance: Document Retrieval and Analysis with Chat History and PDF Integration

## Overview

This is a Streamlit-based web application that enables users to interact with PDF documents using conversational AI. It allows users to upload PDF files, process them, and then ask questions based on the content of the documents. The system uses Groq's AI model (Gemma2-9b-It) to analyze the documents and provide concise answers, while maintaining the conversation history to provide context for follow-up questions.

The app is ideal for use cases such as finance document retrieval, legal document analysis, and any scenario where users need to extract information from uploaded documents interactively.

## Features

- **Document Upload:** Upload one or more PDF documents for processing and analysis.
- **Conversational AI:** Ask questions based on the uploaded documents, with answers based on context extracted from the documents.
- **Contextual Awareness:** The AI is aware of conversation history, providing more accurate answers by taking previous questions into account.
- **Document Splitting and Embedding:** PDFs are split into chunks, and embeddings are created using HuggingFace embeddings for efficient retrieval and search.
- **Session Management:** Maintain separate conversation histories for each session, enabling multiple users to interact with the app simultaneously without conflicts.
- **Groq Integration:** Uses the Groq API for running the AI model (Gemma2-9b-It).

## Prerequisites

Before using this app, ensure that you have the following:

- **Groq API Key:** To access the AI model, you must provide a valid Groq API key. You can obtain it by signing up for Groq's services.
- **Python Libraries:** The app relies on several Python libraries for document processing and AI functionality. Ensure you have the following installed:
    - `streamlit`
    - `langchain`
    - `langchain-groq`
    - `langchain_huggingface`
    - `faiss-cpu`
    - `PyPDF2`
    - `dotenv`
    - `youtube-transcript-api`
You can install the required libraries by running:

```bash
pip install streamlit langchain langchain-groq langchain_huggingface faiss-cpu PyPDF2 dotenv youtube-transcript-api
```

## Setup and Usage

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/your-username/conversational-ai-for-finance.git
   ```

2. **Set Up Environment Variables:**

   Create a `.env` file in the root of your project and add your Groq API key:

   ```
   GROQ_API_KEY=your-groq-api-key
   HF_TOKEN=your-huggingface-token
   ```

3. **Running the App:**

   To start the app, navigate to the project directory and run:

   ```bash
   streamlit run app.py
   ```
   This will launch the app in your default browser.

4. **Uploading Documents:**

   Once the app is running, you can upload one or more PDF documents using the file upload interface. After uploading, you can ask questions related to the contents of the documents.

5. **Interacting with the AI:**

   After uploading the PDFs, type your questions into the provided input field. The AI will use the context from the uploaded documents to answer your questions, while maintaining conversation history for more relevant responses.

6. **Managing Sessions:**

   The app allows you to manage conversation history through the Session ID field. Each session is stored se
