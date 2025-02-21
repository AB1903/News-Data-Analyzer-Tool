# News Data Analyzer 📈

This project is a web application built with **Streamlit** and **Langchain** that analyzes news articles. It allows users to input news article URLs, fetches the content, splits the text into chunks, generates embeddings, and stores them in a **FAISS index** for efficient querying. The app allows users to ask questions, and it retrieves the most relevant answers from the processed news articles.

---

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [Features](#features)
- [Requirements](#requirements)
- [How It Works](#how-it-works)
- [Contributing](#contributing)

---

## Installation

To set up the project locally, follow these steps:

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/news-data-analyzer.git
    ```
2. Navigate to the project directory:
    ```bash
    cd news-data-analyzer
    ```
3. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

4. Set up your environment variables by creating a `.env` file in the root directory and adding your OpenAI API key:
    ```
    OPENAI_API_KEY=your_openai_api_key
    ```

---

## Usage

1. Run the Streamlit app:
    ```bash
    streamlit run app.py
    ```
2. Once the app is running, open your browser and navigate to `http://localhost:8501`.
3. On the sidebar, input 3 URLs of news articles you'd like to analyze.
4. Press the "Process URLs" button to fetch, process, and store embeddings for the articles.
5. Once the data is loaded and processed, type your question in the provided input field.
6. The app will return the answer by searching the processed content and display the relevant sources.

---

## Features
- **Fetch and Process News Articles:** Enter up to 3 URLs to fetch news articles.
- **Text Chunking:** The content is split into chunks of text for better processing and storage.
- **FAISS Indexing:** The embeddings of the text are stored in a FAISS index for efficient similarity search.
- **Real-time Querying:** Ask questions about the news content and get answers based on the processed text.
- **Source Display:** The app shows the relevant sources used to answer the question.

---

## Requirements

Make sure the following packages are installed before running the project:

- **Python 3.x**
- **Streamlit**
- **Langchain**
- **OpenAI**
- **FAISS**
- **python-dotenv**

You can install all the necessary dependencies with:

```bash
pip install -r requirements.txt
```

## How it Works

1. URL Input: The app allows you to input up to 3 URLs in the sidebar.
2. Data Loading: The news articles are fetched using the UnstructuredURLLoader from Langchain.
3. Text Splitting: The content is split into smaller chunks using RecursiveCharacterTextSplitter for better processing.
4. Embeddings Generation: OpenAI embeddings are created for each chunk of text using the OpenAIEmbeddings class.
5. FAISS Index: The embeddings are stored in a FAISS index, which enables efficient querying for relevant answers.
6. Querying: Users can input a question, and the app will use the FAISS index to find the most relevant text chunks to answer the query.

## Contribution

Feel free to open issues or create pull requests to improve this project. Contributions are welcome!
