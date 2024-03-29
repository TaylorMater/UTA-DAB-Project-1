# Data Science Salary Analysis
UTA Data Analysis Bootcamp Project 1

-----------------------------
# Powerpoint Presentation:

https://docs.google.com/presentation/d/1dWSk839n7c2e29vaaeYlXmGo04oD5s5SUkBu3iMJ358/edit#slide=id.p


# Repo Design

`scripts` directory contains the following scripts:

-   api_call_to_csv.ipynb
    >   This is the script that Riley made to reference the World Bank API [(see here)](https://datahelpdesk.worldbank.org/knowledgebase/articles/898581-api-basic-call-structures) which finds the unique country names from the union of `employee_residence` and `company_location` and then requests metrics like population and gdp per capita for those countries. The results are written to `resources/world_bank_api_data.csv`. Some data was not available for some countries, and Jersey was not accepted by their API for any of the data we wanted. Review the script for more details.
-   data_science_analysis.ipynb
    >   This script contains the collection of all group members individual analysis notebooks. This is the main script you would run if you clone this repo. It is literally just the `<name>_notebook.ipynb`'s alll copied together into one place, with minor changes for imports/scaffolding.
-   khadija_notebook.ipynb
    >   This script was developed by Khadija to answer the research questions/tasks assigned to her. It produces all of the `figure00x>.png` in `fiugres/khadija`. Review the script for more details.
-   maria_notebook.ipynb
    >   This script was developed by Maria to answer the research questions/tasks assigned to her. It produces all of the `figure00x>.png` in `fiugres/maria`. Review the script for more details.
-   markdown_cheatsheet.ipynb
    >   This is a notebook Riley created that contains a collection of common markdown commands to aid in the creation of the README, and to act as a reference for other markdown work. It probably should live somewhere else, but he was too lazy to move it.
-   riley_notebook.ipynb
    >   This script was developed by Riley to answer the research questions/tasks assigned to him. It produces all of the `figure00x>.png` in `fiugres/riley`. Review the script for more details.


`resources` directory contains the following:

-   data_science_salries.csv
    >   This is the dataset we downloaded from Kaggle [here](https://www.kaggle.com/datasets/sazidthe1/data-science-salaries?resource=download). For more details review the csv itself.
-   world_bank_api_data.csv
    >   This is the dataset generated from the `api_call_to_csv.ipynb` notebook in the `scripts` directory. It contains information from the World Bank API, mainly population and gdp per capita, for all countries referenced in the `data_science_salaries.csv` file. For more, see the csv itself, or review the script.

 

`figures` directory is self explanatory - it contains directories corresponding to group members. In each group member's directory, you can find the plots that their `<name>_notebook.ipynb` generates. All figures are generated when you run all of the `data_science_analysis.ipynb` file.


`takeaways` directory was a quick directory Riley made to store some notes he learned during the project. It also houses Riley's attempt at a bibliography, but it's not annotated at all and he is sure he missed some links along the way.

-----------------------------

### This project seeks to analyze a robust dataset encompassing data science salaries spanning four years (2020-2024), to extract valuable insights. It will delve into patterns, trends and factors that impact the compensation of professionals in the data science field. The dataset incorporates details like job titles, experience levels, geographic locations and other pertinent factors affecting salaries within the realm of data science.

### Please note - many of the figures were cutoff during the saving process. To see the full figures with less cutoff, you can open a corresponding Jupyter Notebook. `data_science_analysis.ipynb` has everything. 

## Research Questions

### What is the distribution of Data Science Salaries in each year?

Examines salary data over time to gain insights into trends, patterns and changes in compensation within the field of data science.

![image](https://github.com/TaylorMater/UTA-DAB-Project-1/blob/main/figures/khadija/fig001.png)

### What is the average salary for each job title? 

Determines the average salary for each job titles to provide insights into the compensation landscape.


![image](https://github.com/TaylorMater/UTA-DAB-Project-1/blob/main/figures/khadija/fig002.png)

Identifies the highest-paying job titles, to provide valuable insights intoe salary trends, career paths and compensation competitiveness.

![image](https://github.com/TaylorMater/UTA-DAB-Project-1/blob/main/figures/khadija/fig003.png)




### How does the average salary per job title vary by experience?
Based on the information gathered and the graph presented below, we can see how the experience level on each job affects differently depending on the job title. 
As we can see, Applied Scientist can earn around the same or a bigger salary on an entry level compared to other titles as mid, senior and even executive level.
We can also observe how Data Analyst salary does not vary much depending on experience. Others can go from $75K to $200K compared to Data Analyst which according to our data varies only from $75K to $125K.


![image](https://github.com/TaylorMater/UTA-DAB-Project-1/blob/main/figures/maria/fig001.png)




![image](https://github.com/TaylorMater/UTA-DAB-Project-1/blob/main/figures/maria/fig002.png)


### Geographic Analysis

All of the following are ripped straight from the `data_science_analysis.ipynb` notebook, and in particular, from the `riley_notebook` which has been copied inside that notebook.

Very thorough analysis and discussion of these questions in more detail can be found in those notebooks, but I will try to provide some cursory information here as well.

### Which countries pay the highest data science salaries?

First doing the analysis using employee residence as our country.

![image](https://github.com/TaylorMater/UTA-DAB-Project-1/blob/main/figures/riley/fig001.png)


Showing the top 20 because the above graph is too big:

![image](https://github.com/TaylorMater/UTA-DAB-Project-1/blob/main/figures/riley/fig002.png)


Showing the bottom 20:


![image](https://github.com/TaylorMater/UTA-DAB-Project-1/blob/main/figures/riley/fig003.png)

Now doing the analysis but with company location as our country. 

![image](https://github.com/TaylorMater/UTA-DAB-Project-1/blob/main/figures/riley/fig004.png)

Showing the top 20 because the above graph is too big:


![image](https://github.com/TaylorMater/UTA-DAB-Project-1/blob/main/figures/riley/fig005.png)

Showing the bottom 20:


![image](https://github.com/TaylorMater/UTA-DAB-Project-1/blob/main/figures/riley/fig006.png)




### Companies located in which countries posted the most data science jobs?

More analysis in `riley_notebook.ipynb`. But the main thing is - we notice a huge skew. The US seems to have used the tool that generates the dataset far more than other countries, so we are't getting an accurate saturation among all countries. Or at least, it looks like it until we normalize for population (as the US has a much higher populaiton than most countries on these).

We started with employee residence as our location again.


![image](https://github.com/TaylorMater/UTA-DAB-Project-1/blob/main/figures/riley/fig007.png)

Showing the top 10:


![image](https://github.com/TaylorMater/UTA-DAB-Project-1/blob/main/figures/riley/fig008.png)

Now with company location:

![image](https://github.com/TaylorMater/UTA-DAB-Project-1/blob/main/figures/riley/fig009.png)

Showing the top 10:

![image](https://github.com/TaylorMater/UTA-DAB-Project-1/blob/main/figures/riley/fig010.png)


### Which countries (company location) posted the most data science jobs when normalized for population?

Te previous question lets us see a skew towards the US. Is that due to underlying issues in the dataset or to the strength of the Data Science market in the US? One way to get more information on that is to normalize everything by the population. You would expect at least comparable data science jobs per capita in countries like the Netherlands and the UK to the US. 

After seeing the results, it definitely still seems skewed, but not as much as you might have originally thought. 

Sticking with company location for our countries:

![image](https://github.com/TaylorMater/UTA-DAB-Project-1/blob/main/figures/riley/fig011.png)

Showing the top 10:

![image](https://github.com/TaylorMater/UTA-DAB-Project-1/blob/main/figures/riley/fig012.png)


### How does the count of a country's data science jobs in our data set correlate to gdp per capita of said country?

Correlation coefficient was about 0.31. So it is positively correlated, but weakly. Flaws in the data set could explain this, but you could also argue that the internet allows for the proliferation of Data Science jobs even in less developed economies. But considering the skew in the data set, it's hard to be decisive. 

![image](https://github.com/TaylorMater/UTA-DAB-Project-1/blob/main/figures/riley/fig013.png)





### Further questions:
-   What is the experience breakdown of the job market? By year?
-   If we restrict the dataset to just a few countries, what indicators and metrics can we generate that correlate with development indicators? How might they defer? Would there be any advantages? 


-------------------------
## Sources:
Dataset from Kaggle - https://www.kaggle.com/datasets/sazidthe1/data-science-salaries?resource=download

Presentation - https://docs.google.com/presentation/d/1dWSk839n7c2e29vaaeYlXmGo04oD5s5SUkBu3iMJ358/edit#slide=id.p


Other sources can be found in the `takeaways` directory, under `sources.md`
