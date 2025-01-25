# Scrapers Collection

This repository contains a collection of scrapers built with Python, designed to collect and process data from various web sources. They are primarily implemented in Jupyter notebooks and are structured to be flexible and reusable.

## Contents

1. **AlpacaScraper.ipynb**  
   - **Main Function**: Collects information from websites related to Alpaca businesses, extracts information about possible leads and clients from alpacainfo.com.
   - **Data Collected**:
     - Name
     - Address
     - Phone number
     - Website
     - Emails (if available)
   - **Output**: An Excel file (`alpacaInfoScrappingCompletedjustScrap.xlsx`) containing the structured data.

2. **videoRecognitionScraper.ipynb**  
   - **Main Function**: Retrieves URLs for downloading videos, used to train an object identification model.
   - **Data Collected**:
     - Video file names
     - Download links
   - **Output**: Four text files (`file_part_1.txt`, `file_part_2.txt`, `file_part_3.txt`, `file_part_4.txt`) that divide the collected links into batches.

   - **Technical Notes**:
     - Uses Selenium with a headless Chrome browser to interact with the webpage.
     - Includes steps to accept terms of use and load all available items on the page.
     - Requires `chromedriver` configured to function correctly.

3. **TripAdvisorScrapper.ipynb**  
   Incomplete, but tries to get contact information about restaurants close to a zone.


## Requirements

- **Python** 3.10+

### Libraries used:
- `pandas`
- `requests`
- `BeautifulSoup4`
- `brotli`
- `openpyxl`
- `selenium`
- `webdriver-manager`

## Usage Instructions

1. Open the desired notebook in Jupyter Notebook or JupyterLab.
2. Configure the required variables in the initial cells (e.g., target URLs).
3. Execute the cells in the given order to perform the scraping and generate results.
4. The extracted data will be saved in an Excel file or text files as appropriate.
