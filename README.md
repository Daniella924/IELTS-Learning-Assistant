# 🌟 IELTS Learning Assistant System 🌟
Enhanced RAG System with Dynamic Relevance Assessment for IELTS Preparation.

## 📚 Project Overview
IELTS Learning Assistant System is an intelligent learning assistant based on enhanced Retrieval-Augmented Generation (RAG) technology, specifically designed for IELTS candidates. Through dynamic relevance assessment mechanisms, the system can provide highly relevant learning resources and personalized feedback to help users prepare efficiently.

## 🧩 System Architecture
The system consists of three main parts:

### 1. 📝 Preprocessing Stage (Offline)
- **Text Data Collection**: Integrates IELTS textbooks and learning resources 📖

- **Sentence Segmentation**: Uses spaCy to divide text into semantic chunks of 10 sentences 🧠

- **Embedding Generation**: Uses all-mpnet-base-v2 model to generate 768-dimensional vector representations 🔢

- **Vector Storage**: Saves vector data in CSV format 💾

### 2. ⚙️ Main Processing Flow
- **User Query**: Receives user questions 📩

- **Vector Retrieval**: Retrieves relevant content based on dot product similarity 🔍

- **Relevant Content Extractio**n: Gets Top-5 relevant semantic chunks 🥇

- **Relevance Assessment**: Uses 0.65 threshold to evaluate content relevance 🔑

- **LLM Generation**: Uses Gemma-2b-it model to generate responses 🤖

- **Result Display**: Presents answers and related context 💡

### 3. 🎯 Additional Features
- **Writing Evaluation**: Evaluates and improves IELTS essays ✍️

- **Study Plan**: Generates personalized learning roadmap 🗺️

- **Mock Tests**: Provides IELTS practice tests 📝

- **Text-to-Speech**: Uses MMS-TTS-Eng to convert text to speech 🔊

- **Progress Tracking**: Records learning progress and provides feedback 📊

## 🚀 Technical Highlights
- **Dynamic Relevance Assessmen**t: Adjusts response strategy dynamically based on 0.65 threshold 🎯

- **Precise Corpus Chunking**: 10-sentence chunking strategy balances context and precision 🔄

- **Lightweight Model Selectio**n: Uses Gemma-2b-it to balance speed and quality ⚡

- **Multimodal Interaction**: Combines text and speech features to support various learning methods 🗣️

- **Learning Loop Design**: Optimizes study plans through progress tracking feedback 🔁

## 📦 Installation Instructions
### 🖥️ Environment Requirements
- Python 3.8+
- PyTorch 1.12+
- Transformers 4.26+
- spaCy 3.5+

### Installation Steps
Clone repository:
    ```bash
    git clone https://github.com/您的用户名/ielts-learning-assistant.git
    cd ielts-learning-assistant
    ```

Install dependencies:
    ```bash
    pip install -r requirements.txt
    python -m spacy download en_core_web_sm
    ```  

Download necessary models:
    ```bash
    python download_models.py
    ```
    
### 🚀 Usage
#### 1. 🛠️ Preprocess Data
```bash
python preprocessing/run_preprocessing.py --input_dir data/sample_texts --output_dir data/embeddings
```
#### 2. 🖥️ Start System
```bash
python main.py
``` 
Access http://localhost:5000 to use web interface

#### 3. 🔧 API Usage Example
```bash
from core.api import IELTSAssistant  
assistant = IELTSAssistant()  
response = assistant.ask("如何提高IELTS写作分数?")  
print(response)  
```  

### 📂 Project Structure
ielts-learning-assistant/  
├── preprocessing/     
├── core/                
├── features/             
├── ui/                    
├── data/             
├── models/             
├── requirements.txt     
└── main.py          

### 👨‍💻 Team Information
• LEO
• RAY
• Daniella

### 📝 License
MIT

### 🙏 Acknowledgments
Thanks to SentenceTransformer, Google Gemma and Facebook MMS-TTS-Eng for technical support.
