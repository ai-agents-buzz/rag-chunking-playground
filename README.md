# RAG Chunking Playground

> **Compare 6 chunking strategies side-by-side.** Paste your docs, see exactly how fixed-size, recursive, semantic, and 3 other strategies split them differently—with live quality grades, token counts, and export-ready code.

**[Try the Live Tool](https://aiagentsbuzz.com/tools/rag-chunking-playground/)** | **[Read the Strategy Guide](https://aiagentsbuzz.com/guides/rag-chunking-strategies/)**

![RAG Chunking Strategies Comparison](https://aiagentsbuzz.com/images/rag-chunking-preview.png)

---

## Why This Exists

Most RAG tutorials skip chunking or say "use 512 tokens lol." But **chunking strategy matters!**

We built this because:

- ❌ **Fixed-size** cuts words mid-sentence 
- ❌ **Recursive** orphans headers from content
- ❌ **Semantic** costs 10x more and isn't always better

You need to **SEE** the difference, not guess.

---

## Features

✅ **6 strategies compared:** Fixed, Recursive, Sentence, Markdown, Regex, Semantic (coming soon) 
✅ **Live quality grading:** Green (clean), Yellow (warnings), Red (broken chunks)  
✅ **Visual diff view:** Hover any chunk to highlight it in the doc  
✅ **Cost calculator:** Embedding + context window costs for OpenAI/Cohere  
✅ **Export code:** LangChain, LlamaIndex, Haystack snippets  
✅ **Zero backend:** Runs 100% client-side (except semantic uses OpenAI API)  

---

## Quick Start

### Online (Easiest)
Visit **[aiagentsbuzz.com/tools/rag-chunking-playground](https://aiagentsbuzz.com/tools/rag-chunking-playground/)**

### Run On Your Machine
```bash
git clone https://github.com/ai-agents-buzz/rag-chunking-playground
cd rag-chunking-playground
open index.html
```

No build step. No dependencies. Just open `index.html` in your browser.

---

## How It Works

**Architecture:**
- Pure vanilla JavaScript (no frameworks)
- Tokenization via GPT-3 estimation (1 token ≈ 4 chars)
- All processing happens client-side
- Optional: Semantic chunking via OpenAI Embeddings API

**Strategy Comparison:**

| Strategy | Best For | Downside | Avg Quality |
|----------|----------|----------|-------------|
| **Fixed-size** | Speed, simple docs | Cuts mid-sentence | 🟡 54% |
| **Recursive** | Code, markdown | Complex logic | 🟢 69% |
| **Sentence** | Clean boundaries | Uneven sizes | 🟢 72% |
| **Markdown** | Docs with headers | Requires structure | 🟢 76% |
| **Regex** | Custom patterns | Manual tuning | 🟡 Variable |
| **Semantic** | Topic coherence | Slow + costly | 🟢 87% |

**[Full strategy guide with benchmarks →](https://aiagentsbuzz.com/guides/rag-chunking-strategies/)**

---

## Screenshots


### Document View with Inline Chunks
See exactly where each strategy cuts your text, with hover tooltips
![Document Viewing Window]https://aiagentsbuzz.com/images/screenshot-view-window.png

### Query Retrieval Test
Test which chunks get retrieved for a sample query using BM25 ranking
![Query Test]https://aiagentsbuzz.com/images/screenshot-query-retrieval.png


---

## Real-World Use Cases

**1. Debug why your RAG returns garbage**  
Paste your actual docs → see if chunks break mid-thought

**2. Choose the right strategy for your content**  
Compare on your real data, not synthetic examples

**3. Estimate costs before building**  
See embedding + context costs for 1M docs

**4. Teach/learn RAG fundamentals**  
Visual, interactive beats reading theory

---

## Tech Stack

- **Frontend:** Vanilla JavaScript (no frameworks)
- **Styling:** Custom CSS with glassmorphism effects
- **Fonts:** DM Sans, Fira Code, Caveat
- **PDF Support:** PDF.js
- **Token Counting:** GPT-3 estimation (1 token ≈ 4 chars)
- **Optional:** OpenAI API for semantic chunking

---

## Contributing

Found a bug? Have a new strategy idea? **PRs welcome!**

**Ideas for contributions:**
- [ ] Add Anthropic Claude token counting
- [ ] Support PDF/DOCX upload
- [ ] Add "hybrid" strategy (semantic + recursive)
- [ ] Multilingual support

---

## License

**MIT License** - Created by [AI Agents Buzz](https://aiagentsbuzz.com) • March 2026

**Attribution:** Keep the footer attribution and link back to the original tool.

---

## Learn More

📖 **[Full RAG Chunking Strategy Guide](https://aiagentsbuzz.com/guides/rag-chunking-strategies/)** - 4000+ words with benchmarks, decision framework, and real data  
🧰 **[More AI Tools](https://aiagentsbuzz.com)** - Directory of AI agent tools  
🤖 **[AI Agents Directory](https://aiagentsbuzz.com)** - 300+ AI agents reviewed  

---

## Support

⭐ **Star this repo** if it helped you build better RAG systems!

🐛 **Report issues** in the GitHub Issues tab

---

**Built with ❤️ **