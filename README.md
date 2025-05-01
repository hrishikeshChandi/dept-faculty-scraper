# Dept Faculty Scraper

The **Dept Faculty Scraper** is a Flask-based web app that shows faculty names for different departments. It uses Selenium to get the data and stores it in a JSON file for faster access later.

## Features

- Simple web interface to search by department.
- Uses Selenium to get faculty names from the university site.
- Saves results in a local `data.json` file for faster future searches.
- Updates the saved data when new info is found.

## Prerequisites

Before running the app, make sure you have:

1. Python 3.7 or higher
2. Google Chrome browser
3. Chrome WebDriver (automatically managed by `webdriver-manager`)

## Installation

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/hrishikeshChandi/dept-faculty-scraper.git
   cd dept-faculty-scraper
   ```

2. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Set Up ChromeDriver**:
   Make sure Google Chrome is installed. 

## Usage

1. **Run the Application**:
   ```bash
   python app.py
   ```

2. **Access the Application**:
   Open your browser and go to:
   ```
   http://127.0.0.1:8000
   ```

3. **Search for Faculty**:
   - Type the department name (like `cse`, `ise`, `ece`, etc.) in the input box.
   - The app will show the faculty names for that department.

## File Structure

- **app.py**: The main Flask app.
- **templates/index.html**: The web page layout.
- **data.json**: Stores faculty names locally.

## Supported Departments

The app supports these departments:

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
   - You enter the department name.

2. **Search Process**:
   - The app checks the `data.json` file first.
   - If data is missing or old, it uses Selenium to scrape the site.

3. **Cache Update**:
   - New data is saved in `data.json` for next time.

## Technologies Used

- **Flask**: Web app framework.
- **Selenium**: Tool for web scraping.
- **HTML/CSS**: For the frontend.
- **JSON**: For saving data locally.

## Limitations

- If the university website changes, the scraper might stop working.
- Needs an internet connection to fetch data.

## License

This project is licensed under the MIT License.