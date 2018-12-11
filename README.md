# Attain Answers AI Platform Practicum for Attain LLC

### Project Description:
* Business Analytics Practicum Course Project(DNSC 6217), Attain, LLC, Washington DC
* Time: Sep. 2018 – Dec. 2018
* Participants: Xuan Yang, Mengchen Xiao, Weihang Wen, Yinian Lyu, Weichao Zhu
* Instructor: Prof. Shivraj Kanungo
* Company Main Contacts: Tim Pavlick(tpavlick@attain.com), Alex Brown(abbrown@attain.com)
* Final Report: [BA Practicum Final Report.pdf](/Deliverable/BA Practicum Final Report.pdf)
      
      

### Tasks Description
Improving the digital consulting platform with AI & Analytics The team is experimenting with several areas of Attain’s digital consulting platform to bring analytics to bear. The following mini-projects will combine to create an overall analytics upgrade to Attain’s digital consulting platform:

1. Improve ‘Service Selector’. After we have identified the customer & the customer's
requirements, then we source those requirements to Attain capabilities. From the ‘Service Categories’ various services can be selected. The team is working on optimizing the ‘association rules’ which suggest complimentary service sets (to planners).

2. Improve ‘Staffing’ visibility. One of the capabilities Attain applies to jobs is skilled workers. These staffs are currently listed by name. The team is using machine learning to cull through Attain resumes by skill. Once completed planners will be able to select staff, for a job, by querying which staff possesses a given skillset.

3. Design an Analytics Managed Service. AttainAnswers will be an online platform for the delivery of traditional consulting services & Asset-based consulting. An evolution beyond that would be ‘Analytics Managed Services’. Based on a prior engagement pattern, the team is designing & building a prototype of an Analytics Managed Service to be exposed and offered on the AttainAnswers platform.

4. Consulting Risks Analysis. A key execution aspect in consulting engagements is risk management. The team took Attain data, detailing the risk profiles of engagements, and analyzed them for a cause. Insights culled from this analysis will inform how the ‘risk features’ of AttainAnswers will be designed to best assist engagement planners.

5. Bonus task. If time allows the team will examine the AttainAnswers lifecycle and make recommendations for how to analyze holistic engagement performance such that AttainAnswers will become smarter over time. With this insight, the platform can direct executives as to how the customer, partner or Attain fulfillment trends are changing over time.


### Questions we are working on
#### Resume Text Mining
Attain also wants to assign the projects or tasks to appropriate people more efficiently at the beginning of a new project. By utilizing Attain’s AI library, we would conduct unsupervised learning on employees resumes to create index for skills so that each resume could be tagged with one or more skills the employee has, which could help to find the right person with the skills in need.

For the resume files from Attain, we did some basic text mining exploration like word count and word cloud visualization, and text transformation using TF-IDF on the given resumes and have been trying to working on the topic clustering based on LDA model.

1) At first, we did some basic text preprocessing like tokenizer, stemmer, removing stopwords and common punctuations so that the text files are much cleaner for further analysis. See below.

<img src= 'Resumes mining/remove stopwords.png'>

<img src= 'Resumes mining/Lowercase and remove punctuation.png'>

2) Here is the word cloud generated from all the resume files, showing the frequency of the words in the resumes of Attain.

<img src='Resumes mining/word cloud.png'>
      
3) Here are the 20 most common words from the resume files. 
<img src='Resumes mining/20 Most common words from all resume data.png'>
      
4) Here are some common collocations from resume files. 

<img src='Resumes mining/common collocations from all resume data (1).png'>
      
5) Here is another exploratory analysis on the resume files that could be useful when we want to analyze some specific words. 

<img src='Resumes mining/Sentences including word (skill) from all resume data.png'>
      
6) After resume data clean and data exploration, we next step would like to implement text transformation. We referred to TF-IDF theory. This theory could be divided into two concept: one is importance and the other is frequency. TF stands for term frequency, which equals to count(word) / len(document); IDF stand for inverse document frequency namely term importance, which formulated by log( total number of document / count(document_containing_term)). Then we define TF-IDF function in python and apply to resume data. See Graph 3.7. In the graph, we could find the most feature word of each resume order by value of TF-IDF from high to low.

