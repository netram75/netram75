# Hi, I'm Netram 👋

I build backend and distributed data systems in Python, then try to break them to see how they fail.

- 💼 **MTS Intern at Evaratus** (formerly Scaler AI Labs): data export pipelines, a PII masking pipeline on Ray, and the CI that tests it
- 🎓 Computer Science at Scaler School of Technology and BITS Pilani
- 🔍 I like finding where systems fail and building the tests that catch it

## 🛠️ At work

The repos are private, so here is what the work did:

- **At least 3.5x faster masking:** replaced five fixed-time batches with one continuous work queue. On the same 1 TB, 10.3M-file test and 100 machines, it masked more data in 6.25 h than the old design did in 21.7 h
- Tuned and unblocked production PII runs that peaked at **74 TB/day** on ~1,160 EC2 nodes and ~16K Ray workers
- Fixed exports that **reported success with missing data**, including a heartbeat bug that showed a BigQuery restart as complete at 47%
- Merged **25 API integrations** in async Python (DocuSign, GA4, Dropbox, Razorpay, Microsoft Graph), kept inside customer API quotas with layered rate limiting. A 350K-record GitLab export hit zero 429s
- Built a **GitHub Actions check** that runs the real PII pipeline on a temporary Ray cluster in AWS for every PII PR, compares it with main and scores it against labelled data
- **Error analysis on a PII detector:** grouped false positives into 4 error classes and fixed each one, cutting them from **675K to 99**, and built an LLM-as-judge check that decides whether a flagged value is real PII

## 📌 Featured projects

**Systems**

| Project | What it does | Stack |
|---|---|---|
| [faultline](https://github.com/netram75/faultline) | A replicated key-value store built from scratch with only the standard library: an LSM storage engine, Raft (pre-vote, ReadIndex, snapshots) and a Redis-protocol server. Tested by breaking it: a seeded fault simulator, `kill -9` chaos runs and a linearizability checker over every answer clients got. Power-cut tests caught a log-compaction bug that could lose committed entries | Python, asyncio, Raft, Docker |
| [krkn-docs-sync](https://github.com/netram75/-krkn-docs-sync) | GitHub Actions bot that detects krkn-chaos scenario changes and opens documentation PRs automatically | Python, GitHub Actions |

**ML challenges and evals**

| Project | What it does | Stack |
|---|---|---|
| [first-domino](https://github.com/netram75/first-domino) | Find the service that started an outage in systems of 15 to 40 services, from metrics and the call graph. Simulator, grader, baselines and a reference model: **0.784 MAP@3** vs 0.309 for the best baseline. Version 1 was too easy for an AI coding agent, so version 2 is harder. [Kaggle](https://www.kaggle.com/datasets/netramfaran/first-domino-root-cause-incidents) | scikit-learn, pandas, NumPy |
| [real-or-decoy](https://github.com/netram75/real-or-decoy) | Find the real phone and bank account numbers in messy logs and ignore lookalike decoys. Reference model: **0.932 macro F1** vs 0.507 for a shape-only baseline, and 0.895 on layouts and key names it never saw in training. [Kaggle](https://www.kaggle.com/datasets/netramfaran/real-or-decoy-pii-lookalikes) | scikit-learn, pandas |
| [babel-feature-eval-kit](https://github.com/netram75/babel-feature-eval-kit) | Tooling to build and grade blind coding tasks on a real open source project (python-babel) and measure how often coding agents from 3 model families solve them: offline Docker runs, JUnit grading, bundle checks | Python, Docker |
| [Flood segmentation](https://github.com/netram75/aisehack-flood-segmentation) | 3-class segmentation on 8-channel SAR + optical imagery. CE + Dice + Boundary loss, 32x patch sampling on 59 images, 5 controlled experiments (0.170 → 0.1845) | PyTorch, ResNet34-UNet, OpenCV |

Earlier work: [credit card fraud (XGBoost)](https://github.com/netram75/credit-card-fraud-xgboost) · [CIFAR-10 ablation](https://github.com/netram75/cifar10-cnn-image-classification) · [PDF-Agent (RAG)](https://github.com/netram75/PDF-Agent)

## 🌍 Open source

**37 merged PRs:**
[27 in SugarLabs Music Blocks](https://github.com/sugarlabs/musicblocks/pulls?q=is%3Apr+author%3Anetram75+is%3Amerged) ·
[9 in Red Hat's krkn-chaos (CNCF)](https://github.com/search?q=org%3Akrkn-chaos+author%3Anetram75+is%3Apr+is%3Amerged&type=pullrequests) ·
[1 in OWASP Nest](https://github.com/OWASP/Nest/pulls?q=is%3Apr+author%3Anetram75+is%3Amerged)

- **krkn-chaos:** fixed health-check telemetry that logged endpoints as healthy while they were down for the whole run (status hardcoded to True), and a Cerberus route check that never ran
- **Music Blocks:** fixed a tempo bug caused by operator precedence, restored keyboard Tab focus, and added test coverage

## 🧰 Tech stack

**Languages**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat&logo=mysql&logoColor=white)

**Backend and data**

![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat&logo=nodedotjs&logoColor=white)
![Celery](https://img.shields.io/badge/Celery-37814A?style=flat&logo=celery&logoColor=white)
![Ray](https://img.shields.io/badge/Ray-028CF0?style=flat&logo=ray&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis%20%2F%20Valkey-DC382D?style=flat&logo=redis&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat&logo=mongodb&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat&logo=mysql&logoColor=white)
![BigQuery](https://img.shields.io/badge/BigQuery-669DF6?style=flat&logo=googlebigquery&logoColor=white)

**Cloud and DevOps**

![AWS](https://img.shields.io/badge/AWS%20(EC2%2C%20S3%2C%20IAM)-232F3E?style=flat&logo=amazonwebservices&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat&logo=githubactions&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat&logo=linux&logoColor=black)
![Git](https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white)

**Machine learning**

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat&logo=pytorch&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat&logo=scikitlearn&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-150458?style=flat&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-189FDD?style=flat)

## 🏆 Achievements

- **16th of 78 finalists** (from 103 teams), ANRF AISEHack (IIIT Hyderabad, IBM)
- **3rd of 67 teams**, AuraVerse 2.0 hackathon
- **9th in the finals**, Synapse national hackathon
- **Kaggle Expert**
- **Problem solving:** 250+ LeetCode and 300+ Codeforces problems

## 📫 Connect

[LinkedIn](https://linkedin.com/in/netramfaran) · [Kaggle](https://www.kaggle.com/netramfaran)
