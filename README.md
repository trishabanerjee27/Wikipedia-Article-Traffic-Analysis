# DATA-512 Homework 1: Wikipedia Article Traffic Analysis

## Project Goal
The goal of this project is to construct, analyze, and publish a dataset of monthly article traffic for a set of pages from English Wikipedia related to rare diseases. The data spans from July 1, 2015, to September 30, 2024, and is sourced from the Wikimedia Pageviews API. This analysis is part of a homework assignment for the course DATA-512: Professionalism & Reproducibility.

## Source Data License and Terms of Use
The data used in this project is sourced from the Wikimedia Foundation's public API. The dataset adheres to Wikimedia's [Terms of Use](https://foundation.wikimedia.org/wiki/Policy:Terms_of_Use), and it is licensed under the Creative Commons Attribution-ShareAlike 4.0 License ([CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/)). According to the license, the data can be shared and adapted, provided appropriate attribution is given, and any derivative work is distributed under the same license.

## API Documentation
The data for this project was acquired from the following API:
- [Wikimedia Pageviews API](https://doc.wikimedia.org/generated-data-platform/aqs/analytics-api/reference/page-views.html): Provides access to desktop, mobile web, and mobile app traffic data starting from July 2015 through the most recent month.

## Folder Structure
The project files are organized in the following structure:

DATA-512-HOMEWORK_1/
```
│
├── data/
│   ├── rare-disease_cleaned.AUG.2024.csv
│   ├── rare-disease_monthly_cumulative_201507-202409.json
│   ├── rare-disease_monthly_desktop_201507-202409.json
│   └── rare-disease_monthly_mobile_201507-202409.json
│
├── images/
│   ├── Articles with Fewest Months of Data (Desktop and Mobile).png
│   ├── Max and Min Average Page Requests Over Time.png
│   └── Top 10 Peak Page Views Over Time (Desktop and Mobile).png
│
├── src/
│   ├── data_acquisition.ipynb
│   └── data_analysis.ipynb
│
├── LICENSE
└── README.md
```




### Description of Files and Folders

- **data/**: This folder contains the datasets generated through data acquisition and cleaning processes.
    - `rare-disease_cleaned.AUG.2024.csv`: A cleaned CSV file containing metadata and monthly traffic data for Wikipedia articles on rare diseases.
    - `rare-disease_monthly_cumulative_201507-202409.json`: JSON file containing cumulative monthly traffic data for desktop and mobile combined.
    - `rare-disease_monthly_desktop_201507-202409.json`: JSON file containing monthly traffic data for desktop users.
    - `rare-disease_monthly_mobile_201507-202409.json`: JSON file containing monthly traffic data for mobile users.

- **images/**: Contains the visualizations generated during data analysis:
    - `Articles with Fewest Months of Data (Desktop and Mobile).png`: A plot showing the articles with the fewest months of available data.
    - `Max and Min Average Page Requests Over Time.png`: A plot illustrating the maximum and minimum average page requests over time across all articles.
    - `Top 10 Peak Page Views Over Time (Desktop and Mobile).png`: A plot showing the top 10 articles with the highest peak page views.

- **src/**: Contains Jupyter notebooks used for data acquisition and analysis:
    - `data_acquisition.ipynb`: Notebook containing the code for collecting data using the Wikimedia API.
    - `data_analysis.ipynb`: Notebook used to process the data, perform analysis, and generate visualizations.

## Data Files

### Input Data:
1. `rare-disease_cleaned_AUG_2024.csv`: A cleaned dataset with metadata and monthly traffic for selected Wikipedia articles.
2. `rare-disease_monthly_cumulative_201507-202409.json`: Cumulative traffic data combining mobile and desktop page views.
3. `rare-disease_monthly_desktop_201507-202409.json`: Desktop traffic data.
4. `rare-disease_monthly_mobile_201507-202409.json`: Mobile traffic data.

### Output Data:
1. **Articles with Fewest Months of Data (Desktop and Mobile).png**: A visualization of articles with the least amount of data.
2. **Max and Min Average Page Requests Over Time.png**: Visualization showing maximum and minimum average page requests over time.
3. **Top 10 Peak Page Views Over Time (Desktop and Mobile).png**: A plot displaying the articles with the top 10 peak views over the time period.

## Data Schema
For the JSON data files, the schema is:
- `article_name`: The name of the Wikipedia article.
- `access`: Platform (desktop or mobile).
- `year`: The year of the pageviews data.
- `month`: The month of the pageviews data.
- `views`: The number of pageviews for the article on the specified platform during that month.

For the CSV file:
- `article`: The name of the Wikipedia article.
- `platform`: Desktop or mobile.
- `year_month`: Combined year and month.
- `views`: The number of page views for the article on the specified platform and time period.

## Known Issues & Special Considerations
- **Missing Data**: Some articles are missing data for certain months, which can affect trend analysis.
- **Article Merging**: Certain Wikipedia articles may have been merged or renamed, leading to inconsistencies in traffic data.
- **Traffic Anomalies**: Major events or media coverage may cause spikes in page views, affecting overall trend analysis.

## Code Files
- `data_acquisition.ipynb`: Contains code to retrieve article traffic data from the Wikimedia API.
- `data_analysis.ipynb`: Contains the analysis and visualization steps for the project.

## Documentation and License
- **[MIT License](https://opensource.org/licenses/MIT)**: This project is licensed under the MIT License for the code used in the repository.
- **[Wikimedia Foundation Terms of Use](https://foundation.wikimedia.org/wiki/Policy:Terms_of_Use)**: The Wikimedia data is subject to their terms of use.

## Relevant Links
- [Wikimedia Pageviews API](https://doc.wikimedia.org/generated-data-platform/aqs/analytics-api/reference/page-views.html)
- [The Practice of Reproducible Research](http://www.practicereproducibleresearch.org/core-chapters/2-assessment.html)
- [National Organization for Rare Diseases (NORD)](https://rarediseases.org)
