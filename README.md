# Krishivaani

KrishiVaani is a curated conversational Hindi speech dataset designed to tackle the challenges of Automatic Speech Recognition (ASR) in real-world settings, particularly in agriculture. It captures diverse accents, linguistic variations, and domain-specific vocabulary, making it highly relevant for low-resource language research. The dataset also supports downstream tasks like ASR post-correction and validation.

---

## 📁 Repository Structure

### 🔹 ChatGPT/

This directory explores zero-shot and few-shot prompting strategies using ChatGPT for hypothesis correction. It contains three primary subfolders:

- `Known/`
- `Unknown/`
- `OOD/` *(Out-of-Domain)*

Each of these contains:
- `noshot/`
- `oneshot/`
- `threeshot/`
- `sevenshot/`

The shots are selected randomly from the IndicVoice dataset.

Additionally, each of the `Known`, `Unknown`, and `OOD` folders includes:
- `sonar/`  
- `sbert/`  

These folders use **embedding-based similarity** (via Sonar and SBERT) to select:
- `oneshot/`
- `threeshot/`
- `fiveshot/`
- `sevenshot/`

This setup allows comparison between random and semantically selected prompts.

---

### 🔹 Dataset/

This directory contains the core audio and transcription data used for training and evaluation.

#### Structure:
- `Test/`
  - `Known/`
  - `Unknown/`
  - `OOD/`

Each of the above test subsets contains:
- `Audio/`
- `Transcripts/`

- `Train/V2/`
  - `Audio/`
  - `Transcripts/`

The dataset follows a clean and categorized format to facilitate structured evaluation across different data types.

---

### 🔹 LM/ (Language Model Inferences)

This directory contains inference results from the **KVWav2Vec2** model for computing **Word Error Rates (WER)**.

Subfolders:
- `Known/`
- `Unknown/`
- `OOD/`

Each folder stores model inferences corresponding to that data type, used for baseline ASR performance analysis.

---
