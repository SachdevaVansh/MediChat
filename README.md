🩺 MediChat - Medical Assistant

MediChat is an intelligent chatbot designed to help you understand your medical reports. Simply upload your PDF medical documents, and the application will process them, allowing you to ask questions and get concise, relevant answers based on the information within your files.

This application is built using Streamlit for the user interface and leverages LangChain and FAISS for a powerful Retrieval-Augmented Generation (RAG) pipeline. This setup ensures that the chatbot's responses are accurate, contextual, and directly tied to the documents you provide, without the risk of hallucination.

✨ Features

Secure Document Upload: Easily upload one or more PDF medical reports. Your documents are processed locally and are never stored on a server.

Intelligent Q&A: Ask specific questions about your reports, such as "What was my cholesterol level?" or "What does this diagnosis mean?".

Context-Aware Responses: The RAG pipeline retrieves the most relevant sections of your documents to provide accurate answers, eliminating guesswork.

Clean and Modern UI: A sleek, dark-themed interface with intuitive controls makes for a pleasant user experience.

Clear Conversation History: The chat interface maintains a history of your questions and the assistant's responses for easy reference.

🚀 How to Run

Prerequisites
Python 3.8+

An API key for a large language model (LLM) service. The code is configured for a model accessible via EURI_API_KEY, but can be adapted for others like OpenAI, Gemini, etc.

Installation
Clone the repository:

Bash

git clone <repository_url>
cd <repository_name>
Create a virtual environment and activate it:

Bash

python -m venv venv
# On Windows
venv\Scripts\activate
# On macOS/Linux
source venv/bin/activate
Install the required packages:

Bash

pip install -r requirements.txt
Note: The required packages from the provided code snippet are streamlit, langchain, faiss, and a library to read PDFs (e.g., PyPDF2 or pypdf). Make sure to include all necessary dependencies in your requirements.txt file.

Set up your API Key:
Create a .env file in the root directory and add your API key. For example:

EURI_API_KEY="your-api-key-here"
Usage
Start the Streamlit application:

Bash

streamlit run app.py
(Assuming the main file is named app.py)

Open the application:
Your web browser should automatically open to the application's URL (usually http://localhost:8501).

Use the app:

Upload: Use the "Document Uploader" in the sidebar to select your PDF files.

Process: Click the "Process Documents" button to create the document index.

Chat: Once processing is complete, you can begin asking questions in the chat bar at the bottom of the screen.

🛠️ Code Structure
The application is structured into several modular files for clarity and maintainability:

app.py: The main Streamlit application file that orchestrates the UI and logic.

app/ui.py: Contains UI components like the PDF uploader widget.

app/chat_utils.py: Manages interactions with the large language model.

app/config.py: Stores configuration variables, such as API keys.

app/pdf_utils.py: Handles loading and splitting PDF documents into manageable chunks.

app/vectorstore_utils.py: Manages the creation and retrieval from the FAISS vector store.

⚠️ Disclaimer
MediChat Pro is a tool for informational purposes only. It is not a substitute for professional medical advice, diagnosis, or treatment. Always seek the advice of a qualified healthcare provider with any questions you may have regarding a medical condition. Do not disregard professional medical advice or delay in seeking it because of something you have read on this application.
