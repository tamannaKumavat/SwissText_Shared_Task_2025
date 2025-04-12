# SwissTEXT 2025 Shared Task – Stage 3: RAG System for Cleantech QA

This repository contains our solution for Stage 3 of the SwissTEXT 2025 Shared Task:  
**"Accelerating Cleantech Advancements through NLP-powered Text Mining and Knowledge Extraction"**.

## 🧠 Goal

Our team focuses on implementing a RAG-based QA system that extracts insights from cleantech media and patent datasets. We worked on:

- Generating and categorizing QA pairs using LLMs
- Testing and evaluating the baseline RAG system
- Proposing enhancements based on current research

## 📂 Project Structure

We provide three Jupyter notebooks to cover the three main stages of our work:

### 1. QA Pair Generation and Categorization  
🔗 [QA_Pairs.ipynb](./QA_Pairs.ipynb)

- We manually selected cleantech-related topics and split both the Cleantech Media and Patent datasets accordingly.
- Used **LLaMA 3.2 Instruct** to generate QA pairs from selected paragraphs.
- Categorized QA pairs using **BERT-based keyword matching**:

- To better structure and evaluate the generated QA pairs, we defined five categories that reflect major themes in cleantech research and innovation:

    - Factual Questions
    Aim to extract specific pieces of information such as dates, names, locations, or facts. They typically begin with “what,” “when,” “where,” “who,” or “which.”

    - Comparative & Market Analysis Questions
    Focus on comparing technologies, market dynamics, and identifying trends. These questions often include terms like “compare,” “market,” “trend,” or “analysis.”

    - Analytical & Explanatory Questions
    Explore causes, mechanisms, or effects. They are framed with “why,” “how,” or “explain” and are designed to prompt deeper understanding or insight.

    - Government & Corporate Initiatives
    Target the role of policy, regulation, and organizational strategies in cleantech. These questions touch on governance, policies, corporate programs, or regulatory efforts.

    - Sustainability & Technological Innovation Questions
    Highlight advancements and their environmental implications, covering topics such as renewable energy, sustainable technologies, and eco-friendly solutions.

- We evaluated these QA pairs using **Critique Agents** based on three key criteria:
    - **Groundedness**: Is the answer clearly derivable from the paragraph?
    - **Relevance**: Is the question useful in the cleantech NLP context?
    - **Standalone Clarity**: Is the question understandable without context?

### 2. Baseline RAG Evaluation  
🔗 [cleantech_rag.ipynb](cleantech_rag.ipynb)

- Used the tutorial implementation from [Prof. Dr. Daniel Perruchoud](https://github.com/LuciferUchiha/Cleantech-RAG).
- Evaluated the RAG system on both the seed dataset and our generated QA pairs.
- Assessed the system performance based on question category and content relevance.

### 3. RAG System Improvements  
🔗 [RAG_Enhancements.ipynb](./RAG_Enhancements.ipynb)

We propose and/or implemented several enhancements:

- **Alternative Embeddings**: Use **PatentSBERTa** for better domain adaptation.
- **Query Reformulation**: Bridge user question phrasing and document expression gaps.
- **Recursive Chunking**: Chunking at the token level instead of characters.
- **Hybrid Retrieval + Re-ranking**:
    - Combine dense semantic search with BM25 lexical search.
    - Merge top-k results using **Reciprocal Rank Fusion**.

## 📅 Timeline

- **Task Released**: 1st February 2025  
- **Submission Deadline**: 30th April 2025  
- **Organizers**: Guang Lu (HSLU), Susie Xi Rao & Noah Mamie (ETHZ), Janna Lipenkova (Equintel)

## 📫 Contact

For questions about our solution or this repo, feel free to open an issue or contact us.

---

_This project contributes toward cleantech innovation and supports environmental sustainability through AI and NLP research._