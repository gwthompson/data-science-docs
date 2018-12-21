# How to become a data scientist

### 1. Understand the Fundamentals (you may be able to skip)

### stats
- stats intro: http://www.greenteapress.com/thinkstats/

### Linalg
- https://towardsdatascience.com/boost-your-data-sciences-skills-learn-linear-algebra-2c30fdd008cf

### 2. learn the tools for data science:
- I'd recommend keeping these in mind, and then using them all when you begin your projects

#### git 
- intro to git: https://guides.github.com/introduction/git-handbook/
- feature branches: https://www.atlassian.com/git/tutorials/comparing-workflows/feature-branch-workflow

#### an IDE
- recommend pycharm, vscode good to
- learn it well

#### debugger
- built in, in many ides
- also can use ipdb

## To Learn traditional Data Science

### a) Understand the content
- Alik's slides (a lot of solid practical advice)
    - Ask me for them
    - Or go here if you work at Deloitte: https://teams.microsoft.com/l/channel/19%3ac8ca2a1b3ef640d4a8841496cb2dc6a0%40thread.skype/MMF?groupId=285cdc67-512c-499f-ac59-ecccc2fe61fa&tenantId=36da45f1-dd2c-4d1f-af13-5abe46b99921
- Refer to resources below / Google it (thank god for stack overflow) if anything is unclear
    - If all else fails you can ask me :)

### b) Start a Project
- In some contexts you can't use a non-interpretable model, the client needs to know exactly how the model is making the predictions. In those contexts you usually need to use a linear model, this project will give you prepare you for that scenario.
    - It will also develop you feature engineering abilities
    - The nice part about using the xgboost model is it will give you lower bound you know you should be able to hit through feature engineering. Will also be good to compare the two and understand the complexities of each very important and relevant model.
- Steps
    - 1. Make some features
    - 2. Build an xgboost model and evaluate, then engineer more features to get a logistic regression model to perform as effectively
- data: https://www.kaggle.com/c/home-credit-default-risk
    - I'd recommend you put in a db (good practice)
- example: https://github.com/parker84/MMF_UofT/tree/master/credit_risk
- use all the tools mentioned above
- Then try to improve further:
    - Implement different models
    - Engineer more features using more complicated methods (consider different unsupervised approaches)
    - Consider different preprocessing techniques
    - Make sure you understand how these models are working, what are the tradeoffs, why is one performing better than the other, how could you exlpain this to a laman or a fellow Data Scientist?
        - You should be able to justify why one performs better than the other, and should have an idea before you implement it
        - What are the potential biases from each model / feature you engineer?
- Refer to additional resources below when needed
    - You may find the labs from Harvard DS course particularly useful

### c) Learn More and Apply this to your project (or other projects)

#### Data Science
- Harvards DS course: http://cs109.github.io/2015/pages/videos.html
    - I'd recommend skipping:
        - Lab8, rather then spend time learning these tools I'd recommend you learn Docker and pyspark
            - Docker: https://towardsdatascience.com/how-docker-can-help-you-become-a-more-effective-data-scientist-7fc048ef91d5
            - Pyspark: https://www.dezyre.com/apache-spark-tutorial/pyspark-tutorial
        - Lab10, focuses on BOW models, which aren't super effective in comparison to neural nets and used less often 
            - If you're interested getting the best results for NLP you may want to skip this and jump to the neural network section instead
            - That being said when you're focus is on specific words and not general context BOW could be preferred
            - Even if you have small data, you'll likely get better results using transfer learning over BOW models
    - Topics I use less often (but still useful):
        - Experimental Design: L21
        - Bayesian methods: L16-L18
            - Pretty sweet though
            - Handy with:
                - Small data situations and even feature engineering over small groups, the empirical bayes stuff in particular
                - If you need to use a custom model to effective model your data
                - If you need to better represent uncertainty of parameters 
                - Want to use a custom loss function and represent parameter uncertainty
            - With ADVI or conjucate priors can be just as fast as frequentist methods
            - To actually implement these I'd recommend referring to: http://camdavidsonpilon.github.io/Probabilistic-Programming-and-Bayesian-Methods-for-Hackers/
                - the pymc2,3 versions are great, haven't tried the tf version yet
        - Spark and Mapreduce: L15
            - Used with big data
    - Doing the assignments would be good practice, and you can check your work
        - They have the solutions for the 2013 course here: https://github.com/cs109/content

#### ML
- http://www-bcf.usc.edu/~gareth/ISL/ (good practical advice)
- read sections of this book while trying to implement them on the project, for each section try to implement it, and understand all the complexities in relation to your task


#### EDA:
- https://r4ds.had.co.nz/exploratory-data-analysis.html

#### SQL
- https://www.codecademy.com/learn/learn-sql

#### More on Model Bias (Important)
- slides on bias: https://github.com/parker84/data-science-docs/blob/master/ds_topics/model_bias.pptx
- bias from conditioning: https://medium.com/causal-data-science/understanding-bias-a-pre-requisite-for-trustworthy-results-ee590b75b1be
- censorship bias: https://lifelines.readthedocs.io/en/latest/Survival%20Analysis%20intro.html
- some additional examples of bias: https://thenextweb.com/contributors/2018/10/27/4-human-caused-biases-machine-learning/?amp=1
- In your projects, and any of the projects you ever work on you need to be very concerned about these biases. These biases are what will result in catastrophic results in prod, and are much more important than selecting the optimal model


### To Learn neural networks

#### a) Understand neural nets
- Start w Ofer's slides
    - Ask me for them
    - Or if you work at Deloitte see here: https://teams.microsoft.com/l/channel/19%3a4212dae79c4649aab88c14f48105e2ff%40thread.skype/General?groupId=285cdc67-512c-499f-ac59-ecccc2fe61fa&tenantId=36da45f1-dd2c-4d1f-af13-5abe46b99921
- Refer to resources below if anything is unclear
    - For linear algebra stuff see the linalg resource posted in fundamentals
    - For everything else see the deeplearning book / google it :)
    - If all else fails you can ask me :)

#### b) Do a project
- https://www.kaggle.com/c/twitter-sentiment-analysis2/data
- Then try to improve further:
    - Implement different models
    - Consider different preprocessing techniques, can you create more data?
    - Make sure you understand how these models are working, what are the tradeoffs, why is one performing better than the other, how could you exlpain this to a laman or a fellow Data Scientist
        - You should be able to justify why one performs better than the other, and should have an idea before you implement it
    - What are the potential biases?
- use all the tools mentioned above
- I'd recommend using tensorflow as well, as it will force you to develop a deeper understanding of the problem and give you unlimited flexibility for the networks you can build in the future
    - but Keras is good too

#### c) Learn More and Apply this to your project
- Deep learning for NLP: http://cs224d.stanford.edu/syllabus.html
    - looks really solid but I haven't vetted all the content yet
    - They post all midterms and solns posted for you to try as well
- http://www.deeplearningbook.org/
    - read sections of this book while trying to implement them on the project, for each section try to implement it, and understand all the complexities in relation to your task
- See model bias section above
- http://cs231n.github.io/ (a lot of good practical advice)
    - refer to here for tuning and stuff: http://cs231n.github.io/neural-networks-3/



### Additional
- see helpful_data_science_books_and_blogs.md
- (free open DS masters) http://datasciencemasters.org/