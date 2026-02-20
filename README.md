# YouTube Comment Spam Detector

A machine learning pipeline for detecting phishing scams, adult-bait bots, and engagement spam in YouTube comment sections.

---

## 🎯 Problem

YouTube comment sections are frequently targeted by:

- Phishing scams (WhatsApp / Telegram / crypto links)
- Adult-bait bots (explicit engagement traps)
- Engagement spam (“who’s watching in 2026?”, copied comments)
- Link farming and promotional bots

These comments reduce user trust, skew engagement metrics, and expose vulnerable users to harmful content.

This project builds a structured ML pipeline to detect and categorize suspicious comments using:

- Rule-based weak supervision
- TF-IDF + Logistic Regression baseline
- Feature engineering (links, emoji density, repetition patterns)
- Precision-focused evaluation

---

## 🧠 Project Phases

### Phase 1 – Data Collection
- Use YouTube Data API
- Collect comment threads across multiple video categories
- Store structured dataset

### Phase 2 – Weak Supervision & Labeling
- Rule-based labeling for obvious spam patterns
- Manual validation of sampled comments
- Define labeling guidelines

### Phase 3 – Baseline Model
- TF-IDF + Logistic Regression
- Multi-class classification:
  - `adult_bait`
  - `phishing_scam`
  - `engagement_spam`
  - `benign`

### Phase 4 – Moderation Tool (Optional UI)
- Streamlit dashboard to fetch and classify live comments

---

## 📊 Target Metrics

- High precision on `phishing_scam` and `adult_bait`
- Clear confusion matrix reporting
- Error analysis examples

---

## 🛠 Tech Stack

- Python
- YouTube Data API
- pandas / numpy
- scikit-learn
- Streamlit (optional UI)

---

## 🚀 Future Extensions

- Similarity detection for copypasta bots
- URL domain reputation scoring
- Burst pattern detection
- Lightweight NSFW signal integration (ethical use only)

---

## ⚠️ Disclaimer

This project is for educational and research purposes.  
It does not store personal user data beyond publicly available comment metadata.
