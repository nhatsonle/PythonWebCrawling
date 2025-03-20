# VN News Web Crawler

This repository contains a Python-based automated web crawler designed to scrape news articles from the "Vietnamnet" website, specifically from the "Thời Sự" section. The project uses Selenium for web automation and includes a structured process for extracting article titles, abstracts, main content, and authors, and saves the data in a text format for further analysis.

## Features
- Automatically navigates and scrapes content from multiple pages of the "Thời Sự" section on Vietnamnet.
- Extracts article details including:
  - Title
  - Abstract
  - Main content (article body)
  - Author (if available)
- Excludes video-only articles.
- Saves scraped data as text files in a structured folder.

## Installation

### Prerequisites
1. Python 3.7 or later
2. Google Chrome Browser
3. ChromeDriver compatible with your Chrome version

### Install Dependencies
Install the required Python packages using pip:
```bash
pip install selenium pandas tqdm
```


## Usage

### Step 1: Setup ChromeDriver
Ensure ChromeDriver is installed and accessible in your system's PATH. You can download the appropriate version from [ChromeDriver Downloads](https://sites.google.com/a/chromium.org/chromedriver/downloads).

### Step 2: Run the Script
1. Clone this repository:
```bash
git clone https://github.com/your-username/vn_news_crawler.git
cd vn_news_crawler
```
2. Run the script:
```bash
python vn_news_crawler.py
```

### Output
- The script creates a folder named `vn_news corpus` in the current working directory.
- Each scraped article is saved as a `.txt` file with the naming format `article_<ID>.txt`.
- Each file contains the article's title, abstract, content, and author, separated by blank lines.

## Customization
- **Number of Pages:**
  Change the `n_pages` variable in the script to specify the number of pages to scrape.

- **Save Directory:**
  Modify the `root_dir` variable to change the output folder location.

## Notes
- **Headless Mode:**
  The script uses Chrome's headless mode to run without opening a browser window. You can disable it by commenting out or removing the `--headless=new` argument in `chrome_options`.

- **Politeness:**
  The script includes a `time.sleep(1)` delay to avoid overwhelming the server. Consider increasing the delay if you experience connection issues or to comply with the website's terms of service.

- **Error Handling:**
  The script skips articles without valid content or those that are video-only.

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.

## Acknowledgments
- [Selenium Documentation](https://www.selenium.dev/documentation/)
- [Vietnamnet](https://vietnamnet.vn/) for providing the data source.

