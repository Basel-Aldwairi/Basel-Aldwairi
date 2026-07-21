<div align="center">

# Basel Al-Dwairi

### Python Engineer | Applied AI, Computer Vision & Data Systems

Computer Engineering Senior @ German Jordanian University (GJU) · Vice President, GJU AI Club · Erasmus+ Student at Hochschule Bonn-Rhein-Sieg

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/basel-al-dwairi/)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:aldwairi.basel0@gmail.com)
[![Kaggle](https://img.shields.io/badge/Kaggle-20BEFF?style=for-the-badge&logo=kaggle&logoColor=white)](https://www.kaggle.com/baselaldwairi)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Basel-Aldwairi)

</div>

---

## About Me

I build **end-to-end AI systems** - from async web crawlers and embedded hardware, through data pipelines and vector search, up to production-ready UIs. My focus is **Applied AI, Computer Vision, and Python backend engineering**, with a track record of shipping systems that go from raw, messy real-world data to measurable, deployed results.

-  Currently building **ONEplace**, a hybrid dense-sparse-fuzzy retrieval engine for electronics inventory (Senior Graduation Project, GJU)
-  Vice President @ **GJU AI Club** - technical leadership, database design, and live event applications
-  Interned as AI Engineer @ **Orange** - EDA/ML/DL pipelines culminating in a custom RAG system for a national bank
-  Interests: agentic AI, hybrid search & retrieval, real-time computer vision, and systems that bridge hardware and ML

---

## Tech Stack

**Languages**
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-003B57?style=flat-square&logo=sqlite&logoColor=white)
![C](https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)


**AI / ML / Computer Vision**
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)
![Keras](https://img.shields.io/badge/Keras-D00000?style=flat-square&logo=keras&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white)
![MediaPipe](https://img.shields.io/badge/MediaPipe-0097A7?style=flat-square&logo=google&logoColor=white)
![FAISS](https://img.shields.io/badge/FAISS-4285F4?style=flat-square&logo=meta&logoColor=white)
![Gemini](https://img.shields.io/badge/Gemini_API-8E75B2?style=flat-square&logo=googlegemini&logoColor=white)

**Backend & Data Pipeline**
![AsyncIO](https://img.shields.io/badge/AsyncIO-3776AB?style=flat-square&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white)
![ESP32](https://img.shields.io/badge/ESP32-E7352C?style=flat-square&logo=espressif&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)

**UI & Tools**
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![CUDA](https://img.shields.io/badge/CUDA-76B900?style=flat-square&logo=nvidia&logoColor=white)

---

## Featured Engineering Projects

### ONEplace - Hybrid Search Engine for Local Electronics
*Lead Developer & ML Engineer · Senior Graduation Project @ GJU*

There's no central API or aggregator for comparing tech/electronics prices and stock availability in Amman, Jordan - so I built one.

**Architecture:** 4-layer sequential pipeline
`Async Crawling/Scraping` → `Pandas ETL & MongoDB Storage` → `FAISS + BM25 + RapidFuzz Hybrid Engine (fused with RRF)` → `Streamlit UI`

| Metric | Result |
|---|---|
| Precision@5 | **0.82** |
| Recall@5 (Hit Rate) | **1.00** |
| F1@5 | **0.90** |
| Avg. Query Latency | **~54 ms** across 17,000+ indexed products |

**Takeaway:** Reciprocal Rank Fusion across dense (FAISS + `all-MiniLM-L6-v2`), sparse (BM25), and fuzzy (RapidFuzz) retrievers delivers robust results even with noisy, inconsistent product listings scraped from multiple retailers.

`Python` `Streamlit` `FAISS` `Sentence-Transformers` `AsyncIO` `MongoDB`

---

### AIr (Hand) Painting - Real-Time Gesture-Controlled Virtual Canvas

A webcam-based canvas controlled entirely through hand gestures - no mouse, no touch.

**Architecture:** MediaPipe Hands tracks 21 hand landmarks in real time; a custom gesture-recognition engine routes triggers into OpenCV bitwise composition layers (AND/OR/XOR) for zero-lag rendering.

**Features:** Freehand drawing, erasing, Solid vs. Glassy material toggling, and a debounced interactive color/brush menu.

**Takeaway:** Demonstrates low-latency real-time CV pipeline design - landmark tracking, gesture debouncing, and compositing all running smoothly on live video.

`Python` `OpenCV` `MediaPipe` `NumPy`

---

### Mother's Day Poem Generator & Live Event Gallery

A two-part application built for the GJU AI Club's live on-stage ceremony.

**Architecture:** A user-facing app generates personalized poems via Google's Gemini API (`gemini-3-flash-preview`) in 4 languages, streamed back with a typewriter animation and written directly to MongoDB Atlas. A separate live-display app polls Mongo and renders auto-refreshing glassmorphism cards on the event screen.

**Takeaway:** End-to-end LLM-powered UX under live event constraints - multilingual generation, real-time streaming, and a decoupled read/write display architecture.

`Python` `Streamlit` `Gemini API` `MongoDB Atlas`

---

### CoinJo - Jordanian Coin Sorting & Detection System

An end-to-end computer vision + IoT system that classifies coin denominations and signals physical sorting hardware.

**Architecture:** MobileNetV2 (transfer learning) trained on a custom COCO-format dataset. A laptop acts as the central controller over TCP sockets: ESP32-CAM captures on request → model predicts → ESP32 executes the physical sort.

**Takeaway:** Bridges an ML model with real embedded hardware over a socket protocol - model inference driving physical actuation, not just a dashboard output.

`Python` `TensorFlow/Keras` `OpenCV` `TCP Sockets` `Streamlit` `MobileNetV2`

---

### Financial RAG System - Housing Bank of Jordan
*Capstone Project · AI Engineering Internship @ Orange*

A custom Retrieval-Augmented Generation system built to answer financial queries grounded in bank documentation.

**Architecture:** Custom BFT web crawler & scraper → preprocessing → recursive chunking → FAISS vector DB (`all-MiniLM-L6-v2`) → LiquidAI LFM2-2.6B for generation → Streamlit UI with MongoDB caching.

**Takeaway:** Full RAG lifecycle ownership - from sourcing and chunking raw web content to serving grounded, cached LLM responses in a production-style UI.

`Python` `FAISS` `Sentence-Transformers` `LiquidAI LFM` `Streamlit` `MongoDB` `Ubuntu/CUDA`

---

## Professional Experience

**AI Engineer Intern - Orange**
Worked across EDA, ML, and DL pipelines, culminating in a custom Retrieval-Augmented Generation (RAG) system for the Housing Bank of Jordan capstone.

**Vice President - GJU AI Club**
Technical leadership across the club's initiatives: organizing AI events, designing database systems, and building live event applications used on-stage in front of hundreds of attendees.

---

## GitHub Stats

<div align="center">

  <img height="165" src="https://github-readme-stats.vercel.app/api?username=Basel-Aldwairi&show_icons=true&theme=tokyonight&hide_border=true&count_private=true&cache_seconds=86400" />
  <img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Basel-Aldwairi&layout=compact&theme=tokyonight&hide_border=true&cache_seconds=86400" />

  <br/><br/>

  <img src="https://github-readme-streak-stats.herokuapp.com/?user=Basel-Aldwairi&theme=tokyonight&hide_border=true" />

</div>

---

<div align="center">
 
Reach me at **aldwairi.basel0@gmail.com** or connect on [LinkedIn](https://www.linkedin.com/in/basel-al-dwairi/)

</div>