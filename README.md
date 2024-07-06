# Retrieval-Augmented Generation with LlamaIndex

This project demonstrates how to use retrieval-augmented generation (RAG) with LlamaIndex (formerly known as GPT Index) to query a set of documents.

## Setup

### Prerequisites

- Python 3.x
- `pip` package manager
- `dotenv` package for managing environment variables
- Jupyter Notebook

### Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/arsh248/RAG-LLM-App-Using-Llamaindex-and-OpenAI
    cd RAG-LLM-App-Using-Llamaindex-and-OpenAI
    ```

2. Create and activate a virtual environment:

    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3. Install the required packages:

    ```bash
    pip install -r requirements.txt
    ```

4. Create a `.env` file in the root directory and add your OpenAI API key:

    ```plaintext
    OPENAI_API_KEY=your_openai_api_key
    ```

5. Place your documents in a folder named `data` in the root directory.

### Running the Notebook

1. Start Jupyter Notebook:

    ```bash
    jupyter notebook
    ```

2. Open the `app.ipynb` notebook and run the cells to create an index and query it.

### Persistent Storage

The notebook includes functionality to persist the index to disk. The index is stored in the `./storage` directory. If the directory exists, the notebook loads the existing index; otherwise, it creates a new index and saves it.

### Query Response

The response to the query is printed in a formatted manner, including the source of the information.

## Directory Structure

```plaintext
your-repo-name/
│
├── data/                  # Directory containing documents to be indexed
├── storage/               # Directory where the index is persisted (created by the script)
├── .env                   # Environment variables file containing your OpenAI API key
├── app.ipynb              # Jupyter Notebook for indexing and querying documents
├── requirements.txt       # List of required Python packages
└── README.md              # This README file
