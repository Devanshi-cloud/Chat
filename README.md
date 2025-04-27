# InspireHer Chatbot

InspireHer Chatbot is an AI-powered financial and business mentor designed to assist Indian rural women in entrepreneurship, financial literacy, government schemes, and digital empowerment. The chatbot provides detailed, actionable, and culturally appropriate guidance to empower women in rural settings.

## Features

- **Conversational AI**: Uses LangChain and Google Generative AI to provide intelligent and context-aware responses.
- **Document Retrieval**: Loads and processes PDFs, JSON, and text files to retrieve relevant information.
- **Vector Database**: Utilizes Chroma for efficient document storage and retrieval.
- **Customizable Prompts**: Tailored system prompts to ensure responses are simple, structured, and culturally appropriate.
- **FastAPI Integration**: Provides a RESTful API for seamless interaction.

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/your-repo/InspireHer-Chatbot.git
    cd InspireHer-Chatbot
    ```

2. Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```

3. Set environment variables:
    - `HUGGINGFACE_HUB_API_TOKEN`: Your Hugging Face API token.
    - `GEMINI_API_KEY`: Your Google Generative AI API key.

4. Run the application:
    ```bash
    uvicorn main:app --reload
    ```

## API Endpoints

### Chat Endpoint
- **URL**: `/`
- **Method**: `POST`
- **Request Body**:
  ```json
  {
     "query": "Your question here",
     "chat_history": [
        {"role": "user", "content": "Previous user message"},
        {"role": "assistant", "content": "Previous assistant response"}
     ]
  }
  ```
- **Response**:
  ```json
  {
     "response": "AI-generated response"
  }
  ```

## Document Loading

The chatbot supports the following document types:
- **PDFs**: Loaded using `PyPDFLoader`.
- **JSON**: Parses JSON files into LangChain `Document` objects.
- **Text Files**: Reads `.txt` files for additional context.

## Vector Database

- **Embeddings**: Uses Hugging Face's `sentence-transformers/all-MiniLM-L6-v2` for feature extraction.
- **Persistence**: Stores vectors in a Chroma database for efficient retrieval.

## System Prompt

The chatbot is designed to:
- Provide detailed and actionable responses.
- Use simple and clear language.
- Offer culturally appropriate advice tailored to rural Indian women.

## Example Use Case

1. **User Query**: "What are the government schemes for women entrepreneurs?"
2. **Response**:
    - Detailed information about schemes.
    - Eligibility criteria, required documents, and application process.
    - Contact information for further assistance.

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE).

## Contact

For questions or support, please contact [your-email@example.com].  