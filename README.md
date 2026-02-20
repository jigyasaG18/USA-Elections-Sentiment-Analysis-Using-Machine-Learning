# USA Elections Sentiment Analysis Using Machine Learning 🗳️🤖

## Overview

This project aims to analyze public sentiment towards the two major U.S. presidential candidates—Donald Trump and Joe Biden—by examining tweets collected from social media platforms. Leveraging Natural Language Processing (NLP) techniques and machine learning, we evaluate whether the overall public opinion leans positively or negatively, providing insights that could help in predicting election outcomes.

---

## Introduction

Elections are complex social phenomena that reflect the collective preferences of the population. In the digital era, social media platforms like Twitter serve as real-time repositories of public sentiment, capturing opinions, emotions, and reactions from millions of users. Analyzing this data can reveal trends, shifts in opinion, and potential voting behavior.

### Why Sentiment Analysis? 

Sentiment analysis is a subset of NLP that involves computationally identifying and categorizing opinions expressed in text. It transforms qualitative data (tweets) into quantitative metrics (positive, negative, neutral), facilitating objective analysis of public mood.

---

## Data Collection & Description

### Data Sources

- **Trump.csv 🦅**: Contains tweets related to Donald Trump.
- **Biden.csv 🗳️**: Contains tweets related to Joe Biden.

Each dataset includes:

- `user`: Twitter handle of the user.
- `text`: The tweet content.

### Sample Data 📝

#### Trump.csv 🦅

| user             | text 📝                                                                                 |
|------------------|----------------------------------------------------------------------------------------|
| manny_rosen      | @sanofi please tell us how many shares the Crown Prince owns? 🤔                   |
| osi_abdul        | https://t.co/atM98CpqF7 Like, comment, RT #MAGA 🇺🇸                                 |
| Patsyrw          | Your AG Barr is as useless &amp; corrupt as ever... 😡                                |
| ScoobyMcpherson | This is the moment when Trump shows true leadership! 🇺🇸✨                            |
| bjklinz         | I’m sorry, Donald. No. #POTUS 🚫🗳️                                                        |

#### Biden.csv 🗳️

| user             | text 📝                                                                                         |
|------------------|------------------------------------------------------------------------------------------------|
| MarkHodder3     | @JoeBiden And we’ll find out who won in 2026... 🗳️🤔                                       |
| K87327961G      | @JoeBiden Your Democratic Nazi Party cannot be trusted... 😠                                |
| OldlaceA        | @JoeBiden So did Lying Barr... 😤                                                              |
| meryn1977       | @JoeBiden You'll just try to calm those waters... 🌊✌️                                       |
| BSNelson114     | @JoeBiden 96 days 96 dias #VoteJoeBiden2020 🇺🇸🗳️                                              |

---

## Methodology

### 1. Data Preprocessing

- **Loading the Data**: Import CSV files containing tweets for each candidate.
- **Initial Inspection**: View sample tweets to understand data structure.
- **Cleaning**: (Optional in this context) Remove URLs, mentions, special characters, and emojis if necessary during preprocessing.

### 2. Sentiment Analysis with TextBlob

The core of our analysis uses the **TextBlob** library, which provides a straightforward API for sentiment detection.

- **Polarity**: Measures the sentiment of a tweet.
  - Range: [-1.0, 1.0]
  - > 0: Positive sentiment
  - < 0: Negative sentiment
  - = 0: Neutral sentiment

- **Subjectivity**: Measures opinionated content.
  - Higher values indicate more subjective tweets.

### 3. Sentiment Classification

- Calculate the sentiment polarity for each tweet.
- Assign labels based on polarity:
  - `positive` if polarity > 0
  - `negative` if polarity < 0
  - `neutral` if polarity = 0 (later filtered out for clarity)

### 4. Data Filtering & Balancing

- Remove neutral tweets to focus on clear sentiment indicators.
- Balance datasets to ensure equal representation for both candidates, preventing bias.

### 5. Sentiment Distribution Analysis

- Count and calculate the percentage of positive and negative tweets per candidate.
- Use these proportions to infer public support.

### 6. Visualization

- Generate bar plots comparing positive and negative sentiments for Trump and Biden.
- Visual aids help in quickly understanding public opinion trends.

---

## Results & Insights

Based on the sentiment analysis:

- **Trump**:
  - Approximately **55% positive** tweets.
  - Approximately **45% negative** tweets.

- **Biden**:
  - Approximately **61% positive** tweets.
  - Approximately **39% negative** tweets.

These results suggest a more favorable online sentiment towards Biden during the analyzed period, which could correlate with voter support.

---

## Visualizations

Using Plotly, we present grouped bar charts comparing sentiment proportions.

---

## Conclusion

This project demonstrates how social media sentiment analysis can serve as an auxiliary tool in political forecasting. While it's not definitive, the public mood reflected in tweets provides valuable insights into electoral dynamics. Incorporating more sophisticated NLP models and temporal analysis can further enhance prediction accuracy.

---

## Future Work

- Implement advanced models like VADER, BERT, or RoBERTa for improved sentiment detection.
- Analyze sentiment trends over time to observe shifts approaching the election.
- Incorporate additional social media platforms (Facebook, Reddit) for broader coverage.
- Explore correlation between tweet volume, engagement metrics, and polling data.

---

## References

- [TextBlob Documentation](https://textblob.readthedocs.io/en/dev/)
- [Natural Language Processing Fundamentals](https://nlp.stanford.edu/)
- [Sentiment Analysis Techniques](https://monkeylearn.com/blog/sentiment-analysis/)

---
