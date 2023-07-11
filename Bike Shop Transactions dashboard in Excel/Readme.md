# Bike Shop Dashboard in Excel

## Project Overview
The Bike Shop Dashboard in Excel aims to provide a visually compelling and interactive representation of bike shop sales data. This workbook explores and analyzes the sales data, summarizing it in an intuitive dashboard.

## Installation and setup
To use the Bike Shop Dashboard, follow these steps:
1. Download the file "Bike_Shop_Dashboard.xlsx".
2. Open the downloaded file in Excel.

### Source Data
The "bicycle store dataset" used in this project was obtained from Kaggle.com. You can find the dataset [here](https://www.kaggle.com/datasets/rohitsahoo/bicycle-store-dataset).

### Data Acquisition
The data was directly downloaded from Kaggle.com.

### Data Preprocessing
The original data was provided in four separate CSV files. They were combined into different tabs within an Excel (.xlsx) file. The necessary data for the dashboard was consolidated into a tab called "Working Sheet" using the XLOOKUP() function. The data was converted into a table on this sheet, and additional columns such as "Transaction Month," "Month Name," and "Quarter" were extracted for slicer usage. The "Online" column was transformed from True/False format to "Online" and "Offline" using the IFS() function. Finally, the "Profit" column was calculated as the difference between "List Price" and "Standard Cost."

The main challenges during data preprocessing were handling incomplete data and formatting the transaction dates. The Customer Address file did not have customer IDs, but the Customer Demographic file contained the necessary information. Approximately 127 transactions had no corresponding customer data, which were removed from the Working Sheet to ensure a cleaner dashboard. However, these rows were not deleted from the source tabs or the original data.

Regarding the transaction dates, they were initially in a day-month-year order. Excel misinterpreted dates starting with 1-12 as the day rather than the month, resulting in a dd/mm/yyyy display format. Formulas such as =DATE(YEAR(D6),DAY(D6),(MONTH(D6))) were used to reverse this formatting issue. For the remaining dates displayed as d-m-yyyy, the formula =DATE(RIGHT(D8,4),MID(D8,4,2),LEFT(D8,2)) was used to extract the dates. 
 
## How to Use the Project
The primary tab in the workbook is named "Dashboard." All slicers and checkboxes on this tab affect all tables simultaneously, providing a synchronized experience. Both multi-select and single-select options are available for filtering the data.

To access the underlying data for the dashboard, navigate to the "Pivot Table" tab. The charts in the dashboard are driven by pivot tables found on this tab. All pivot tables source their data from "Table1" in the "Working Sheet" tab. The transaction table on the "Pivot Table" tab is a copy of the transactions tab, while the remaining columns are populated using VLOOKUP() to fetch data from other source tabs.

## Results and evaluation
The analysis and dashboard successfully present the desired insights. However, some concerns arise regarding the data's uniformity. Sales data appears remarkably steady from month to month, with an almost equal split between online and offline sales and a nearly even distribution among bike brands. While this may be legitimate, it raises suspicions of potential artificial creation. Unfortunately, the dataset's provider has not responded to comments requesting further information.

## Visuals
![Dashboard](Visuals/Bike_Dashboard_Screenshot.JPG)

## Future work
Here are some potential areas for future work and enhancements to the Bike Shop Dashboard:

1. Simplify and clean up the dashboard, possibly splitting it into multiple pages. 
2. Data Visualization Enhancements: Experiment with different visualization techniques, styles, or visualization tools such as Power BI to enhance the visual appeal and clarity of the dashboard. Consider incorporating infographics, geographic maps, or interactive data visualizations for a richer user experience.
## Credits
- Dataset: [Bicycle Store Dataset](https://www.kaggle.com/datasets/rohitsahoo/bicycle-store-dataset) by Rohit Sahoo. 
- Inspired by and learned from [Lean Excel Solutions' YouTube video](https://www.youtube.com/watch?v=bjLIA1vSqGs).

## License
[GNU General Public License, version 2](https://www.gnu.org/licenses/old-licenses/gpl-2.0.en.html)

