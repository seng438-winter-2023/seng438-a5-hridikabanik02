**SENG 438- Software Testing, Reliability, and Quality**

**Lab. Report \#5 – Software Reliability Assessment**

| Group \#:       |   |
|-----------------|---|
| Student Names:  |    |
|         Radia Jannat        |   |
|         Hridika Banik        |   |
|        MD Shaherier Khan         |   |
|       Mohammad Abbas Kazmi          |   |

# Introduction

This lab introduced us to the analysis of integration test data using reliability assessment tools and how critical it is to ensure the quality and reliability of systems. We put into practice two methods for assessing failure data: 

1) Reliability growth testing 
2) Reliability assessment using Reliability Demonstration Chart (RDC)

These methods are crucial in the real world because they give useful information on the effectiveness and dependability of systems, leading to programmers spotting possible problems early on and taking the necessary steps to fix them. Utilizing these assessment tools helps stakeholders make educated decisions regarding the dependability of their systems and take the necessary steps to increase their performance and longevity.

Our goal for this lab was to acquire hands-on experience in evaluating the dependability of a hypothetical system by examining its failure data that was collected during integration testing. To implement the two methods for assessing failure data mentioned above, this lab was divided into two sections that solely focused on each of the methods.  

In the first part of our lab, we needed to set up a reliability growth assessment tool, such as SRTAT or CSFRAT, and create diagrams illustrating the system under test's (SUT) failure rate and reliability. CASRE was a tool that would help us select useful data. We tried using CASRE, which did not work due to being a very old software which is not supported by the current windows machines. For the reliability growth testing we decided to set up and use C-SFRAT as our reliability growth assessment tool. We are now familiar with the characteristics and usage of a reliability growth testing tool. 

For the second part of our lab, we were familiarized with the Reliability Demonstration Chart (RDC) tool and its usage. One of the main objectives for this section was to help us gain an understanding of how to determine the adequacy of testing for a given MTTF of the SUT through plotting the test data.

Upon completing this lab, we have a better comprehension of reliability growth testing and its significance. In this lab report, we have outlined the testing tools utilized in the experiment, including C-SFRAT or SRTAT, on the provided failure data set which comprises various test data files, and we selected one for each of the failure data analysis methods.


# Assessment Using Reliability Growth Testing 
From the given options we decided to use C-SFRAT as our testing tool. Following the instructions on the lab report we were able to successfully set up C-SFRAT. To open a failure dataset in C-SFRAT we decided to change up the data accordingly. C-SFRAT accepts a .csv file, so we moved over the data from Failure Report 3(word doc) to a .csv file and changed the headings of the columns as well. Once the .csv file was ready, we imported that failure dataset on C-SFRAT and this is the graph that was produced:

