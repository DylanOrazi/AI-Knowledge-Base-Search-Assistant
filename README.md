# AI Knowledge Base Search Assistant

A Python desktop application that uses semantic search and a local AI model to answer natural-language questions from a controlled technical knowledge base.

The application ranks relevant documents, generates source-grounded answers, displays citations and confidence information, tracks recent searches, and supports TXT exports.

---

## Features

- Natural-language knowledge base search
- Semantic similarity using sentence embeddings
- AI-generated grounded answers
- Source-backed fallback responses
- Relevance percentage scoring
- Confidence labels
- Source citations
- Top matching articles
- Category filtering
- Recent search history
- Weak-match and no-match handling
- Current result export
- Session log export
- Dark-themed Tkinter GUI

---

## Knowledge Base Topics

The included sample knowledge base covers:

- Wi-Fi troubleshooting
- Printer troubleshooting
- Microsoft Teams audio issues
- Multi-factor authentication
- Password and account access

Additional `.txt` knowledge base articles can be added later.

---

## How It Works

1. The user enters a natural-language question.
2. The application loads the local knowledge base.
3. Sentence embeddings compare the question with each document.
4. Documents are ranked by semantic similarity.
5. The strongest relevant article is selected.
6. A grounded AI answer is generated from that article.
7. If the generated answer is weak or unreliable, a source-based fallback is used.
8. The application displays the answer, source, relevance score, confidence level, and top matches.

---

## Technologies

- Python
- Tkinter
- Sentence Transformers
- Hugging Face Transformers
- FLAN-T5
- PyTorch
- Visual Studio Code

---

## Project Structure

```text
AI Knowledge Base Search Assistant/
├── app.py
├── requirements.txt
├── README.md
├── data/
│   └── knowledge_base/
│       ├── mfa_setup.txt
│       ├── microsoft_teams_audio.txt
│       ├── password_reset.txt
│       ├── printer_troubleshooting.txt
│       └── wifi_troubleshooting.txt
├── exports/
├── screenshots/
└── src/
    ├── answer_generator.py
    ├── document_loader.py
    ├── search_engine.py
    └── utils.py
```

---

## Installation

Clone or download the repository.

Install the required dependencies:

```bash
pip install -r requirements.txt
```

Run the application:

```bash
python app.py
```

The first launch may take longer while the required AI models are downloaded and cached locally.

---

## Search Categories

The application includes the following filters:

- All
- Wi-Fi
- Printing
- Microsoft Teams
- MFA
- Password / Account

Selecting a category limits the semantic search to documents associated with that topic.

---

## Search Results

Successful searches can display:

- AI-generated answer
- Source article title
- Source filename
- Relevance percentage
- Confidence level
- Full source article
- Top matching documents

This provides transparency into where the answer came from and how strongly the search matched the available knowledge base.

---

## Grounded AI Responses

The application uses retrieved knowledge-base content as context for the local language model.

The AI is instructed to answer using only the information found in the selected source document.

Additional safeguards detect low-quality output such as:

- Extremely short answers
- Excessive repetition
- Repeated negative responses
- Incomplete generated responses
- Certain contradictions with the source material

When unreliable output is detected, the application uses a source-grounded fallback response instead.

---

## Relevance and Confidence

Semantic similarity scores are converted into percentage-based relevance scores.

The application also assigns confidence labels:

- High
- Moderate
- Low
- Very Low

Weak matches below the configured threshold are rejected instead of being presented as reliable answers.

---

## Search History

The application keeps a recent-search history during the current session.

Each successful search records:

- User question
- Best matching article
- Relevance score

Only successful searches are recorded. Weak or unrelated searches are excluded.

---

## Error Handling

The application includes handling for:

- Empty searches
- Missing knowledge-base content
- Weak semantic matches
- Unrelated questions
- Search failures
- Repetitive AI responses
- Low-quality generated answers

Users receive clear messages when the system cannot confidently answer a question.

---

## Export Options

The application includes two TXT export features.

### Export Current Result

Saves the currently displayed search result to a `.txt` file.

### Export Session Log

Saves successful searches from the current application session, including:

- Timestamp
- User question
- Best matching article
- Relevance score

---

## Skills Demonstrated

- Python development
- AI automation
- Semantic search
- Sentence embeddings
- Retrieval-based AI workflows
- Local language model integration
- Prompt engineering
- Source-grounded answer generation
- AI fallback logic
- Relevance scoring
- Confidence classification
- Tkinter GUI development
- Category filtering
- Search history
- Error handling
- File processing
- TXT reporting
- Application testing
- Technical documentation