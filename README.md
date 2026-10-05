# AI Knowledge Base Search Assistant

## Overview

AI Knowledge Base Search Assistant is a Python desktop application that allows users to search a local knowledge base using natural-language questions.

The project combines semantic search, relevance scoring, grounded answer generation, source citations, category filtering, search history, and TXT exports inside a custom Tkinter GUI.

The goal of the project is to demonstrate how AI-assisted retrieval can be used to find and present useful information from a controlled set of knowledge-base documents.

---

## Key Features

- Natural-language search
- Semantic search using sentence embeddings
- Relevance percentage scoring
- Confidence labels
- Top matching knowledge-base articles
- Grounded AI-generated answers
- Source-backed fallback responses
- Explicit source citations
- Category filtering
- Recent search history
- Weak/no-match handling
- Current-result TXT export
- Session-log TXT export
- Custom dark-theme Tkinter interface

---

## Knowledge Base

The project currently includes sample articles covering:

- Password and account access
- Printer troubleshooting
- Wi-Fi troubleshooting
- Microsoft Teams audio troubleshooting
- Multi-factor authentication

The knowledge base can be expanded by adding additional text-based support articles.

---

## AI and Search Workflow

The application follows a retrieval-first workflow:

1. The user enters a natural-language question.
2. Knowledge-base documents are loaded from local text files.
3. Sentence embeddings are used to compare the question against the available articles.
4. Documents are ranked by semantic similarity.
5. The highest-ranked article is selected when its relevance score meets the minimum threshold.
6. The application generates a grounded response using the retrieved article.
7. If the local model produces weak, repetitive, or unreliable output, the application falls back to source-backed guidance.
8. The source article, relevance score, confidence level, and top matches are displayed for transparency.

---

## Technologies Used

- Python
- Visual Studio Code
- Tkinter
- sentence-transformers
- Hugging Face Transformers
- FLAN-T5
- PyTorch
- pathlib
- Local text-based knowledge-base files

---

## Project Structure

```text
AI Knowledge Base Search Assistant/
│
├── app.py
├── requirements.txt
├── README.md
│
├── data/
│   └── knowledge_base/
│       ├── mfa_setup.txt
│       ├── microsoft_teams_audio.txt
│       ├── password_reset.txt
│       ├── printer_troubleshooting.txt
│       └── wifi_troubleshooting.txt
│
├── src/
│   ├── answer_generator.py
│   ├── document_loader.py
│   ├── search_engine.py
│   └── utils.py
│
├── exports/
└── screenshots/

# AI Knowledge Base Search Assistant

## Overview

AI Knowledge Base Search Assistant is a Python desktop application that allows users to search a local knowledge base using natural-language questions.

The project combines semantic search, relevance scoring, grounded answer generation, source citations, category filtering, search history, and TXT exports inside a custom Tkinter GUI.

The goal of the project is to demonstrate how AI-assisted retrieval can be used to find and present useful information from a controlled set of knowledge-base documents.

---

## Key Features

- Natural-language search
- Semantic search using sentence embeddings
- Relevance percentage scoring
- Confidence labels
- Top matching knowledge-base articles
- Grounded AI-generated answers
- Source-backed fallback responses
- Explicit source citations
- Category filtering
- Recent search history
- Weak/no-match handling
- Current-result TXT export
- Session-log TXT export
- Custom dark-theme Tkinter interface

---

## Knowledge Base

The project currently includes sample articles covering:

- Password and account access
- Printer troubleshooting
- Wi-Fi troubleshooting
- Microsoft Teams audio troubleshooting
- Multi-factor authentication

The knowledge base can be expanded by adding additional text-based support articles.

---

## AI and Search Workflow

The application follows a retrieval-first workflow:

1. The user enters a natural-language question.
2. Knowledge-base documents are loaded from local text files.
3. Sentence embeddings are used to compare the question against the available articles.
4. Documents are ranked by semantic similarity.
5. The highest-ranked article is selected when its relevance score meets the minimum threshold.
6. The application generates a grounded response using the retrieved article.
7. If the local model produces weak, repetitive, or unreliable output, the application falls back to source-backed guidance.
8. The source article, relevance score, confidence level, and top matches are displayed for transparency.

---

## Technologies Used

- Python
- Visual Studio Code
- Tkinter
- sentence-transformers
- Hugging Face Transformers
- FLAN-T5
- PyTorch
- pathlib
- Local text-based knowledge-base files

---

## Project Structure

```text
AI Knowledge Base Search Assistant/
│
├── app.py
├── requirements.txt
├── README.md
│
├── data/
│   └── knowledge_base/
│       ├── mfa_setup.txt
│       ├── microsoft_teams_audio.txt
│       ├── password_reset.txt
│       ├── printer_troubleshooting.txt
│       └── wifi_troubleshooting.txt
│
├── src/
│   ├── answer_generator.py
│   ├── document_loader.py
│   ├── search_engine.py
│   └── utils.py
│
├── exports/
└── screenshots/

---

## How to Run

1. Download or clone the project.
2. Open the project folder in Visual Studio Code.
3. Create or activate a Python virtual environment.
4. Install the required dependencies:
```pip install -r requirements.txt
5. Run the application.
```Python app.py

The first launch may take longer while the required AI models are downloaded and cached locally.

--- 

## Search Categories
The GUI currently supports:
- All
- Wi-Fi
- Printing
- Microsoft Teams
- MFA
- Password / Account
Selecting a category limits the semantic search to the relevant knowledge-base article group.

---

## Error and No-Match Handling
The application includes safeguards for:
- Blank searches
- Missing knowledge-base content
- Weak semantic matches
- Unrelated questions
- Search errors
- Repetitive or low-quality generated answers
Weak matches are rejected instead of being presented as reliable results.

---

## Export Features
The application can export:
- The current search result
- The current session search log
Exports are saved as TXT files for easy review and documentation.

---

## Skills Demonstrated
- Python development
- AI automation
- Semantic search
- Sentence embeddings
- Retrieval-based AI workflows
- Local language-model integration
- Prompt design
- Hallucination safeguards
- Source-grounded responses
- Tkinter GUI development
- Search filtering
- Error handling
- File processing
- TXT reporting
- Application testing
- Technical documentation

---
















