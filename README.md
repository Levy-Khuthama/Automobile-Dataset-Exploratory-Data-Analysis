# Automobile-Dataset-Exploratory-Data-Analysis
Cleaning and exploring the classic Automobile dataset (205 cars, 26 attributes) with pandas, matplotlib and seaborn to answer questions about price, fuel economy, engine size and manufacturers.

This project was completed as part of the Artificial Intelligence online bootcamp (Stellenbosch University in partnership with HyperionDev).

What's inside
File	Description
automobiles.ipynb	Full notebook: data cleaning, categories, and the visualisations
EDA_Report_Automobile_Dataset.pdf	Written report summarising the findings with charts
report_figures/	The charts produced by the notebook, saved as PNG files
Dataset

The Automobile dataset describes cars by make, body style, drive type, dimensions, engine details, fuel economy (city and highway MPG) and price. Missing values are stored as ?, which the notebook reads as NaN. The data file (automobile.txt) is not included in this repo; add it next to the notebook to run it.

Data cleaning
Dropped the redundant normalized-losses and symboling columns.
Checked for duplicate rows (none were found).
Removed 12 rows with missing values, leaving 193 cars and 24 columns.
Converted numeric columns to appropriate types: floats for continuous measurements and int64 for counts, prices and MPG.
Questions explored
Question	Finding
Which manufacturer is the most fuel efficient?	Chevrolet has the highest average city MPG, but it has only 3 cars in the cleaned data. Jaguar, Mercedes-Benz and Porsche are at the low end.
How does engine size relate to price?	Strong positive relationship (Pearson r = 0.89), with premium brands forming high-priced outliers.
Which are the most expensive cars?	Mercedes-Benz and BMW dominate; the most expensive car is a Mercedes-Benz hardtop at $45,400. Porsche also appears in the top five.
Which cars have the largest engines?	Jaguar and Mercedes-Benz fill most of the top ten, with BMW completing it.
Which manufacturer has the most models?	Toyota (32 cars), then Nissan (18) and Honda/Mitsubishi (13 each). This reflects the dataset, not real-world market share.
How are hatchbacks distributed?	63 hatchbacks, led by Toyota (14) and Mitsubishi (9).
Visualisations

Show Image

Show Image

The full set of six charts is in report_figures/ and in the PDF report.

Key takeaways
Price rises with engine size, but size isn't everything: brand also pushes prices up, which creates the outliers.
The most fuel-efficient manufacturers are mainly makers of small, cheap cars, while the luxury and large-engine brands (Jaguar, Mercedes-Benz, Porsche) have the lowest city MPG.
Rankings by manufacturer depend on how many cars each has in the dataset, so small groups (like Chevrolet) should be read with care.
The cleaned dataset is ready for predictive modelling, such as predicting price.
Tech stack

Python · pandas · NumPy · matplotlib · seaborn · Jupyter

How to run
Clone the repo.
Install dependencies:
bash
   pip install pandas numpy matplotlib seaborn jupyter
Place automobile.txt in the same folder as the notebook.
Run all cells in automobiles.ipynb. The charts are saved to report_figures/.
