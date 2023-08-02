# Matplotlib_challenge
# Background
 The study at Pymaceuticals, Inc. involved 249 mice with SCC tumors who received various drug regimens, including our drug of interest, Capomulin. Over a period of 45 days, we observed and measured tumor development to compare the performance of Capomulin against other treatment regimens. For this study, our responsibilities included generating all the necessary tables and figures for the technical report of the clinical study. We analyzed the data to provide insights and visualizations that would help the executive team make informed decisions regarding the effectiveness of the treatments.
As per the results of the study, the performance of Capomulin was compared to other drug regimens. The data have been presented through various tables and figures, statistics, scatter plots, and box plots to illustrate the tumor volume trends, treatment effectiveness, and identify potential outliers.
# Observation
* The bar graph shows that the drug regimen Capomulin was tested on the maximum number of mice (230), followed by Ramicane (228).
* The pie chart shows the ‘Male’ and ‘Female’ mouse used for the experiment (51%,49%) is close in numbers.
* The boxplot shows that for Infubinol there is one outlier with a Tumor Volume of 36.321346. An outlier is a data point that lies far away from the other values in the dataset. It plays an important role in data analysis.
* A correlation coefficient is 0.83 between mouse weight and average tumor volume for the Capomulin regimen. A positive correlation means that if one variable increases, the other variable also increases as well. So, as the mouse weight increases, the average tumor volume tends to increase.
# Challenges
One of the first challenges that was faced during the script writing was when creating a clean DataFrame by dropping the duplicate mouse by its ID. I was using the syntax: df.drop_duplicates(subset=None, keep= ‘first’, inplace = False, ignore_index= False) {source listed in Referrence). It ended up giving me wrong total and errors. I had to use AskBcs for help in solving the issue. The next issue was when generating a scatter plot of average tumor volume vs. mouse weight for the Capomulin regimen. The error kept stating that the variable 'capomulin_data' and 'average_tumor_volume' were not found. It seems that the error was caused by the absence of the column 'Weight (g)' in the DataFrame average_tumor_volume. This is because I didn't include the 'Weight (g)' column in the DataFrame when calculating the average tumor volume. So, to fix the issue I used merge  method to the DataFrame average_tumor_volume with the original capomulin_data DataFrame to include the weight information. 
# Conclusion
In summary, the study revealed promising results for Capomulin, by showing significant reduction in tumor volume over the 45-day treatment period. The reports and visualizations provide an overview on Capomulin’s performance in the study. The outcome puts Capomulin as a strong candidate for further development and clinical trials and has potential in the future.
References
* https://sparkbyexamples.com/pandas/pandas-get-list-of-all-duplicate-rows/
* https://sparkbyexamples.com/python/pandas-dataframe-loc/
* https://sparkbyexamples.com/pandas/pandas-aggregate-functions-with-examples/?expand_article=1
* https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.sort_values.html
* AskBcs Learning Assistance.
* Tutoring By Simon Rennocks via Calendly.
