### LLM Evaluation Hub

# 🧠 LLM Evaluation Hub

An open-source tool to systematically evaluate prompts, compare LLM performance, and track cost, latency, and accuracy — all in one place.

## 🚀 Why?
Prompt engineering is still trial-and-error. This hub lets you run tests like a developer — with test cases, metrics, and comparisons across models and versions.

## 🔧 Features
- 🔍 **Prompt Playground**: Compare GPT-4, Claude, etc.
- 🧪 **Test Case Evaluator**: Run JSON/CSV prompt+expected pairs
- 📊 **Metrics Dashboard**: Accuracy, latency, cost per run
- 🔁 **Async Job Runner**: Process large test sets smoothly
- 🧠 **Feedback Loop** (WIP): Score model quality over time

## 🛠 Tech Stack
- **Backend**: FastAPI + PostgreSQL
- **Async Tasks**: Celery + Redis
- **LLM API**: OpenAI (GPT-4), Anthropic Claude
- **Frontend**: (Optional) React / Streamlit / CLI
- **Deployment**: Docker + Render/Fly.io

## 🗂 Project Structure
```
llm-eval-hub/
├── backend/             # FastAPI backend
│   ├── main.py          # API entrypoint
│   ├── routes/          # API routes
│   ├── services/        # Business logic
│   ├── models/          # SQLAlchemy + Pydantic
│   └── utils/           # Helpers
├── worker/              # Celery task queue
├── frontend/            # Optional UI
├── tests/               # Unit tests
├── docker-compose.yml
├── .env.example
└── README.md
```

## 📦 Setup
```bash
git clone https://github.com/yourname/llm-eval-hub.git
cd llm-eval-hub
cp .env.example .env
# Fill in OpenAI keys, DB URL, etc.
docker-compose up --build
```

## 📤 Sample Input Format
```json
[
  {"input": "Summarize: Apple released new iPhones...", "expected": "Apple announced new iPhones"},
  {"input": "Extract date: Our meeting is on April 5.", "expected": "April 5"}
]
```

## 📈 Roadmap
- [x] Prompt Playground API
- [x] Batch Evaluation Runner
- [x] PostgreSQL result storage
- [ ] Vector search for prior prompts
- [ ] Slack or CLI interface
- [ ] Model scoring w/ feedback loop

## 📄 License
MIT

---
_👋 Built by Brielle Nguyen to make prompt testing less painful and more reliable._
