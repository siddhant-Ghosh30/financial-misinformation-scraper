# Financial Misinformation Scraper

## 📌 Overview

This project scrapes financial misinformation fact-check articles from multiple websites and converts them into a structured dataset.

The goal is to identify and analyze patterns in financial scams, fake investment schemes, and misleading claims circulating online.

This is part of the ongoing research at the TAPMI-Max Planck partner group.

---

## 🚀 Features

* Scrapes articles from multiple fact-checking platforms
* Supports both:

  * Direct article URLs
  * Listing/search pages (bulk extraction)
* Extracts structured fields:

  * Institution
  * Scam Vector
  * Misinformation Type
  * Core Claim
  * Original Post
  * Image Text
  * Image URL
* Uses NLP (spaCy) for entity detection
* Includes data quality filtering

---

## 🧰 Tech Stack

* Python
* BeautifulSoup
* Newspaper3k
* spaCy
* Pandas

---

## ⚙️ Setup Instructions

### 1. Clone the repository

```bash
git clone https://github.com/siddhant-Ghosh30/financial-misinformation-scraper.git
cd financial-misinformation-scraper
```

### 2. Create virtual environment

```bash
python3 -m venv venv
source venv/bin/activate   # Mac
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
python -m spacy download en_core_web_sm
```
or
```bash
pip install newspaper3k pandas beautifulsoup4 lxml spacy jupyter
pip install lxml_html_clean
```
---

## ▶️ Usage

1. Open `scraper.ipynb`
2. Add URLs in:

```python
seed_urls = [
    ...
]
```

3. Run the script

Output:

```
financial_misinfo_dataset.csv
```

---

## 📊 Output Format

| Column         | Description               |
| -------------- | ------------------------- |
| Institution    | Entity being impersonated |
| Scam_Vector    | Medium of scam            |
| Misinfo_Type   | Type of misinformation    |
| Core_Claim     | False claim extracted     |
| Original_Tweet | Source post               |
| Image_Text     | Text in image             |
| Image_URL      | Image link                |

---

## ⚠️ Limitations

* Heuristic-based extraction (not perfect)
* Some websites may block scraping
* Image text is approximated (no OCR)

---

## 🔮 Future Improvements

* Use LLM for better claim extraction
* Add OCR for image text
* Improve classification accuracy
* Scale scraping with async pipelines

---

## 👤 Author

Siddhant Ghosh
