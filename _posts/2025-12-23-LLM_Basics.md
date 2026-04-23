# LLM Basics

## 1. What is an LLM?
**LLM (Large Language Model)** is an AI trained on huge amounts of text to understand and generate human-like text.

### What it can do
- Answer questions  
- Summarize text  
- Translate languages  
- Write code and content  

### How it works

---

## 2. What is a Token?
**token** is a small piece of text the model reads.

### Examples
- `"Hello"` → 1 token  
- `"ChatGPT"` → 2 tokens (`Chat` + `GPT`)  
- `"I love AI!"` → 4 tokens  

### Rule of thumb
- 1 token ≈ 4 characters  
- 1 token ≈ ¾ of a word  

### Why tokens matter
- API cost is based on tokens  
- Models have max token limits  
- Total cost = input tokens + output tokens  

---

## 3. OpenAI Model Comparison (2025)

Choosing the right model depends on **reasoning depth, speed, and cost**.

| Model Family | Best For | Context Window | Key Highlight |
|-------------|--------|---------------|---------------|
| o1-series | Complex math, coding, science | 128K+ | Strong reasoning (chain-of-thought) |
| GPT-5 | Advanced reasoning, massive data | 400K | Largest context, highest intelligence |
| GPT-4o | General multimodal use | 128K | Best balance of speed & intelligence |
| GPT-4 Turbo | Long document analysis | 128K | Enterprise reliability |
| GPT-3.5 Turbo | Simple, cheap tasks | 16K | Very fast, legacy support |

---

## 4. Model Limits – Key Terms
- **Model**: Which LLM you use  
- **Context window**: Max input + output tokens  
- **Max output tokens**: Maximum response size  
- **Knowledge cutoff**: Last training date  

### Important rule
If input is large → output must be smaller.

---

## 5. Rate Limiting (TPM)
**TPM = Tokens Per Minute**

- Counts input + output tokens  
- Limit resets every minute  

### If limit is exceeded
- API returns **429 error**
- Request is blocked  

### Best practices
- Track token usage  
- Retry after delay  
- Split large jobs  

---

## 6. Temperature & Top-P
These control **randomness and creativity**.

### Temperature (0 – 2)
- Low → accurate, repeatable  
- High → creative, varied  

**Recommended usage**
- Code / facts → `0.0 – 0.3`  
- General → `0.5 – 0.8`  
- Creative → `0.8 – 1.5`  

### Top-P (0 – 1)
- Limits word choices to the most likely ones  
- Lower → safer answers  
- Higher → more variety  

---

## 7. Types of Models

### Reasoning Models (o1 series)
- Better thinking and planning  
- Slower and more expensive  
- Best for math, logic, complex code  

### GPT Models
- Fast and cost-effective  
- Good for chat, writing, summaries  

### Large vs Mini Models
- **Large** → smarter, slower, costly  
- **Mini** → faster, cheaper, less accurate  

---

## 8. Prompt Engineering (Simple Rules)
**Prompt engineering = how you ask the model**

### Best practices
- Be clear and direct  
- Say what you want (not what you don’t)  
- Specify output format  
- Break big tasks into small ones  

**Example**

Summarize this in 3 bullet points.
## 9. Prompt Authority (Who Wins)

Order of importance:

1. **System** (platform rules)
2. **Developer** (app rules)
3. **User** (your prompt)
4. **Guidelines** (suggestions)
5. **Assistant output** (no authority)

> Higher-level rules **cannot be overridden** by lower-level ones.

---

## 10. Zero-Shot vs Few-Shot

### Zero-Shot
- No examples  
- Simple tasks  
- Fast  

### Few-Shot
- 2–5 examples  
- Complex or strict formatting  
- More reliable output  

---

## 11. AI Stack (Big Picture)

### 4 Layers
1. **Application** – UI, chatbot, app  
2. **Model & Orchestration** – LLMs, agents, workflows  
3. **Infrastructure** – APIs, cloud, GPUs  
4. **Data** – databases, embeddings, RAG  

## Typical flow

User → App → Data (RAG) → LLM → Response

## One-Line Summary
- LLMs work on **tokens**  
- Cost and limits depend on tokens  
- Temperature & Top-P control randomness  
- Model choice balances speed, cost, and intelligence  
- Clear prompts give better results  
- AI apps use **Application + Model + Infrastructure + Data**
