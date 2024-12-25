# 🏅 Olympic Games Medalist Event Timeline Generation

## 📖 Overview

This repository contains the source code and documentation for a data-driven project that generates an **event timeline** for the Tokyo 2020 Summer Olympics using Twitter data. The system employs **Natural Language Processing (NLP)** and **clustering algorithms** to detect, summarize, and visualize events from social media posts. The project focuses on extracting medal-winning events, including details such as medalists, their countries, sports, and events.

---

## ⚙️ System Architecture

The project pipeline consists of the following components:

1. **Data Acquisition**:
   - Secondary Twitter data from Kaggle
   - External medalist and sports data crawled from [Wikipedia](https://www.wikipedia.org) and [Edudwar](https://www.edudwar.com/)

2. **Data Preprocessing**:
   - Noise removal (stop words, URLs, emojis, punctuation)
   - Tokenization and Named-Entity Recognition (NER)

3. **Event Detection & Summarization**:
   - Extracts key attributes: medalist name, country, sport, event, medal type, and timestamp.
   - Summarizes tweets into event clusters using `k-means`.

4. **Visualization**:
   - Generates timeline charts using `matplotlib` to depict event sequences.

---

## 🧠 Methodologies

- **NLP Techniques**:
  - Named-Entity Recognition (NER) for identifying medalists and countries.
  - TF-IDF Vectorization for filtering noise in tweets.
- **Clustering**:
  - `k-means` clustering for grouping tweets into event clusters.
  - Count vectorization for event label extraction.
- **Visualization**:
  - Timeline charts to represent medal events chronologically.

---

## 📂 Datasets

1. **Twitter Data**:
   - Dataset: Tokyo 2020 tweets with the hashtag `#Tokyo2020` (160,549 tweets from Kaggle).
   - Timeframe: 24 July 2021 – 27 July 2021 (first 4 days of the Olympics).
2. **Crawled Data**:
   - Medalist details from Wikipedia.
   - Sports and event lists from [Edudwar](https://www.edudwar.com/).

---

## 📊 Results

### Performance Metrics

- The system detected **41.5% of gold medal events**, **9.2% of silver medal events**, and **14.6% of bronze medal events**. 
- Most accurate for **gold medal events**, as social media users tend to post more about these.

### Visualizations

The following timeline charts were generated:
1. Winning countries for all medal types over the 4-day period.
2. Individual timelines for gold, silver, and bronze medals.
3. Day-wise breakdown of events.

## 🖼️ Example Visualizations

### 1. Overall Event Timeline

<div align="center">
  <img src="figures/Tokyo%202020%20winning%20countries%20within%20Entire%20time%20range%20-%20result.png" alt="Overall Timeline" style="width:70%;">
</div>

*Figure 1: Timeline chart showing medal-winning countries for all medal types during Tokyo 2020.*

---

### 2. Gold Medal Events

<div align="center">
  <img src="figures/Tokyo%202020%20Gold%20medal%20winning%20countries%20-%20result%20.png" alt="Gold Medal Timeline" style="width:70%;">
</div>

*Figure 2: Timeline chart focusing on gold medal-winning countries during Tokyo 2020.*

---

### 3. Verification Data Comparison (Day 1)

<div align="center">
  <img src="figures/Tokyo%202020%20Day%201%20details%20-%20verification.png" alt="Day 1 Verification" style="width:70%;">
</div>

*Figure 3: Verification timeline for Day 1, comparing system results against official data.*

## ⚠️ Disclaimer

This project was developed as part of a group coursework assignment. Please use this project for reference or educational purposes only, and exercise caution if applying it to other use cases.
