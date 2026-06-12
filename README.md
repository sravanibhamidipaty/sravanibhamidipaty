<!-- ===== Header / Hero ===== -->
<p align="center">
  <!-- Optional banner -->
  <!-- <img src="https://raw.githubusercontent.com/sravanibhamidipaty/sravanibhamidipaty/main/header.png" alt="Header" /> -->
</p>

<h1 align="center">Hi there! I'm Sravani Bhamidipaty 👋</h1>

<p align="center">
  <a href="https://readme-typing-svg.demolab.com/demo/">
    <img
      src="https://readme-typing-svg.demolab.com?duration=2500&pause=800&center=true&vCenter=true&width=600&lines=Software+Engineer+%40+Grainger;Graduate+TA+%7C+MSCS+%40+Georgia+Tech+%28AI%29;Building+MLOps+platforms+end-to-end;Human-centered%2C+production-ready+AI;Open+Source+Software+Contributor"
      alt="Typing SVG"
    />
  </a>
</p>
<p align="center">
  <!--<a href="#-about-me">👨‍💻 About Me</a> &nbsp;|&nbsp;-->
  <!-- <a href="https://drive.google.com/file/d/13BsAvlclfenGVblK8O3qcS1RhP4pxNEg/view?usp=sharing">📄 Resume</a> &nbsp;|&nbsp; -->
  <a href="mailto:sravanibhamidipaty@gmail.com">✉️ Email</a> &nbsp;|&nbsp;
  <a href="https://linkedin.com/in/sravani-bhamidipaty">🔗 LinkedIn</a>
</p>

