<h1>DELIVERABLE 1</h1>

<h2>Team members</h2>
1
Riya Rajeshkumar Jain
801254411
2
Chris Overcash
800939915
3
Aditya Nitinbhai Thakkar
801272248
4
Aadit Bagga
801317907


<h2>Communication Plan</h2>

We are using GitHub for communication and for the project repository. The link to the repository is stated below.

<h2>Business problem</h2> 
Kaggle Link: Diabetes 130 US hospitals for years 1999-2008 | Kaggle
Link to original data source: UCI Machine Learning Repository: Diabetes 130-US hospitals for years 1999-2008 Data Set


<h2>Dataset</h2>
We are using a data set of hospital visits at 130 unique hospitals over the course of 10 years (1999-2008) in which diabetes was the diagnosis or cause for a hospital visit. The length of stay for these patients was at least one day and less than two weeks.

Link - https://www.kaggle.com/datasets/brandao/diabetes?select=diabetic_data.csv

<h2>Research objectives</h2>

Research objectives will include the following:
Correlation of hospital readmissions and which hospital was visited
Correlation between race, gender, and age and hospital readmissions
Correlation between race, gender, and age of diabetes diagnosis
What factors are the strongest predictors that a person will be readmitted in the future
Which hospitals are most effective in their treatment of diabetes patients
Correlation between any other common symptoms of diabetes diagnosis/patients.

<h1>DELIVERABLE 2</h1>

<h2>Data Preparation</h2>

•	To begin our data preparation, we created an S3 bucket and uploaded our dataset. A screenshot of the bucket and data in it is below. 
![image](https://user-images.githubusercontent.com/91394443/200417027-10b6838a-2c85-42a5-b494-cf6243720b4c.png)

•	We then used amazon Sage Maker to import all of the libraries and load the dataset for our initial data preparation, as shown below.

![image](https://user-images.githubusercontent.com/91394443/200417082-89e3bcdd-8d30-49dd-89dd-cbacecacd282.png)

•	We then Checked the shape of our data (101,766 rows and 50 columns) and checked what data type each value/column represented.
•	The next part was figuring out which data was incomplete or irrelevant. We used a simple code to count the number of instances in each column that had missing data, which was represented in the dataset as a "?"
•	We also used the describe function to get a better understanding of each column as a whole.
•	Next we dropped rows that were missing data in the "race", and all of the diagnosis columns.

![Exploring Data Project](https://user-images.githubusercontent.com/91394443/200417293-4fe23337-e6a1-49f2-836a-92c5f9e2551f.png)

•	This is how our data was prepared to be ready for visualization. More data manipulation might be required if issues arise in the future.

<h2>Exploratory Data Analysis</h2>

Below is the first visualization we performed. The graph below represents the number of medications of each patient and how many days they were in the hospital. There is not much of a correlation between the number of medications a patient was taking and how long their hospital stay was.

![image](https://user-images.githubusercontent.com/91394443/200417812-1a7303ad-1dc8-4300-9ba5-af04160be420.png)

Below is another visualization we executed which shows the length of time that passed between each patient being readmitted to the hospital and if they were readmitted at all. This graph shows that a majority, over half of the patients in this dataset, were not readmitted at all. Of those that were readmitted, most were readmitted more than a month after their initial visit. The graph below that is a simpler graph that only represents whether or not a patient was readmitted. The second graph reaffirms the first graph in that most patients were not readmitted.

![image](https://user-images.githubusercontent.com/91394443/200417884-6ab4c0af-60d2-4b0d-a835-73d23dd0865e.png)

![image](https://user-images.githubusercontent.com/91394443/200417915-8e8d34af-ff40-4069-ad53-9d223b983177.png)

The visualization below shows the correlation between a patients race and their diagnosis of diabetes. As the graph represents, a vast majority of diabetic patients were Caucasian, (greater than any other race by about 50,000 patients).

![image](https://user-images.githubusercontent.com/91394443/200417990-84a52f94-9734-4c42-8876-6e0a03abede4.png)

The same thing was done in the graph below but instead of comparing the correlation between races, we compared the gender of the patients. While more patients were female, this comparison was much closer than the race graph above. The number of female patients were 54,708 while the number of male patients was 47,055 with only one patient with an invalid answer.

![image](https://user-images.githubusercontent.com/91394443/200418029-ce73ae58-d3b2-4ea8-a17b-350f76165cf1.png)

The graph below shows the correlation of patients and their age, along with whether they were readmitted or not. Most patients who were diagnosed were aged 50 years old or older. The highest concentration of patients was in the 70- to 80-year-old range. The highest number of readmitted patients was also in the 70- to 80-year-old range.

![image](https://user-images.githubusercontent.com/91394443/200418099-fbd29017-56a5-4fc3-a1c9-a912ab76095c.png)

The last visualization we executed was to see how long most patients stayed in the hospital when they were admitted for diabetes. The most common length of time in the hospital was 3 days with the next most common being only 2 days. This is a good sign as these patients are receiving quick and quality care and not in serious condition having to stay in the hospital for an extended amount of time.

![image](https://user-images.githubusercontent.com/91394443/200418141-78ab613d-e44a-4e0a-a5cf-39c71e327463.png)
