# pandas_challenge

This repository brings a python pandas solution. This project used 
two datasets in csv format, one is schools_complete.csv file wich includes the following
informations in columns School ID,school_name,type,size,budget and the other dataset is students_complete.csv file 
which includes the followling information in columns Student ID,student_name,gender,year,school_name,
reading_scoreand maths_score. The assignment analysis report is linked with Jupyter Notebook.

Dependencies and setup

import pandas as pd


Load the file and read the data as following;

school_data_to_load = "PyCitySchools/schools_complete.csv"
student_data_to_load = "PyCitySchools/students_complete.csv"

school_data = pd.read_csv(school_data_to_load)
student_data = pd.read_csv(student_data_to_load)

school_data_complete = pd.merge(student_data, school_data, how="left", on=["school_name", "school_name"])


school_data_complete.head()

	The dataset encompasses a total of 15 schools, 39,170 students. The total students average reading score is 69.98 which is lower than the average math score 70.33. When we see the passing rate reading 84.42% has a lower rate than math 86.07%, the overall passing rate is 72.80%. This is indicate that student's score more in math than reading.

	Holden High School students hold higher average of math and reading comparing all schools and grades. Grade 10th students hold a higher average Math score 75.10 and grade 11th students possess a higher average reading score 73.31.

Table of Contents
	Import Dependencies and Setup
	Load, Read and Merge the Data
	Local Government Area Summary
	School Summary
	Highest-Performing Schools (By % Overall Passing)
	Lowest-Performing Schools (By % Overall Passing)
	Maths Scores by Year
	Reading Scores by Year
	Scores by School Spending
	Scores by School Size
	Scores by School Type
