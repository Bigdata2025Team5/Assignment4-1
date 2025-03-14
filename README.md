# Assignment4


## Links 
Codelabs : https://codelabs-preview.appspot.com/?file_id=1ibR7swpZmM5--BO9HV6jA_pQWA80h_mt2lWQlNWOzMw#0

Front-end (Stremlit): https://damgassignment4-dvnn8diaea6xjifv7hfxbp.streamlit.app/

Back-end (Fast-api): https://api-695260164759.us-central1.run.app

---

## 📌 Problem Statement
The use of digital documentation increases, users frequently encounter difficulties effectively retrieving and analyzing data from sizable PDF files. Manual reading, searching, and summarization are necessary for traditional methods, which are laborious, ineffective, non-scalable, and challenging to implement. We suggest a Streamlit-based web application that makes use of Large Language Models (LLMs) through FastAPI and LiteLLM in order to overcome these difficulties. Information retrieval will be smooth and effective because of this system's ability to automate document summaries and enable natural language querying.

---

## 🛠️ Technology Used

[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/)
[![FastAPI](https://img.shields.io/badge/fastapi-109989?style=for-the-badge&logo=FASTAPI&logoColor=white)](https://fastapi.tiangolo.com/)
[![Amazon AWS](https://img.shields.io/badge/Amazon_AWS-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white)](https://aws.amazon.com/)
[![Python](https://img.shields.io/badge/Python-FFD43B?style=for-the-badge&logo=python&logoColor=blue)](https://www.python.org/)
[![Docker](https://img.shields.io/badge/Docker-%232496ED?style=for-the-badge&logo=Docker&color=blue&logoColor=white)](https://www.docker.com)
[![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=Streamlit&logoColor=white)](https://streamlit.io/)
[![Google Cloud](https://img.shields.io/badge/Google_Cloud-%234285F4.svg?style=for-the-badge&logo=google-cloud&logoColor=white)](https://cloud.google.com)
---

## 🏗️ Architecture Diagram
![AI Application Data Pipeline](https://github.com/Bigdata2025Team5/Assignment4/blob/main/Architecture_Diagram/ai_application_data_pipeline_llms.png?raw=true)

---

## 🔑 Features & How to Run Locally
Step 1: Clone the Repository
Open a terminal or command prompt.
Run the following command to clone the repository:
git clone <repository_url>
cd Assignment_4

Step 2: Create a Virtual Environment
Create and activate a virtual environment:
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

Step 3: Install Dependencies
Install the required dependencies:
pip install -r requirements.txt

Step 4: Configure Environment Variables
Create a .env file in the root directory.
Add required credentials such as API keys for AWS, LLM’s (GPT-4o, Gemini, Claude, Grok, Deepseek), etc.
AWS_ACCESS_KEY=<your_access_key>
AWS_SECRET_KEY=<your_secret_key>

Step 5: Run the Redis Server
Start the Redis Server
docker run -d --name redis -p 6379:6379 redis:latest
The successful output should show “Redis”
docker start redis

Step 6: Run the Backend Server
Start the FastAPI backend server:
uvicorn backend.app:app --reload
The API will be available at http://127.0.0.1:8000.

Step 7: Run the Frontend Dashboard
Start the Streamlit dashboard:
streamlit run frontend/dashboard.py
Open the displayed local URL to access the dashboard.

Step 8: Use the Application
Choose an LLM Model: Select an LLM model (e.g., GPT-4, Gemini, Claude) to use for summarization and Q&A.
Upload a PDF or Enter a URL: Upload a PDF file or enter a website URL, then click "Process" to extract text and structured content.
Summarize the Document: Click "Summarize" to generate and display a summary of the extracted content.
Ask Questions on the Document: Enter a question, click "Ask Question," and view the AI-generated response.
View Token Usage & Cost: Check token usage, cost per token, and total processing cost for each request.
Download Processed Data: Select a processed document and click "Download Markdown" to retrieve the extracted content.
View Logs & Task Status: Monitor the processing status of summarization and Q&A tasks, and wait for results if still processing.

---

## 📂 Project Structure
```
├── Architecture_Diagram
│   └── ArchitectureDiagram_Ass4.ipynb
    ├── ai_application_data_pipeline_llm.png
├── POC
│   ├── Streamlitpoc.py
│   ├── docker-compose.yml
├── api
│   ├── Dockerfile
│   ├── main.py
│   ├── openSourcePdf.py
│   ├── requirements.txt
├── app
│   ├── Dockerfile
│   ├── app.py
│   ├── requirements.txt
├── worker
│   ├── Dockerfile
│   ├── worker.py
│   ├── requirements.txt
├── AiDisclosure.md
├── README.md

```

---
## References

- https://pymupdf.readthedocs.io/
- https://aws.amazon.com/s3/
- https://platform.openai.com/docs/guides/gpt/gpt-models
- https://docs.aimlapi.com/api-references/text-models-llm/google/gemini-2.0-flash-exp
- https://api-docs.deepseek.com/
- https://docs.anthropic.com/en/docs/welcome
- https://docs.x.ai/docs/tutorial

---

## 👥 Team Information
| Name            | Student ID    | Contribution |
|----------------|--------------|--------------|
| **Pranjal Mahajan** | 002375449  | 33.33% |
| **Srushti Patil**  | 002345025  | 33.33% |
| **Ram Putcha**  | 002304724  | 33.33% |

---
