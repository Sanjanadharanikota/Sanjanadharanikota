<h1 align="center">
  👋 Hi, I'm <span style="color:#0077B5;">Sanjana Dharanikota</span>
</h1>

<p align="center">
  <a href="https://www.linkedin.com/in/sanjana-dharanikota">
    <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"/>
  </a>
  <a href="https://github.com/Sanjanadharanikota">
    <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white"/>
  </a>
  <a href="mailto:dharanikotasanjana@gmail.com">
    <img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white"/>
  </a>
</p>

<div align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&weight=600&size=22&pause=1000&color=0077B5&center=true&vCenter=true&width=900&lines=BE+Information+Technology+%40+Vasavi+College+of+Engineering;CGPA+9.24+%7C+Top+1%25+NPTEL+Java+%7C+Elite+Gold;Full+Stack+Dev+%7C+AI%2FML+%7C+Distributed+Systems;Built+FRA+Atlas+%7C+NanoURL+%7C+DeTinyLLM;GSSoC+%26+SSoC+Open+Source+Contributor;SIH+2025+National+Finalist+%7C+AWS+AI+Scholar" />
</div>

<br/>

<p align="center">
  <img src="https://img.shields.io/badge/🟢%20Open%20to-SDE%20%7C%20Full%20Stack%20%7C%20ML%20Engineer%20Roles-success?style=for-the-badge"/>
</p>

---

## 🎓 Education

| Degree | Institution | Score | Year |
|--------|-------------|-------|------|
| BE — Information Technology | Vasavi College of Engineering, Hyderabad | CGPA: 9.24/10 | 2023 – 2027 |

---

## 📊 GitHub Stats

<p align="center">
  <img width="49%" src="https://github-readme-stats.vercel.app/api?username=Sanjanadharanikota&show_icons=true&theme=tokyonight&hide_border=true&count_private=true" />
  <img width="49%" src="https://github-readme-streak-stats.herokuapp.com/?user=Sanjanadharanikota&theme=tokyonight&hide_border=true" />
</p>

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Sanjanadharanikota&layout=compact&theme=tokyonight&hide_border=true" />
</p>

<p align="center">
  <img src="https://github.com/Sanjanadharanikota/Sanjanadharanikota/blob/output/github-contribution-grid-snake.svg" alt="snake animation"/>
</p>

---

## 🚀 Featured Projects

### 🌿 🏞️ FRA Atlas: A WebGIS-Based Intelligent Frontier for Forest Rights Decision Support
> An AI-powered WebGIS platform for integrated monitoring of Forest Rights Act (FRA) implementation — digitizing records, classifying land via satellite, and delivering blockchain-backed, LLM-driven governance support.

