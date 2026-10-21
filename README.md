# Mallikarjun Jadi — Machine Learning Engineer Portfolio

> **Machine Learning Engineer | Full-Stack Developer | DSA Java Problem Solver**

Personal portfolio showcasing my work in **machine learning, computer vision, LLM fine-tuning, classical ML, and full-stack development**.

The portfolio is designed around one principle:

> **Build the model. Measure the result. Understand the failure. Ship something usable.**

Rather than presenting projects as simple demos, each major project includes its **dataset, methodology, evaluation results, engineering decisions, limitations, and links to the implementation**.

---

## 🌐 Portfolio

**Live Portfolio:** `Add your deployed URL here`

**GitHub:** [github.com/MallikarjunJD](https://github.com/MallikarjunJD)

**LinkedIn:** [linkedin.com/in/mallikarjunjadi](https://www.linkedin.com/in/mallikarjunjadi/)

**Hugging Face:** [huggingface.co/MallikarjunJadi](https://huggingface.co/MallikarjunJadi)

**LeetCode:** [leetcode.com/u/MallikarjunJadi](https://leetcode.com/u/MallikarjunJadi/)

---

## 👨‍💻 About

I am a final-year **B.E. Computer Science and Engineering student** at AGMR College of Engineering and Technology, Hubli, affiliated with VTU.

My primary interests are:

* Machine Learning
* Deep Learning
* Computer Vision
* LLM Fine-Tuning
* Retrieval-Augmented Generation
* Model Evaluation
* Full-Stack Development
* Data Structures & Algorithms

I enjoy working on problems where I can go beyond training a model and investigate whether the resulting system actually works reliably.

---

## 🚀 Featured Work

### 1. LoRA vs QLoRA Fine-Tuning of Qwen2.5-1.5B

A controlled study comparing the base Qwen2.5-1.5B-Instruct model with **LoRA and QLoRA adapters** for agricultural question answering.

**Highlights:**

* Dataset: KisanVaani agricultural QA
* 4,000 training examples
* 500 validation examples
* 500 held-out test questions
* LoRA with rank 16
* QLoRA with 4-bit NF4 quantization
* TRL `SFTTrainer`
* PEFT
* Hugging Face Transformers
* Kaggle GPU training

### Results

| Model |    ROUGE-L | BERTScore F1 |   Token F1 |
| ----- | ---------: | -----------: | ---------: |
| Base  |     0.1074 |       0.8482 |     0.1590 |
| QLoRA |     0.2189 |       0.8784 |     0.2649 |
| LoRA  | **0.3559** |   **0.9046** | **0.3973** |

The project also documents an evaluation bug discovered during development where the three models initially produced nearly identical outputs.

The evaluation pipeline was rebuilt using isolated adapters, self-tests, identical prompts, and consistent decoding settings.

**Repository:**
https://github.com/MallikarjunJD/fine-tuning-research

**LoRA Adapter:**
https://huggingface.co/MallikarjunJadi/qwen2.5-1.5b-agri-qa-lora

**QLoRA Adapter:**
https://huggingface.co/MallikarjunJadi/qwen2.5-1.5b-agri-qa-qlora

---

### 2. EuroSAT Dual-Mode Land Cover Classifier

A computer vision system for classifying satellite imagery using either:

* RGB imagery
* 13-band Sentinel-2 multispectral imagery

Built with a custom **ResNet-style CNN with Squeeze-and-Excitation attention** using PyTorch.

### Results

| Input                 | Test Accuracy |
| --------------------- | ------------: |
| RGB                   |        97.58% |
| 13-band Multispectral |    **97.90%** |

The project includes a deployed Streamlit application and Hugging Face model checkpoints.

**Repository:**
https://github.com/MallikarjunJD/eurosat-land-cover-classification

**Live Demo:**
https://eurosat-land-cover-classification.streamlit.app

---

### 3. House Prices — Advanced Regression

A tabular machine learning pipeline for predicting housing prices using engineered features, model tuning, and ensemble learning.

**Techniques:**

* Feature engineering
* CatBoost
* XGBoost
* Optuna
* Scikit-learn
* 10-fold cross-validation
* Weighted ensemble

**Result:**

> **0.11799 RMSE (log-scale)** on the Kaggle public leaderboard.

**Repository:**
https://github.com/MallikarjunJD/House-Prices-Advanced-Regression

---

### 4. Fixmate — Multi-Role Service Booking Portal

A full-stack service-booking platform built with the MERN-oriented stack.

The application contains separate dashboards and workflows for:

* Administrators
* Clients
* Workers

The system supports **40+ service categories** with CRUD routes and application logic implemented manually.

**Stack:**

* MongoDB
* Express.js
* Node.js
* JavaScript

**Repository:**
https://github.com/MallikarjunJD/Fixmate_service_portal

---

## 🧠 Engineering Principles

The portfolio is built around several engineering habits demonstrated through the projects.

### 1. Compare Against a Baseline

Model improvements are reported against the original baseline rather than presenting an isolated score.

For example, the Qwen fine-tuning study evaluates:

**Base → QLoRA → LoRA**

under the same test conditions.

### 2. Distrust Surprising Results

During the Qwen evaluation, all three models initially produced nearly identical outputs.

Instead of assuming the training had failed, I investigated the evaluation pipeline and identified an adapter-loading issue.

The evaluation was rebuilt with isolated models, self-tests, and consistent inference settings.

### 3. Keep Training and Inference Consistent

The EuroSAT project uses a shared normalization configuration between training and inference so that deployed inputs follow the same preprocessing assumptions as training data.

### 4. Separate Model Behavior From Knowledge

Fine-tuning improved the style and relevance of generated agricultural answers, but it did not eliminate factual hallucinations.

That observation motivates the next stage of the work:

**Fine-Tuning + Retrieval-Augmented Generation**

---

## 🛠️ Technical Skills

### Languages

* Python
* Java
* JavaScript
* C

### Machine Learning

* Deep Learning
* Computer Vision
* CNNs
* Residual Networks
* Attention Mechanisms
* Ensemble Learning
* Model Evaluation
* Hyperparameter Optimization

### LLM Engineering

* LoRA
* QLoRA
* PEFT
* 4-bit Quantization
* Hugging Face Transformers
* TRL
* bitsandbytes
* ROUGE
* BERTScore

### ML Libraries

* PyTorch
* Torchvision
* Scikit-learn
* XGBoost
* CatBoost
* Optuna
* Pandas
* NumPy
* Matplotlib

### Tools & Deployment

* Git
* GitHub
* Hugging Face Hub
* Streamlit
* Gradio
* Kaggle GPU

### Full Stack

* MongoDB
* Express.js
* Node.js
* JavaScript

### Problem Solving

* Data Structures & Algorithms
* Java
* Competitive Programming
* 250+ LeetCode problems
* 1745+ contest rating

---

## 📊 Portfolio Highlights

| Metric                         |      Result |
| ------------------------------ | ----------: |
| EuroSAT Multispectral Accuracy |  **97.90%** |
| EuroSAT RGB Accuracy           |  **97.58%** |
| Qwen LoRA ROUGE-L              |  **0.3559** |
| Qwen Base ROUGE-L              |  **0.1074** |
| House Prices Kaggle RMSE       | **0.11799** |
| LeetCode Problems              |    **250+** |
| LeetCode Contest Rating        |   **1745+** |

> Metrics represent different datasets, evaluation protocols, and objectives. They should not be interpreted as directly comparable performance numbers.

---

## 📁 Project Structure

```text
portfolio/
│
├── index.html
├── resume.pdf
├── resume.docx
└── README.md
```

The portfolio is intentionally lightweight and does not require a frontend framework.

---

## 💻 Run Locally

Because the portfolio is a static website, no backend or package installation is required.

### Option 1 — Open directly

Open `index.html` in a browser.

### Option 2 — Run a local server

Using Python:

```bash
python -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

Using VS Code, you can also use the **Live Server** extension.

---

## 🚀 Deployment

The portfolio is a static HTML/CSS/JavaScript website and can be deployed using services such as:

* GitHub Pages
* Vercel
* Netlify
* Cloudflare Pages

### GitHub Pages

1. Push the repository to GitHub.
2. Open the repository's **Settings**.
3. Go to **Pages**.
4. Select the deployment source.
5. Deploy from the repository branch containing `index.html`.
6. Open the generated portfolio URL.

---

## 📄 Resume

The portfolio provides access to both versions of my resume:

* `resume.pdf`
* `resume.docx`

The PDF is intended for recruiter viewing and applications.

---

## 🎯 Current Focus

I am currently looking for **Machine Learning / Applied AI Engineering internships** where I can contribute to:

* Model training
* Evaluation
* Computer vision
* LLM fine-tuning
* Retrieval-augmented systems
* ML deployment
* End-to-end AI engineering

My next planned project is an **Agricultural AI Advisory System combining fine-tuning with RAG**, with an emphasis on grounding model responses in verified agricultural information.

---

## 📬 Contact

**Email:** [mallikarjunjadi9@gmail.com](mailto:mallikarjunjadi9@gmail.com)

For collaboration, internship opportunities, or technical discussions:

* LinkedIn: https://www.linkedin.com/in/mallikarjunjadi/
* GitHub: https://github.com/MallikarjunJD
* Hugging Face: https://huggingface.co/MallikarjunJadi
* LeetCode: https://leetcode.com/u/MallikarjunJadi/

---

## 📜 License

This portfolio is personal work intended to showcase my projects, skills, and engineering experience.
