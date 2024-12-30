# JobMarketEDA
Explanation of the Script
Loading the Data:

The script starts by loading the job listings from a CSV file using Pandas.
It displays the first five entries to verify that the data has been loaded correctly.
Data Preprocessing:

It removes any job listings that lack a description.
All job descriptions are converted to lowercase to ensure uniformity, which aids in regex matching.
If the descriptions contain HTML tags, they are removed to clean the text.
Defining Skills and Qualifications:

A dictionary named skills categorizes various key skills and qualifications such as programming languages, tools, databases, machine learning techniques, degrees, and soft skills.
Regex patterns are compiled for each category to efficiently search through the job descriptions.
Extracting Skills and Qualifications:

The script defines a function extract_skills that uses the compiled regex patterns to find matches within each job description.
It ensures that duplicate skills within the same description are not double-counted by converting matches to a set.
The extracted skills are aggregated using Python's Counter to count the frequency of each skill across all job listings.
Visualization:

The script creates a plots directory to save all generated visualizations.
For each skill category, it plots the top N (default 20) skills using horizontal bar charts. These plots are saved as PNG files in the plots directory.
Generating Word Clouds:

A word cloud is generated from all job descriptions combined, excluding common stopwords to highlight the most prominent terms.
The word cloud image is saved in the plots directory.
Summary Report:

The script prints out the top 10 skills in each category to the console, providing a quick textual summary of the findings.
A final message indicates the completion of the EDA and the location of the saved plots.
