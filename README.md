# Smart Library System (SLS) - AI-Powered Book Management

## 📌 Overview
The Smart Library System (SLS) is an advanced, Django-based web application designed to modernize university library operations. It goes beyond traditional CRUD systems by integrating Natural Language Processing (NLP) to offer multilingual semantic search and intelligent, content-based book recommendations.

## ✨ Key Features
* **AI-Powered Semantic Search:** Utilizes the `paraphrase-multilingual-MiniLM-L12-v2` model via `SentenceTransformers` to understand search intent in both Arabic and English, rather than relying on exact keyword matching.
* **Smart Recommendations:** Generates personalized book suggestions based on a student's academic major (e.g., Software Engineering, AI) and their borrowing history using cosine similarity scoring.
* **Admin Analytics Dashboard:** Features a comprehensive dashboard for tracking active loans, calculating average reading times, and performing "Gap Analysis" on missing books based on user search logs.
* **Automated Borrowing Lifecycle:** Handles borrowing requests, automated due date calculations (14 days), inventory adjustments, and status tracking (Pending, Active, Returned, Rejected).

## 🛠️ Tech Stack
* **Backend:** Python, Django 6.0
* **AI & NLP:** `sentence-transformers`, `numpy` (High-performance vector embeddings)
* **Frontend:** HTML5, Bootstrap 5 (RTL support for Arabic UI)
* **Database:** SQLite (Configured for easy local setup)

## 📐 System Architecture
> **Note:** Included in the `docs/` folder are exported UML diagrams created with PlantUML.
* **Use Case Diagram:** Illustrating Student vs. Admin functionalities.
* **Entity Relationship Diagram (ERD):** Displaying relations between Core models.

## 🚀 Installation & Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/YourUsername/smart-library-system.git
   cd smart-library-system


Create and activate a virtual environment:

python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate


Install dependencies:

pip install -r requirements.txt


Note: Downloading the AI model during the first run may take a few moments.

Apply migrations and populate dummy data:

python manage.py makemigrations
python manage.py migrate
python manage.py populate_db


Generate AI Embeddings:

python manage.py update_embeddings


Run the development server:

python manage.py runserver
