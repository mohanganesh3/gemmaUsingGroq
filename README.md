# Gemma Model Document Q&A

This application uses the power of Groq and Google Generative AI to perform document-based question answering. Users can input a question, and the system will retrieve the most relevant information from a set of PDF documents and generate a response based on the provided context.

## Features:
	•	Upload and load PDF documents into the system.
	•	Vector embedding to transform documents into searchable data.
	•	Use of the Groq model for question answering based on document content.
	•	Seamless integration with Google Generative AI for embeddings and document processing.
	•	Displaying answers with context from the documents.

## Requirements:
	•	Python 3.8 or later
	•	streamlit
	•	langchain
	•	langchain_groq
	•	langchain_core
	•	langchain_google_genai
	•	langchain_community
	•	python-dotenv
	•	FAISS
	•	google-api-python-client

## You can install the required libraries by running the following command in your terminal:

pip install streamlit langchain langchain_groq langchain_core langchain_google_genai langchain_community python-dotenv faiss google-api-python-client

## Setup:
	1.	Clone the repository or download the project files.
     git clone https://github.com/your-username/your-repository-name.git
     cd your-repository-name
	2.	Create a .env file in the root directory and add your API keys:
    GROQ_API_KEY=your_groq_api_key
    GOOGLE_API_KEY=your_google_api_key
	3.	Place your PDF documents in the ./US_CENSUS directory for document embedding.

## Running the Application:
	1.	Run the Streamlit app with the following command:
    streamlit run app.py
	2.	The application will load, and you will be able to input your questions in the provided text input field. Click the “Documents Embedding” button to prepare the document vectors,     which will then be stored in a vector store. Once the vectors are ready, you can ask questions, and the model will provide answers based on the documents.

## How It Works:
	1.	Vector Embedding: The system uses Google Generative AI embeddings to convert PDF documents into vector embeddings. The documents are split into chunks using a recursive text splitter for better processing.
	2.	Question Answering: The Groq-powered Llama3 model answers questions based on the context retrieved from the documents stored in the FAISS vector database.
	3.	Displaying Results: When a question is asked, the relevant document context is fetched and displayed alongside the answer, giving transparency into the sources of the information.

## Example:
	•	Input: “What is the population growth in the US according to the 2020 census?”
	•	Output: The model will search through the documents, find the relevant sections, and generate an answer based on the context of those sections.

