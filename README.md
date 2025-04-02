# LangChain RetrievalQA Chatbot

This project implements a Retrieval-based Question Answering (RetrievalQA) chatbot using [LangChain](https://github.com/langchain-ai/langchain). The chatbot is designed to answer questions based on the content of provided PDF documents.

## Features

- **PDF Integration**: Processes and extracts text from PDF documents to build a knowledge base.
- **Retrieval-based QA**: Utilizes LangChain's RetrievalQA to fetch relevant information in response to user queries.
- **Interactive Interface**: Provides a user-friendly interface for asking questions and receiving answers.

## Requirements

- Python 3.x
- Jupyter Notebook
- Required Python packages listed in `requirements.txt`

## Setup Instructions

### Clone the Repository

```bash
git clone https://github.com/vivek2540p/langchain_RetrievalQA_Chatbot.git
```

### Navigate to the Project Directory

```bash
cd langchain_RetrievalQA_Chatbot
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Set Up Environment Variables

Ensure you have an OpenAI API key. Set it as an environment variable:

```bash
export GEMINI_API_KEY='your_api_key'
```

Alternatively, you can create a `.env` file in the project directory and add:

```ini
GEMINI_API_KEY=your_api_key
```

### Run the Jupyter Notebook

```bash
jupyter notebook
```

### Open and Execute `app.ipynb`

In the Jupyter Notebook interface, open `app.ipynb` and execute the cells to interact with the chatbot.

## Usage

- **Adding PDF Documents**: Place your PDF documents (e.g., `FAQ.pdf`) in the project directory. The chatbot will process these documents to build its knowledge base.
- **Interacting with the Chatbot**: After processing the PDFs, you can ask questions related to the content of the documents, and the chatbot will provide relevant answers.

## How It Works

1. **Document Loading**: The chatbot uses LangChain's `PyPDFLoader` to load and extract text from PDF documents.
2. **Text Splitting**: The extracted text is split into manageable chunks using `CharacterTextSplitter` to facilitate efficient processing.
3. **Embedding Generation**: Embeddings for the text chunks are generated using OpenAI's embedding model.
4. **Vector Store Creation**: The embeddings are stored in a vector database (`Chroma`) to enable fast similarity searches.
5. **RetrievalQA Chain**: A `RetrievalQA` chain is set up, combining the language model and the retriever to answer user queries based on the stored knowledge.

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request with your improvements.

## License

This project is licensed under the MIT License.

