# FAQbot_bank
📚 Introduction
Automated FAQ systems play an important role in bank customer service by providing instant answers to frequently asked questions. The chatbot runs on a structured dataset of predefined FAQs and integrates Sentence-BERT for semantic matching, Facebook AI Similarity Search (FAISS) for efficient vector retrieval, NLTK for keyword-based fallback, and GPT for generating consistent responses.

🛠️ How It Works
1. Query Understanding: User input is preprocessed (e.g., tokenized and normalized).
2. Semantic Matching: Sentence-BERT converts the query and FAQ dataset into embeddings.
3. Keyword-Based Matching: NLTK performs keyword-based fallback to find a close match.
4. FAISS retrieves the most relevant FAQ based on vector similarity.
5. Response Generation: GPT dynamically generates a coherent response based on the retrieved FAQ or query context.

📂 Project Structure
FAQbot_bank/
│
├── data/
│   ├── BankFAQs.csv         # FAQ dataset from https://github.com/MrJay10/banking-faq-bot/blob/master/BankFAQs.csv
│
├── models/
│   ├── sentence_bert/          # Converts the query and FAQ dataset into embeddings
│   ├── nltk/                   # Keyword-Based Matching
│   ├── faiss_index/            # Retrieves the most relevant FAQ based on vector similarity
│   ├── GPT-3.5 API/            # Response Generation
│
├── src/
│   ├── FAQ_chatbot.ipynb       # Includes all major functions
│   ├── pdf2csv.py              # Convert other dataset [PDF (word)] to [Excel] format
│
└── README.md                   # Project documentation
