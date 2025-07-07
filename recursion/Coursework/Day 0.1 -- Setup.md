
> [!info] 🚀 AI Engineering Bootcamp – Day 0
> Welcome to **Day 0** of your **AI Engineering Bootcamp**, designed to build your skills from foundational setup to advanced deployable AI systems with a focus on **Responsible AI**.
> 
> Over the next five weeks, you will:
> - Develop production-ready prompt engineering and RAG pipelines  
> - Integrate agentic AI workflows with safety and evaluation guardrails  
> - Build a capstone AI application demonstrating responsible engineering practices
> 
> Today sets the stage for your entire journey by ensuring your **environment is robust, your mindset is aligned with AI safety principles, and your goals are clearly defined**.

## **🗓️ Day 0: Goals**

- Validate your environment (Python, OpenAI, Docker)
- Run a test Docker container (Milvus setup prep)
- Reflect on AI Safety and Responsible AI principles
- Define success criteria for this learning journey

---

## 🛠️ Environment Setup Summary

- [x] **Create project folder:** `daemons/ai_bootcamp`

- [x] **Setup virtual environment:**

```bash
python3 -m venv .venv
source .venv/bin/activate
````

- [x] **Upgrade pip:**

```
pip3 install --upgrade pip
```

- [x] **Install required libraries:**

```
pip3 install openai langchain sentence-transformers milvus pymilvus neo4j fastapi uvicorn docker python-dotenv
```

- [ ] **Validate Python + OpenAI API connectivity** with a test script:

```
from openai import OpenAI

client = OpenAI()

response = client.chat.completions.create(
    model="gpt-3.5-turbo",
    messages=[
        {"role": "system", "content": "You are a helpful assistant."},
        {"role": "user", "content": "Say hello, AI world!"}
    ]
)

print(response.choices[0].message.content)
```

Expected output: “Hello, AI world!” or similar.

- [x] **Test Docker installation:**

```
docker run hello-world
```

Expected output: Confirmation that Docker is installed and running containers.

- [ ] **(Optional) Pull and run Milvus container:**

To prepare for your upcoming RAG module:

```
docker pull milvusdb/milvus:v2.3.0
docker run -d --name milvus-standalone -p 19530:19530 -p 9091:9091 milvusdb/milvus:v2.3.0
docker ps
```

Expected outcome: A container named milvus-standalone is running.

- [ ] **Confirm VSCode extensions installed:** Python, Docker, Jupyter
