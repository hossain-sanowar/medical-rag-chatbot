# 🏥 Medical RAG Chatbot

A production-ready **Retrieval-Augmented Generation (RAG)** chatbot for medical document question answering using **LangChain, FAISS, Flask, Docker, Jenkins, Trivy, and AWS App Runner**.

---

## 📌 Overview
This project builds an end-to-end **LLMOps pipeline**:
- Ingest medical documents (PDFs)
- Create embeddings
- Store in FAISS vector DB
- Retrieve relevant context
- Generate answers using LLMs
- Deploy via CI/CD pipeline to AWS

---

## 🧰 Tools & Technologies
- Python
- LangChain
- FAISS
- Hugging Face
- Flask
- Docker
- Jenkins (CI/CD)
- Trivy (Security scanning)
- AWS ECR & App Runner

---

## 🖼️ Architecture

### 🔧 Tools Overview
![Tools Overview](docs/medical_chatbot_tools_overview.png)

### 🔄 Workflow
![Workflow](docs/medical_chatbot_workflow.png)

---

## ⚙️ Setup Instructions

### 1️⃣ Clone Repository
```bash
git clone https://github.com/data-guru0/LLMOPS-2-TESTING-MEDICAL.git
cd LLMOPS-2-TESTING-MEDICAL
```

### 2️⃣ Create Virtual Environment
```bash
python -m venv venv
venv\Scripts\activate   # Windows
```

### 3️⃣ Install Dependencies
```bash
pip install -e .
```

### 4️⃣ Run Locally
```bash
python app/main.py
```

---

## 🔐 Environment Variables
Create `.env` file:

```env
HF_TOKEN=your_huggingface_token
HUGGINGFACEHUB_API_TOKEN=your_token
```

---

## 🐳 Docker

### Build Image
```bash
docker build -t medical-rag-chatbot .
```

### Run Container
```bash
docker run -p 5000:5000 medical-rag-chatbot
```

---

## 🚀 CI/CD Pipeline (Jenkins)

### Steps
1. Setup Jenkins (Docker)
2. Connect GitHub
3. Add Jenkinsfile
4. Build pipeline

### Pipeline Stages
- Checkout
- Build Docker Image
- Trivy Scan
- Push to AWS ECR
- Deploy to App Runner

---

## 🔍 Security (Trivy Scan)
```bash
trivy image medical-rag-chatbot
```

---

## ☁️ AWS Deployment

### Services Used
- AWS ECR (Image Registry)
- AWS App Runner (Deployment)

### Steps
1. Create ECR repo
2. Push image from Jenkins
3. Deploy via App Runner
4. Add environment variables

---

## 📊 Features
- Document-based QA
- Fast retrieval (<2s)
- Scalable deployment
- Secure CI/CD pipeline

---

## 🧹 Cleanup
```bash
docker system prune -a -f
```

---

## 👨‍💻 Author
**Md Sanowar Hossain**
