---
layout: post

title: Sentiment Analysis
subtitle: Recognizing emotions in textual data in customer verbatims
thumbnail-img: /assets/img/sentiment-analysis-research-icon.jpg
cover-img: /assets/img/sentiment-analysis-research-thumbnail.jpg

tags: [Sentiment analysis]

comments: true

pinned: true
---

Sentiment Analysis is an established task in the field of machine learning. With the emergence of new technologies, the community has continuously introduced novel approaches to perform sentiment analysis. This task remains crucial, as it is essential for automated text processing. At DataLab Groupe, we have developed our own sentiment analysis models by harnessing advancements in natural language processing and deep neural networks.

# Introduction
The DataLab Groupe, in collaboration with 5 pilot regional banks, has developed a solution that allows the analysis of customer verbatims from IRC (_Indice de Recommandation Client_) surveys using Artificial Intelligence. The AI allows the analysis of verbatims along 3 axes:

1. **Identification of the topics mentioned by the customer**
2. **Qualification of polarity determining whether the tone of speech is positive, neutral, or negative**
3. **Detection of emotions including joy, anger, sadness, or neutrality**

In this blog post, we will primarily focus on the last two topics.

# Qualification of polarity
The process of polarity qualification involves assigning a positive, neutral, or negative polarity to each of the identified themes (task n°1). This task becomes more complex by a factor equal to the number of themes that need to be detected.

# Detection of emotions
Unlike the previous task, emotion detection applies to the entire verbatim. In this case, the goal is to assign an emotion, including joy, anger, sadness or neutral, to the content of the analyzed text.

# Developed model
For our specific use case, we implemented a multi-task approach, training all three tasks simultaneously. The rationale behind this approach was the strong interdependence among the tasks, and our hypothesis was that joint learning would lead to improved results compared to training separate models for each task. Through experimentation, we confirmed this hypothesis.

The model we developed is a transformer-based language model. We extended it by adding three classification heads, each dedicated to one of the tasks. The entire system was then trained end-to-end, enabling it to address all tasks simultaneously.

# Conclusion
To sum up, we have successfully developed an in-house AI solution that can analyze customer feedback from IRC surveys. This solution is capable of identifying the topics mentioned by the customer, qualifying the polarity of the speech, and detecting the emotions conveyed. The solution is deployed at the group scale.

Future research and improvement opportunities will likely focus on managing ambiguity (such as irony), subjectivity (like distinguishing between sadness and anger), and noise, which are inherently present in this type of data.
