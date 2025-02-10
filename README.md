# Eventbrite Data Scraper

This project scrapes event data from **Eventbrite** and saves the extracted information into an Excel file. The scraper uses **Selenium, BeautifulSoup, and Pandas** to fetch and process event details.

## Features
- Extracts event names, descriptions, dates, venues, organizers, and ticket prices.
- Downloads and saves event thumbnail images.
- Stores data in an **Excel** file.

## Requirements
Ensure you have **Python 3.x** installed and set up.

### Install Dependencies
Run the following command to install the required dependencies:
```bash
pip install -r requirements.txt
```

## ChromeDriver Setup
This scraper uses **Selenium WebDriver** with Google Chrome. You need to install **ChromeDriver** that matches your **Chrome browser version**.

### **1. Check Your Chrome Version**
- Open Google Chrome.
- In the address bar, type:
  ```
  chrome://settings/help
  ```
- Note down your **Chrome version** (e.g., `133.0.6943.59`).

### **2. Download Matching ChromeDriver**
- Go to the Chrome for Testing downloads page:  
  [https://googlechromelabs.github.io/chrome-for-testing/](https://googlechromelabs.github.io/chrome-for-testing/)
- Find the version matching your **Chrome version** and download the appropriate **ChromeDriver**.
- Extract the downloaded file and move **chromedriver.exe** to a suitable directory (e.g., `C:/webdrivers/`).

### **3. Update the Script with ChromeDriver Path**
Modify the script to use your ChromeDriver path:
```python
service = Service('C:/webdrivers/chromedriver.exe')
driver = webdriver.Chrome(service=service)
```

## How to Run the Scraper
1. Ensure you have installed dependencies and ChromeDriver.
2. Run the script:
   ```bash
   python app.py
   ```
3. The extracted data will be saved in **eventbrite_data.xlsx**.

## Output
- **Excel file**: Contains event details.
- **Images**: Downloaded event images saved in `eventbrite_images/` folder.

## Notes
- You may need to update **ChromeDriver** when Chrome updates.
- Adjust `time.sleep()` values in the script if pages load too slowly.

### **Enjoy scraping! 🚀**
