# Ice Breaker

Ice Breaker is a Flask-based web application that generates personalized conversation starters by analyzing LinkedIn and Twitter profiles using LangChain and OpenAI.

## Features

- Looks up a person's LinkedIn and Twitter profiles from their name
- Summarizes their professional background and interests
- Generates a fun, personalized ice breaker to kick off a conversation

## Getting Started

### Prerequisites

- Python 3.10
- [pipenv](https://pipenv.pypa.io/)

### Installation

```bash
pipenv install
```

### Configuration

Create a `.env` file in the project root (see `.env.example`) with the following variables:

- `OPENAI_API_KEY` - OpenAI API for LLM
- `SCRAPIN_API_KEY` - Scrapin.io for LinkedIn data
- `TAVILY_API_KEY` - Tavily for web search
- `TWITTER_API_KEY`, `TWITTER_API_SECRET`, `TWITTER_ACCESS_TOKEN`, `TWITTER_ACCESS_SECRET` - Optional Twitter API

Optional LangSmith tracing:

- `LANGCHAIN_TRACING_V2=true`
- `LANGCHAIN_API_KEY`
- `LANGCHAIN_PROJECT=ice_breaker`

### Running the Application

```bash
pipenv run python app.py
```

## Development

```bash
# Format code with Black
pipenv run black .

# Sort imports with isort
pipenv run isort .

# Lint code with pylint
pipenv run pylint [module_name]
```

See [`CLAUDE.md`](CLAUDE.md) for more details on the project architecture.
