# Hospitality AI Chatbot: Neural Network Intent Classifier & Flask API

An intelligent, context-driven conversational assistant designed for hotel web platforms. The system uses a feedforward neural network built with **PyTorch** and **NLTK** for natural language understanding (intent classification), integrated into a **Flask REST API** containerized with **Docker**.

---

## 📌 Features & Architecture
- **Natural Language Processing (NLP):** Tokenization, stemming, and Bag-of-Words vectorization using `nltk`.
- **Deep Learning Core:** Multi-layer PyTorch neural network trained on custom intent schemas (`intents.json`).
- **RESTful Backend:** Lightweight Flask service processing incoming chat payloads (`POST` requests) and serving contextual responses.
- **Frontend-Ready:** Pre-configured endpoints and JavaScript integration for client applications.
- **Containerized Deployment:** Reproducible setup using Docker and Docker Compose.

---

## 🛠️ Tech Stack
- **Languages:** Python 3.9+, JavaScript, HTML/CSS
- **Machine Learning & NLP:** PyTorch, NLTK, NumPy
- **Backend & APIs:** Flask, REST APIs (JSON payloads)
- **DevOps & Environment:** Docker, Docker Compose

---

## 📂 Project Structure
```text
├── data/
│   └── intents.json        # Training corpus (tags, patterns, and responses)
├── models/
│   └── data.pth            # Trained PyTorch model weights
├── static/
│   ├── app.js              # Frontend asynchronous fetch logic
│   └── style.css           # Chat widget styling
├── templates/
│   └── base.html           # Web interface template
├── app.py                  # Flask API server & routing
├── chat.py                 # Standalone inference script
├── model.py                # Neural network architecture definition
├── nltk_utils.py           # Text preprocessing utilities
├── train.py                # Pipeline for model training and evaluation
├── Dockerfile              # Docker runtime container definition
├── docker-compose.yml      # Multi-container orchestration
├── requirements.txt        # Python package dependencies
└── README.md
```

---
### 🚀 Getting Started
Option 1: Run with Docker Compose (Recommended)
Ensure you have Docker and Docker Compose installed:

```Bash
# Clone the repository
git clone [https://github.com/kathyhernndez/YOUR_REPO_NAME.git](https://github.com/kathyhernndez/YOUR_REPO_NAME.git)
cd YOUR_REPO_NAME

# Build and launch the containerized application
docker-compose up -d
Navigate to http://localhost:5000 in your browser to access the chat interface. To stop the service:
```

```Bash
docker-compose down
Option 2: Local Setup (Virtual Environment)
Clone the repository and prepare the environment:
```
```Bash
git clone [https://github.com/kathyhernndez/YOUR_REPO_NAME.git](https://github.com/kathyhernndez/YOUR_REPO_NAME.git)
cd YOUR_REPO_NAME
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
Train the intent classification model:
```
```Bash
python train.py
This processes intents.json and exports the trained weights to data.pth.

Verify the model via CLI (Optional):
```
```Bash
python chat.py
Start the Flask server:
```
```Bash
python app.py
Open http://127.0.0.1:5000 in your browser.
```
---
### 📊 Dataset Schema (intents.json)
The chatbot's domain knowledge is defined via a structured JSON corpus:
```
tag: Target intent label (e.g., "booking", "check-in", "pricing").

patterns: Sample user inputs used for text vectorization and training.

responses: Curated outputs returned upon high-confidence intent classification.
```
----
### 📬 Authors & Contacts
- Katherine Hernández — Software Engineer & Applied AI
- Cristian D. Avella - Data Engineer 
