# Attain Answers AI Platform Practicum for Attain LLC

### Project Description:
* Business Analytics Practicum Course Project(DNSC 6217), Attain, LLC, Washington DC
* Time: Sep. 2018 – Dec. 2018
* Participants: Xuan Yang, Mengchen Xiao, Weihang Wen, Yinian Lyu, Weichao Zhu
* Instructor: Prof. Shivraj Kanungo
* Company Main Contacts: Tim Pavlick(tpavlick@attain.com), Alex Brown(abbrown@attain.com)

### Problem Description
* The problem we are trying to solve is to help Attain. Inc, improve its digital consulting platform. Attain. Inc, a risk consulting company, now is planning to build a brand new consulting platform based on Attain Answers which is a cloud-based collaborative work
environment. 
* By leveraging the Attain Answers, we first can import and store the customers’ profile, services that Attian might provide and project information so that we can then build project plan, divide the plan into small steps and assign them to appropriate ones. Some jobs will be executed by Artificial Intelligence library and the place we kick in is to build Human Analytics Managed Services used to analyze public attitude and reflection towards certain topics which may lead to risks. Thus, to identify risk, what we do is to build a pipeline connecting a web scraping platform called Webhose and social network analysis platform called Maltego. After finished the pipeline, we will be working on Anti-semitism & Antifa topic and analyze how people who against Anti-semitism & Antifa connecting with each other or other organizations and what risk they might cause. The last part of the project is to evaluate the job execution. After the project finished, all these information will be stored in database and used to analyze customers’ demand trend by using unsupervised learning. And what we do is to improve Attain consulting services by using that trend.
* Besides, to better and faster execute the plan, the company needs to choose the right members. This is another place we will be part of it. We will index everyone’s skills on their resumes and find the one with skills suitable for different plans, by utilizing the AI
library.
* The another problem is that will risk factors e.g, schedule, budget, etc. influence the overall project risk and if they do, what is the relationship between them? The dataset Attain provides us with 8 projects and two aspects of risk in every project. One aspect focuses on difference in risk assessment between project manager risk and Attain assessment. Another one shows the way risk assessment project manager obtained by timing the rates of probability and impact. With the help of risk data, we are able to see the upcoming risks and prevent risks with high impact and high probability during planning job execution phase and job execution phase.

### Questions we are going to answer
#### Anti-semitism & Antifa trends across the sites
* One topic we are working on is Anti-semitism & Antifa trends across the sites. Customer of Attain is specifically interested in understanding Anti-semitism & Antifa trends across the sites. Since both of these trends can cause violence, customers really want to understand how these trends are developing and whether they are trending toward violent expression. However, typically our customer would conduct research on extremism groups by reading news, blogs or articles from website to website, which might be time-consuming and might make some underlying connections to be overlooked. What Attain wants to do is to look at these groups from a more macro perspective and to provide insights that might be imperceptible when looking from only one aspect.
* To be more specific, we want to figure out the leaders and members in these extremism groups, and the platform that they use to communicate and exchange information within the group. We would also look into major movements they have organized, focusing on their ideology, strategy, plans, and both physical and nonphysical assets. In addition, utilizing social network analysis, we would analyze the relationship between different entities involved to see whether they are concentrated in one area or connected by one specific person or organization. 
* Besides, we are also interested in how dangerous these groups are. We would detect and then examine their threat language and also analyze their energy and physical assets to figure out their ability of turning into actual violence so that we could identify risks in advance.

#### Risk data
* Another topic we are working on is the to understand the risk within Attain. We examined Attain risk data to understand if it is possible to predict recurring risks from the risk factors provided. The risk data we got has the probability, impact and criticality for 8 different projects overtime and each project has the same risk factors such as resources and quality. Here, the criticality equals probability times the impact. We want to see if there is a pattern in the risk data and those risks can be predicted by a model. Therefore, the company can know on which month the risk for the project will increase and be well prepared for those risks.

#### Resume Text Mining
* Attain also wants to assign the projects or tasks to appropriate people more efficiently at the beginning of a new project. By utilizing Attain’s AI library, we would conduct unsupervised learning on employees resumes to create index for skills so that each resume could be tagged with one or more skills the employee has, which could help to find the right person with the skills in need.

#### Proposal Text Mining
* Just like creating index for skills in resumes, Attain would also like to create index for topics in proposals. We would utilize Attain’s AI library to conduct unsupervised learning on proposals and build a model that could extract the main topics in a specific proposal. By doing so, managers could save plenty of time and efforts of reading proposals that have dozens of pages.

### Expected Outcome
The platform based on Webhose API and Maltego would mainly work for the purpose to help Attain build Human Analytics Managed Services platform and thus finish the skeleton of entire digital consulting platform, and the result of risk data analysis could be used to provide some data-driven suggestions to the consultants in the attain company.

### Procedures:
* Used Attain Answers AI library for text mining analysis on more than 100 Attain resumes, which allows Attain to search by specific skills needed, for a given job, and to find the correct person based on Python; 
* Organized, explored, analysed, visualized Attain risk data to predict recurring risks from 12 independent variables provided, e.g., schedule, budget, etc.using R, Tableau, SAS JMP; 
* Implemented Market Basket Association analysis to train machine learning model in order to match customers’ demand with Attain’s service using SAS JMP;
* Researched, preformed, completed social network analysis and human behaviors analysis projects on Anti-semitism & Antifa topic using Webhose.io API, and Meltego.

