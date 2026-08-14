# 📚 Books to Scrape — Web Scraping & EDA

> Turning a mock bookstore into a clean, analysis-ready dataset — one `<article>` tag at a time.

![Python](https://img.shields.io/badge/Python-3.x-3776AB?logo=python&logoColor=white)
![BeautifulSoup](https://img.shields.io/badge/BeautifulSoup4-Web%20Scraping-8A2BE2)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Wrangling-150458?logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-11557C)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

## 🗂️ What is this?

This project was built as **Task 1** of the **CodeAlpha Data Analytics Internship**. It scrapes every single book listed on [Books to Scrape](https://books.toscrape.com) — a sandbox e-commerce site built specifically for practicing scraping — and turns the raw HTML into a clean, structured dataset ready for analysis.

No shortcuts, no APIs. Just `requests`, `BeautifulSoup`, and 50 pages of patience.

## ✨ What it does

The pipeline walks through the full data lifecycle, start to finish:

1. **Fetch** — sends HTTP requests to all 50 catalogue pages
2. **Parse** — extracts title, price, stock availability, and star rating for every book using BeautifulSoup
3. **Structure** — loads everything into a pandas DataFrame
4. **Clean** — strips currency symbols, casts prices to numeric types, checks for nulls and duplicates
5. **Explore** — runs summary statistics across the full catalogue
6. **Visualize** — charts rating distribution, price distribution, and average price per rating
7. **Export** — saves the cleaned dataset back out as CSV

## 📊 By the numbers

| Metric | Value |
|---|---|
| Books scraped | **1,000** |
| Pages crawled | **50** |
| Average price | **£35.07** |
| Price range | **£10.00 – £59.99** |
| Fields captured | Title, Price, Availability, Rating |

**Rating breakdown:**

| ⭐ Rating | Count |
|---|---|
| One | 226 |
| Three | 203 |
| Five | 196 |
| Two | 196 |
| Four | 179 |

## 🛠️ Tech Stack

| Tool | Role |
|---|---|
| `requests` | Fetching raw HTML from each page |
| `BeautifulSoup4` | Parsing HTML and extracting book data |
| `pandas` | Structuring, cleaning, and analyzing the dataset |
| `matplotlib` | Visualizing ratings and price trends |

## 📁 Project Structure

```
├── Task1.ipynb                    # Full notebook: scrape → clean → analyze → visualize
├── books_data.csv                 # Sample scrape (page 1 only)
├── books_dataset.csv              # Raw dataset — all 1,000 books, uncleaned
├── books_dataset_cleaned.csv      # Final cleaned dataset, ready for analysis
└── Screenshot *.png                # Output snapshots from the notebook run
```

## 🚀 Getting Started

**1. Clone the repo**
```bash
git clone https://github.com/bsurendrareddy1114-source/codealpha_Web-Scraping-.git
cd codealpha_Web-Scraping-
```

**2. Install dependencies**
```bash
pip install requests beautifulsoup4 pandas matplotlib
```

**3. Run the notebook**
```bash
jupyter notebook Task1.ipynb
```
Run all cells top to bottom — the scraper will hit all 50 pages live, so it needs an internet connection.

## 🔍 Key Insights

- Book prices are fairly spread out, ranging from **£10 to just under £60**, with no single price point dominating the catalogue.
- **One-star** books are surprisingly the most common rating in the dataset — a fun reminder that this is demo data, not real reviews.
- The dataset required minimal cleaning beyond stripping the `£` symbol from prices — a good first project for practicing the full scrape-to-insight workflow without getting stuck on messy edge cases.

## 🎯 Skills Demonstrated

- HTTP requests & pagination handling
- HTML parsing with BeautifulSoup
- Data cleaning (regex-based text stripping, type casting)
- Exploratory Data Analysis with pandas
- Data visualization with matplotlib
- End-to-end pipeline thinking, from raw HTML to insight-ready CSV

## 🙌 Acknowledgements

Built during the **CodeAlpha Data Analytics Internship**, using [Books to Scrape](https://books.toscrape.com) — a purpose-built sandbox site for scraping practice.

---

*If you found this useful, consider ⭐ starring the repo!*
