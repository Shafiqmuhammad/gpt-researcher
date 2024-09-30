

### Step 1 - Download the project and navigate to its directory

```git clone https://github.com/assafelovic/gpt-researcher.git
cd gpt-researcher
```
### Step 3 - Set up API keys using two methods: exporting them directly or storing them in a .env file.
For Linux/Windows temporary setup, use the export method:
```
export OPENAI_API_KEY={Your OpenAI API Key here}
export TAVILY_API_KEY={Your Tavily API Key here}

LLM_PROVIDER=google
GEMINI_API_KEY=[Your OpenAI API Key here]
```
For a more permanent setup, create a .env file in the current gpt-researcher directory and input the env vars (without export).

-  The default LLM is GPT, but you can use other LLMs such as claude, ollama3, gemini, mistral and more. To learn how to change the LLM provider, see the LLMs documentation page. Please note: this project is optimized for OpenAI GPT models.
- The default retriever is Tavily, but you can refer to other retrievers such as duckduckgo, google, bing, searchapi, serper, searx, arxiv, exa and more. To learn how to change the search provider, see the retrievers documentation page.

## Run with Docker

### Step 1 - Install Docker

### Step 2 - Clone the '.env.example' file, add your API Keys to the cloned file and save the file as '.env'
```
export OPENAI_API_KEY={Your OpenAI API Key here}
export TAVILY_API_KEY={Your Tavily API Key here}

LLM_PROVIDER=google
GEMINI_API_KEY=[Your OpenAI API Key here]
```

### Step 3 - Within the docker-compose file comment out services that you don't want to run with Docker.
```
docker-compose up --build
```
### Step 4 - By default, if you haven't uncommented anything in your docker-compose file, this flow will start 2 processes:
- the Python server running on localhost:8000
- the React app running on localhost:3000
Visit localhost:3000 on any browser and enjoy researching!


