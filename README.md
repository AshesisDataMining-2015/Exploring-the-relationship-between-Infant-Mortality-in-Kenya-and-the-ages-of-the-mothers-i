Exploring the relationship between GDP of countries/percentage of GDP allocated to Health/Infant Mortality Rate/Number of Healthworkers. How are these related..what kind of relationship can be drawn between them?

ISABEL DZIFA ATTU

DATA DISCOVERY AND SOURCES. This data was discovered from UN.org and it consists of GDP, Percentage of GDP spent on Health , Number of healh workers who attend to birth and The IMR(Infant Mortality rate ) for the various countries.

http://data.un.org/Data.aspx?d=MDG&f=seriesRowID%3a561 
http://data.un.org/Data.aspx?q=Health&d=WHO&f=MEASURE_CODE%3aWHS7_108 
http://data.un.org/Data.aspx?q=Health&d=MDG&f=seriesRowID%3a570 
http://data.un.org/Data.aspx?q=GDP&d=WDI&f=Indicator_Code%3aNY.GDP.MKTP.CD

EXPLORATORY DATA ANALYSIS

A. TYPE OF DATA AND ANALYSIS TECHNIQUE USED

  I had always know that i wanted to do something Unsupervised because I love to find out the relationships that exist between stuff and that was why i chose the kind of data i used. My data were  unrelated and thus after googling the various methods of analysing unsupervised data, i settled on K-means clustering because it would help to find out the relationships between my variables which are GDP, Percentage of GDP spent on Health , Number of healh workers who attend to birth and The IMR(Infant Mortality rate ) for the various countries.
QUESTION FORMULATION AND HYPOTHESIS GENERATION: I felt the urge to explore the political and social factors that affect Infant Mortality rates and not go with the ususal flow of looking into health causes of IMR.

QUESTIONS: 1. What is the relationship can be drawn between the GDP, Skilled Health Workers who attend to birth, GDP allocated to health and IMR. 2. Has Infant Mortality gotten better or worse over the years?

B. CLEANING DATA After deciding to do K-means the first step was to clean the data. I did this using R and excel. Seeing as the GDP was large numbers that were given in exponential format, there was the need to R format this to meet R's preferences with regards to numerical data. Also i had to merge the different files to produce one one frame with which I could work. After producing this frame , there was the need to convert the countries' column to numeric in order to better perform my clustering and elimiate common errors like 'Error, Script out of bounds Eror' , 'Na's in Foreign function error','Subscript out of bounds erroe', amongst others. Sometimes in trying to convert data values into numeric, i realised that N/A values were coerced into the data frame and this watsed quite some time

C. PLAYING AROUND WITH R The first thing i did was compare the relationships between the various variables independently before clustering all of them into one graph. I found the relationship between GDP and infant mortality of the various countries using K-means as will be displayed after running my R script. As i also found the relationship between IMR and Amount of money dedicated to health by the various countries. I also found out the increase or decrease in OMR over the different years essentially from 1993-2011.

I finally included all of these variables into one K-means graph and assessed the relationship between all of these variables and which countries fall into the various clusters that were formed.

D.RESULTS

At the end of the project I realised that 1. Countries that have High GDP tend to allocate more money to the Health sector . They also have Skilled personnel attending to births and thus, low IMR. 2.With regards to time , factors like technology have decreased IMR over the years for the developed countries, while the developing countries were still lagging behind with high rates of IMR

The graphs would give a better view of results. They are in the Data folder.
