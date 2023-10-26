---
layout: post

title: Sentiment Analysis
subtitle: Recognizing emotions in textual data in customer verbatims
thumbnail-img: /assets/img/research.png
cover-img: /assets/img/research.png

tags: [Sentiment analysis]

comments: true

pinned: true
---

# Introduction

The DataLab Groupe, in association with 5 pilot regional banks, has developed a solution that allows the analysis of customer verbatims from IRC (_**I**ndice de **R**ecommandation **C**lient_) surveys using Artificial Intelligence. The AI allows the analysis of verbatims along 3 axes:

1. Identification of the topics mentioned by the customer
2. **Qualification of polarity (positive, neutral, or negative tone of speech)**
3. **Detection of emotions (joy, anger, sadness, or neutral)**

The last two topics are the main focus of this blog post.


# Qualification of polarity
The process of polarity qualification involves assigning a positive, neutral, or negative polarity to each of the identified themes (task n°1). This task becomes more complex by a factor equal to the number of themes that need to be detected.


# Detection of emotions
Unlike the previous task, emotion detection applies to the entire verbatim. In this case, the goal is to assign an emotion - joy, anger, sadness or neutral - to the content of the analyzed text.


# Developed model
For our use case, we adopted a multi-task approach where all three tasks were learned simultaneously. The idea was that, given the close relationship between the three tasks, joint learning would yield better results than three separately trained models (a fact confirmed by experimentation). The developed model was based on a CamemBERT, to which three classification heads were added, and the whole system was trained end-to-end to address all tasks at once.


# Conclusion
To sum up, the DataLab Groupe, in collaboration with five regional banks, has successfully developed an 100% in-house AI solution that can analyze customer feedback from IRC surveys. This solution is capable of identifying the topics mentioned by the customer, qualifying the polarity of the speech, and detecting the emotions conveyed. The solution is currently being deployed at the group scale.

Future research and improvement opportunities will likely focus on managing ambiguity (such as irony), subjectivity (like distinguishing between sadness and anger), and noise, which are inherently present in this type of data.



