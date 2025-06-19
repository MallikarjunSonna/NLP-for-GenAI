# NLP Lesson 4: Text Representation (Turning Text into Numbers)

## 📌 Why This Matters:
Machines don’t understand words — they understand **numbers**.  
So we must **convert text into numerical representations** that ML or LLMs can learn from.

---

## 🧠 4 Ways to Represent Text

| Method                  | Works Well For           | Limitation                          |
|------------------------|--------------------------|-------------------------------------|
| 1. Bag of Words (BoW)  | Simple classification     | Ignores word order, context         |
| 2. TF-IDF              | Text importance ranking   | Still ignores context               |
| 3. Word Embeddings     | Semantic meaning (Word2Vec, GloVe) | Pre-trained, limited domain     |
| 4. Transformer Embeddings | Deep context-aware understanding | Requires GPU or cloud setup       |

---

## 🔹 1. Bag of Words (BoW)

### 📘 Concept:
Create a vocabulary of all unique words, then represent each sentence as a vector showing **word counts**.

### 📌 Example:

Sent 1: "I love NLP"  
Sent 2: "NLP is fun"

### ✅ Vocabulary:
["I", "love", "NLP", "is", "fun"]

### 🔢 Vectors:

| Sentence        | Vector                |
|----------------|------------------------|
| "I love NLP"   | [1, 1, 1, 0, 0]        |
| "NLP is fun"   | [0, 0, 1, 1, 1]        |

### 🚫 Limitation:
- No understanding of **context**
- "I love NLP" = "NLP love I"

---

## 🔹 2. TF-IDF (Term Frequency - Inverse Document Frequency)

### 📘 Concept:
TF = how often a word appears  
IDF = how rare that word is across documents

TF-IDF = importance of a word in a document, relative to the entire dataset

### 💡 Use-case:
- Text classification (e.g., spam, sentiment analysis)
- Keyword extraction

### 🔢 Output:
- Gives you **weighted vectors**, not just counts

---

## 🔹 3. Word Embeddings (Word2Vec, GloVe)

### 📘 Concept:
Maps words into high-dimensional **dense vectors** where similar meanings are close in space.

Example:
king - man + woman ≈ queen

### ✅ Use-cases:
- Text similarity
- Word analogy tasks
- Better than BoW and TF-IDF

### ⚙️ Tools:
- gensim for Word2Vec
- Pretrained GloVe embeddings

---

## 🔹 4. Transformer-based Embeddings (BERT, GPT)

### 📘 Concept:
Words are represented **in context** using the Transformer architecture.
- "Bank" in "river bank" ≠ "bank" in "money bank"
- Captures **position**, **meaning**, and **sentence-level context**

### ✅ Use-cases:
- Question answering
- Chatbots
- Document similarity
- LLM fine-tuning

### 🧰 Tools:
- transformers library (by Hugging Face)

---

## ✅ Summary Table

| Method        | Captures Meaning? | Captures Order? | Best For                        |
|---------------|-------------------|------------------|---------------------------------|
| Bag of Words  | ❌ No             | ❌ No            | Simple models, fast search     |
| TF-IDF        | ❌ No             | ❌ No            | Keyword importance, filtering  |
| Word2Vec      | ✅ Yes            | ❌ Partial       | Semantics, similarity          |
| BERT Embeds   | ✅ Deep Context   | ✅ Yes           | Chatbots, Q&A, GenAI models    |

---

## 🧠 Real-World GenAI Connection

| Use-case         | Under the Hood                    |
|------------------|-----------------------------------|
| Chatbots (GPT)   | Uses Transformer-based embeddings |
| Text summarizer  | Uses contextual embeddings        |
| Resume matcher   | Uses Word2Vec / Sentence-BERT     |
