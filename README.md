Name: Priyanka Chaurasiya  
USN:1CR25AI088  
Project Title: AI-Based Research-Paper Summarization System  

## 🛠️ System Specifications & Requirements

### 1. Hardware Requirements
* **Processor:** Intel Core i5/i7 (8th Gen or above) or AMD Ryzen 5/7. (NVIDIA GPU with CUDA support recommended for local inference).
* **RAM:** Minimum 8 GB (16 GB recommended for handling heavy Transformer models).
* **Storage:** Minimum 10 GB of free solid-state drive (SSD) space for dependency installations and local model caching.

### 2. Software Requirements
* **Operating System:** Windows 10/11, macOS, or Linux (Ubuntu 20.04+).
* **Language Environment:** Python 3.9 or higher.
* **Core Libraries:** Hugging Face `transformers`, `torch` or `tensorflow`, `PyPDF2` / `pdfplumber` (for text extraction), `sentence-transformers`.
* **Deployment/UI Framework:** Streamlit, Gradio, or FastAPI.

### 3. AI & Model Specifications
* **Architecture:** Transformer-based Encoder-Decoder architecture.
* **Core Models:** Fine-tuned `BART-large-CNN` or `T5-base` for abstractive summarization.
* **Embedding Model:** `all-MiniLM-L6-v2` for semantic chunking and key phrase ranking.
* **Context Window:** Handles papers up to 1024 to 2048 tokens per text chunk.

---

## 📋 Functional & Security Specifications

### 1. Functional Specification
* **Document Ingestion:** Accepts single or multiple PDF file uploads or direct web URLs.
* **Text Preprocessing:** Automated tokenization, removal of non-text artifacts (headers, footers, equations), and structural sectioning (Abstract, Methodology, Results).
* **Dual Summarization Modes:** * *Extractive:* Highlighting critical key sentences directly from the text.
  * *Abstractive:* Generating novel, human-like summaries of dense concepts.
* **Keyphrase Extraction:** Identification of core technical keywords using TF-IDF or TextRank algorithms.

### 2. Security Specification
* **Data Privacy:** Local execution mode available to ensure uploaded intellectual property/research papers are not leaked to external APIs.
* **Input Validation:** Strict file type validation (`.pdf`, `.txt`) to prevent malicious script injection or buffer overflow attacks via modified PDF structures.
* **Secure Session Handling:** Clear system memory caches after user sessions expire to ensure no local storage build-up of proprietary data.
---

## 🎯 Expected Output

When a user processes a document, the system generates a clean, multi-tabbed interface dashboard containing:
1. **Executive Summary:** A concise 3-5 sentence overview of the entire paper.
2. **Structural Breakdown:** * **Objective:** What problem the paper solves.
   * **Methodology:** The AI/Engineering approach used.
   * **Results:** Major metrics or key breakthroughs achieved.
3. **Keywords & Themes:** A visual tag-cloud or table listing the top 10 foundational concepts found in the document.
---
## 🔍 Mini-Specification Line (Example)
> **Req-ID: SRS-SUM-04** | **Module:** Summary Generator | **Input:** Standardized Text Chunks | **Process:** Abstractive Pipeline Transformation via BART Model | **Output:** 250-word structured text summary containing primary methodology and conclusions.

**Github Link:** [AI-Based-Research-paper-Summarization-System](https://github.com/priyankaaiml25-hub/AI-Based-Research-paper-Summarization-System)

   