![1](https://user-images.githubusercontent.com/101438221/230685422-19804a3e-0de7-4708-9ddb-c8d9e9962052.png)
This graph was seen in the Data Upload and Model Selection tab of C-SFRAT. 

Then we selected all the models listed out under the Select Hazard Functions to produce the graph below:
![2](https://user-images.githubusercontent.com/101438221/230685465-95e42c03-371f-4a79-a7cf-84daac588ea3.png)
In the Model Results and Predictions tab, we can view all the models that we selected for our failure data to see which of the models best fit with the graph generated from the failure data. 

![3](https://user-images.githubusercontent.com/101438221/230685486-980ac7d7-d0a8-49f3-9865-9ed18d8528ab.png)
In the Model Comparison tab we could see all the data from the models selected in a table. Clicking on the header sorts the table in ascending order and that way we could see what models best fit our failure dataset’s graph. We checked the log-likelihood for the biggest number and the AIC for the smallest value, and we can conclude that the model NB2 is the best fit model with our failure dataset.

![4](https://user-images.githubusercontent.com/101438221/230685513-8a13ec37-e6ba-45c3-bb23-cf61ee585acb.png)
The graph above is the Failure Intensity graph that was created after selecting all the models.

# Assessment Using Reliability Demonstration Chart 
As we have come to learn, a Reliability Demonstration Chart (RDC) is very useful in assessing failure data when we have limited failure data, when the duration of failures is unknown, and to determine if the target failure rate or Mean Time To Failure (MTTF) is met. To examine the system’s reliability performance, failure data is gathered at various time points and then plotted graphically to analyze any trend it shows.

From the given options, we chose to use the RDC-11 tool for this section of the lab. As mentioned in the lab document, RDC-11 is an Excel worksheet and a macro. The RDC we were given in the excel sheet consisted of the Cumulative Failure Count on the vertical axis, while the Normalized Value of the Number of Input Events is plotted on the horizontal axis. After plotting our data points, with the help of the RDC we were able to visualize the graph of system reliability over a certain number of input events, and then understand the systems performance.
We chose Failure Report 3 for this part of the lab, so this is the failure data we input into RDC-11 in the Failure Data sheet. The initial dataset had 24 rows of data, where the dataset consisted of each of the failures being listed along with its failure time recorded in seconds. However, the RDC-11 only had 16 rows of data that it accepted. According to Failure Report 3, the last failure was recorded at 903 seconds. Considering an error margin, we assumed the end time for the system to be at 960 seconds. Then we divided the 960 seconds in the 16 rows of the RDC-11 and wrote the cumulative failure count according to the Failure Report 3 data as well. After getting familiarized with how to read the graph and how to work with it, we came to the conclusion that our MTTF was 40 and our MTTFMin was 42.

1.RDC for MTTFMin
<img width="277" alt="5" src="https://user-images.githubusercontent.com/101438221/230686000-a5874814-b311-4370-9a32-a41b7b8f2e8d.png">

The graph displays the plot for MTTFmin which is 42 in this case as mentioned before. The plot shown above was created using the failure data that we input and then we determined the MTTFMin through a process of experimentation. The MTTF calculation for this specific graph is 960/24 = 40. Then to find the MTTFMin, we put in values close to the MTTF value to see when the graph had just crossed over from the Continue Test(yellow) region to the Accept(green) region. Based on the trend shown, it appears that the system's reliability is within an acceptable range for our Failure Intensity Objective(FIO), without significantly dipping into the rejection zone.

2.RDC for twice of MTTF
<img width="278" alt="6" src="https://user-images.githubusercontent.com/101438221/230686064-781b3aa4-1b39-43dc-9887-f8460d102e74.png">

The graph above displays the plot for twice the MTTF which is 80 in this case. After locating the MTTFmin plot, the parameters were reworked to achieve twice the original MTTF value. Doing so moved the graph farther into the Rejection(red) zone, which is consistent with the changes we made to the graph. From what we can conclude looking at this graph is that it appears that the system's reliability is not within an acceptable range for our Failure Intensity Objective(FIO), since it significantly rises into the Rejection(red) zone.

3.RDC for half MTTFMin
<img width="278" alt="7" src="https://user-images.githubusercontent.com/101438221/230686130-b5396252-d9a3-4cc3-b95f-45d05b7b3cfe.png">

The graph above displays the plot for half of MTTFMin which is 21 in this case. After locating the MTTFmin plot, the parameters were reworked again to achieve half the original MTTFMin value. This trend shows a stronger inclination towards the acceptable range, which corresponds to the changes we made to the graph. Hence, we can conclude that it appears that the system's reliability is well within the acceptable range for our Failure Intensity Objective(FIO), since it significantly rises into the Accept(green) zone.


# Comparison of Results
Continuous testing of a system or product to find and correct flaws or failures until the reliability objective is met is known as reliability growth testing (RGT). To find and address flaws and increase the reliability of the system, testing it in various settings, situations, and inputs is required. A reliability growth curve is often used to illustrate the desired continuous increase in reliability over time.
On the other hand, based on a small sample of test data, reliability assessment using RDC is a statistical method that estimates the likelihood that a system will achieve its reliability requirements. RDC entails creating a graph that displays the likelihood of achieving the reliability target in relation to the quantity of test units that have been used. The graph is based on statistical models that account for the variation in the test data and the ambiguity in the reliability estimations.

RDC is a statistical approach that forecasts the likelihood of attaining the reliability objective based on a finite quantity of test data, whereas RGT is a process of continuous improvement that comprises testing and repairing until the reliability target is attained. When the system is anticipated to get better over time or when the dependability objective is not clearly stated, RGT is more appropriate. When the system is anticipated to reach a specific degree of dependability before being launched, RDC is better suited for those circumstances.


# Discussion on Similarity and Differences of the Two Techniques
These two failure data assessment techniques are similar, yet are very different when we look into them in more detail below:

1.Both the techniques use the concepts of failure times and Mean Time to Failure(MTTF) in order to evaluate the reliability and performance of the system under test (SUT).

2.Both the techniques require failure data to be gathered during the testing process. However, they differ in the ways this failure data is collected. For reliability growth testing, the systems are continuously monitored  and the failures are recorded as they occur. While for reliability assessment using RDC, failure data is collected only at certain points in time, for example the way we did in predetermined intervals.

3.Once we have gathered the failure data from both the techniques after the testing process, the next step for both the methods is to analyze the data we have. For reliability growth testing, we were able to view the trends and patterns using the different mathematical models. However, for reliability assessment using RDC, the failure data was plotted on a graph to visualize the cumulative number of failures over the (normalized value of) number of input events to assess the system's reliability performance at specific time points during testing.

4.In practice, the reliability growth testing is a very extensive testing technique because it needs a good amount of failure data since it aims to address reliability issues as they arise and work on them continuously to enhance the system’s reliability. Reliability assessment using RDC on the other hand requires only a limited amount of data that is used to plot the data on a graph to see whether it falls on the Rejected or the Accept region, or somewhere in between. That is what determines the whole system’s reliability using an RDC.

5.Lastly, both the methods require some tools to be able to view the failure data and to analyze them. For reliability growth testing, we needed to have an understanding of statistical analysis with tools, how to view reliability trends using the different modeling methods, and other failure data analysis techniques. But for reliability assessment using RDC, we required an understanding of graphical analysis techniques, and just using the RDC-11 tool and its features.

# How the team work/effort was divided and managed
In our team, we divided the workload evenly for the lab report. We initially focused on understanding the installation and usage of the tools, as well as interpreting the data. We then explored the functionalities of each tool and their relevance to system testing. After conducting the experiments and analyzing the results, all team members contributed to compiling a comprehensive lab report with thoroughness and accuracy.


# Difficulties encountered, challenges overcome, and lessons learned
Various tools can be used to evaluate a system's dependability; however, they are only simulations and should not replace rigorous testing. However, their reliability is not guaranteed as much of the data they produce is calculated and approximated. Additionally, using these tools also requires a comprehensive understanding of each function and result interpretation. Nevertheless, learning about these tools is essential because they are frequently used in industry and becoming familiar with them can be advantageous in the future. The difficulty that we faced was CASRE not working on any of our laptops as it is an old software, and is not compatible with the system. Initially, we encountered some challenges in determining the steps to find the outcomes of the exercises. However, through diligent efforts, we were able to grasp the concepts by referencing the lecture notes and conducting additional research.


# Comments/feedback on the lab itself
The TAs were very helpful and helped us in understanding the lab requirements and what we needed to achieve for the report.

