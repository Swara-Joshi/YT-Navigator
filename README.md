# 🔴 YT Navigator

## 📋 Overview

YT Navigator is an AI-powered application that helps you navigate and search through YouTube channel content efficiently. Instead of manually watching hours of videos to find specific information, YT Navigator allows you to:

1. **🔍 Search through a channel's videos** using natural language queries
2. **💬 Chat with a channel's content** to get answers based on video transcripts
3. **⏱️ Discover relevant video segments** with precise timestamps

## ✨ Main Features

- **🔐 Authentication**: Secure login and independent sessions
- **📺 Channel Management**: Scan up to 100 videos per channel and get a summary
- **🔍 Search**: Find relevant video segments using Semantic Search
- **💬 Chat**: Have conversations with an AI that has knowledge of the channel's content

## 🧰 Technology Stack

- **🖥️ Backend**: Django, PostgreSQL, PGVector, Structlog
- **🧠 AI & ML**: LangGraph, Sentence Transformers, BM25, Groq (qwen-qwq-32b, llama-3.1-8b-instant)
- **⚙️ Data Processing**: BeautifulSoup, Scrapetube, youtube-transcript-api
- **🎨 Frontend**: Django templates with modern CSS

## 🚀 Installation

### 💻 Without Docker

1. Clone the repository and create virtual environment
   ```bash
   git clone https://github.com/yourusername/yt-navigator.git
   cd yt-navigator
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   pip install -e .
   ```

2. Set up environment and database
   ```bash
   cp .env.example .env
   python manage.py migrate
   ```

3. Run the server
   ```bash
   make dev  # for development
   make prod  # for production
   ```

### 🐳 With Docker

1. Set up environment and run
   ```bash
   cp .env.example .env  # Make sure POSTGRES_HOST=db
   make build-docker
   make run-docker
   ```

## 📖 Usage

1. **📝 Register and Login** to get started
2. **🔗 Connect a YouTube Channel** by entering its URL
3. **📥 Scan Videos** (choose quantity - up to 100)
4. **🔍 Search for Information** across all videos
5. **💬 Chat with the Channel** AI about content

## 📈 Version Information

Current version: 0.1.2 (March 2025)

**Recent Changes**: Added Langsmith dataset creation and example addition

**Known Issues**: Poor exception handling, UI mobile issues, English-only support

## 👥 Team Contributions

| Team Member | Areas of Contribution |
|-------------|------------------------|
| Ramy Solanki | • System architecture and backend development<br>• Django app structure and core functionality<br>• Semantic search with PGVector<br>• Docker and deployment setup |
| Advaith Krishna Vasisht | • LangGraph conversational agent<br>• Embedding pipeline using Sentence Transformers<br>• Hybrid search algorithm (vector + BM25)<br>• Transcript processing and segmentation |
| Swara Joshi | • UI/UX design and implementation<br>• Chat interface with async messaging<br>• Search result visualization<br>• Documentation and testing |


### Code Standards

We use Black for formatting, Ruff for linting, and isort for import sorting, enforced with pre-commit hooks.

```bash
pre-commit install
pre-commit run --all-files
```

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.
