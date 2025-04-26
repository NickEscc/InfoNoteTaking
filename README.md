# RAG Notes

This is a RAG based AI note-taking application that lets you import data in the form of PDF's, and then have an AI use that data to answer questions about the content and only the content of the PDF's

## Features

- Import individual PDF files or batches of PDFs.
- Automatically process and store PDF content in a MongoDB Atlas vector database.
- Ask questions based on the imported documents using a user-friendly GUI.
- Leverages OpenAI's GPT-3.5-turbo for generating accurate responses.fghm

## Prerequisites

Before running the application, ensure you have the following:

1. Python 3.8 or higher installed.
2. MongoDB Atlas account and a configured cluster.
3. OpenAI API key for GPT models.
4. Required Python packages installed (see below).

## Installation

1. Clone the repository or download the project files.
2. Install the required Python packages using pip:
   ```bash
   pip install pymongo langchain langchain-openai langchain-community langchain-core langchain-mongodb tkinter
   ```
3. Create a `key_param.py` file in the project directory with the following content:
   ```python
   openai_api_key = "your_openai_api_key"
   MONGO_URI = "your_mongodb_atlas_uri"
   ```

## Usage

1. Run the application:
   ```bash
   python Rag_test
   ```
2. Use the GUI to:
   - Import individual PDFs or batches of PDFs.
   - Ask questions based on the imported documents.

## File Structure

- `Rag_test`: Main Python script containing the application logic.
- `key_param.py`: Configuration file for API keys and MongoDB URI.
- `README.md`: Documentation for the project.

## Notes

- Ensure your MongoDB Atlas cluster has a vector search index named `vector_index`.
- The application uses OpenAI's GPT-3.5-turbo model with a temperature of 0 for deterministic responses.
