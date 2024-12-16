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

- **Funding** This project was funded by a Campion Grant awarded by Manchester Statistical Society. See https://manstatsoc.org/ for more information.
- **Report** An external link to the report accompanying this project can be found here: MSS REPORT LINK WHEN PUBLISHED.

## Features

- **Automated Data Extraction**: Scrapes Trustpilot reviews for selected housing providers.
- **Data Cleaning and Preprocessing**: Cleans the extracted data for accurate analysis.
- **Text Classification**: Categorizes reviews into predefined categories (e.g., Maintenance, Customer Service).
- **Reporting**: Generates summary reports and visualizations of findings.

## Project Structure

```
SocialHousing/
│
├── Housing Association Review Classification and Theme Visualization.ipynb  #  Notebook for classifying reviews and visualizing themes in housing association data.
├── Keyword Analysis 1 Star Reviews.ipynb  #  Notebook for analyzing keywords within 1 star housing association reviews.
├── LICENSE  #  Project license file.
├── README.md  #  Repository overview, setup instructions, and usage guidelines.
├── Themes2D.xlsx  #  Excel file containing theme data, with keywords for HACT UK Data Standards classes, for visualization and further analysis.
├── Trustpilot Review Single Page Extractor.ipynb  #  Notebook for scraping reviews from a single Trustpilot page.
└── Trustpilot Review Extraction Compilation.ipynb  #  Notebook for systematically extracting across multiple Trustpilot pages.

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

Edit the extraction.py file to specify the housing providers you want to analyze.

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

#### Run the Data Extraction Tool

You can run the data extraction tool using the provided script or via a Jupyter notebook.

**Using Jupyter Notebook:**

Open `Trustpilot Review Extraction Compilation.ipynb` and run the cells sequentially.

### Classification

The classification component processes the extracted reviews and categorizes them based on predefined criteria.

**Using Jupyter Notebook:**

Open `Housing Association Review Classification and Theme Visualization.ipynb` and run the cells sequentially.

## Dependencies

Required Python packages are:

- **Requests**: HTTP library for web scraping.
- **BeautifulSoup4**: Web scraping.
- **pandas**: Data manipulation and analysis.
- **scikit-learn**: Machine learning for classification.
- **Matplotlib**: Data visualization.
- **Seaborn**: Data visualization.
- **Jupyter Notebook**: Interactive development.

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
