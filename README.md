# Dept Faculty Scraper

## Overview

This is a simple and handy web app that helps you fetch and view faculty member names from different departments at **MSRIT** (Ramaiah Institute of Technology). Whether you're a student looking for faculty info or just curious, this tool scrapes the official department pages using **Selenium**, caches the results, and displays them through a clean **Flask** web interface.

## Features

- **DepartmentS:** Search for faculty lists by entering a supported department name.
- **Local Caching:** Saves previously fetched results in a local file (`data.json`) so future lookups are faster.
- **Live Scraping:** If a department’s data isn’t cached, it automatically visits the MSRIT site to fetch it.
- **Simple Web Interface:** Enter a department name in a form and get a neatly displayed list of faculty.
- **Fast Response:** Reuses cached data whenever available to keep things quick.

## How It Works

1. On the homepage, enter a department name (e.g., `cse`, `ece`, etc.).
2. The app checks if that department’s faculty list is already cached in `data.json`.
3. If not found, it launches **headless Chrome** with **Selenium**, scrapes the department page, and pulls faculty names.
4. The scraped data is saved for future use, and displayed on the page.
5. If something goes wrong, like a wrong department name or a website issue, the app lets you know.

## Supported Departments

The app only works with certain departments. Here’s the list you can choose from:

- aerospace
- architecture
- aids
- aiml
- cse
- ise
- biotech
- me
- chemical
- chemistry
- civil
- cse aiml
- cyber
- eiess
- eee
- ece
- humanities
- iem
- maths
- mba
- mca
- medical electronics
- physics
- ete

_Make sure to type the department name exactly as shown above (e.g., `cse`, not `CSE`)._

## Technologies Used

- **Python:** Powered by Flask for the web server.
- **Selenium:** Automates Chrome to scrape department pages.
- **webdriver_manager:** Takes care of downloading and managing the right ChromeDriver version.
- **HTML with Jinja2:** Renders the frontend template dynamically.

## Setup and Usage

### 1. Clone the Repository

```bash
git clone https://github.com/hrishikeshChandi/dept-faculty-scraper.git
cd dept-faculty-scraper
```

### 2. Install Dependencies

Make sure you have **Python 3.7+** installed, then run:

```bash
pip install -r requirements.txt
```

### 3. Run the App

```bash
python main.py
```

The app will start at `http://localhost:8000`.

### 4. Use the App

- Open your browser and go to `http://localhost:8000`.
- Enter a department name (see supported list above).
- Submit the form to view the list of faculty members.
- If it’s your first time requesting that department, it may take a few seconds to fetch.

## Project Structure

- `main.py` – Core logic: runs the Flask server and handles scraping.
- `templates/index.html` – HTML form and results display.
- `data.json` – Auto-generated file that stores cached faculty data.
- `requirements.txt` – Python packages you need to install.
- `README.md` – This documentation.

## Notes

- **Chrome browser** must be installed on your machine.
- The app uses **headless Chrome**, so everything runs in the background.
- If the structure of MSRIT’s site changes, scraping might break – but that can be fixed by updating the logic in `main.py`.
- This is a personal/educational project. Always respect website scraping policies and terms of use.

## License

This project is licensed under the MIT License
