<h1>DELIVERABLE 1</h1>

<h2>Team members</h2>
Riya Rajeshkumar Jain 801254411

Chris Overcash 800939915

Aditya Nitinbhai Thakkar 801272248

Aadit Bagga 801317907


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

The first thing we did to analyze the data was we created an analysis using Amazon Glue so that you can see an overview of what each column contains. There is a total correlations part, a box plot for each column, and a summary of each column and the data contained there. Because of this instance being private, this cannot be shared but the screenshots below give a good visualization of what it looks like in Amazon Glue.

![Amazon Glue Column Statistics](https://user-images.githubusercontent.com/91394443/200427601-c61da7e9-e890-464c-ba0d-06c92e96e379.png)

![Amazon Glue overviewp1](https://user-images.githubusercontent.com/91394443/200427519-ffcda80f-051a-4085-968d-615ea13a730b.png)

![AmazonGluep2](https://user-images.githubusercontent.com/91394443/200427559-4f9ed3ae-02f4-4f58-90e7-30bd87f87030.png)

![Amazon Glue p3](https://user-images.githubusercontent.com/91394443/200427583-d42152f0-972e-44d4-8901-3a279d2a54e5.png)

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

<h2>Dashboard</h2>

Below are the graphs we used for the dashboard. This was created using Amazon Quicksight. Due to cost limitations, the dashboard cannot be exported. These graphs give a great overview of what we are trying to analyze, the correlations between age, gender and race and diabetes diagnosis/hospital readmissions. A screenshot of our Quicksight dashboard is shown in the screenshot below.

![Quicksight Dashboard](https://user-images.githubusercontent.com/91394443/200450619-34da1e71-6b66-4360-9854-e886aabb3c04.png)

<h1>DELIVERABLE 3</h1>

<h2>ML Model, Evaluation, Optimization, Results</h2>

Below Are the result of the ML model

<h3>Logistic Regression</h3>

A predicted model for the logistic regression is shown in the image below. We are comparing both data sets for readmission in this model. The predicted data and actual data are compared on a graph that compares the amount of readmissions that occurred or did not occur based on predicted and actual data. However, this is less accurate.

![Screen Shot 2022-12-11 at 12 18 30 AM](https://user-images.githubusercontent.com/50045937/206887789-56fa3b0a-bbfe-42e9-b6ee-3c23aeeb537a.png)
![Screen Shot 2022-12-11 at 12 29 33 AM](https://user-images.githubusercontent.com/50045937/206888058-474b0550-7f40-4e6f-a35f-36c4a1ffddc8.png)

<h3>Random Forest Classifier</h3>

Here we are using Random Forest Classifier to predict the data. In this model we are comparing both datas for readmitted patients. There is a comparison graph for the predicted data and actual data that shows the comparison between how many readmisions happened or not with predicted and actual data. This is more accurate than the Logistic Regression model.

![Screen Shot 2022-12-11 at 12 24 02 AM](https://user-images.githubusercontent.com/50045937/206887932-b0945d60-6e1d-4389-9def-0101b3972fd4.png)
![Screen Shot 2022-12-11 at 12 30 33 AM](https://user-images.githubusercontent.com/50045937/206888077-e8218a52-db16-4d89-a0f5-575494b82f91.png)

<h3>Super Vector Machine</h3>

Here we are using another model called Super vector Machine. In this model we are comparing both datas for readmissions. There is a comparison graph for the predicted data and actual data that shows the comparison between how much readmision happened or not with predicted and actual data. This model is also as acurate as the Random Forest Classifier. We can compare result for the both and they are almost same.

![Screen Shot 2022-12-11 at 12 27 06 AM](https://user-images.githubusercontent.com/50045937/206887995-956b50a3-3feb-4482-bbae-3076d7369f8e.png)
![Screen Shot 2022-12-11 at 12 31 12 AM](https://user-images.githubusercontent.com/50045937/206888096-43e30ce8-dbeb-4654-b262-40e0384d5a77.png)
