# Web Scraper for Wuzzuf Job Listings

## Overview
This project is a web scraper designed to extract job listings for **Data Analyst** roles from Wuzzuf.net. It utilizes **Python**, **requests**, and **BeautifulSoup** to fetch and parse job postings, making it easier to analyze job market trends.

## Features
- Scrapes job postings from Wuzzuf.net.
- Extracts key job details, including:
  - Job title
  - Company name
  - Location
  - Date posted
  - Job type (full-time, part-time, remote, etc.)
  - Salary (if available)
  - Job link for further details
- Supports pagination to scrape multiple pages of job listings.
- Stores extracted data in a structured format using **Pandas**.
- Can export the data into CSV format for further analysis.

## Prerequisites
Ensure you have **Python 3.x** installed on your system and install the required dependencies:

```bash
pip install requests beautifulsoup4 pandas
```

## Installation
1. Clone this repository:
   ```bash
   git clone https://github.com/your-repo/web-scraper-wuzzuf.git
   ```
2. Navigate to the project directory:
   ```bash
   cd web-scraper-wuzzuf
   ```
3. Install dependencies (if not already installed):
   ```bash
   pip install -r requirements.txt
   ```

## Usage
To run the scraper and extract job listings, use the following command:

```python
from scraper import scrape_wuzzuf

data = scrape_wuzzuf(num_pages=5)  # Scrapes 5 pages of job listings
```

### Saving Data to CSV
To save the extracted job listings to a CSV file, use the following:
```python
import pandas as pd

data = scrape_wuzzuf(num_pages=5)
data.to_csv("wuzzuf_jobs.csv", index=False)
print("Data saved to wuzzuf_jobs.csv")
```

## Handling Website Restrictions
- **Respect the website’s terms of service**: Scraping data without permission can violate site policies.
- **Avoid sending too many requests in a short time**: Implementing delays using `time.sleep()` can prevent temporary IP bans.
- **Use headers to mimic a real browser**: Helps in avoiding bot detection.

## Potential Improvements
- Implementing **proxy rotation** to bypass restrictions.
- Adding **multi-threading** to speed up scraping.
- Enhancing data cleaning and structuring.


