# AI Chatbot Exploration Portfolio

This section of my portfolio showcases several chatbot projects and experiments, progressing from rule-based systems to neural network and transformer-based conversational agents.[file:4][file:3][file:1][file:2]

## 1. Chatbot Landscape Exploration

**Goal:** Analyze real-world customer service chatbots (e.g., Amazon, Geico, Chase) to understand current industry practices and limitations.[file:4]

**What I did:**
- Interacted with multiple production chatbots and documented their behaviors, response patterns, and failure modes.[file:4]
- Identified that most systems were template- or flow-based with little to no true NLP, struggling with free-form user input.[file:4]
- Reflected on the gap between scripted assistants and AI-driven conversational agents, framing opportunities for improvement.[file:4]

**Key takeaways:**
- Rule-based flows are fast and cheap but brittle when users deviate from expected paths.[file:4]
- There is significant room for AI-based chatbots that can handle open-ended, domain-specific queries more intelligently.[file:4]

---

## 2. Information-Retrieval Chatbot (NLP + TF‑IDF)

**Goal:** Build a simple FAQ-style chatbot that can answer questions about chatbots using classical NLP and information retrieval.[file:3]

**What I built:**
- Scraped educational content about chatbots from the web and stored it as a text corpus for the bot to reference.[file:3]
- Performed preprocessing with NLTK (tokenization, lowercasing, lemmatization, stopword removal) to normalize text.[file:3]
- Implemented a TF‑IDF vectorizer and cosine similarity to retrieve the most relevant sentence as the bot’s response.[file:3]
- Added intent-like handling for greetings and fallback responses when similarity scores were too low.[file:3]

**Technical highlights:**
- Python, NLTK, scikit-learn (`TfidfVectorizer`, cosine similarity).[file:3]
- Demonstrated how a purely retrieval-based chatbot can be built without deep learning while still leveraging NLP.[file:3]

---

## 3. Neural Network Intent Classification Chatbot

**Goal:** Move from retrieval-based responses to an intent-driven chatbot using a custom neural network classifier.[file:1]

**What I built:**
- Defined a small intent set (e.g., greeting, busy, bye) and created labeled example sentences for each.[file:1]
- Built a simple bag-of-words representation to encode user sentences into fixed-length feature vectors.[file:1]
- Trained a feed-forward neural network (Keras + TensorFlow) to classify user input into one of the defined intents.[file:1]
- Mapped predicted intents to hand-crafted responses, enabling multi-turn interactions and exit commands.[file:1]

**Technical highlights:**
- Used dense layers with sigmoid and softmax activations for multi-class intent classification.[file:1]
- Implemented preprocessing, encoding, model training, and evaluation (accuracy on a small test set).[file:1]
- Showcased end-to-end flow: text preprocessing → vectorization → neural model → conversational behavior.[file:1]

---

## 4. Transformer-Based Conversational AI (DialoGPT)

**Goal:** Experiment with large pre-trained language models for more natural, open-domain conversations.[file:2]

**What I built:**
- Integrated Microsoft’s DialoGPT-medium model via Hugging Face Transformers to power a console chatbot.[file:2]
- Implemented a `ChatBot` class that:
  - Loads tokenizer and model checkpoints.
  - Maintains conversation history for context across turns.
  - Encodes user input, appends an end-of-sentence token, and generates responses with `generate`.[file:2]
- Added logic for:
  - Recognizing “bye/quit/exit” to gracefully end the session.[file:2]
  - Simple fallback responses when the model output was not usable.[file:2]

**Technical highlights:**
- Python, PyTorch, Hugging Face `AutoTokenizer` and `AutoModelForCausalLM`.[file:2]
- Demonstrated practical handling of token limits, chat history management, and user experience considerations.[file:2]

---

## Skills Demonstrated

Across these projects, the work covers:

- **NLP fundamentals:** Tokenization, lemmatization, stopword removal, TF‑IDF, cosine similarity.[file:3]
- **Classical vs. neural approaches:** Rule-based flows, retrieval-based QA, intent classification with neural networks.[file:1][file:3]
- **Deep learning & transformers:** Keras/TensorFlow feed-forward networks and transformer-based dialogue models (DialoGPT).[file:1][file:2]
- **Practical chatbot design:** Conversation flow, fallbacks, exit conditions, and critical analysis of real-world systems.[file:4][file:2][file:1][file:3]


