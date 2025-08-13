# Atliq Hotels Data Analysis Project

## Description
This project analyzes booking data for AtliQo Hotels, a fictional hospitality chain, to derive actionable insights on revenue, occupancy, and booking platform performance. Built using Python, it employs Pandas for data manipulation, Seaborn, and Matplotlib for visualizations, such as revenue distribution by booking platform. The analysis spans properties across cities (Delhi, Mumbai, Hyderabad, Bangalore) and room classes (Standard, Elite, Premium, Presidential) from May to August 2022. Key metrics include occupancy rates, revenue realized, and cancellation trends, enabling strategic decisions like optimizing booking platforms or pricing. This project, part of the Codebasics ML course, showcases descriptive analytics skills for the hospitality industry.

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Features](#features)
- [Analysis Details](#analysis-details)
- [Contributing](#contributing)
- [Contact](#contact)

## Installation
Follow these steps to set up the project locally:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/atliqo-hotels-data-analysis.git
   ```
2. **Navigate to the Project Directory**:
   ```bash
   cd atliqo-hotels-data-analysis
   ```
3. **Create a Virtual Environment**:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```
4. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```
   Required packages:
   - pandas
   - numpy
   - seaborn
   - matplotlib

5. **Ensure Dataset Availability**:
   Place the datasets (`dim_rooms.csv`, `new_data_august.csv`, `dim_hotels.csv`, `dim_date.csv`, `fact_aggregated_bookings.csv`, `fact_bookings.csv`) in the `data/` folder.

## Usage
To explore the data analysis:

1. **Run the Jupyter Notebook**:
   - Open `notebooks/AtliQo Hotels Data Analysis Project.ipynb` in Jupyter Notebook.
   - Execute the notebook to load datasets, perform exploratory data analysis (EDA), and generate visualizations (e.g., revenue by booking platform).
   - Example visualization: Pie chart showing revenue distribution across platforms (direct online, logtrip, tripster, makeyourtrip).

### Example
```python
# Example visualization in the notebook
import pandas as pd
import matplotlib.pyplot as plt
df_booking_all = pd.read_csv("data/fact_bookings.csv")
df_booking_all.groupby("booking_platform")["revenue_realized"].sum().plot(kind="pie")
plt.show()
```

Output:
- Pie chart displaying the proportion of revenue realized from each booking platform (e.g., direct online, makeyourtrip).

## Project Structure
```
atliqo-hotels-data-analysis/
├── data/                                       # Input datasets
│   ├── dim_rooms.csv
│   ├── new_data_august.csv
│   ├── dim_hotels.csv
│   ├── dim_date.csv
│   ├── fact_aggregated_bookings.csv
│   ├── fact_bookings.csv
├── notebooks/                                  # Jupyter Notebook for analysis
│   ├── AtliQo Hotels Data Analysis Project.ipynb
├── requirements.txt                            # Project dependencies
└── README.md                                   # Project documentation
```

## Features
- **Data Integration**: Combines multiple datasets (hotels, rooms, dates, bookings) for comprehensive analysis.
- **Exploratory Data Analysis**: Analyzes revenue, occupancy rates, and booking patterns by city, room class, and platform.
- **Visualizations**: Uses Seaborn and Matplotlib to create charts (e.g., pie chart for revenue by platform, occupancy trends).
- **Metrics**: Calculates occupancy percentages, revenue realized, and cancellation rates to inform business strategies.
- **Data Quality Handling**: Addresses issues like negative guest counts in booking data.

## Analysis Details
- **Datasets**:
  - `dim_rooms.csv`: Maps room IDs (RT1–RT4) to classes (Standard, Elite, Premium, Presidential).
  - `dim_hotels.csv`: Lists 25 properties across Delhi, Mumbai, Hyderabad, and Bangalore, categorized as Luxury or Business.
  - `dim_date.csv`: Covers dates from May to July 2022, with week numbers and day types (weekday, weekend).
  - `fact_bookings.csv`: Detailed booking records with revenue, status (Checked Out, Cancelled, No Show), and platform.
  - `fact_aggregated_bookings.csv`: Aggregated bookings by property, date, and room category.
  - `new_data_august.csv`: August 2022 data for occupancy analysis.
- **Key Insights**:
  - Revenue distribution by booking platform (e.g., direct online vs. makeyourtrip).
  - Occupancy rates by property and city (e.g., Atliq Exotica in Mumbai at 100% on August 1, 2022).
  - Temporal trends (e.g., weekday vs. weekend bookings).
- **Tools**: Python with Pandas for data manipulation, NumPy for numerical operations, Seaborn/Matplotlib for visualizations.

## Contributing
Contributions are welcome! To contribute:

1. Fork the repository.
2. Create a feature branch:
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. Commit your changes:
   ```bash
   git commit -m "Add your feature description"
   ```
4. Push to the branch:
   ```bash
   git push origin feature/your-feature-name
   ```
5. Open a pull request.

Please follow PEP 8 standards and include tests for new features.

## Contact
For questions or feedback, reach out to:
- Mail ID: kavineshdhanush@gmail.com