<img src='Resumes mining/TF-IDF.png'>

7) The next step is document clustering by using Doc2Vec algorithm. This method differ from word count or TF-IDF or LDA. Because it takes word order into account, but LDA only cares word by word seperately. In the future, we can search a target resume by descripting on word group or sentences level, for example, have 5+ years experience on Python and proficient in project management.

<img src='Resumes mining/Doc2Vec.png'>


#### HAMS (Human Analytics Managed Services)
* We are developing an analytics services to classify and visualize people’s opinions via custom internet search.The workflow is first crawling the data from the Internet, where client could define the search terms and data source, and then importing all data into a temporary database. Next, we build models to filter and classify the data queried from database. Finally, we would visualize the results in Maltego Application. 

<img src= 'Social Network Analysis/Pipeline.png'>

* One topic we are working on is Anti-semitism & Antifa trends across the sites. Customer of Attain is specifically interested in understanding Anti-semitism & Antifa trends across the sites. Since both of these trends can cause violence, customers really want to understand how these trends are developing and whether they are trending toward violent expression. However, typically our customer would conduct research on extremism groups by reading news, blogs or articles from website to website, which might be time-consuming and might make some underlying connections to be overlooked. What Attain wants to do is to look at these groups from a more macro perspective and to provide insights that might be imperceptible when looking from only one aspect.
* To be more specific, we want to figure out the leaders and members in these extremism groups, and the platform that they use to communicate and exchange information within the group. We would also look into major movements they have organized, focusing on their ideology, strategy, plans, and both physical and nonphysical assets. In addition, utilizing social network analysis, we would analyze the relationship between different entities involved to see whether they are concentrated in one area or connected by one specific person or organization. 
* Besides, we are also interested in how dangerous these groups are. We would detect and then examine their threat language and also analyze their energy and physical assets to figure out their ability of turning into actual violence so that we could identify risks in advance.
* For the social network analysis platform part, we found a new and easy way to achieve the result which is the visualization of the json data from the Webhose in Maltego. Basically, what we are doing now is using the Local Transforms in Maltego which can transform python scripts to the configuration package that Maltego can use and then visualizing relationships between entities in the way we want. For now, we’ve visualized  over 1000 entities and below screenshoot is our newest outcome. In short, three centers of the network are three site types, blogs, news and discussions. Outer nodes are sites like reddit.com, 4chan.org, freerepublic.com, etc. Next level of nodes are section titles under different sites for instance, /pol/ - Politically Incorrect - 4chan, The Donald - America First!, etc. The inferior nodes are different threads under section titles like “Trump Rally”, “MSM blatantly lies about Antifa violently attacking Proud Boys. Skips over the fact that the three arrested were ANTIFA, not Proud Boys.”, etc. The outest nodes are posts under different threads. 

<img src= 'Social Network Analysis/Social Network Analysis 01.png'>

#### Risk data
*Another topic we are working on is the to understand the risk within Attain. We examined Attain risk data to understand if it is possible to predict recurring risks from the risk factors provided. The risk data we got has the probability, impact and criticality for 8 different projects overtime and each project has the same risk factors such as resources and quality. Here, the criticality equals probability times the impact. We want to see if there is a pattern in the risk data and those risks can be predicted by a model. Therefore, the company can know on which month the risk for the project will increase and be well prepared for those risks.

1) Descriptive analysis

For descriptive analysis, we utilize aggregated values of each factor for plotting trending lines across all months. Specifically, we preprocess average of each factor for every same month across all projects. Then we could see in general the trending fluctuation of each factor overtime. According to the result, we found, in general, project risk getting worse in winter focusing in November, December and January. On the contrary, May, June and Febrary are generally likely to have smooth project going. 

<img src= 'Risk data/Aggregated trending line.png'>

