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

# This lab introduced us to the analysis of integration test data using reliability assessment tools and how critical it is to ensure the quality and reliability of systems. We put into practice two methods for assessing failure data: 

1) Reliability growth testing 
2) Reliability assessment using Reliability Demonstration Chart (RDC)

These methods are crucial in the real world because they give useful information on the effectiveness and dependability of systems, leading to programmers spotting possible problems early on and taking the necessary steps to fix them. Utilizing these assessment tools helps stakeholders make educated decisions regarding the dependability of their systems and take the necessary steps to increase their performance and longevity.

Our goal for this lab was to acquire hands-on experience in evaluating the dependability of a hypothetical system by examining its failure data that was collected during integration testing. To implement the two methods for assessing failure data mentioned above, this lab was divided into two sections that solely focused on each of the methods.  

In the first part of our lab, we needed to set up a reliability growth assessment tool, such as SRTAT or CSFRAT, and create diagrams illustrating the system under test's (SUT) failure rate and reliability. CASRE was a tool that would help us select useful data. We tried using CASRE, which did not work due to being a very old software which is not supported by the current windows machines. For the reliability growth testing we decided to set up and use C-SFRAT as our reliability growth assessment tool. We are now familiar with the characteristics and usage of a reliability growth testing tool. 

For the second part of our lab, we were familiarized with the Reliability Demonstration Chart (RDC) tool and its usage. One of the main objectives for this section was to help us gain an understanding of how to determine the adequacy of testing for a given MTTF of the SUT through plotting the test data.

Upon completing this lab, we have a better comprehension of reliability growth testing and its significance. In this lab report, we have outlined the testing tools utilized in the experiment, including C-SFRAT or SRTAT, on the provided failure data set which comprises various test data files, and we selected one for each of the failure data analysis methods.


# Assessment Using Reliability Growth Testing 

# Assessment Using Reliability Demonstration Chart 

# 

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

# 

# Difficulties encountered, challenges overcome, and lessons learned
Various tools can be used to evaluate a system's dependability; however, they are only simulations and should not replace rigorous testing. However, their reliability is not guaranteed as much of the data they produce is calculated and approximated. Additionally, using these tools also requires a comprehensive understanding of each function and result interpretation. Nevertheless, learning about these tools is essential because they are frequently used in industry and becoming familiar with them can be advantageous in the future. The difficulty that we faced was CASRE not working on any of our laptops as it is an old software, and is not compatible with the system. Initially, we encountered some challenges in determining the steps to find the outcomes of the exercises. However, through diligent efforts, we were able to grasp the concepts by referencing the lecture notes and conducting additional research.


# Comments/feedback on the lab itself
The TAs were very helpful and helped us in understanding the lab requirements and what we needed to achieve for the report.

