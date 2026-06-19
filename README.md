# pharma_med

A Flask-based medical chat assistant that uses LangChain, Pinecone, and Groq to build a retrieval-augmented generation (RAG) workflow for medical knowledge search.

## Features

- Web chat interface built with Flask and HTML templates
- Semantic retrieval using Pinecone vector embeddings
- LLM-based response generation with Groq's `ChatGroq`
- Document embedding pipeline provided via `src.helper`
- Environment-based configuration for API keys

## Requirements

- Python 3.10+
- `pip` package manager
- Pinecone account and API key
- Groq API key

## Installation

1. Clone the repository or copy the project files.
2. Create and activate a virtual environment:

```bash
python -m venv venv
venv\Scripts\activate
```

3. Install dependencies:

```bash
pip install -r requirements.txt
```

4. Install the project package:

```bash
pip install -e .
```

## Configuration

Create a `.env` file in the project root with your API keys:

```env
PINECONE_API_KEY=your_pinecone_api_key
GROQ_API_KEY=your_groq_api_key
```

## Running the app

Start the Flask server from the project root:

```bash
python app.py
```

Then open your browser at `http://localhost:5000`.

## Project structure

- `app.py` - Flask application and chat endpoint
- `src/helper.py` - embedding download and Pinecone setup logic
- `src/prompt.py` - system and chat prompt templates
- `templates/chat.html` - chat UI template
- `static/style.css` - UI styling
- `requirements.txt` - required Python dependencies
- `setup.py` - package metadata

## Notes

- Ensure the Pinecone index name matches the value in `app.py` (`medibot` by default).
- This project assumes your embeddings and vector store are already initialized or can be created by the helper logic.

## License

This project is provided "as is". Update the license details as needed.
