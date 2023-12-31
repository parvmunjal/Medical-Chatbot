# Medical Chatbot Project

Overview

This project implements a medical chatbot using state-of-the-art language models and Pinecone for efficient vector storage and retrieval. The chatbot leverages CTransformers and Sentence Transformers for question-answering capabilities.

Requirements

Make sure you have the following dependencies installed before running the chatbot:

CTransformers==0.2.5
Sentence Transformers==2.2.2
Pinecone-client
Langchain==0.0.225
Flask
PyPDF
python-dotenv
You can install these dependencies by running:
bash
Copy code
```
pip install -r requirements.txt
```
Project Structure

src/helper.py: Contains utility functions for loading embeddings, splitting text, and downloading Hugging Face embeddings.
src/prompt.py: Defines the prompt template used in the chatbot.
app.py: The main Flask application file that initializes the chatbot and handles user interactions.
Usage

Set up your environment by creating a .env file with the required environment variables:
env
Copy code
PINECONE_API_KEY=your_pinecone_api_key
PINECONE_API_ENV=your_pinecone_api_environment
Run the Flask application:
bash
Copy code
```
python app.py
```
The chatbot will be accessible at http://127.0.0.1:5000/.
Access the chatbot through the web interface or send POST requests to http://127.0.0.1:5000/get with the user's message.
Customization

You can customize the chatbot's behavior by modifying the logic in the chat route of app.py. Currently, it checks for a specific question ("who is your founder") and provides a hardcoded response. You can extend this logic to handle additional commands or questions.

Additional Notes

The project uses the LLAMA model for question-answering, and the models are loaded using CTransformers.
Pinecone is utilized as the vector store for efficient document retrieval.
The chatbot's web interface is built using Flask.
Feel free to explore and enhance the functionality of the medical chatbot according to your requirements.
