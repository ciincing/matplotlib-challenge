# Observations & Inferences
1. The correlation between mouse weight and the average tumor volume is 0.84 which is a strong positive correlation. 
2. Capomulin and Ramicane treatments are better at reducing tumor sizes in mice, according to the graph called "# of Timepoints vs Drug Regiment". 
3. When the Capomulin regimen was used on Mouse I509, it greatly reduced the tumor size from its peak of tumor size 48 mm^3 to 41mm^3 in the span of 40 days. 

# matplotlib-challenge README
I had just joined Pymaceuticals, Inc., a new pharmaceutical company specializing in anti-cancer medications. The company had recently started screening for potential treatments for squamous cell carcinoma (SCC), a commonly occurring form of skin cancer.

As a senior data analyst at the company, I was given access to the complete data from their most recent animal study. In this study, 249 mice identified with SCC tumors received treatment with a range of drug regimens. We observed and measured tumor development over a period of 45 days. The purpose of the study was to compare the performance of Pymaceuticals' drug of interest, Capomulin, against the other treatment regimens.
In order to generate tables and figures required for a technical report of the clinical study, I first ran the provided package dependency and data imports, and then merged the mouse_metadata and study_results DataFrames into a single DataFrame.

I displayed the number of unique mice IDs in the data, and then checked for any mouse ID with duplicate time points. I displayed the data associated with that mouse ID, and then created a new DataFrame where this data was removed. I used this cleaned DataFrame for the remaining steps.

I displayed the updated number of unique mice IDs.

I created a DataFrame of summary statistics. I ensured that each drug regimen had a row, with the regimen names contained in the index column.

For each drug regimen, I included a column for the following statistics: mean, median, variance, standard deviation, and SEM of the tumor volume. It's worth noting that there are multiple methods to produce these results, so the specific method used is less important compared to obtaining the desired outcome.

I generated two identical bar charts to display the total number of rows (Mouse ID/Timepoints) for each drug regimen throughout the study.

The first bar chart was created using the Pandas DataFrame.plot() method.

The second bar chart was created using Matplotlib's pyplot methods.

I also generated two identical pie charts to show the distribution of female versus male mice in the study.

The first pie chart was created using the Pandas DataFrame.plot() method.

I calculated the final tumor volume of each mouse across four of the most promising treatment regimens: Capomulin, Ramicane, Infubinol, and Ceftamin. Then, I calculated the quartiles and IQR and determined if there were any potential outliers across all four treatment regimens. Here are the steps I followed:

I created a grouped DataFrame that displayed the last (greatest) time point for each mouse. Then, I merged this grouped DataFrame with the original cleaned DataFrame.

I created a list to hold the treatment names and another empty list to store the tumor volume data.

I looped through each drug in the treatment list, located the rows in the merged DataFrame corresponding to each treatment, and appended the resulting final tumor volumes for each drug to the empty list.

To determine outliers, I used the upper and lower bounds and printed the results.

Using Matplotlib, I generated a box plot that illustrated the distribution of the final tumor volume for all the mice in each treatment group. I highlighted any potential outliers in the plot by changing their color and style.

The second pie chart was created using Matplotlib's pyplot methods.

I selected a single mouse that was treated with Capomulin and generated a line plot to show the tumor volume versus time point for that mouse.

I also generated a scatter plot to illustrate the relationship between mouse weight and the average observed tumor volume for the entire Capomulin treatment regimen.

I calculated the correlation coefficient and performed a linear regression analysis between mouse weight and the average observed tumor volume for the entire Capomulin treatment regimen.

Next, I plotted the linear regression model on top of the previous scatter plot to visualize the relationship between mouse weight and tumor volume in the Capomulin treatment regimen. 
