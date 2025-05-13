# Multilingual Travel Visa Assistant
This is a multilingual visa assistant built with LangChain, FAISS, GPT-4, and Deep Translator. You can ask visa related questions in any language, and it will:

1. Detect your language

2. Translate the question to English

3. Retrieve relevant info from official visa websites

4. Generate an answer with GPT-4

5. Translate the answer back to your language

## Features

- Multilingual support (over 100 languages via Deep Translator)

- Real-time data scraping from government visa sites

- GPT-4 via LangChain for better, grounded answers

- Fast search with FAISS vectorstore

- Interactive chatbot with Gradio UI

## Tech Stack

- LangChain

- OpenAI GPT-4 (langchain_openai)

- HuggingFace Embeddings (all-MiniLM-L6-v2)

- FAISS

- BeautifulSoup + Requests (scraping)

- Deep Translator

- Gradio (interface)

- langdetect (for language detection)

## About the Translator
We're using [``` deep-translator ```](https://github.com/nidhaloff/deep-translator), an open-source Python library that interfaces with various free translation providers, including Google Translate. It supports a wide range of languages and is suitable for most common translation needs.

### Supported Languages: 
You can find the list of supported languages and translation providers in the official documentation: https://deep-translator.readthedocs.io/en/latest/usage.html#check-supported-languages

If a translation fails or isn’t available, the bot will fall back to English.

## Getting Started

### 1. Clone the repo
```
git clone https://github.com/zarinhq/multilingual-visa-assistant.git
cd multilingual-travel-assistant
```

### 2. Create a virtual environment
```
python3 -m venv env
source env/bin/activate
```

### 3. Install dependencies 
```
pip install -r requirements.txt
```

### 4. Create a .env file
Add your OpenAI API key like this:
```
OPENAI_API_KEY=your_openai_key
```
### 5. Launch the notebook
```
jupyter notebook 
```

### 6. Open and run multilingual_visa_assistant.ipynb

## Limitations

- Some languages may fail if deep-translator doesn’t support them

- Long scraping sessions may slow down response (keep depth low)

- Currently uses OpenAI GPT-4 — billing applies per token