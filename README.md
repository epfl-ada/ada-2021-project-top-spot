# Brexit under the lens

### 1. Abstract:

Brexit was the withdrawal of the United Kingdom from the European Union. The United Kingdom is the first and so far the only member state to have left the EU, after 47 years of having been a part of the union. It is an event that has made people very vocal and different opinions have been shared, particularly in the media. In this project, we want to put this event under the microscope and investigate several aspects of it. First, we want to do a descriptive analysis: When did we start mentioning Brexit, which words are used the most in our database, which are the main authors of the quotes, which media have relayed the information the most, etc. 

### 2. Research Questions: 
A list of research questions you would like to address during the project.
- The media's coverage of Brexit from 2015 to 2020 considering data in Quotebank:
	- When did the media start to mention Brexit? How many quotations are related to Brexit? 
	- How did the number of quotations change over time?
- Media views towards Brexit:
	- Which media have relayed the information the most? 
	- What is the country of origin of these media? 
	- What media and websites tend to have positive or negative statements towards the situation? 
- Who issued these quotes, and what were the main opinions:
	- How many active speakers are mentioned? 
	- What are the main topics discussed? 
	- What were their professions? 
	- Where do they come from? 
	- How has the number of active speakers changed over the different periods of Brexit? 
	- What is their sentiment about the situation, content or not content, independently of their opinion on pro or against Brexit?  
	- Did they change their perception during this period? 
	- How are the different sentiments of the speakers distributed by countries?

### 3. Proposed additional datasets 

- Add more attributes to the data (topic, profession, country, gender, nationality..)

	- [Speaker attributes dataset](https://drive.google.com/drive/folders/1VAFHacZFh0oxSxilgNByb1nlNsqznUf0) provided by ADA teaching group. 
- Using beautiful soup to extract the country of the domain through [this source](https://icannwiki.org/Country_code_top-level_domain) .

### 4. Methods 

- **Data collection:**
  To merge quotebank with the additional datasets, we have filtered those quotations related to Brexit by identifying possible keywords related to Brexit. We have already combined quotations with speaker attributes by joining with QIDs. 

- **Media Coverage Analysis:**
  We will perform descriptive analysis and visualize the results with scatter plots, histograms to show how the change of media attention to Brexit over time.

- **Media SentimentsViews towards Brexit Analysis:**
	We will perform sentiment analysis on all quotations. Then we are going to visualise the overall sentiment of each media(which is defined as “domain” in our current dataset)  towards Brexit. What’s more, we could compare the sentiment of the media over different countries.
- **Analysis of who delivered the quotes and what the prominent opinions were:**
	- Performing the sentimental analysis on quotations by using VADER Python library to identify active speakers for pro-Brexit/anti-Brexit.
	-  Applying spectral Clustering for speakers and to different subclass professions over time. 
	-  Using the n-garms and LDA topic modeling, we want to identify the top topic to find some top reasons that they are pro-Brexit or anti-Brexit. 
	-  Visualizing the change of predominant opinions pro-Brexit and anti-Brexit and the central topics and points mentioned

-  **Hypothesis of media’s influence on speakers:**
	- We want to discuss our results in the previous two points: the analysis of media sentiment towards Brexit and the speaker analysis. In more specific terms, we want to relate the nationality ranking of speakers who have positive feelings towards Brexit with the country ranking of media outlets that show overall positive attitudes towards Brexit, and the same applies towards negative groups.

### 5. Proposed Timeline
![alt text](https://github.com/epfl-ada/ada-2021-project-top-spot/blob/main/img/proposed_timeline.png)

### 6. Organization within the team:
A list of internal milestones up until project Milestone 3

| Task Name                                                    | Responsible  Member                                          |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| Brain storm and set the topic of the project                 | All team members                                             |
| Preprocess the dataset                                       | Chen Jingrong; Ben Hassen Mahdi                              |
| Performing initial analysis                                  | Agnaou Zineb; Haoyu Sheng                                    |
| Writing README file                                          | All team members                                             |
| Sentiment Analysis                                           | Ben Hassen Mahdi                                             |
| LDA and ngrams for defining the topics                       | Agnaou Zineb                                                 |
| Simple data visualization  (Histograms, Scatter Plots, Word Cloud) | Chen Jingrong                                          |
| Spectral Clustering                                          | Haoyu Sheng                                                  |
| Summarizing inferences                                       | All team members                                             |
| Find the template of website                                 | All team members                                             |
| Set the skeleton of website                                  | All team members                                             |
| Add the data visualisation to the website                    | Each member responsible for the part they were assigned  above |
| Refine the website                                           | All team members                                             |

### 7. Questions for TAs :
- Could we change, either add or delete, some sections ? Depending on the information we find along,  on the workload and time available ?
- Can we use the result of the sentiment analysis to determine if a speaker supports Brexit or not?
