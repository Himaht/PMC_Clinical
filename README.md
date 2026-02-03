# PMC Table Extractor (Python + pandas) — PubMed Central Article Tables to CSV + Visualizations

This project extracts structured tables from a PubMed Central (PMC) research article and converts them into analysis-ready datasets using **Python** and **pandas**. It also includes basic **matplotlib** visualizations for quick exploratory data analysis (EDA).

**Source article:** https://pmc.ncbi.nlm.nih.gov/articles/PMC11786524/

---

## Why this project
Many real-world analytics problems start with messy data embedded in web pages or documents. This pipeline demonstrates:
- automated data extraction
- data cleaning and transformation with pandas
- reproducible outputs (CSV exports)
- basic EDA and visualization with matplotlib

This is especially useful for data science workflows involving clinical and research literature.

---

## How it works
1. Fetch the full-text XML for the article using **PMC’s supported OAI-PMH service** (more reliable than scraping HTML pages directly).
2. Identify table blocks in the XML (`table-wrap` nodes).
3. Convert each table into a `pandas.DataFrame`.
4. Clean column names and text fields.
5. Export each table to CSV with timestamped filenames.
6. Generate quick visualizations (missingness, distributions, top categories).

---

## Tech Stack
- Python
- pandas
- requests
- BeautifulSoup (XML parsing)
- lxml
- matplotlib

---

## Running in Google Colab (recommended)
This project is designed to run smoothly in **Google Colab**, which avoids local environment and PATH issues.

### 1) Install dependencies
```bash
pip install pandas requests beautifulsoup4 lxml matplotlib
