# Call Center Analysis

![Dashvizz](https://user-images.githubusercontent.com/103915142/231853938-07ff8bc2-333d-488e-8e2e-69bff0ae9137.jpg)
#

Imagine you're the manager of a busy call center for a large telecommunications company. Every day, your team receives hundreds of calls from customers with a variety of questions and issues. You're always looking for ways to improve the customer experience and increase efficiency, but you're not quite sure where to start.

That's where this analysis comes in. Over the course of few nights – Actually just two😉 – I delved into the call center dataset to uncover key insights and identify opportunities for improvement. I got the dataset from a #DataChallenge WhatsApp group and upon downloading the dataset, I wore my detective mask and began to check if I could identify patterns or trends in the data that would be worthy of investigation. 

So, buckle up and get ready for a deep dive into the call center dataset. In the following story, I’ll take you through the analysis step by step, highlighting the challenges faced, the insights uncovered, and the impact of my findings.

### 1. Data Gathering and Cleaning
As mentioned earier, the dataset was gotten from a #DataChallenge WhatsApp group.
I excitedly opened the file, and was quick to realize that the data was already cleaned, with all the missing values meaning the calls placed at that time wasn't answered and couldn't have been resolved too., making the data somewhat boring and predictable. All I had to do was replace all empty cells with 0 and ensured all numerical columns were in their right format.
However, having a clean data was actually a blessing in disguise, as it saved me a lot of time and effort that would have been spent on cleaning the data myself. phew!

### 2. Data Exploration
**A**. There are 5001 rows and 14 columns. 

**B**. I created 2 columns and extracted the months from the Date column and the hour the calls came through from the Time column. Well in the course of analyzing, I figured that I didn't need to extract the Hours because Excel Pivot table has features that provide such. Cool right!!

**C**. It should be noted that in the rating column, cells containing "0" values have their calls unanswered... So we would be careful when analysing the rating column.


BEFORE -- Original Data

![before excel](https://user-images.githubusercontent.com/103915142/231898624-ec880b43-e2d9-4e28-8919-593e8c4f0842.jpg)

AFTER -- Trasformed Data

![after excel](https://user-images.githubusercontent.com/103915142/231898940-e53d5ad3-e513-4eaa-b516-2342b6630667.jpg)

### 3. Data Analysis

> **Question 1:** What day, time, and month were the busiest?

Knowing the busiest day, time, and month for a call center is crucial in optimizing staff scheduling and resource allocation to ensure high customer satisfaction, minimize wait times, and maximize operational efficiency.

     
 Busiest Days                                                                                        |  Busiest Times
-------------------------------------------------------------------------------------------------------------|------------------------- 
![1a](https://user-images.githubusercontent.com/103915142/231903363-73ea6b2f-0ca2-45d1-b896-28da43493fcb.jpg)| ![1b](https://user-images.githubusercontent.com/103915142/231903433-9b1140ac-4b7c-4b84-80be-c56d3592b50a.jpg)

Least Busiest Days                                                                                          |  Months
-------------------------------------------------------------------------------------------------------------|------------------------- 
![1d](https://user-images.githubusercontent.com/103915142/231903937-87bb4fb5-1226-4a64-966e-6e311db6a04a.jpg)| ![1c](https://user-images.githubusercontent.com/103915142/231903966-dfd522b8-7d92-4145-8d9f-c328291aa8d1.jpg)

VISUALS:

![2a d](https://user-images.githubusercontent.com/103915142/231905837-5f99c8c3-8aca-4e29-8336-a32b6812caed.jpg)
































