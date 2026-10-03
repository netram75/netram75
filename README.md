# Hi, I'm Netram 👋

I build machine learning systems and the software around them: data pipelines, model evaluation, and production backends.

- 💼 **MTS Intern at Evaratus** (formerly Scaler AI Labs), working on data pipelines and ML evaluation
- 🎓 Computer Science at Scaler School of Technology and BITS Pilani
- 🔍 I like finding where models fail and building the tests that catch it

## 🛠️ Software engineering

- **114 merged PRs (~140K lines)** to production codebases at work (private repos)
- Built **25 data pipelines** from real-world APIs (GA4, DocuSign, Dropbox, Razorpay and more), handling rate limits, pagination and silent data loss
- Scaled a detection and masking pipeline to **50+ TB** of data on a distributed **Ray** fleet (AWS EC2, S3, GCS)
- **32 merged open source PRs:**
  [22 in SugarLabs Music Blocks](https://github.com/sugarlabs/musicblocks/pulls?q=is%3Apr+author%3Anetram75+is%3Amerged) ·
  [9 in Red Hat's krkn-chaos (CNCF)](https://github.com/search?q=org%3Akrkn-chaos+author%3Anetram75+is%3Apr+is%3Amerged&type=pullrequests) ·
  [1 in OWASP Nest](https://github.com/OWASP/Nest/pulls?q=is%3Apr+author%3Anetram75+is%3Amerged)

## 🤖 Machine learning and evaluation

- **Error analysis of an NER-based PII detector:** grouped false positives into 4 error classes and fixed each one, cutting them from **675K to 99**
- Built **LLM-as-judge validation** that decides whether a flagged value is real PII, and measured precision on real data
- **16th of 78 finalist teams** (from 103) at ANRF AISEHack (IIIT Hyderabad, IBM): flood segmentation from satellite imagery
- **Kaggle Expert**

## 📌 Featured projects

| Project | What it does | Stack |
|---|---|---|
| [Flood segmentation](https://github.com/netram75/aisehack-flood-segmentation) | 3-class segmentation on 8-channel SAR + optical imagery. CE + Dice + Boundary loss, 32x patch sampling on 59 images, 5 controlled experiments (0.170 → 0.1845) | PyTorch, ResNet34-UNet, OpenCV |
| [PDF-Agent](https://github.com/netram75/PDF-Agent) | RAG agent that answers only from the uploaded PDF, with two-stage refusal, page citations, multilingual support and an automated eval suite | Python, LLMs, RAG |
| [ai-agent-cli](https://github.com/netram75/ai-agent-cli) | Autonomous CLI agent with a ReAct reasoning loop and tool use | Node.js, Groq |
| [krkn-docs-sync](https://github.com/netram75/-krkn-docs-sync) | GitHub Actions bot that detects krkn-chaos scenario changes and opens documentation PRs automatically | Python, GitHub Actions |
| [Credit card fraud](https://github.com/netram75/credit-card-fraud-xgboost) | 284K transactions, 0.17% fraud. Judged by precision and recall, not accuracy: ROC-AUC 0.979, fraud F1 0.86 | XGBoost, scikit-learn, pandas |
| [CIFAR-10 ablation](https://github.com/netram75/cifar10-cnn-image-classification) | Ablation study: 75% → 78% (augmentation) → 80.8% (batch norm), with confusion-matrix error analysis | TensorFlow/Keras |

## 🧰 Tech stack

**Languages**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![C++](https://img.shields.io/badge/C%2B%2B-00599C?style=flat&logo=cplusplus&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat&logo=openjdk&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat&logo=mysql&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)

**Web and backend**

![React](https://img.shields.io/badge/React-20232A?style=flat&logo=react&logoColor=61DAFB)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat&logo=nodedotjs&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)
![REST APIs](https://img.shields.io/badge/REST%20APIs-555555?style=flat)

**Machine learning and data**

![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-150458?style=flat&logo=pandas&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat&logo=scikitlearn&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-189FDD?style=flat)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=flat)
![Seaborn](https://img.shields.io/badge/Seaborn-4C72B0?style=flat)

**Deep learning and GenAI**

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat&logo=pytorch&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat&logo=tensorflow&logoColor=white)
![Keras](https://img.shields.io/badge/Keras-D00000?style=flat&logo=keras&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat&logo=opencv&logoColor=white)
![LLMs](https://img.shields.io/badge/LLMs-4B0082?style=flat)
![RAG](https://img.shields.io/badge/RAG-4B0082?style=flat)
![LLM as judge](https://img.shields.io/badge/LLM--as--judge-4B0082?style=flat)
![FAISS](https://img.shields.io/badge/FAISS-0467DF?style=flat)
![ChromaDB](https://img.shields.io/badge/ChromaDB-FF6446?style=flat)

**Cloud, infra and data stores**

![AWS](https://img.shields.io/badge/AWS%20(EC2%2C%20S3)-232F3E?style=flat&logo=amazonwebservices&logoColor=white)
![Google Cloud Storage](https://img.shields.io/badge/GCS-4285F4?style=flat&logo=googlecloud&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![Ray](https://img.shields.io/badge/Ray-028CF0?style=flat&logo=ray&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat&logo=githubactions&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat&logo=linux&logoColor=black)
![Git](https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat&logo=mysql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat&logo=mongodb&logoColor=white)

**Evaluation:** precision, recall, F1, ROC-AUC, Dice/IoU, ablations, error analysis, class imbalance

## 🏆 Achievements

- **16th of 78 finalists** (from 103 teams), ANRF AISEHack (IIIT Hyderabad, IBM)
- **3rd of 67 teams**, AuraVerse 2.0 hackathon
- **9th in the finals**, Synapse national hackathon
- **Kaggle Expert**

## 📫 Connect

[LinkedIn](https://linkedin.com/in/netramfaran) · [Kaggle](https://www.kaggle.com/netramfaran)
