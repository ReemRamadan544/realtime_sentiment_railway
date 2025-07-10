# 🎯 Real-Time Twitter Sentiment Pipeline with Streamlit & Big Data Stack

> This project delivers a real-time sentiment analysis system for Twitter-like data using a full big data stack and cloud-native architecture.  
> It combines **Apache Kafka** for ingestion, **Apache Spark** for stream processing, **NLTK (VADER)** for sentiment classification, and dual dashboards using **Streamlit** and **Flask**.  
> Persistent storage is handled via **MongoDB Atlas**, while deployment and CI/CD are managed through **Docker** and **GitHub Actions**, making the pipeline fully scalable and production-ready in the cloud.


---

## 🚀 Live App  
🔗 [web-production-c660f.up.railway.app](https://web-production-c660f.up.railway.app)


---

## 🧠 Features

- 🐦 Simulates real-time tweet ingestion from CSV via Kafka
- ⚡ Spark Structured Streaming pipeline for live sentiment classification
- 💬 NLP pipeline using **VADER** for positive, neutral, and negative labels
- 📊 Streamlit dashboard for:
  - Sentiment distribution
  - Word clouds by sentiment
  - Sentiment over time
  - Keyword-based filtering
- 🧾 Flask + MongoDB dashboard for data exploration and persistence
- 🔁 Dockerized setup with **CI/CD** via GitHub Actions
> This project was designed as a fully cloud-native architecture. The entire pipeline—from data ingestion to processing and visualization—is deployable and scalable on cloud platforms using Docker, CI/CD pipelines, and MongoDB Atlas.


---


## 📂 Project Structure

```
├── kafka_producer.py           # Sends CSV lines to Kafka topic
├── spark_streaming.py          # Processes Kafka messages with Spark
├── flask_dashboard.py          # Flask app to show MongoDB-stored results
├── static/styles.css           # CSS for Flask frontend
├── templates/dashboard.html    # HTML template for dashboard
├── requirements.txt            # Python dependencies
├── .github/workflows/deploy.yml # CI/CD with GitHub Actions
├── Dockerfile                  # Docker setup
├── sentimentdataset.csv        # Input tweets (simulated)
├── sentiment_results.csv       # Output tweets with sentiment
```



## 🔧 Technologies Used

| Component        | Tool/Framework          |
|------------------|-------------------------|
| Data Ingestion   | Apache Kafka            |
| Stream Processing| Apache Spark (Structured Streaming) |
| Sentiment Analysis | VADER (NLTK)          |
| Backend Storage  | MongoDB Atlas           |
| Dashboards       | Streamlit + Flask       |
| Containerization | Docker + Docker Compose |
| CI/CD            | GitHub Actions          |

---
## ☁️ Cloud Deployment Highlights
-  **Railway Deployment**: Dashboard is hosted live using Railway Cloud Platform.
-  **MongoDB Atlas**: Stores sentiment results and tweet metadata in a secure cloud database.
-  **CI/CD with GitHub Actions**: Every push to GitHub triggers an automatic deployment workflow.
-  **Dockerized Services**: All components are containerized for easy deployment and scaling.

## 📈 Implementation Phases

### Phase 1 – Prototyping in Google Colab
- Used `VADER` to classify tweets from CSV.
- Generated visualizations (WordClouds, bar charts).
- Limitation: No Kafka/Spark on Colab → moved to local.

### Phase 2 – Real-Time Kafka + Spark
- Kafka → Spark Streaming → MongoDB or CSV.
- Docker used to orchestrate Kafka & Zookeeper.
- Enabled scalable, real-time NLP processing.

### Phase 3 – Streamlit & Flask Dashboards
- Streamlit for real-time frontend with:
  - Pie & line charts
  - WordClouds per sentiment
  - Live auto-refresh & export
- Flask with MongoDB for persistent visualization.

---

## 🧪 Datasets

| File | Purpose |
|------|---------|
| `sentimentdataset.csv` | Input data used for simulation |
| `sentiment_results.csv` | Output sentiment results used by Streamlit |

---

## 👩‍💻 Authors

Project developed collaboratively by the **Big Data & AI Engineering Team**:

- **Reem Ramadan** – Biomedical Informatics  
- **Mena Osman** – AI Engineer  
- **Yomna Refaat**  
- **Mariam Mostafa**  
- **Mariam Eslam**  
- **Nayera Ibrahim**
