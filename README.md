# AI Chat Log Summarizer

This project is a Python-based tool designed to read and summarize chat logs between a user and an AI. It parses conversations, calculates message statistics, extracts key topics, and generates a concise summary. The tool leverages the Natural Language Toolkit (NLTK) for robust text processing and keyword extraction.

## Project Description

The `AI Chat Log Summarizer` aims to provide a quick overview of conversations stored in `.txt` files. It parses the conversation, and produces a simple summary including message counts and frequently used keywords. This project showcases basic NLP capabilities using Python, with an optional nltk-based keyword extraction.

## Features

* **Input Handling:** Reads `.txt` files containing chat logs between a user and an AI.
* **Chat Log Parsing:** Separates messages by speaker (User: and AI:) and stores them for analysis.
* **Message Statistics:** Counts total messages, and counts messages from User vs. AI.
* **Keyword Analysis:**
    * Extracts the top 5 most frequently used words.
    * Excludes common stop words (e.g., "the", "is", "and").
    * Can optionally use a simple NLTK for better keyword extraction.
* **Summary Generation:** Outputs a clear summary that includes:
    * Total number of exchanges.
    * Nature of the conversation (based on keyword topics).
    * Most common keywords.
* **Multiple Chat Logs (Bonus):** Allows summarization of multiple chat logs from a folder.

## How to Run

Follow these steps to set up and run the chat summarizer.

### Prerequisites

* Python 3.6+
* `pip` (Python package installer)

### 1. Clone the Repository (if applicable)

If this code is part of a GitHub repository, you would typically clone it first:
```bash
git clone <your-repository-url>
cd <your-repository-name>
```

### 2. Install Dependencies
The project requires the `nltk` library.
```bash
pip install nltk
```

### 3. Run `chat_summerizer.ipynb` file
Input file : `chat.txt` 
```bash
User: Hello!
AI: Hi! How can I assist you today?
User: Can you explain what machine learning is?
AI: Certainly! Machine learning is a field of AI that allows systems to learn from data.
User: What are some applications of machine learning?
AI: Machine learning is used in recommendation systems, natural language processing, image recognition etc.
User: That sounds interesting. Thanks!
AI: You're welcome!
```
Output : 
     
![image](https://github.com/user-attachments/assets/1dc0ea17-8301-4fe2-8cf5-a17743990ecb)

### 4. Run `chat_summ_nltk.ipynb` file (Bonus Part)
Now we can read multiple `.txt` files in a folder <br>
Input files in `chat_logs` folder
1. `chat1.txt`
```bash
User: Hello!
AI: Hi! How can I assist you today?
User: Can you explain what machine learning is?
AI: Certainly! Machine learning is a field of AI that allows systems to learn from data.
User: What are some applications of machine learning?
AI: Machine learning is used in recommendation systems, natural language processing, image recognition etc.
User: That sounds interesting. Thanks!
AI: You're welcome!
```
2. `chat2.txt`
```bash
User: Hi, can you tell me about Python? 
AI: Sure! Python is a popular programming language known for 
its readability. 
User: What can I use it for? 
AI: You can use Python for web development, data analysis, 
AI, and more.
```
3. `chat3.txt`
```bash
User: Hello! 
AI: Hi! How can I assist you today? 
User: Can you explain what machine learning is? 
AI: Certainly! Machine learning is a field of AI that allows systems to 
learn from data. 
```

Output : 
```bash

--- Summarizing Chat Logs in 'chat_logs' ---

Processing: chat1.txt
Summary:
The conversation had 8 exchanges.
The user asked mainly about machine and learning.
Most common keywords: machine, learning, systems, assist, field.
--------------------------------------------------------------------------------

Processing: chat2.txt
Summary:
The conversation had 4 exchanges.
The user asked mainly about python and use.
Most common keywords: python, use, tell, sure, popular.
--------------------------------------------------------------------------------

Processing: chat3.txt
Summary:
The conversation had 4 exchanges.
The user asked mainly about machine and learning.
Most common keywords: machine, learning, assist, field, ai.
--------------------------------------------------------------------------------

```

### File Structure
```
project_folder/
├── chat_summerizer.py          # Main summarizer script
├── chat_summ_nltk.py           # Bonus: Summarizer using NLTK
├── chat.txt                    # Sample chat input
├── nltk_data/                  # NLTK data directory
│   ├── tokenizers/
│   │   └── punkt/
│   └── corpora/
│       ├── stopwords/
│       └── wordnet/
└── chat_logs/                  # Sample chat logs
    ├── chat1.txt
    ├── chat2.txt
    └── chat3.txt
```


<br>
<br>

### Thanks for reading. 
