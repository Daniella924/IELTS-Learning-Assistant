# 🌟 IELTS Learning Assistant System 🌟
Enhanced RAG System with Dynamic Relevance Assessment for IELTS Preparation.

## 📚 项目概述
IELTS Learning Assistant System 是一个智能学习助手，基于增强检索增强生成（RAG）技术，专为IELTS考生设计。通过动态相关性评估机制，系统能够提供高度相关的学习资源和个性化反馈，帮助用户高效备考。

## 🧩 系统架构
系统分为三个主要部分：

### 1. 📝 预处理阶段（离线）
- **文本数据收集**：整合IELTS教材和学习资源 📖
- **句子分割**：使用spaCy将文本分割为10句话的语义块 🧠
- **嵌入生成**：使用all-mpnet-base-v2模型生成768维向量表示 🔢
- **向量存储**：以CSV格式保存向量数据 💾

### 2. ⚙️ 主处理流程
- **用户查询**：接收用户问题 📩
- **向量检索**：基于点积相似度检索相关内容 🔍
- **相关内容提取**：获取Top-5相关语义块 🥇
- **相关性评估**：使用0.65阈值评估内容相关性 🔑
- **LLM生成**：使用Gemma-2b-it模型生成回答 🤖
- **结果展示**：呈现答案及相关上下文 💡

### 3. 🎯 附加功能
- **写作评估**：评价和改进IELTS作文 ✍️
- **学习计划**：生成个性化学习路线图 🗺️
- **模拟测试**：提供IELTS模拟试题 📝
- **文本转语音**：使用MMS-TTS-Eng转换文本为语音 🔊
- **进度跟踪**：记录学习进度和提供反馈 📊

## 🚀 技术亮点
- **动态相关性评估**：根据0.65阈值动态调整回答策略 🎯
- **精细化语料分块**：10句话为单位的分块策略平衡上下文和精度 🔄
- **轻量级模型选择**：使用Gemma-2b-it保证速度和质量平衡 ⚡
- **多模态交互**：结合文本和语音功能支持多种学习方式 🗣️
- **学习闭环设计**：通过进度跟踪反馈优化学习计划 🔁

## 📦 安装说明

### 🖥️ 环境要求
- Python 3.8+
- PyTorch 1.12+
- Transformers 4.26+
- spaCy 3.5+

### 安装步骤
1. 克隆仓库：
    ```bash
    git clone https://github.com/您的用户名/ielts-learning-assistant.git
    cd ielts-learning-assistant
    ```
2. 安装依赖：
    ```bash
    pip install -r requirements.txt
    python -m spacy download en_core_web_sm
    ```
3. 下载必要模型：
    ```bash
    python download_models.py
    ```

### 🚀 使用方法

#### 1. 🛠️ 预处理数据
```bash
python preprocessing/run_preprocessing.py --input_dir data/sample_texts --output_dir data/embeddings
```

#### 2. 🖥️ 启动系统
```bash
python main.py
```
访问 http://localhost:5000 使用Web界面

#### 3. 🔧 API使用示例
```bash
from core.api import IELTSAssistant  
assistant = IELTSAssistant()  
response = assistant.ask("如何提高IELTS写作分数?")  
print(response)  
```

### 📂 项目结构
ielts-learning-assistant/  
├── preprocessing/       # 预处理阶段代码  
├── core/                # 主流程代码  
├── features/            # 附加功能代码  
├── ui/                  # 用户界面代码  
├── data/                # 示例数据  
├── models/              # 模型配置  
├── requirements.txt     # 项目依赖  
└── main.py              # 主程序入口  

### 👨‍💻 团队信息
•	LEO
•	RAY
•	Daniella

### 📝 许可证
MIT

### 🙏 致谢
感谢SentenceTransformer、Google Gemma和Facebook MMS-TTS-Eng提供的技术支持。


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
