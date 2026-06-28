# DOT-AND-KEY---BRAND-HEALTH-AND-CUSTOMER-SENTIMENT-ANALYSIS
# Dot & Key — Brand Health & Customer Sentiment Analysis
### A Data Analytics Project by Kanishka Kumari

---

## Project Summary

This is an unsolicited data analytics project built to demonstrate real-world analytical thinking to **Dot & Key**, one of India's fastest-growing D2C skincare brands. The project involved scraping 1,000 real customer reviews from their Google Play Store app, processing and analysing the data in Python, and presenting findings through an interactive 4-page Power BI dashboard — all built in a single day.

**The core question this project answers:**
> *"What are real customers saying about Dot & Key — and what does the data tell us about where the brand is winning and losing?"*

---

## Tools & Technologies

| Tool | Purpose |
|---|---|
| Python (Google Colab) | Web scraping, data cleaning, feature engineering |
| google-play-scraper | Scraped 1,000 reviews from Google Play Store |
| Pandas | Data transformation, keyword analysis, CSV export |
| Power BI Desktop | Interactive 4-page dashboard with DAX measures |
| DAX | Custom measures for sentiment %, reply rate, filters |

---

## Data Collection

- **Source:** Dot & Key's official Google Play Store app (`com.dotandkey`)
- **Method:** Python `google-play-scraper` library run in Google Colab
- **Volume:** 1,000 reviews (newest first, Aug 2025 – Jun 2026)
- **Fields collected:** Review text, star rating, date, brand reply, reply date, app version

> Note: Flipkart and the brand's own website were attempted first but blocked by bot protection. Google Play Store provided cleaner and more reliable data.

---

## Data Processing & Feature Engineering

**Sentiment Classification**
Each review classified by star rating:
- Positive → 4 or 5 stars
- Neutral → 3 stars
- Negative → 1 or 2 stars

**Theme Tagging**
Reviews tagged across 4 business themes using keyword matching:
- Delivery & Orders
- App Experience
- Customer Service
- Product Quality

A single review could be tagged with multiple themes to capture full context.

**Keyword Frequency Analysis**
Top 20 keywords extracted from positive and negative reviews separately after removing stopwords — revealing what customers love vs. what frustrates them most.

**Month Column**
YYYY-MM format derived from the date field for time-series trend analysis in Power BI.

---

## Dashboard Structure

The final Power BI dashboard has 4 pages with navigation buttons:

**Page 1 — Executive Summary**
KPI cards showing Total Reviews (1,000), Positive % (53%), Negative % (43.8%), Neutral % (3.2%). Monthly sentiment trend line chart from Sep 2025 to Jun 2026. Sentiment distribution donut chart.

**Page 2 — What Are Customers Complaining About?**
Horizontal bar chart of top customer pain points across 4 themes. Delivery & Orders leads at 395 mentions — nearly 2x more than any other category. Key insight text box summarising the finding.

**Page 3 — How Well Does Dot & Key Listen?**
KPI cards showing Total Replied (656), Reply Rate % (65.6%), Negative Reviews Replied (327), Positive Reviews Replied (308). Reveals 111 negative reviews went completely unanswered.

**Page 4 — Customer Complaints: In Their Own Words**
Table of most critical negative reviews with full review text, date, and sentiment. Real customer voices making the data human and actionable for the brand team.

---

## Key Findings

| Metric | Value |
|---|---|
| Total Reviews | 1,000 |
| Positive Sentiment | 53.0% |
| Negative Sentiment | 43.8% |
| Neutral Sentiment | 3.2% |
| Brand Reply Rate | 65.6% |
| Negative Reviews Unanswered | 111 of 438 |
| Top Pain Point | Delivery & Orders (395 mentions) |
| 2nd Biggest Issue | App Experience (217 mentions) |

---

## Insights

- Customers genuinely love Dot & Key's products — "good", "love", "amazing", "sunscreen", "skin results" dominate positive reviews. The formulations work.
- But customers are being lost at the delivery stage — 395 negative mentions around orders not arriving, no tracking updates, and wrong items received.
- App experience is the 2nd biggest issue — login failures, order tracking bugs, and UI issues are hurting retention.
- A BOGO offer in Aug 2025 triggered a spike in complaints — multiple customers received 1 product instead of 2 with no resolution from support.
- 65.6% reply rate shows active community management but 111 negative reviews went unanswered — a gap that risks long-term brand trust.
- Recent data (Jun 2026) shows improving positive sentiment (123 positive vs 34 negative) — the brand appears to be course-correcting.

**One line summary:**
> *Dot & Key has a strong product — but is losing customers due to operational failures in delivery and app experience.*

---

## Files in This Repository

```
├── README.md                          — This file
├── dotandkey_scraper.ipynb            — Google Colab notebook (scraping + processing)
├── dotandkey_final.csv                — Cleaned dataset (1,000 reviews)
├── DotAndKey_Dashboard.pbix           — Power BI dashboard file
└── DotAndKey_CaseStudy.pdf            — Full project case study PDF
```

---

## How to Run

1. Open `dotandkey_scraper.ipynb` in Google Colab
2. Run all cells in order — scraping takes about 30 seconds
3. Download the generated `dotandkey_final.csv`
4. Open `DotAndKey_Dashboard.pbix` in Power BI Desktop
5. Update the data source to point to your downloaded CSV

---

## About the Analyst

**Kanishka Kumari**
Data Analyst | Power BI | SQL | Python | Data Storytelling

- Email: kanishkaa040104@gmail.com
- LinkedIn: linkedin.com/in/kanishka-kumari04
- GitHub: github.com/KanishkaRana
- Portfolio: kanishkakumari.my.canva.site/dataanalyst2025

---

*This project was built independently as a portfolio piece and unsolicited pitch to Dot & Key. All data scraped is publicly available on Google Play Store.*
<img width="928" height="560" alt="image" src="https://github.com/user-attachments/assets/0f59c1a0-1594-410f-8322-48e94bc82d37" />

