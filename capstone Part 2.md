##This  a markdown file

# Part 2 - new project - job skills

Four days ago I switch my capstone which was to predict changes in population using selected features. I was having trouble finding consistent meaningful data. After discussing my data issues with Haley, we came to the conclusion that my capstone should be abandoned and that I should pursue one that I was passionate about.  One of my many functions, as a professor in the Computer Information Systems department at a very large community college in Dayton, is to help students identify what careers they would be best suited for and help them get either an internship or job in chosen IT field.

New Problem Statement: Identify the skills sets employers require for data scientists, data engineers, and data analysts.   

Why: This model can be used at my college for the following reasons: 
    1. To identify different skills sets needed for Sinclair’s degrees.   
    2. Provide valuable insights when revising curriculum. 
    3. Assist employers in identifying the job title for a given set of job duties.  Some small employers have trouble labeling the type of student they need for a job or internship. 
    4. Assist students when developing their LinkedIn profile and resume.  

Data will be scraped from Glassdoor and Indeed, a job/career/company information websites and USA Jobs.  Glassdoor provides information from both employees and former employees and employers. Employers can submit their salaries, job and company reviews,  questions from interviews, and other information. Not all information is easily obtainable (this is an issue expanded upon below).  USA Jobs is the federal government’s website which has an API.  Dayton has a lot of federal jobs since we have a major Air Force base (employment =25,000) 

In order to access Glassdoor’s API I had to apply for access. I did so and was granted access.  

Methods 
The project involves scrapping data from Glassdoor and Indeed, two job/career websites. Data will include job descriptions. I am going to focus on the larger cities: NYC. San Francisco, and Chicago. Once back in Dayton I will scrap Indeed for jobs related to our degrees at Sinclair: Network Engineering (Cisco), Network Manager (MS servers), Software Development, Web Development, Cyber Security, and User Support. 

Models 
    1. NLP: This project will use national language processing to  identify the words most used in each of the job descriptions. CountVectorizer will be used to count word occurrences and ignore stop words.  
    2. Cluster analysis (K-means will be performed with the target equal to either data scientist, data engineer, or data analyst). The model will be trained on a subset of data and then tested to see the model can the job category. 

    3. Unsupervised machine learning will be used to visualize groups of jobs.  
    
Risks and Assumptions 

Risk: That I will not be able to scrap meaningful data with the tools I know how to use.  
Risk: That the job descriptions will not have the job requirements (which what I really need). Unfortunately Glassdoor limits access to their data.  Monster and other websites do not have APIs and they do not want you to scrap their data.  LinkedIn has a specific warning not to. 
Risk: Is the data I scrap reliable. If you do a google search for Glassdoor you will find positive and negative reviews. Some say that it is a place for an employee to write a negative review as a way of venting, others say it is a great source of information for the job seeker. Like everything take it with a grain of salt.  
Assumption: That the results from Indeed and Glassdoor can be merged together to produce one answer to my problem statement.  
Assumption: That I will be able to apply my results to revising curriculum and advising students 

Revision of initial goals and success criteria 
No revision since this is a completely new project 

Create a local database 
Database will be created in SQL with mapping to Access.  Access is what our internship office uses.  
The database design needs to accommodate job descriptions that are sent to the internship office.  My goal is to use this model at Sinclair.

Data cleaning/munging techniques 
    Remove any rows with missing data 
    Remove any words that to not provide any benefit to the results 
    Remove any duplicates 
 
 
Where I stand right now 
I have scraped data from Glassdoor and I am currently struggling to extract data from it.  Scraping from Indeed is easy. 
 