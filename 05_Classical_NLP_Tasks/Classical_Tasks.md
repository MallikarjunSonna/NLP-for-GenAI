# NLP Lesson 5: Classical NLP Tasks

These tasks are the building blocks of most real-world NLP systems like:
- Chatbots
- Resume parsers
- QA systems
- Translation engines

---

## 🧱 Core Classical NLP Tasks:

### 🔹 1. Tokenization
**What:** Split a sentence into words or sub-words  
**Example:** "I love NLP." → ["I", "love", "NLP", "."]

**Tools:** nltk.word_tokenize, spaCy, transformers

---

### 🔹 2. Part-of-Speech (POS) Tagging
**What:** Assign word types — noun, verb, adjective, etc.  
**Example:** "I love NLP" → [("I", PRP), ("love", VBP), ("NLP", NNP)]

**Why it matters:** Helps understand grammar and context.

**Use-cases:** Grammar correction, summarization, sentence parsing

---

### 🔹 3. Named Entity Recognition (NER)
**What:** Extract real-world entities — names, locations, dates, money, etc.  
**Example:** "Google was founded in California in 1998."  
→ [("Google", ORG), ("California", LOC), ("1998", DATE)]

**Use-cases:** Resume parsing, news categorization, info extraction

---

### 🔹 4. Lemmatization & Stemming
- **Stemming:** Chops word to base form (not always accurate)
- **Lemmatization:** Uses grammar + vocab to find root word

**Example:** "running", "runs", "ran" → "run"

**Tools:** NLTK, spaCy

---

### 🔹 5. Chunking (Shallow Parsing)
**What:** Group words into phrases like noun phrases (NP), verb phrases (VP)  
**Example:** "The tall man" → NP (noun phrase)

**Why:** Useful for extracting info without full sentence parsing

---

### 🔹 6. Dependency Parsing
**What:** Understand how words relate to each other  
**Example:** "John saw Mary with a telescope" → Who used the telescope? (Ambiguity in dependency)

**Use-case:** Needed in deep NLP tasks like translation, summarization

---

## 🧠 Summary Table

| Task            | What it Does                  | Tools         | Use-case Example             |
|------------------|-------------------------------|---------------|------------------------------|
| Tokenization     | Split into words/subwords     | NLTK, spaCy   | Preprocessing for LLMs      |
| POS Tagging      | Identify word types           | NLTK, spaCy   | Grammar checker             |
| NER              | Extract names/places/dates    | spaCy, HuggingFace | Resume parsing         |
| Lemmatization    | Normalize word to base form   | spaCy, NLTK   | Matching word variants      |
| Chunking         | Group words into phrases      | NLTK, spaCy   | Phrase extraction           |
| Dependency Parse | Understand sentence structure | spaCy         | Question answering systems  |

---

## 📌 Real-World GenAI Use

| GenAI Feature          | Behind the Scenes        |
|------------------------|--------------------------|
| Chatbot understanding  | POS + Dependency Parsing |
| Resume entity match    | NER + Lemmatization      |
| Prompt optimization    | Tokenization + Parsing   |
