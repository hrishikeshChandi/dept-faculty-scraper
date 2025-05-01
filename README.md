
# Dept Faculty Scraper

The **Dept Faculty Scraper** is a Flask-based web application that retrieves and displays faculty names for various departments from a specified university website. It uses Selenium for web scraping and a JSON file for caching data locally.

## Features

- User-friendly web interface for selecting a department.
- Retrieves faculty names dynamically using Selenium.
- Caches faculty names in a local `data.json` file for faster subsequent searches.
- Automatically updates the cache when new data is available.

## Prerequisites

Before running the application, ensure that the following are installed:

1. Python 3.7+
2. Google Chrome browser
3. Chrome WebDriver (managed automatically using `webdriver-manager`)

## Installation

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/hrishikeshChandi/dept-faculty-scraper.git
   cd dept-faculty-scraper
   ```

2. **Install Dependencies**:
   Install the required Python libraries using:
   ```bash
   pip install -r requirements.txt
   ```

3. **Set Up ChromeDriver**:
   The application automatically manages ChromeDriver using `webdriver-manager`. Ensure you have Google Chrome installed.

## Usage

1. **Run the Application**:
   Start the Flask server by running:
   ```bash
   python app.py
   ```

2. **Access the Application**:
   Open a web browser and navigate to:
   ```
   http://127.0.0.1:8000
   ```

3. **Search for Faculty**:
   - Enter the department name (e.g., `cse`, `ise`, `ece`, etc.) in the input field.
   - The application will fetch and display the faculty names for the selected department.

## File Structure

- **app.py**: The main Flask application.
- **templates/index.html**: The HTML template for the web interface.
- **data.json**: A local cache file for storing faculty names.

## Supported Departments

The application supports the following departments:

- Aerospace
- Architecture
- AI & DS
- AI & ML
- CSE
- ISE
- Biotechnology
- Mechanical
- Chemical Engineering
- Chemistry
- Civil Engineering
- CSE AI & ML
- Cybersecurity
- EIE
- EEE
- ECE
- Humanities
- IEM
- Maths
- MBA
- MCA
- Medical Electronics
- Physics
- ETE

## How It Works

1. **User Input**:
   - Users input the department name.

2. **Search Process**:
   - The application first checks the `data.json` file for cached data.
   - If the department data is not found or outdated, it uses Selenium to scrape the faculty names from the university website.

3. **Cache Update**:
   - Scraped data is stored in `data.json` for future use.

## Technologies Used

- **Flask**: Backend framework for the web application.
- **Selenium**: Web scraping tool for fetching faculty names dynamically.
- **HTML/CSS**: Frontend interface.
- **JSON**: Local caching mechanism.

## Limitations

- The application relies on the university website's structure. Changes to the website may break the scraper.
- Requires a stable internet connection for scraping.

## License

This project is licensed under the MIT License.

---

Feel free to contribute or raise issues if you encounter any problems!
```