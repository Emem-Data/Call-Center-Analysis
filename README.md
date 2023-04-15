# Call Center Analysis

![Dashboard](https://user-images.githubusercontent.com/103915142/232046216-1ba939cc-d450-4837-984f-bcf12f0e59af.jpg)

#

Imagine you're the manager of a busy call center for a large telecommunications company. Every day, your team receives hundreds of calls from customers with a variety of questions and issues. You're always looking for ways to improve the customer experience and increase efficiency, but you're not quite sure where to start.

That's where this analysis comes in. Over the course of a few nights – Actually just two😉 – I delved into the call center dataset to uncover key insights and identify opportunities for improvement. I got the dataset from a #DataChallenge WhatsApp group and upon downloading the dataset, I wore my detective mask and began to check if I could identify patterns or trends in the data that would be worthy of investigation. 

So, buckle up and get ready for a deep dive into the call center dataset. In the following story, I’ll take you through the analysis step by step, highlighting the challenges faced, the insights uncovered, and the impact of my findings.

## 1. Data Gathering and Cleaning


As mentioned earlier, the dataset was gotten from a #DataChallenge WhatsApp group.
I excitedly opened the file and quickly realized that the data was already cleaned, with all the missing values meaning the calls placed at that time weren't answered and couldn't have been resolved too, making the data somewhat boring and predictable. All I had to do was replace all empty cells with 0 and ensure all numerical columns were in the right format.
However, having clean data was a blessing in disguise, as it saved me a lot of time and effort that would have been spent cleaning the data myself. phew!

## 2. Data Exploration
**A**. There are 5001 rows and 14 columns. 

**B**. I created 2 columns and extracted the months from the Date column and the hour the calls came through from the Time column. Well in the course of analyzing, I figured that I didn't need to extract the Hours because the Excel Pivot table has features that provide such. Cool right!!

**C**. It should be noted that in the rating column, cells containing "0" values have their calls unanswered... So, we would be careful when analyzing the satisfaction rating column by excluding ratings of “0”.


BEFORE -- Original Data

![before excel](https://user-images.githubusercontent.com/103915142/231898624-ec880b43-e2d9-4e28-8919-593e8c4f0842.jpg)

AFTER -- Transformed Data

![after excel](https://user-images.githubusercontent.com/103915142/231898940-e53d5ad3-e513-4eaa-b516-2342b6630667.jpg)

## 3. Data Analysis

<p align="center">
An analysis of a call center that involves evaluating metrics such as average handling time, call volume, customer satisfaction, and call resolution rate to identify areas for improvement and optimize performance.
</p>

> ### **QUESTION 1:** WHAT DAY, TIME AND MONTH WERE THE BUSIEST?



<br>



Knowing the busiest day, time, and month for a call center is crucial in optimizing staff scheduling and resource allocation to ensure high customer satisfaction, minimize wait times, and maximize operational efficiency.

     
Busiest Days                                                                                        |  Busiest Times
-------------------------------------------------------------------------------------------------------------|------------------------- 
![1a](https://user-images.githubusercontent.com/103915142/231903363-73ea6b2f-0ca2-45d1-b896-28da43493fcb.jpg)| ![1b](https://user-images.githubusercontent.com/103915142/231903433-9b1140ac-4b7c-4b84-80be-c56d3592b50a.jpg)

Least Busiest Days                                                                                          |  Months
-------------------------------------------------------------------------------------------------------------|------------------------- 
![1d](https://user-images.githubusercontent.com/103915142/231903937-87bb4fb5-1226-4a64-966e-6e311db6a04a.jpg)| ![1c](https://user-images.githubusercontent.com/103915142/231903966-dfd522b8-7d92-4145-8d9f-c328291aa8d1.jpg)

VISUALS:

![2a d](https://user-images.githubusercontent.com/103915142/231905837-5f99c8c3-8aca-4e29-8336-a32b6812caed.jpg)

![2b c](https://user-images.githubusercontent.com/103915142/232043464-42ce4e5a-1260-4e3e-8245-85beefcd3a9e.jpg)



![why_1a](https://user-images.githubusercontent.com/103915142/232208965-5a543283-60ce-458d-9c09-f8f5dcc2ce7b.jpg)


<br>


>### **QUESTION 2:** WHAT TOPICS WERE DISCUSSED THE MOST?


<br>



By understanding the most discussed topics, the call center can identify areas where their customer service is falling short. This information can be used to train agents on how to handle these topics better, which can improve the overall customer experience.
Also, if customers are repeatedly calling about the same issue, it could indicate a problem that needs to be addressed. By addressing the root cause of the issue, call center organizations can reduce the number of calls they receive about that topic.

     
Topics Discussed the Most                                                                                   |  Topics by Month
-------------------------------------------------------------------------------------------------------------|------------------------- 
![3a](https://user-images.githubusercontent.com/103915142/231994848-07efcfa1-e4af-4bfe-a206-f9a0ab1dc597.jpg)| ![3b](https://user-images.githubusercontent.com/103915142/231996053-874b8b16-17da-400f-bbc7-c91c7afc6719.jpg)


<br>



>### **QUESTION 3:** HOW WELL WERE THE TOPICS TREATED?


<br>



![3c](https://user-images.githubusercontent.com/103915142/232044889-e3db6be9-beb2-40ed-8143-9a45bf7ec998.jpg)


So, I began to wonder why these topics were unanswered or unresolved, especially the topics on technical support. 
I checked the "Average speed of answer in seconds by Topics" to see if I could get an answer. But to my surprise, it was revealed that on average, technical support calls were picked up in 53 seconds, which is the topic with the fastest answered call on an average.

![4a](https://user-images.githubusercontent.com/103915142/232004429-ea1f9144-45a5-4eb3-9c8e-3940aba6c502.jpg)

> __If the calls for technical support were answered the fastest on average, why is it still the most unanswered and unresolved topic?__

I suspected it had to do with the agents, maybe someone has a habit of keeping customers waiting for too long. So I checked and I wasn't wrong after all!

![4b](https://user-images.githubusercontent.com/103915142/232005670-e902a264-e5fd-4965-9be3-ca98588f7e10.jpg)

The table above shows that Joe has mostly been answering calls later than other agents. Averagely Joe picked up technical support calls after one minute, and it is possible the caller got tired of waiting and hung up. 


<br>



> ### **QUESTION 4:** AGENT AVERAGE SPEED OF ANSWER IN SECONDS?


<br>


Call center organizations often have SLAs in place with their clients, which specify the maximum amount of time customers should wait before their calls are answered. By monitoring the average speed of answering calls, call center organizations can ensure that they are meeting these SLAs and avoid penalties for failing to do so.

Table                                                                                                        |  Chart
-------------------------------------------------------------------------------------------------------------|------------------------- 
![5a](https://user-images.githubusercontent.com/103915142/232028044-1a7b3527-2de0-4cf7-b50e-3eecd1f98416.jpg)| ![5b](https://user-images.githubusercontent.com/103915142/232028080-404d14cc-4a5c-45d7-8d0b-d5f3922ab04d.jpg)


<br>



> ### **QUESTION 5:** AGENT SATISFACTORY RATING?


<br>



Knowing the satisfaction rating of agents for a call center is crucial as it helps to improve customer experience, increase retention rates, and boost overall business performance.

<br>


![6a](https://user-images.githubusercontent.com/103915142/232038940-27299773-699e-4cee-bbe7-b96802ee8e20.jpg)


## 4. DATA INSIGHTS

### 1. When it comes to running a call center, it's essential to understand when your customers are calling and how busy your agents are. By analyzing call center data from January to March 2021, we gained insights into the busiest day, hour, and month. Here's what we found:


&nbsp;&nbsp;&nbsp;&nbsp;**The Busiest Day:**

As we examined the data, one day stood out as the busiest: January 11, 2021. On this day, the call center received a significant increase in calls compared to other days in the period. Also, it was noticed that among the top 6 busiest days, the 11th day of each month appeared on the list. This surge in traffic could be attributed to a range of factors such as a promotional campaign, or service outage. It's essential to investigate what might have caused this peak to ensure you're prepared to handle similar traffic in the future.

&nbsp;&nbsp;&nbsp;&nbsp;**The Busiest Hour:**

Next, we looked at the busiest hour of the day. We found that the call center was busiest at 1 PM, followed by 11 AM, 5 PM, and 4 PM. This pattern suggests that customers may be more likely to call during their lunch break or in the late afternoon when their workday is coming to a close. It's worth considering scheduling more agents to work during these peak hours to reduce wait times and improve customer satisfaction.

&nbsp;&nbsp;&nbsp;&nbsp;**The Busiest Month:**

Next, we examined call center traffic by month. We found that January was the busiest month, with a significantly higher number of calls than February and March. This could be due to seasonal factors, such as post-holiday customer inquiries or new year resolutions. However, it's worth noting that February and March are traditionally quieter months for many industries. Understanding these trends can help you plan for the future and optimize your staffing levels accordingly.




### 2. As a call center manager, understanding the most common topics your customers call about can help you optimize your resources and improve customer satisfaction.


&nbsp;&nbsp;&nbsp;&nbsp;**The Most Common Topics:**

Our analysis revealed that customers called most often about Streaming, followed by Technical Support, and Payment Method. This suggests that customers are having the most issues with streaming content, technical difficulties, and payment processing. It's worth investigating why these issues are occurring and identifying ways to improve the customer experience in these areas.

&nbsp;&nbsp;&nbsp;&nbsp;**The Least Common Topics:**

On the other end of the spectrum, we found that Contract-related and Admin Support topics had the least number of calls. This could indicate that customers have a good understanding of the contract terms and are not encountering many issues related to administrative tasks. However, it's worth reviewing these topics to ensure that customers are receiving the support they need and identifying any areas for improvement.

&nbsp;&nbsp;&nbsp;&nbsp; Our analysis also shows that the three most discussed topics, Streaming, Technical Support, and Payment Method, topped the chart in January with the highest call volume for each. This trend continued in March, with the same topics having the highest call volume. However, February was different - while these topics still had high call volume, the counts of the two least common topics, Contract-related and Admin Support, were higher than in March. This resulted in February having a higher overall call volume compared to March.


### 3. In our previous analysis, we identified the top five customer topics based on call volume from January to March 2021. In this follow-up analysis, we'll explore how well these topics were handled by the call center, as well as the average speed of answers for each topic.

&nbsp;&nbsp;&nbsp;&nbsp;**Topic Resolution:**

Our analysis shows that the majority of calls were answered and resolved by call center agents, indicating that the center is performing well in terms of handling customer issues. Additionally, we found that the three most discussed topics - Streaming, Technical Support, and Payment Method - had higher resolution rates than the other topics. This suggests that agents may have more experience and training in handling these topics compared to the other less-discussed topics.

&nbsp;&nbsp;&nbsp;&nbsp;**Average Speed of Answer:**

We also analyzed the average speed of answer (ASA) for each topic, which measures the time it takes for a call center agent to answer a customer call. Our data shows that Technical Support topics had the fastest average speed of answer, followed by Contract-related topics, Admin Support, Payment Method, and Streaming topics, which had the highest ASA. The average speed of answers for all topics ranged from 53.8 seconds to 55.44 seconds, which suggests that agents were able to answer calls within a minute on average.

&nbsp;&nbsp;&nbsp;&nbsp; Our data shows that Agent Joe had a higher average speed of answer compared to other agents, especially for Streaming and Technical Support topics. On average, Joe took 61 and 62 seconds to answer calls related to these topics, respectively. This suggests that there may be room for improvement in Joe's response time, which could lead to more satisfied customers.

&nbsp;&nbsp;&nbsp;&nbsp; Interestingly, we found that Technical Support topics had a higher count of unanswered and unresolved calls despite having a faster average speed of answers compared to other topics. Additionally, Streaming topics had the third-highest count of unresolved calls. These findings suggest that there may be other factors contributing to call resolution rates besides the average speed of the answer.



### 4. In our next analysis, we identified the agent’s average speed of answer in seconds. As I dug deeper into the data, I discovered that not all agents are created equal when it comes to answering calls.

&nbsp;&nbsp;&nbsp;&nbsp; Diane, the star agent, was lightning-fast on the phone, answering calls on average in just 52 seconds. Her quick response time helped to keep customers satisfied and prevent them from getting frustrated and taking their business elsewhere. Jim and Steward were close behind Diane, answering calls in under a minute.

&nbsp;&nbsp;&nbsp;&nbsp; Joe, in particular, had an average response time of 57.9 seconds, making him the slowest agent on the team. Customers calling in for help were left waiting for almost a minute before Joe picked up the phone, leading to frustration and dissatisfaction.

&nbsp;&nbsp;&nbsp;&nbsp; The difference in response times between agents may seem small, but in a call center, every second counts. A delay of just a few seconds can mean the difference between a satisfied customer and a lost one. By identifying the agents who were struggling to keep up with the pace of the call center, the team can work to improve their response times and provide better service to their customers.



### 5. In any call center, the quality of service provided by agents is an essential factor in ensuring customer satisfaction. In my analysis, I explored the agent’s satisfactory ratings to find out how the customers perceive the services rendered by the different agents.

&nbsp;&nbsp;&nbsp;&nbsp; Interestingly, despite Dan having the third slowest rate of response (SRR) to calls, he was the agent with the highest number of "5" satisfactory ratings, indicating that customers were more satisfied with his services compared to the other agents. Martha followed closely behind Dan in the rating, despite bagging the second slower rate of response to calls. Jim and Diane, who had faster rates of response, were also highly rated by customers.

&nbsp;&nbsp;&nbsp;&nbsp; However, on the other hand, the ratings of Stewart and Joe were less impressive, with Joe having the least number of "5" ratings. Interestingly, even though Stewart had the third-fastest SRR to calls, his satisfactory ratings were among the lowest, indicating that customers might not have been satisfied with the quality of his services.

&nbsp;&nbsp;&nbsp;&nbsp; Also, we saw that the agents were rated “3” and “4” more than they were rated a “5” which indicates that most customers weren’t utterly satisfied. 


## RECOMMENDATIONS

-- The company should consider scheduling more agents to work during peak hours to reduce wait times and improve customer satisfaction.

-- If Streaming and Technical Support are the most common issues, it may be worth allocating more resources to these areas or providing additional training to agents.

-- The higher average speed of answer by Agent Joe may be a potential area for improvement to ensure that customers receive prompt attention and that their issues are resolved promptly. 

-- Provide additional training to the agents who have slower response times or consider implementing new technology or processes to help speed up call response times across the board.

-- While a fast SRR to calls is essential in a call center, it is not the only factor that determines customer satisfaction. Factors such as the ability to communicate effectively, solve customers' problems, and provide excellent customer service also play crucial roles in ensuring customer satisfaction.


## CONCLUSION

Overall, we discovered that the busiest month was January, and the busiest times for the call center are 11 AM, 1 PM, 4 PM, and 5 PM. With the peak by 1 PM. We also found that customers mostly call for streaming, technical support, and payment-related topics. 
In terms of agent performance, Diane had the fastest rate of answering calls, while Joe had the slowest. Asides from Joe's slow response time, he received a lower count of "5" satisfactory ratings compared to other agents. We also saw that response time alone does not necessarily determine customer satisfaction. It's important to consider other factors such as empathy, problem-solving skills, and overall customer service experience. By identifying these key insights, the call center can better allocate resources, prioritize training and coaching for agents, and improve overall customer satisfaction.
























