# Bike Shop Transactions Dashboard in Excel
## Project Description

I built this workbook to supplement the Python and SQL projects in my portfolio. Although Excel wasn't covered in the Data Analyst track I recently completed on Dataquest.io, I've used it extensively in my education and various jobs over the last 20+ years.  My goal was to combine the skills I've found to be most useful and have seen in multiple job postings into one worksheet, particularly vlookups, pivot tables, and data visualization, and summarize it all in a visually compelling and interactive dashboard.  

I found the Bike Shop dataset on Kaggle.  As an avid mountain biker, I wanted a bike-related dataset that was not one of the ubiquitous bike-sharing sets. Though there is no information about the source of the data, It appears to be from a bike shop in Australia.  

My main challenges were dealing with incomplete data and formatting the transaction dates.  The Customer Address file  has no customer ID; fortunately the Customer Demographic file does and had all of the information I needed.  I found there are about 127 transactions with no corresponding customer data.  I deleted those rows from the Working Sheet to create a cleaner dashboard, but did not remove them from the source tabs or the original data.  The one major formatting issue was the transaction date.  It is in day, month, year order.  It appears at some point any dates starting with 1-12 were converted to Excel serial and show up as d/m/yyyy, while the rest are general format and in the form d-m-yyyy.  I tried several methods to fix this and ended up using Date and String functions to rearrange the two formats independently. 

Ultimately, I was able to create the kind of analysis and dashboard I wanted, but I have questions about the data.  It is almost too uniform an a lot of ways.  The sales are very steady from month to month, almost perfectly split between online and offline sales, and nearly uniformly divided between bike brands.  While it's possible it is legitimate, I am left wondering if it might have been artificially created.  Unfortunately the user who posted the dataset hasn't responded to the comments that have been posted asking for more information. 

## How to Install and Run the Project
Download and open the file Bike_Shop_Dashboard.xlsx

## How to Use the Project
The main tab is called Dashboard.  All of the slicers and checkboxes affect all tables.  Both multi-select and single-select options are available.  

To view the underlying data, select the Pivot Table tab. The charts are all driven by the pivot tables on that tab, and all pivot tables are sourced from Table1 in the Working Sheet tab.  The transaction table on that tab was copied from the transactions tab, and the rest of the columns are pulled from the other data source tabs using vlookups. 

## Credits
- Thanks to Rohit Sahoo.  I used the dataset from his [Kaggle](https://www.kaggle.com/datasets/rohitsahoo/bicycle-store-dataset) dataset. 
- I took inspiration and learned a few new skills from this  [YouTube video](https://www.youtube.com/watch?v=bjLIA1vSqGs) by Lean Excel Solutions

## License

[GNU General Public License, version 2](https://www.gnu.org/licenses/old-licenses/gpl-2.0.en.html)