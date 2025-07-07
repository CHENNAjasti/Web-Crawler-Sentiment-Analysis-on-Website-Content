# 🕷️ Web Crawler & Sentiment Analysis on Website Content

This project is a complete pipeline for **scraping website content** and performing **sentiment analysis** on the extracted text. It takes an input Excel file containing a list of public website URLs, extracts and cleans the textual data from each page, and computes a sentiment score based on custom-defined word lists.

---

## 📌 Features

- ✅ Reads URLs from an input Excel file (`input.xlsx`)
- ✅ Extracts content from webpages (paragraphs, lists, etc.)
- ✅ Cleans HTML by removing headers, scripts, and irrelevant tags
- ✅ Filters out stop words using `stopwords.txt`
- ✅ Computes sentiment scores using `positive-words.txt` and `negative-words.txt`
- ✅ Outputs cleaned text and sentiment results per website

---

## 📁 Project Structure


---

## 🧪 How It Works

1. **Load Input**  
   The script reads `input.xlsx`, which contains labels (e.g., `site001`) and their corresponding URLs.

2. **Web Scraping**  
   For each URL, HTML content is fetched and parsed using `BeautifulSoup`.

3. **Text Extraction**  
   Extracts visible text from `<p>`, `<li>`, and other relevant tags.  
   Removes headers, scripts, and styling elements.

4. **Preprocessing**  
   Tokenizes the text  
   Removes punctuation, extra spaces, and stop words

5. **Sentiment Analysis**  
   Words are matched against positive and negative lexicons.  
   A simple rule-based formula calculates the sentiment score.

---

## 📊 Output (Example)

| Website Label | URL                         | Sentiment Score | Classification |
|---------------|------------------------------|------------------|----------------|
| site001       | https://example.com/page1    | 5                | Positive       |
| site002       | https://example.com/page2    | -3               | Negative       |

*Note: This is a sample. Actual output may vary based on content and word lists.*

---

## 🚀 Getting Started

### 1. Install Requirements

```bash
pip install -r requirements.txt
