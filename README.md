# Testing with Selenium

## Introduction

This project demonstrates automated testing using Selenium WebDriver. It includes test scripts for web applications to ensure functionality, performance, and usability.

## Features
- Automated UI testing using Selenium
- Support for multiple browsers (Chrome, Firefox, Edge)
- Integration with pytest for test execution
- Data-driven testing using CSV or JSON files
- Headless browser testing support
- Logging and reporting using Allure

## Prerequisites
- Python 3.x installed
- Browser drivers installed (ChromeDriver, GeckoDriver, etc.)
- Required Python packages installed

## Installation
Clone the repository and install dependencies:

```sh
# Clone the repository
git clone https://github.com/your-username/testing-with-selenium.git
cd testing-with-selenium

# Create a virtual environment (optional but recommended)
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`

# Install dependencies
pip install -r requirements.txt
```

## Configuration
Ensure that the appropriate web driver is placed in the system PATH or specify its location in the script.

## Running Tests
Execute tests using pytest:

```sh
pytest tests/
```

Run tests with detailed output:

```sh
pytest -v --html=report.html --self-contained-html
```

Run tests in headless mode:

```sh
pytest --headless
```

## Writing Your Own Tests
1. Create a new test file in the `tests/` folder.
2. Import `pytest` and `selenium`.
3. Write test functions using `pytest` format.
4. Use `setup` and `teardown` methods for driver initialization.

Example:

```python
import pytest
from selenium import webdriver

def test_google_search():
    driver = webdriver.Chrome()
    driver.get("https://www.google.com")
    assert "Google" in driver.title
    driver.quit()
```

## Reporting
Generate an HTML report:

```sh
pytest --html=report.html
```

