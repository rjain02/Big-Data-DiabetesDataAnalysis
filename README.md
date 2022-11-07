#DELIVERABLE 1
Team members
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


Communication Plan:- We are using GitHub for communication and for the project repository. The link to the repository is stated below.

Project Repository:-  https://github.com/rjain02/Big-Data-Shipping-Project

Business problem:- 
Kaggle Link: Diabetes 130 US hospitals for years 1999-2008 | Kaggle
Link to original data source: UCI Machine Learning Repository: Diabetes 130-US hospitals for years 1999-2008 Data Set


Dataset:- We are using a data set of hospital visits at 130 unique hospitals over the course of 10 years (1999-2008) in which diabetes was the diagnosis or cause for a hospital visit. The length of stay for these patients was at least one day and less than two weeks.

Research objectives:- Research objectives will include the following:
Correlation of hospital readmissions and which hospital was visited
Correlation between race, gender, and age and hospital readmissions
Correlation between race, gender, and age of diabetes diagnosis
What factors are the strongest predictors that a person will be readmitted in the future
Which hospitals are most effective in their treatment of diabetes patients
Correlation between any other common symptoms of diabetes diagnosis/patients.

Data Preparation
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