[![FRA Atlas](https://img.shields.io/badge/GitHub-FRA--Atlas-181717?style=for-the-badge&logo=github)](https://github.com/Sanjanadharanikota/FRA-Atlas)

- **OCR + Gemini LLM pipeline** — scanned FRA paper documents are extracted via Tesseract/Google Vision and structured into verified JSON records by Gemini LLM
- **Forensic blockchain integrity** — every record is SHA-256 chained sequentially; edits ripple hash recalculations forward and every change is captured in a full before/after audit log
- **Google Earth Engine + MobileNetV2 CNN** — Sentinel-2 satellite imagery is fetched, classified into 10 land cover types (EuroSAT-trained), and immutably linked to each FRA claim
- **Hybrid RAG Decision Support System** — government policy PDFs chunked, embedded via Gemini (`embedding-001`), and retrieved with cosine similarity for per-applicant scheme recommendations (PM-KISAN, MGNREGA, Jal Jeevan Mission, etc.)
- **Interactive WebGIS atlas** — React Leaflet map with density heatmaps, village coverage zones, deterministic spatial jitter, and Gemini geocoding fallback for obscure village names
- **Role-based access control** — JWT (HS256) + PBKDF2-SHA256 with `admin` and `analyst` roles; health endpoints for production readiness

**Tech:** `React 18` `TypeScript` `Vite` `Tailwind CSS` `shadcn/ui` `React Leaflet` `FastAPI` `Python` `PostgreSQL` `PostGIS` `Google Earth Engine` `Gemini AI` `LangChain` `TensorFlow/Keras` `MobileNetV2` `Tesseract OCR` `pypdf` `JWT` `Docker`

---

### 🤖 DeTinyLLM — Dual-Stage Framework for AI-Generated Text Detection
> A dual-stage NLP framework that detects AI-generated text by first paraphrasing it with a fine-tuned T5 model and then classifying the original–paraphrase pair using a divergence-aware RoBERTa classifier.

- **Stage 1 — Controlled Paraphrase Transformation:** A fine-tuned **T5** model generates a semantically faithful paraphrase of the input; human-written text produces high divergence while AI-generated text stays lexically close to the original
- **Stage 2 — Divergence-Aware Pairwise Classification:** Fine-tuned **RoBERTa** takes the original + paraphrase as a pair and classifies based on the divergence signal — achieving strong accuracy on the AI_Human dataset
- **Baseline comparison:** TF-IDF + Logistic Regression baseline (50k features, bigrams) benchmarked for accuracy, AUC-ROC, and inference speed against the full dual-stage pipeline
- **Efficiency analysis:** Computational benchmarking across N=10 trials comparing DeTinyLLM end-to-end latency vs. standalone baselines on GPU (CUDA) with AMP
- End-to-end inference demo with fixed human-written and AI-generated examples to validate the pipeline's real-world decision boundary

**Tech:** `Python` `PyTorch` `HuggingFace Transformers` `T5` `RoBERTa` `scikit-learn` `Pandas` `NumPy` `Datasets` `ROUGE` `Google Colab` `CUDA`

---

### 🔗 NanoURL — Scalable Cloud-Based Distributed URL Shortening System
> A distributed, fault-tolerant, high-performance URL shortener engineered for massive scale with real-time analytics and sub-millisecond redirections.

[![NanoURL](https://img.shields.io/badge/GitHub-NanoURL-181717?style=for-the-badge&logo=github)](https://github.com/Sanjanadharanikota/NanoURL-A-Scalable-Cloud-Based-Distributed-URL-Shortening-System)

- **Apache ZooKeeper** handles distributed ID coordination via token-range locking — each Node.js instance claims a range and generates Base62 IDs locally, eliminating single-point-of-failure bottlenecks
- **Redis cache-aside strategy** delivers sub-millisecond redirections; Bloom Filters prevent unnecessary DB lookups for non-existent keys
- **Nginx** reverse proxy with load balancing across multiple backend instances for high availability
- Real-time **click analytics dashboard** with interactive timelines, password-protected links, smart metadata previews, and themed QR code generation
- Fully containerised with **Docker Compose** — entire stack (React, Node, MongoDB, Redis, ZooKeeper, Nginx) spins up with a single command

**Tech:** `React` `SCSS` `Node.js` `Express.js` `MongoDB` `Redis` `Apache ZooKeeper` `Nginx` `Docker` `Docker Compose` `Base62 Encoding` `Bloom Filters`

---

### 💰 Wealth Navigator — Secure AI Financial Co-Pilot
> A full-stack AI finance platform integrating **10+ financial data streams** across banking and investments.

- Real-time transaction analysis, anomaly detection & predictive financial forecasting
- End-to-end security with **OAuth2, JWT & AES-256** encryption
- Interactive data visualisations powered by **D3.js / Chart.js**
- Push notifications and multi-channel alerts via **Twilio** and **Firebase**

**Tech:** `React.js` `Tailwind CSS` `Node.js` `Express.js` `MongoDB` `OpenAI` `FinGPT` `PyTorch` `Plaid API` `OAuth2` `JWT` `AES-256` `D3.js` `Chart.js` `Twilio` `Firebase`

---

## 🏆 Achievements & Awards

- 🥇 **NPTEL Programming in Java** — Top **1%** nationally | **Elite Gold Certificate** *(2026)*
- 🏆 **VJ Hackathon** — Top 20 / 5,118 teams nationally | **Best Girls Team Award**
- 🏅 **Smart India Hackathon 2025** — National Pre-Finale Qualifier
- ☁️ **AWS AI & ML Scholarship** — Udacity *"Future AWS AI Engineer"* Nanodegree
- 🎯 **MSME 5.0 Ideathon** — Shortlisted in Top 12 / 234 proposals (Govt. of India)

---

## 🛠 Tech Stack

### Languages
![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![C](https://img.shields.io/badge/C-00599C?style=for-the-badge&logo=c&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

### Web & Frameworks
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Node.js](https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white)
![Express.js](https://img.shields.io/badge/Express.js-404D59?style=for-the-badge)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![Bootstrap](https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white)

### Databases & Tools
![MongoDB](https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-336791?style=for-the-badge&logo=postgresql&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-00000F?style=for-the-badge&logo=mysql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Postman](https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white)
![VS Code](https://img.shields.io/badge/VS%20Code-007ACC?style=for-the-badge&logo=visual-studio-code&logoColor=white)
![Figma](https://img.shields.io/badge/Figma-F24E1E?style=for-the-badge&logo=figma&logoColor=white)

### AI / ML & Cloud
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)
![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge&logo=python&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white)
![Google Earth Engine](https://img.shields.io/badge/Google%20Earth%20Engine-4285F4?style=for-the-badge&logo=googleearth&logoColor=white)

---

## 🌍 Open Source Contributions

<p align="center">
  <img src="https://img.shields.io/badge/GirlScript%20Summer%20of%20Code-Contributor-orange?style=for-the-badge&logo=github&logoColor=white"/>
  <img src="https://img.shields.io/badge/Social%20Summer%20of%20Code-Contributor-blueviolet?style=for-the-badge&logo=github&logoColor=white"/>
</p>

Currently an active contributor in ongoing open source programs — collaborating with developers across the country, reviewing codebases, submitting PRs, and building in public.

- 🟠 **GirlScript Summer of Code (GSSoC)** — Contributing to real-world open source projects, collaborating with maintainers, and shipping production-ready code
- 🟣 **Social Summer of Code (SSoC)** — Active contributor working on community-driven open source repositories

---

## 📜 Certifications

| Certificate | Issuer |
|-------------|--------|
| Future AWS AI Engineer Nanodegree | Udacity × AWS |
| Programming in Java — **Elite Gold (Top 1%)** | NPTEL |
| Full Stack Developer Bootcamp | GeeksforGeeks |
| Postman API Fundamentals — Student Expert | Postman |
| Python Skills Certification | HackerRank |
| Problem Solving Through Programming in C | NPTEL, IIT Kharagpur |

---

## 📬 Let's Connect

I'm a **final-year BE student actively looking for full-time opportunities** as an **SDE / Full Stack / ML Engineer**.

📧 **dharanikotasanjana@gmail.com** | 📍 Hyderabad, India

---

<p align="center">
  <i>"From forest rights to financial forecasting — I build systems that matter."</i>
</p>

![](https://komarev.com/ghpvc/?username=Sanjanadharanikota&color=0077B5)
