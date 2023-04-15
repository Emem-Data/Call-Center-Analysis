# Call Center Analysis

![Dashboard](https://user-images.githubusercontent.com/103915142/232046216-1ba939cc-d450-4837-984f-bcf12f0e59af.jpg)

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

## 3. Data Analysis

> ### **QUESTION 1:** WHAT DAY, TIME, AND MONTH WERE THE BUSIEST?


<br>



Knowing the busiest day, time, and month for a call center is crucial in optimizing staff scheduling and resource allocation to ensure high customer satisfaction,      minimize wait times, and maximize operational efficiency.

     
Busiest Days                                                                                        |  Busiest Times
-------------------------------------------------------------------------------------------------------------|------------------------- 
![1a](https://user-images.githubusercontent.com/103915142/231903363-73ea6b2f-0ca2-45d1-b896-28da43493fcb.jpg)| ![1b](https://user-images.githubusercontent.com/103915142/231903433-9b1140ac-4b7c-4b84-80be-c56d3592b50a.jpg)

Least Busiest Days                                                                                          |  Months
-------------------------------------------------------------------------------------------------------------|------------------------- 
![1d](https://user-images.githubusercontent.com/103915142/231903937-87bb4fb5-1226-4a64-966e-6e311db6a04a.jpg)| ![1c](https://user-images.githubusercontent.com/103915142/231903966-dfd522b8-7d92-4145-8d9f-c328291aa8d1.jpg)

VISUALS:

![2a d](https://user-images.githubusercontent.com/103915142/231905837-5f99c8c3-8aca-4e29-8336-a32b6812caed.jpg)

![2b c](https://user-images.githubusercontent.com/103915142/232043464-42ce4e5a-1260-4e3e-8245-85beefcd3a9e.jpg)


<br>


>### **QUESTION 2:** WHAT TOPICS WERE DISCUSSED THE MOST?


<br>



By understanding the most discussed topics, the call center can identify areas where their customer service is falling short. This information can be used to          train agents on how to handle these topics better, which can improve the overall customer experience.
Also, if customers are repeatedly calling about the same issue, it could indicate a problem that needs to be addressed. By addressing the root cause of the issue,call center organizations can reduce the number of calls they receive about that topic.
     
Topics Discussed the Most                                                                                   |  Topics by Month
-------------------------------------------------------------------------------------------------------------|------------------------- 
![3a](https://user-images.githubusercontent.com/103915142/231994848-07efcfa1-e4af-4bfe-a206-f9a0ab1dc597.jpg)| ![3b](https://user-images.githubusercontent.com/103915142/231996053-874b8b16-17da-400f-bbc7-c91c7afc6719.jpg)


<br>



>### **QUESTION 3:** HOW WELL WERE THE TOPICS TREATED?


<br>



![3c](https://user-images.githubusercontent.com/103915142/232044889-e3db6be9-beb2-40ed-8143-9a45bf7ec998.jpg)


So I began to wonder why these topics were unaswered or unresolved, especially for the topics on Techical support. 
I checked the "Average speed of answer in seconds by Topics" to see if I could get an answer. But to my suprise, it was revealed that no an average, techical          support calls were picked in 53 seconds, which is the fastest call by topic answered averagely.

![4a](https://user-images.githubusercontent.com/103915142/232004429-ea1f9144-45a5-4eb3-9c8e-3940aba6c502.jpg)

>> __If the calls for Techical supports were aswered the fastest averagely, the why is it still the most uaswered ad uresolved topic?__

I suspected it had to do with the agents, maybe someone has a habit of keeping customers waiting for too long. So I checked and I wasn't wrong afterall!.

![4b](https://user-images.githubusercontent.com/103915142/232005670-e902a264-e5fd-4965-9be3-ca98588f7e10.jpg)

The table above shows that Joe has mostly been answering calls later than other agents. Averagely Joe picked Techical support calls after ooe mintues, and it is possible the caller got tired of waiting and hung up. 


<br>



> ### **QUESTION 4:** AGENT AVERAGE SPEED OF ANSWER IN SECONDS?


<br>


Call center organizations often have SLAs in place with their clients, which specify the maximum amount of time customers should wait before their calls are            answered. By monitoring the average speed of answering calls, call center organizations can ensure that they are meeting these SLAs and avoid penalties for            failing to do so.

Table                                                                                                        |  Chart
-------------------------------------------------------------------------------------------------------------|------------------------- 
![5a](https://user-images.githubusercontent.com/103915142/232028044-1a7b3527-2de0-4cf7-b50e-3eecd1f98416.jpg)| ![5b](https://user-images.githubusercontent.com/103915142/232028080-404d14cc-4a5c-45d7-8d0b-d5f3922ab04d.jpg)


<br>



> ### **QUESTION 5:** AGENT SATISFACTORY RATING?


<br>


![6a](https://user-images.githubusercontent.com/103915142/232038940-27299773-699e-4cee-bbe7-b96802ee8e20.jpg)


### 4. DATA INSIGHT































