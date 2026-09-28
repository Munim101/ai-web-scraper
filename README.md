# AI Web Scraper

A Streamlit app that scrapes any web page and uses a local LLM (LLaMA 3 via Ollama) to pull out exactly the data you ask for.

**Built with:** Python, Streamlit, Selenium, BeautifulSoup, LangChain, Ollama (LLaMA 3)

## How it works

1. Enter a URL. Selenium opens the page in Chrome and grabs the HTML.
2. BeautifulSoup strips scripts and styles and keeps the readable text.
3. Describe what you want (for example, "all product names and prices").
4. The text is split into chunks and LLaMA 3 extracts the matching data.

## Setup

```bash
pip install -r requirements.txt
# Install Ollama from https://ollama.com, then:
ollama pull llama3
```

Download the ChromeDriver that matches your Chrome version and put `chromedriver.exe` in this folder.

```bash
streamlit run main.py
```

## Files

| File | What it does |
|------|--------------|
| `main.py` | Streamlit UI |
| `scrape.py` | Selenium scraping and HTML cleanup |
| `parse.py` | LLaMA 3 parsing with LangChain |

Author: [Munim Awal](https://munimawal.com)
