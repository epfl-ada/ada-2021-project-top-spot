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
	- How sentiments of quotations revealed by top 10 medias change over recent years?
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
	- To merge quotebank with the additional datasets, we have filtered those quotations related to Brexit by identifying possible keywords related to Brexit. We have already combined quotations with speaker attributes by joining with QIDs. 

- **Media Coverage Analysis:**
 	 - We will perform descriptive analysis and visualize the results with scatter plots, histograms to show how the change of media attention to Brexit over time.

- **Media Sentiments towards Brexit Analysis:**
	-  We will perform sentiment analysis on all quotations. Then we are going to visualise the overall sentiment of each media, defined as “domain” in our current dataset, towards Brexit. Furthermore, we could compare the sentiment of the media over different countries.
	
- **Analysis of who delivered the quotes and what the prominent opinions were:**
	-  Using the n-garms and LDA topic modeling, we want to identify the top topics to find some of the reasons that motivated their opinions. 
	-  Visualizing the change of predominant opinions and the central topics and points mentioned.
	
-  **Hypothesis of media’s influence on speakers:**
	- We want to discuss our results in the previous two points: the analysis of media sentiment towards Brexit and the speaker analysis. In more specific terms, we want to relate the nationality ranking of speakers who have positive feelings towards Brexit with the country ranking of media outlets that show overall positive attitudes towards Brexit, and the same applies to the negative attitudes.

### 5. Organisation of github:
 We kept the data processing notebook that concerned milestone 2. We added one Notebook for our analysis, one for our LDA and one for our future improvements. We have split our code for version and storage reasons, details are found below:

- [DataProcessing_EDA.ipynb](https://github.com/epfl-ada/ada-2021-project-top-spot/blob/main/DataProcessing_EDA.ipynb) : Contains essentially the results of the previous for Milestone 2.  Here you will find details of how we processed the data, as well as all the relevant features. You will also find some preliminary plots and a preview of the results for the Sentiment Analysis.
- [Analysis.ipynb](https://github.com/epfl-ada/ada-2021-project-top-spot/blob/main/Analysis.ipynb): answering our main questions. 
- [LDA.ipynbb](https://github.com/epfl-ada/ada-2021-project-top-spot/blob/main/LDA.ipynb): Since the packages used to perform the part with LDA require specific package versions that are not uniform with the rest of our analysis, we were compelled to put this part in a different notebook. Unfortunately, the notebook does not allow to see the interactive results. We invite you to consult [this link]( https://colab.research.google.com/drive/17yDMfJ9TAXIvVnlL3YPpR7tRVn-bxfjf#scrollTo=e852b175) which directs you to the associated Colab where you can visualize all the results. 
- [FutureImprovements.ipynb](https://github.com/epfl-ada/ada-2021-project-top-spot/blob/main/FutureImprovements.ipynb): contains our Spectral Clustering Analysis. Since the File is very big, we can't see the preview in Github. You can access the associated [Colab](https://colab.research.google.com/drive/1PC8Ht0AmwjlDcsgtEIF9JuQ_wKUaDEJn?usp=sharing) to see the plots. 

### 6. Website/ Data story:
A more concise version of our analysis and results will be available on our website. To have access to it, please click on the following link. 


### 7. Future Improvements :
-  Spectral clustering was applied for speakers and for different subclasses over time.  We first encoded the category features-nationality, polarity, and occupation-using two methods: hot encoding and target encoding. We then used the T-SNE method to compress the features and generate tsne_x,tesn_y so that they could be plotted in 2D or 3D graphs. We obtained some plots and results, but we will leave the final interpretation and more advanced implementation of the T-SNE approach to be done as a future improvement.

### 8. Organization within the team:
A list of internal milestones up until project Milestone 3

| Task Name                                                    | Responsible  Member                                          |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| Brain storm and set the topic of the project                 | All team members                                             |
| Preprocess the dataset                                       | Chen Jingrong; Ben Hassen Mahdi                              |
| Performing initial analysis                                  | Agnaou Zineb; Haoyu Sheng                                    |
| Writing README file                                          | All team members                                             |
| Sentiment Analysis                                           | Agnaou Zineb                                             |
| LDA and ngrams for defining the topics                       | Ben Hassen Mahdi                                              |
| Simple data visualization  (Histograms, Scatter Plots, Word Cloud) | All team members                                           |
| Spectral Clustering                                          | Chen Jingrong                                                  |
| Summarizing inferences                                       | Agnaou Zineb                                             |
| Find the template of website                                 | All team members                                             |
| Set the skeleton of website                                  | All team members                                             |
| Add the data visualisation to the website                    | Chen Jingrong; Haoyu Sheng                                    |
| Refine the website                                           | All team members                                             |


### 9. (OLD)Proposed Timeline
![alt text](https://github.com/epfl-ada/ada-2021-project-top-spot/blob/main/img/proposed_timeline.png)

### 10. (OLD)Questions for TAs :
- Could we change, either add or delete, some sections ? Depending on the information we find along,  on the workload and time available ?
- Can we use the result of the sentiment analysis to determine if a speaker supports Brexit or not?

