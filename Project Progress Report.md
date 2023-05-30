# Milestone 3 Project Progress Report
**Summary**: In this week, our group focused on runing the data on T5 and fine-tuning on the FlanT5 model.


## Engineering Updates:
*Data*: our dataset includes sample cover letters scrapped from Indeed. We have created a scrapper to help us collect the data from the website for the next step. The data is about 1000 cover letters, with each contains about 500 words. We are using 340 cover letters as mini batch for the current pilot study. The scrapper can be found [here](https://github.ubc.ca/MDS-CL-2022-23/COLX_585_CoverGenie/blob/master/Milestone_2/Data_scraping.ipynb)


*Methods & Engineering*: 
- The sample cover letters are going to be the initial input, we generate the job descriptions and resumes using OpenAI API, this way we are making sure we have matched The API generator can be found [here](https://github.ubc.ca/MDS-CL-2022-23/COLX_585_CoverGenie/blob/master/Milestone_2/api-generator.ipynb)
- We then stored the cover letters, resumes and job descriptions into a dataframe in .csv format, find the data
- We are going to use this final data to train and finetune the FlanT5 model. 

** Previous Works: apart from referencing the studies from last week, we also read and thought the paper on FlanT5 named "Scaling Instruction-Finetuned Language Models" is an interesting read this week. This is relevant to our project because it is proved that finetuning language models on a collection of datasets phrased as instructions has been shown to improve model performance and generalization to unseen tasks.

** Results: We have tried the FlanT5 base model for in this code. As the model is still huge it was not very well fit to run in both the Google colab and local machine. We are also trying other methods to make the model easier to run it for 300+ examples


*Challenges*: as mentioned in the summary and engineering updates, our biggest challenge is that we do not have resource to obtain the high quality of cover letters. Upon discussion with mentors, we decided to make full of chatgpt! This is not an ideal scenario but it's feasible and suggested by mentors.


# Updates from the original proposal

# Introduction: 
The goal of our project is to build a fine-grained mini-ChatGPT (named “CoverGeni”) , which is designed to generate resumes and cover letters based on job descriptions from the tech field. By nature, it is a language generation task, and it takes the job description as input to a sequence of text and turns it into a structured, certain style of resumes and cover letters. This might involve parameter efficient finetuning, reinforcement learning and prompting engineering to some extent. 

updates: Our goal hasn't changed at this point and we don't wish to change the project idea at this point, we just tweaked a bit on data collection and methodology after taking into many factors into consideration. 


# Motivation and Contributions/Originality:
The motivation for the project is quite straightforward, we wanted to to develop a fine-grained mini-ChatGPT (named “CoverGeni”) that can generate resumes and cover letters based on job descriptions from the tech field. The project aims to provide a solution to the problem of creating a structured and certain style of resumes and cover letters that can be tailored to specific job descriptions in the tech industry. 

We believe this is important and relevant to us in the way that it can save time and effort for job seekers and hiring managers by automating the process of creating resumes and cover letters. Additionally, it can help job seekers to create more targeted resumes and cover letters that are specifically tailored to the requirements of the job, increasing their chances of being hired. 

The contribution of the project is the development of an efficient and effective language generation model that can generate resumes and cover letters based on job descriptions from the tech industry. The project will also explore techniques such as parameter efficient fine-tuning, reinforcement learning, and prompting engineering to improve the quality and efficiency of the model. We are hoping to provide some insights on the specific application of language generation to the task of creating resumes and cover letters for the tech industry. The project aims to provide a more targeted solution to a common problem faced by job seekers and hiring managers. 

# Data:
Scope of Corpus

[updated]Genre: job description/cover letters/resumes

[updated]Source: cover letters from Indeed

Size: a typical cover letter consists of 500 words and a typical job description consists of around 800~1000 tokens,we are aiming to collect at least 1000 examples

Language: English 

Data format: The corpus will be stored as a .csv file 

# Engineering:
computing infrastructure: Google Colab 

[updated]deep learning method: language generation with T5/GPT2. -> we will be training/finetuning FlanT5. 

framework: PyTorch 

# Previous Works (minimal):

We have reviewed a similar project which was carried out using T5. The model is a fine-tuned version of t5-base on cover letter samples scraped from Indeed and JobHero. The author has explored the following hyperparameters such as learning rate, train batch, eval batch size, seed and optimizer etc., which is a great example of taking multiple hyperparameters into consideration into our project. For more information, please refer to [this](https://huggingface.co/nouamanetazi/cover-letter-t5-base)


There’s another project related to fine-tuned job resumes based on gpt2, which could be a reference as well, click [here]( https://huggingface.co/czw/gpt2-base-chinese-finetuned-job-resume)


[updates]: This one doesn’t contain a lot of information but it is based on gpt2 as well. (*we will not consider this anymore)

[papers on the use of FlanT5](https://arxiv.org/pdf/2210.11416.pdf)

# Evaluation:
Our main metrics would be BLEU score and perplexity. We want to also include some visualizations of statistics as a vehicle of serving insights from the project. We will see and modify components of our project once we start working on engineering.

[updates]: we learnt a new metric ROUGE score this week, which allows us to measure the quality of text summarization by computing the frequency of overlapping n-grams between the summary (that we generate from the fine-tuned FlanT5) and the reference one (which is from the Indeed). In the meantime, we will still consider using multiple metrics such as BLEU score and perplexity to evaluate our final outcomes.

# Results: 

[updates]: We have tried the FlanT5 base model for in this code. As the model is still huge it was not very well fit to run in both the Google colab and local machine . We are also trying other methods to make the model easier to run it for 300+ examples

**PLEASE ADD THE RESULTS HERE**

# Challenges: 

[updates]: We are working with 300 cover letters for now. If the model fine tuning requires more data, we need to collect some more cover letters.
