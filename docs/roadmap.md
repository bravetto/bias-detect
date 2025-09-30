# Roadmap

The goal of this project is to build a lightweight module that can detect bias in sentences **while being context-aware**, without relying on heavy ML models or external APIs.  
The solution should run fully offline and work in environments like Chrome and VS Code extensions.

---

## Phase 1 – Core Pattern Detection (Baseline)
- Implement `detectBias(text)` with a simple keyword/regex list.  
- Categorize bias patterns (e.g., gender, age, race, appearance, disability).  
- Ensure the module runs in browser environments without Node.js dependencies.  

---

## Phase 2 – Context-Aware Parsing
- Add lightweight syntactic analysis (subject, verb, adjective).  
- Detect when bias words are applied to **people** vs neutral objects.  
  - Example: `"She is emotional"` → biased.  
  - Example: `"The movie is emotional"` → neutral.  
- Build a minimal parser or use small grammar-based heuristics.  

---

## Phase 3 – Hybrid Rules + Micro NLP
- Expand detection rules beyond raw keywords:
  - Only flag adjectives when modifying human subjects.  
  - Detect intensifiers like “too”, “overly”, “not enough” that signal bias.  
- Optionally integrate **very small pre-computed embeddings or vectors** (few MB) for distinguishing biased vs neutral contexts.  
- Keep the model lightweight enough for extensions (< 20 MB target). 
- Detect Bias from AST.

---

## Phase 4 – Integration & Extensibility
- Provide a simple **API** (`detectBias(text)`) for developers to embed in their own apps.  
- Add configuration options:
  - Custom bias word lists.  
  - Strict vs lenient detection modes.  

---

## Guiding Principles
- **Offline-first**: No reliance on external APIs.  
- **Lightweight**: No heavy ML models like BERT.  
- **Context-aware**: Avoid false positives by analyzing grammar and context.  
- **Extensible**: Designed to grow with community contributions.  
