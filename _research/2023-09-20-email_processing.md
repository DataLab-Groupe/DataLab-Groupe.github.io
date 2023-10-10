---
layout: post

title: Email Processing
subtitle: Using AI to understand et automatically process emails
thumbnail-img: /assets/img/research.png
cover-img: /assets/img/research.png

tags: [emails]

comments: true

pinned: true
---

# Introduction

Email processing is a critical aspect of modern communication, especially in business environments. It involves the extraction, classification, and management of information from emails. However, the process is not as straightforward as it seems. It presents several challenges, including content segmentation, email theme classification, response generation, and email anonymization. This blog post delves into these challenges and explores solutions currently developed within the group and ongoing/future research directions.

# Content Segmentation

Content segmentation involves separating the core email from its history and signature. This is crucial in understanding the context and purpose of the email, which may include forwarded messages or reply threads. To do so, techniques ranging from regular expressions to advanced NLP models can be used.

For example, for removing the signature from an email body, we use a [Bi-LSTM](https://www.cs.toronto.edu/~graves/icann_2005.pdf) on body sentences. Each sentence is encoded into a vector by concatenating a Bi-LSTM encoder on words and a BI-LSTM encoder on characters. Hence, the resulting vector encodes both the word level and the character-level semantics of a sentence. For each sentence, we then classify if it is part of the body or part of the signature. 

# Classification of email theme and attachments

Email theme classification is main challenge and purpose in email processing. It involves identifying the main subject(s) or object of the email and the action related to it. For instance, the object could be a "credit card," and the action could be "block" or "renew."

This can be achieved through multilabel classification or a two-stage model. The former involves assigning multiple labels to an email, while the latter involves classifying the object first and then the action. Basic models like tf-idf coupled with machine learning or deep learning models like [CamemBERT](https://arxiv.org/abs/1911.03894) variants can be used for this purpose.

Attachments classification is currently done using the convolutional neural networks [VGG16](https://arxiv.org/abs/1409.1556) in which we transferred weights learned on two datasets: a corporate dataset of 300K scanned documents and the [Tobacco dataset](https://github.com/mailgun/forge).

# Response Generation

Generating responses to emails is a complex task that involves understanding the email's content and context and formulating an appropriate response. The current solution is based on a model that chooses the appropriate answer from a finite set of possible answers based of expert hand-made rules.
An ongoing research topic is the use of on-premise Large Language Models for this purpose. The challenge lies in generating responses that are personnalized, contextually and grammatically correct, and convey the intended message. Recent models, such as [LLAMA-2](https://arxiv.org/abs/2307.09288), show promise in this area, but they require prompting, optimization, finetuning and/or adaptation.

# Email Anonymization

Email anonymization involves removing sensitive data from emails, such as names, social security numbers, and other personally identifiable information. This is crucial for maintaining privacy and complying with data protection regulations without affecting the email's overall context and meaning.
We treat email anonymization as an NER task. Thus, we use [FlauBERT](https://arxiv.org/abs/1912.05372) to classify each word in an email into a set of predefined personal data fields. Detected fields are then deleted, replaced with a mask (e.g., [NAME] for names), or replaced with an equivalent fake entity (e.g., replace the name _Antoine_ by _Clément_). 


# Conclusion

Email processing is a complex task that presents several challenges. However, with the right strategies and tools, these challenges can be overcome. In this blog, we presented a brief overview of our developped solutions. Theese solutions were co-designed with business banking experts to meet their needs and already deployed in part of the Credit Agricole group. Some of them are currently used by the back-office of the housing loan department’s customer service.