<!--<p align="center">
  ![Profile Views](https://komarev.com/ghpvc/?username=sravanibhamidipaty&style=flat-square&color=blue)
</p>-->

---

## 👩‍💻 About Me
 ```python
__author__ = "Sravani Bhamidipaty"
__location__ = "Chicago, IL"
__email__ = "sravanibhamidipaty@gmail.com"

stacks = {
    "Languages": ["Python", "Java", "C++", "JavaScript", "SQL"],
    "AI/ML": [
        "TensorFlow", "PyTorch", "Scikit-learn",
        "Transformers (Hugging Face)", "OpenCV",
        "Deep Learning", "NLP", "Computer Vision"
    ],
    "Data": ["Pandas", "NumPy", "Matplotlib", "Seaborn"],
    "Software Dev": ["OOP", "DSA", "REST APIs", "FastAPI", "Git/GitHub", "Unit Testing"],
    "Cloud & DevOps": ["AWS (S3, EC2, SageMaker)", "Docker", "Grafana"],
    "Databases": ["MySQL", "PostgreSQL", "MongoDB"]
}

def about_me():
    print(f"👩‍💻 {__author__} | {__location__}")
    print(f"📫 Reach me at: {__email__}")
    print("🚀 Passionate about building intelligent systems, scalable software, and data-driven solutions.")
    print("🌱 Exploring cutting-edge AI while sharpening software engineering fundamentals.")
    print("💡 Always learning, always building.")

if __name__ == "__main__":
    about_me()
 ```
---

## 🏗️ Featured Projects

#### **[Mock Payment Gateway API](https://github.com/sravanibhamidipaty/mock-payment-gateway-api)**
The architecture Stripe and Adyen use to handle money at scale — implemented end-to-end. Solves the hard problem: **a single click must never charge a customer twice**, even under retries, double-submits, or mid-flight crashes.

**Technologies Used:** Python · FastAPI · Kafka · Redis · PostgreSQL · Docker · Prometheus · Grafana · GitHub Actions

**Key Design Decisions:**
* API deduplicates via Redis (`O(1)` idempotency-key lookup, 24h TTL) and returns `202 Accepted` instantly — the user never waits on the DB
* Kafka decouples ingestion from processing; write path stays fast, worker scales independently
* Background worker persists charges transactionally, fires webhooks with **exponential backoff + Dead Letter Queue** — no accepted payment is silently lost
* Production-grade observability: Prometheus metrics, liveness/readiness probes, structured JSON logging, pre-provisioned Grafana dashboard
* Full CI: `ruff`, `black`, `mypy`, async unit tests + **Testcontainers** integration tests against real PostgreSQL

---

#### **[Mac Observability Stack (productivity-lgtm)](https://github.com/sravanibhamidipaty/productivity-lgtm)**
Event-driven macOS telemetry agent that replaces CPU-heavy polling with Apple's native `NSWorkspace` OS hooks. **Zero idle CPU overhead** — the agent sleeps until the kernel fires a window-switch event, then captures workspace activity and deep-linked browser context.

**Technologies Used:** Python · AppKit · NSWorkspace · Grafana · Loki · Mimir · Tempo · Docker Compose

**Key Design Decisions:**
* Observer Pattern via `NSWorkspaceDidActivateApplicationNotification` — wakes only on kernel-broadcast events
* Async AppleScript subprocess extracts active Chrome tab URL and maps it to a productivity category
* Full LGTM backend (Loki for logs, Mimir for metrics, Tempo for traces) — all containerized with persistent Docker volumes

---

#### **[Open Source Contribution — golang/go](https://github.com/sravanibhamidipaty/open-source-software-contributions)**
Fixed a bug in the **Go standard library** (`crypto/x509.VerifyHostname`) where zone-scoped IPv6 addresses like `fe80::1%eth0` were incorrectly falling through to DNS name matching instead of IP matching, breaking TLS certificate verification on link-local IPv6 networks.

**Technologies Used:** Go · `crypto/x509` · `net/netip` · Gerrit code review

**Key Details:**
* Root cause: `net.ParseIP` returns `nil` for zone-scoped IPv6 — fixed by switching to `netip.ParseAddr` with `.WithZone("")` before SAN comparison
* Patch reviewed and approved by Go core maintainers (Roland Shoemaker, Daniel McCarney); CI (LUCI-TryBot) passed
* **Merged into `golang/go` master** — [commit 6a8455f](https://github.com/golang/go/commit/6a8455f), June 2026

---
## 🏆 LeetCode Stats
<p align="center"> <!-- Heatmap --> <img src="https://leetcard.jacoblin.cool/sravanibhamidipaty?theme=dark&font=Baloo%202&ext=heatmap" alt="LeetCode Card" /> </p> <p align="center"> <a href="https://leetcode.com/sravanibhamidipaty">Check out my LeetCode profile →</a> </p>

---
## 📈 GitHub Stats

<!--<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=sravanibhamidipaty&show_icons=true&theme=radical" alt="GitHub Stats" />
</p>-->

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=sravanibhamidipaty&layout=compact&theme=radical" alt="Top Languages" />
</p>

<!--<p align="center">
  <img src="https://streak-stats.demolab.com?user=sravanibhamidipaty&theme=radical" alt="GitHub Streak" />
</p>-->
---

## 🚀 Tech Stack  

### 💻 Languages  
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white) ![Java](https://img.shields.io/badge/Java-007396?style=for-the-badge&logo=java&logoColor=white) ![C++](https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white) ![JavaScript](https://img.shields.io/badge/JavaScript-F7E017?style=for-the-badge&logo=javascript&logoColor=black) ![SQL](https://img.shields.io/badge/SQL-336791?style=for-the-badge&logo=postgresql&logoColor=white)  

### 🤖 AI / Machine Learning  
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white) ![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white) ![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white) ![HuggingFace](https://img.shields.io/badge/Transformers-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black) ![LangChain](https://img.shields.io/badge/LangChain-0F9D58?style=for-the-badge&logo=chainlink&logoColor=white) ![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white) ![OCR](https://img.shields.io/badge/OCR-Tesseract%2FPaddleOCR-FF6F61?style=for-the-badge&logo=google&logoColor=white) ![Computer Vision](https://img.shields.io/badge/Computer%20Vision-4285F4?style=for-the-badge&logo=opencv&logoColor=white) ![NLP](https://img.shields.io/badge/NLP-FF5733?style=for-the-badge&logo=spacy&logoColor=white)  

### 📊 Data & Visualization  
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white) ![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white) ![Matplotlib](https://img.shields.io/badge/Matplotlib-005C55?style=for-the-badge&logo=plotly&logoColor=white) ![Seaborn](https://img.shields.io/badge/Seaborn-3792CB?style=for-the-badge&logo=python&logoColor=white) ![NetworkX](https://img.shields.io/badge/NetworkX-005571?style=for-the-badge&logo=networkx&logoColor=white) ![Datadog](https://img.shields.io/badge/Datadog-632CA6?style=for-the-badge&logo=datadog&logoColor=white) ![Grafana](https://img.shields.io/badge/Grafana-F46800?style=for-the-badge&logo=grafana&logoColor=white)  

### 🛠️ Software Development  
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white) ![REST APIs](https://img.shields.io/badge/REST-02569B?style=for-the-badge&logo=apollographql&logoColor=white) ![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white) ![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white) ![CI/CD](https://img.shields.io/badge/CI%2FCD-0A0A0A?style=for-the-badge&logo=jenkins&logoColor=white) ![OOP](https://img.shields.io/badge/OOP-008080?style=for-the-badge&logo=java&logoColor=white)  

### ☁️ Cloud & DevOps  
![AWS](https://img.shields.io/badge/AWS-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white) ![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white) ![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white) ![Airflow](https://img.shields.io/badge/Airflow-017CEE?style=for-the-badge&logo=apacheairflow&logoColor=white) ![Terraform](https://img.shields.io/badge/Terraform-844FBA?style=for-the-badge&logo=terraform&logoColor=white)  

### 🗄️ Databases & Messaging  
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white) ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white) ![MongoDB](https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white) ![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white) ![Kafka](https://img.shields.io/badge/Kafka-231F20?style=for-the-badge&logo=apachekafka&logoColor=white)  

### 🌱 Currently Learning  
![Responsible AI](https://img.shields.io/badge/Responsible%20AI-00A67E?style=for-the-badge&logo=ai&logoColor=white) ![Advanced LLMOps](https://img.shields.io/badge/LLMOps-8A2BE2?style=for-the-badge&logo=openai&logoColor=white) ![LangChain Advanced](https://img.shields.io/badge/LangChain%20Advanced-0F9D58?style=for-the-badge&logo=chainlink&logoColor=white)  

---
## 🔗 Connect With Me
<p align="center"> <a href="https://linkedin.com/in/sravani-bhamidipaty"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white" /></a> <a href="mailto:sravanibhamidipaty@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=flat&logo=gmail&logoColor=white" /></a> <a href="https://github.com/sravanibhamidipaty"><img src="https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white" /></a> <a href="https://leetcode.com/sravanibhamidipaty"><img src="https://img.shields.io/badge/LeetCode-000000?style=flat&logo=leetcode&logoColor=orange" /></a> </p>

---

<p align="center">⭐️ From <a href="https://github.com/sravanibhamidipaty">sravanibhamidipaty</a></p>
