# AnalyticsPython_StatsCan
This repository explores 2022 Canadian Labour Force Survey. 

All tasks for this repository is completed use Python 3 on Jupyter Notebook. The following popular libraries were used:
- Numpy
- Pandas
- Matplotlib
- Seaborn

## Task One: Data Download
Data is downloaded as per given instructions. The monthly Labour Force Survey files are stored in /Datasets, along with a copy of the reference file ('LFS_PUMF_EPA_FGMD_variables.csv')

## Task Two: Creating and Mapping
The file used for this task is 'Creating Mapping File.ipynb', and follows the below steps to create mapping files:
- Loading the supplemental table in Pandas Dataframe
- Creating a function to extract the row locations of each reference
- Striping whitespaces from variable names
- Creating a function to store all required variable values into reference dataframes
- Creating all required reference dataframes
- Saving all required reference dataframes as csv files in the /Datasets folder with common prefix 'ref_'

## Task Three: Extracting and Merging Data
The file used for this task is 'Extracting and Merging Data.ipynb', and follows the below steps to create an anlytical table:
- Loading Jan2022 Labour Force Survey to determine all transformations required
- Loading all reference files required to perform the transformations, they are created from Task Two
- Performing data transformations on Jan2022 file, ensuring all transformations are correctly applied
- Creating a function to perform all data transformations for the all other monthly files
- Applying all data transformations for the all other monthly files using the function created above
- Combining all transformed monthly files into one dataframe
- Saving dataframe as /Datasets/FinalDF.csv

## Task Four: Tracking SDG Goal 8: Promote sustained, inclusive and sustainable economic growth, full and productive employment and decent work for all
The file used for this task is 'Tracking SDG Goal 8.ipynb', and follows the below steps to create functions and graphs to answer below 3 Questions:
- Loading the FinalDF created from previous task

### Question 1 - What is the unemployment rate in each quarter of the given year?
- Created a function to find unemployment rate by quarter
- Created a function to return a graph representing the result

### Question 2 - What is the average tertiary (postsecondary or greater) education attainment rate among the youth (15 - 29) for each province?
- Created a function to find the average tertiary rate for youth
- Created a function to return a graph representing the result

### Question 3 - What are the top 5 industries that have the highest rate of involuntary part-time work?
- Created a function to find the top 5 industries with the highest rate of involuntary part-time work
- Created a function to return a graph representing the result

- Saving all the response tables and graphs in /Datasets, with common prefix 'output'

## Task Five: Tracking SDG Goal 5: Achieve gender equality and empower all women and girls
The file used for this task is 'Tracking SDG Goal 5.ipynb', it explore the different metrics from the 2022 Labour Force Surveys to better understand Canada's alignment with the UN Goal

As with previous task, all the response tables and graphs in /Datasets, with common prefix 'output'

## Thought Process
Here is the link to to [UN Sustainable Development Goal 5](https://sdgs.un.org/goals/goal5). 
My objective is to use the Labour Force Survey data to better understand how Canada is doing in terms of meeting the Targets and Indicators outlined in the UN Sustainable Development Goal 5, and any insights on where we are behind, and how we can improve as a country.

### Exploring Goal 5.1 End all forms of discrimination against all women and girls everywhere:
Since this is one of the most important metric of this Goal, I wanted to explore how this is reflected in the Labour Force Survey.
I believe by comparing the unemployment rate between males and females at each education level, I would gain insights on whether there is any evidence of discrimination against women in the labour force.
My assumption is that if there is no discrimination against women in the labour force, the unemployment rate between men and women should be comparative.

Result of my findings:
I observed a gap in unemployment rate between male and females, with unemployment rate for females higher at both the lower and higher end of education levels. 
This brings concerns with the availability of opportunities for the female labour force who are less educated, as I believe there is a higher risk of poverty for females who meet the criteria of little education and lack of employment.
Furthermore, the data also shows that as long as one graduates high school (education level >1), the unemployment rate significantly drops.

Recommendation:
Push for programs to hire for females who are less educated, and put programs in place to encourage the completion of high school diploma for females of all ages.

### Exploring 5.5.2: Proportion of women in managerial positions:
This UN specified goal advocates for providing women with equal opportunities to be in management positions.The NOC_10 variable in the Labour Force Survey gives indication of whether a participant is in managerial position. This gave me the opportunity to explore percentage of women in managerial positions based on age group.

Result of my findings:
I observed significant under-representation of women in every age group compared with men. This is not an ideal scenario, and calls for closer examination on how the situation can be improved 

Recommendations:
To meet the UN goal of increasing women in managerial positions, the Canadian government must bring more awareness to this issue, and work with businesses to help provide an workplace environment where women can succeed as much as men.

### Exploring Goal 5.6.2, Education Level for women of all ages
This UN specified goal advocations equal access for women on many issues including education. As explored previously, by obtaining a high school diploma, it significantly increase one's chance of being employed. Given that, I wanted to explore whether there is an education gap between men and women, by using high school graduation percentage as a key indicator.

Results of my findings:
I found that females actually have a higher high school completion rate in almost all age groups this means Canada as a country is doing well in providing women with access to education.

Recommendations:
Canada's accomplishment in providing women with education should be studied and to help implement the same for other countries.
Although Canada is doing well in terms of providing basic education to women, this further signifies the unequality that still exists in the workplace. As previously pointed out, women in managerial positions significantly lacks their men counterparts. I recommend exploring of other factors, besides education, that contributes to one's promotion to management.