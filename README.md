# Web Scraping with Python — Wikipedia Data Extraction

## Overview
This project demonstrates web scraping using Python to extract structured data from a live Wikipedia page. The notebook scrapes the **"List of Largest Companies by Revenue"** Wikipedia table, handles real-world HTML parsing challenges, and builds a clean pandas DataFrame ready for analysis.

---

## What This Project Does

### Target
Wikipedia page: *List of largest companies by revenue*
Extracted fields: **Company Name, Industry, Revenue (USD billions), Profit, Employees, Headquarters**

### Step-by-Step Workflow

1. **Import libraries** — BeautifulSoup (bs4), requests, and pandas
2. **Handle 403 error** — initial request blocked; resolved by adding a custom User-Agent header to mimic a browser request
3. **Parse HTML** — BeautifulSoup selects the main `wikitable sortable` from the page
4. **Extract headers** — table column names cleaned by removing auxiliary caption cells
5. **Handle rowspans** — custom logic tracks active HTML rowspans to correctly fill cells that span multiple rows, ensuring data integrity across all extracted rows
6. **Build DataFrame** — assembled rows converted into a pandas DataFrame with columns: Name, Industry, Revenue, Profit, Employees, Headquarters
7. **Clean columns** — dropped irrelevant columns (Ref., State-owned) and displayed final output

### Sample Output
Top companies extracted include Amazon, Walmart, State Grid Corporation, Saudi Aramco — with revenue figures in USD billions (e.g., Amazon: $716B).

---

## Technologies Used

- **Python**
- **BeautifulSoup (bs4)** — HTML parsing
- **requests** — HTTP requests with custom headers
- **Pandas** — DataFrame construction and manipulation
- **Jupyter Notebook**

---

## Key Challenges Solved

- **403 Forbidden error** — resolved with custom User-Agent header
- **HTML rowspan handling** — manually tracked multi-row cells to prevent data misalignment


---

## Author
**Sawrave Ahmed**
- GitHub: [github.com/Sawrave007](https://github.com/Sawrave007)
- LinkedIn: [linkedin.com/in/sawrave-ahmed007](https://linkedin.com/in/sawrave-ahmed007)
