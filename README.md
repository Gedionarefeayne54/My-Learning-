# AI Foundations, History & Terminology

> A quick-reference primer on how AI-powered applications differ from traditional software, why they exist now, and the core vocabulary you'll run into when building with them.

## 📌 Big Idea

AI-powered applications are **traditional software + a model intelligence layer**. The AI doesn't replace the application — it adds a new capability for meaning, prediction, generation, and personalization on top of the same backend, database, and UI you already know.

## 🆚 Traditional vs. AI-Powered Applications

**Core logic**
- Traditional: rules written directly by developers
- AI-powered: rules + model predictions/generated responses

**Search behavior**
- Traditional: exact keyword matching
- AI-powered: meaning-based (semantic) matching

**Output style**
- Traditional: fixed and predictable
- AI-powered: varies with model, prompt, and settings

**Best for**
- Traditional: forms, payments, CRUD, permissions, exact workflows
- AI-powered: chat, recommendations, summarization, semantic search, generation

**Main risk**
- Traditional: too rigid to understand user intent
- AI-powered: can hallucinate or be inconsistent if not controlled

**Example — search:**
\`\`\`sql
-- Traditional: exact keyword match
SELECT * FROM questions
WHERE title LIKE '%React%' OR body LIKE '%React%';
\`\`\`
A search for "frontend library" returns nothing here, even though a post about React is exactly what the user wants — the words just don't match literally.

**AI-powered equivalent:** the system embeds the query, compares it against stored vectors, and ranks results by similarity — so "frontend library" correctly surfaces posts about React, Vue, or Angular.

## 🕰️ Why AI Apps Are Emerging Now

AI research isn't new, but three shifts made AI-powered apps mainstream:

1. **Model-as-a-Service (APIs)** — Companies like OpenAI, Google, and Anthropic train and host massive models. Developers no longer need a PhD in ML; calling an LLM is as simple as calling any other web API (prompt in, generated response out).
2. **Hardware (GPUs)** — Parallel processing on modern GPUs made training and real-time inference fast enough for practical use, enabling chatbots, coding assistants, and image generators to respond in seconds.
3. **Developer Tooling (DX)** — A tooling ecosystem now exists specifically for AI apps (see Glossary below), mirroring how React/Angular/Vue simplified web development a decade ago.

## 📖 Glossary of Core Terms

- **Semantic search** — Search based on meaning/similarity rather than exact keyword matches
- **Embedding** — A numeric vector representation of text (or other data) capturing its meaning
- **Vector database** — A database (e.g., Pinecone) optimized for storing embeddings and retrieving semantically similar items — acts as "long-term memory" for AI apps
- **LLM (Large Language Model)** — A model trained on huge text corpora that generates or predicts text
- **LangChain** — A framework that "glues" together the steps of an AI app — input handling, retrieval, prompting, LLM calls, and output formatting
- **Vercel AI SDK** — A toolkit that bridges AI backends and UIs, notably enabling streamed (word-by-word) responses
- **Streaming** — Displaying model output incrementally as it's generated, instead of waiting for the full response
- **Hallucination** — When a model generates plausible-sounding but incorrect or fabricated output
- **Inference** — Running a trained model to produce a prediction or output (as opposed to training it)

## 🌍 Real-World Examples

- **Code assistants** — predict likely next code from context (imports, function names, comments); great for boilerplate, risky for security/payment/auth logic.
- **Recommendation systems** — learn from watch time, likes, and skips to personalize feeds (e.g., social media).
- **Ride-hailing (Uber/Lyft/Meter Taxi)** — AI-driven pricing, routing, and rider–driver matching based on demand, traffic, and location data.

## 🧭 Guiding Principle

> Never accept code (or output) you cannot explain in your own words. AI is a co-pilot, not the captain — like GPS, it's powerful, but if it fails and you can't read the map yourself, you're stuck.

---
*Based on course notes: "The Rise of AI-Powered Applications."*