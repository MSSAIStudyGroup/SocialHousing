# Trustpilot Housing Reviews Analysis

[![License: CC0-1.0](https://img.shields.io/badge/License-CC0_1.0-lightgrey.svg)](https://github.com/MSSAIStudyGroup/SocialHousing/blob/main/LICENSE)
![Python Version](https://img.shields.io/badge/python-3.8%2B-blue)

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
  - [Data Extraction](#data-extraction)
  - [Classification](#classification)
- [Dependencies](#dependencies)
- [Configuration](#configuration)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Overview

The **Trustpilot Housing Reviews Analysis** project aims to extract and analyze Trustpilot reviews for various housing providers. The project consists of two main components:

1. **Data Extraction**: Automates the retrieval of Trustpilot reviews for specified housing providers.
2. **Classification**: Processes and classifies the extracted reviews to identify key issues and sentiment trends.

This analysis helps in understanding tenant satisfaction, common complaints, and areas requiring improvement for housing providers.

An external link to the report accompanying this project can be found here: MSS REPORT LINK WHEN PUBLISHED.

## Features

- **Automated Data Extraction**: Scrapes Trustpilot reviews for selected housing providers.
- **Data Cleaning and Preprocessing**: Cleans the extracted data for accurate analysis.
- **Text Classification**: Categorizes reviews into predefined categories (e.g., Maintenance, Customer Service).
- **Sentiment Analysis**: Determines the overall sentiment of each review.
- **Comprehensive Reporting**: Generates summary reports and visualizations of findings.

## Project Structure

```
trustpilot-housing-reviews-analysis/
│
├── data/
│   ├── raw/                 # Raw extracted data
│   ├── processed/           # Cleaned and processed data
│
├── notebooks/
│   ├── Data_Extraction.ipynb
│   ├── Classification.ipynb
│
├── src/
│   ├── extraction/
│   │   ├── scraper.py       # Script for scraping Trustpilot reviews
│   │   └── utils.py         # Utility functions for data extraction
│   │
│   ├── classification/
│   │   ├── classifier.py    # Script for classifying reviews
│   │   └── preprocess.py    # Data preprocessing for classification
│   │
│   └── visualization/
│       ├── report.py        # Script to generate reports and visualizations
│       └── charts.py        # Helper functions for creating charts
│
├── tests/
│   ├── test_scraper.py
│   ├── test_classifier.py
│   └── test_utils.py
│
├── requirements.txt         # Python dependencies
├── README.md
├── LICENSE
└── .gitignore
```

## Installation

### Prerequisites

- **Python 3.8+**: Ensure you have Python installed. You can download it [here](https://www.python.org/downloads/).

### Clone the Repository

```bash
git clone https://github.com/yourusername/trustpilot-housing-reviews-analysis.git
cd trustpilot-housing-reviews-analysis
```

### Create a Virtual Environment

It's recommended to use a virtual environment to manage dependencies.

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

## Usage

### Data Extraction

The data extraction component scrapes Trustpilot for reviews related to specified housing providers.

#### Configure Housing Providers

Edit the `src/extraction/scraper.py` file to specify the housing providers you want to analyze.

```python
# Example
housing_providers = [
    "msvhousing",
    "clarionhousing",
    "onehousing",
    "onward",
    "yourhousinggroup",
    "jigsawhomes",
    "placesforpeople",
    "guinnesspartnership"
]
```

#### Run the Scraper

You can run the scraper using the provided script or via a Jupyter notebook.

**Using the Script:**

```bash
python src/extraction/scraper.py
```

**Using the Jupyter Notebook:**

Open `notebooks/Data_Extraction.ipynb` and run the cells sequentially.

### Classification

The classification component processes the extracted reviews and categorizes them based on predefined criteria.

#### Preprocess the Data

Ensure that the data is cleaned and preprocessed before classification.

```bash
python src/classification/preprocess.py
```

#### Run the Classifier

Execute the classification script to categorize the reviews.

```bash
python src/classification/classifier.py
```

**Using the Jupyter Notebook:**

Open `notebooks/Classification.ipynb` and run the cells sequentially.

### Generate Reports

After classification, generate comprehensive reports and visualizations.

```bash
python src/visualization/report.py
```

## Dependencies

All required Python packages are listed in `requirements.txt`. Key dependencies include:

- **BeautifulSoup4**: For web scraping.
- **Selenium**: For browser automation (if needed).
- **pandas**: Data manipulation and analysis.
- **scikit-learn**: Machine learning for classification.
- **NLTK / SpaCy**: Natural language processing.
- **Matplotlib / Seaborn**: Data visualization.
- **Jupyter Notebook**: Interactive development.

To install all dependencies:

```bash
pip install -r requirements.txt
```

## Configuration

### Trustpilot Access

Depending on the Trustpilot scraping approach, you might need:

- **API Access**: If using Trustpilot's API, ensure you have the necessary API keys.
- **WebDriver Setup**: If using Selenium, download the appropriate WebDriver (e.g., ChromeDriver) and ensure it's in your system's PATH.

### Environment Variables

Create a `.env` file in the root directory to store sensitive information like API keys.

```env
TRUSTPILOT_API_KEY=your_api_key_here
```

Ensure to load these variables in your scripts using packages like `python-dotenv`.

## Contributing

Contributions are welcome! Please follow these steps:

1. **Fork the Repository**
2. **Create a Feature Branch**

   ```bash
   git checkout -b feature/YourFeature
   ```

3. **Commit Your Changes**

   ```bash
   git commit -m "Add some feature"
   ```

4. **Push to the Branch**

   ```bash
   git push origin feature/YourFeature
   ```

5. **Open a Pull Request**

## License

This project is licensed under the CC0-1.0 (LICENSE).

## Contact

For any questions or suggestions, please open an issue or contact [guy@fuza.co.uk](mailto:guy@fuza.co.uk).

---

*Disclaimer: This project is not affiliated with Trustpilot or any of the housing providers mentioned. It is intended for educational and analytical purposes only.*
