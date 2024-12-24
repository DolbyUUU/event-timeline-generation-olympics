# Tokyo 2020 Event Timeline Generation

## Overview

This repository contains the source code and documentation for a data-driven project that generates an **event timeline** for the Tokyo 2020 Summer Olympics using Twitter data. The system employs **Natural Language Processing (NLP)** and **clustering algorithms** to detect, summarize, and visualize events from social media posts. The project focuses on extracting medal-winning events, including details such as medalists, their countries, sports, and events.

---

## System Architecture

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

## Methodologies

- **NLP Techniques**:
  - Named-Entity Recognition (NER) for identifying medalists and countries.
  - TF-IDF Vectorization for filtering noise in tweets.
- **Clustering**:
  - `k-means` clustering for grouping tweets into event clusters.
  - Count vectorization for event label extraction.
- **Visualization**:
  - Timeline charts to represent medal events chronologically.

---

## Dataset

1. **Twitter Data**:
   - Dataset: Tokyo 2020 tweets with the hashtag `#Tokyo2020` (160,549 tweets from Kaggle).
   - Timeframe: 24 July 2021 – 27 July 2021 (first 4 days of the Olympics).
2. **Crawled Data**:
   - Medalist details from Wikipedia.
   - Sports and event lists from [Edudwar](https://www.edudwar.com/).

---

## Results

### Performance Metrics

- The system detected **41.5% of gold medal events**, **9.2% of silver medal events**, and **14.6% of bronze medal events**. 
- Most accurate for **gold medal events**, as social media users tend to post more about these.

### Visualizations

The following timeline charts were generated:
1. Winning countries for all medal types over the 4-day period.
2. Individual timelines for gold, silver, and bronze medals.
3. Day-wise breakdown of events.