Also we would like to show the percentage of each factor accounting for total in every month. So we also visualized aggregated bar plot over time. According to the plot shows, the highest level of criticality is 9.857 and the lowest level of criticality is 2.333. Besides, Budget and Resource are generally the most dangerous factors which we should pay more attention to.

<img src= 'Risk data/Aggregated Bar Chart.png'>

In addition, we are also curious about the multicollinearity of these measure factors. So we also conduct correlation analysis by binary table as well as statistical probability to see how strong of their positive or negative relationships.

<img src= 'Risk data/Correlation_01.png'>

2) Time Series Predictive Analysis

For the risk data, we has the criticality for 8 different projects overtime and each project has the same 13 risk factors such as resources and quality. Last time, we wanted to see if there was a pattern in the risk data and those risks could be predicted by a model. But the time series models for the overall risk and risks for different projects we got had a low R square. Therefore, we made some improvements for the models such as adding seasonal dummies, different kind of trends and ARMA model for seasonals. As we expected, the R square increased a lot, which is more than 0.7. Here are the results from SAS for the overall risk and the resources risk. For example, the resources risk factor, the R Square is even more than 0.8. The R square increased and the error decreased significantly after we use the hyperbolic trend.

<img src= 'Risk data/Time Series 01.png'>

<img src= 'Risk data/Time Series 02.png'>

<img src= 'Risk data/Time Series 03.png'>

<img src= 'Risk data/Time Series 04.png'>


### Results
1.	Resume Topic Modelling with LDA model.

With the help of the optimal LDA model, 8 topics from the resume files were concluded and we could demonstrate the words in the 8 topics using wordcloud. The visualizat show the frequency of the words in each topic that we get from the optimal LDA model, which can give us a clear view of the frequency of the words. Here is the output of the wordcloud for the 8 topics respectively.

2. Resume Text Classification

As for the resume classification, the convolutional model reached a accuracy of 0.85 after validation. The loss curves and accuracy curves are shown below.

3. HAMS (Human Analytics Managed Services)

The gray nodes are sites like “reddit.com”, “4chan.org”, “freerepublic.com”, etc. In this case, the site is only “reddit.com”. Next level of green nodes are section titles (subreddit) under different sites for instance, “STRAYING OUTSIDE OF THE STATUS QUO IS FOR MELVINS”, etc. The red inferior nodes are different threads under section titles like “Centrist conspiracy theorists”, “the meaning of christmas”, etc. The outest yellow nodes are posts under different threads.

<img src='Social Network Analysis/Visulization.png'>

4. Risk Data

As we expected, the R square increased a lot, which is more than 0.7. Here are the results from SAS for the overall risk and the resources risk. For example, the resources risk factor, R Square is even more than 0.8. The R square increased and the error decreased significantly after we use the hyperbolic trend. With those descriptive analyses and time series models, we can predict the risks for each risk factor and overall factor, which can provide those engagement planners with insightful information when they are executing the projects.

### Conclusions:
1. Platform Improvements

* Improved how consulting services get picked for jobs
* Improved Attain’s ability to understand their workforce and pick the right people for jobs
* Improved Attain’s ability to understand market conditions affecting the job
* Improved Attain’s understanding of which factors drive engagement risk

2. Business Improvements

* Better source jobs (services and staff)
* Understand engagement context & risks to avoid
* Leads to more intelligent job execution


### Procedures:
* Improved Association Rule Mining Analysis to train machine learning model in order to match customers’ demand with Attain’s service using Python Apriori algorithms;
* Used Attain Answers AI library for text mining analysis on more than 100 Attain resumes, which allows Attain to search by specific skills needed, for a given job, and to find the correct person based on Python LDA algorithms; 
* Organized, explored, analysed, visualized Attain risk data to predict recurring risks from 13 independent variables provided, e.g., schedule, budget, etc.using R, Tableau, SAS Time Series Analysis; 
* Researched, preformed, completed social network analysis and human behaviors analysis projects on Anti-semitism & Antifa topic using Webhose.io API, and Meltego.

