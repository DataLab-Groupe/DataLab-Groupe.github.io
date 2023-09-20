---
layout: page
title: Gen AI
subtitle: "Learn more about our works on Generative AI"

share-title: DataLab Groupe - Gen AI
share-description:  Learn more about our works on Generative AI
cover-img: "/assets/img/fond-ca.jpg"
---

# Learn more about our works on Generative AI


## R&D

### GenIAL : generative AI Lab plateforme

GenIAL, standing for Generative AI Lab, is an innovative platform developed by the DataLab Groupe. The platform is designed as a showcase for various use cases pertaining to text generative AI. GenIAL covers use cases in several areas such as text classification, information extraction, and more, thereby showcasing the diversity of applications where AI can be effectively employed.

One of the key features of GenIAL is its comparative analysis of multiple approaches. Users are given the opportunity to compare and contrast open source models vs proprietary models, optimized vs vanilla models, and default vs very advanced prompts. These features provide a unique perspective on the strengths and weaknesses of each type of approach/model, fostering a deeper understanding of Generative AI. It also emphasizes a visual approach to AI, aiming to make the technology more accessible and engaging. Instead of solely focusing on prompts and scripts, GenIAL presents AI concepts visually, aiding in comprehension and providing a more intuitive user experience.

This platform is currently used by the DataLab Groupe to showcase its R&D experiments.

### Benchmarking commercial vs opensource GenAI models

The DataLab Groupe conducted a comprehensive benchmarking study comparing commercial and open-source textual generative AI models. The use cases for this research included sentiment analysis, information extraction, data anonymization, and many more. The DataLab performed the experiments using both private data (for on-premise and open-source models only) and public datasets.

The study's findings revealed that despite the growing interest and enthusiasm over generative AI, it generally underperformed when compared to smaller, task-specific models. This underperformance was particularly noticeable given that the generative AI models required significantly more computational power, particularly in terms of GPU resources, to operate. This added requirement presents an additional challenge when it comes to implementing these models in real-world scenarios.

However, the research also highlighted the unique advantages of generative AI models. These models proved particularly useful in scenarios where there was little to no data available, thanks to their zero-shot or few-shot learning capabilities. This allows these models to make predictions without (or with few) prior examples, which can be highly valuable in certain situations.

## Business Use cases

### Marketing, SEO

This approach of using generative AI for SEO content generation could greatly enhance the efficiency and effectiveness of digital marketing strategies. By automating the process, marketing teams could save significant time and resources that would otherwise be spent on manual keyword research and content creation. Furthermore, the improved positioning of web pages can lead to increased visibility and traffic, potentially driving higher conversion rates and revenue.

In this context, the use case of SEO content generation involved leveraging generative AIs to optimize digital content. More specifically, it involves generating elements such as secondary keywords, a lexical field, or even a structure from a main keyword, which will support the writing of an article on a website.

### News summarization

The DataLab Groupe conducted a use case study exploring the application of generative AI in summarizing technical and scientific papers. Given the length of some papers, reaching up to approximately 80 pages, a major feat was the significant time saving that the use of AI could offer. Several methods and long prompt engineering phases were tested to determine the most efficient and accurate approach.

The study found that while the AI was able to produce syntactically correct summaries, it was not without challenges. A notable issue was the occurrence of 'hallucination' - the model would generate information that was not present in the original text, often drawing from the paper references. This highlighted the need for caution when using such models, as they can inadvertently introduce errors or misrepresentations in the summaries.

Despite these challenges, the use of generative AI for summarizing lengthy scientific and technical papers demonstrates promising potential, with further improvements and refinements needed to mitigate hallucination and enhance accuracy.

### Information extraction from customers proof documents

DataLab Groupe undertook a comprehensive study on the use of generative AI in the context of information extraction from customer proof documents. This involved testing several models, both open source and commercial.

Open source models were evaluated in an on-premise environment against task-specific models developed internally, such as DocParser. This comparison aimed to assess the performance of general-purpose models against those specifically designed for the task at hand.

Commercial models (GPT 3.5/4) were also tested, using open-source data for benchmarking. SROIE dataset, a widely used resource in the field of information extraction, was employed for this purpose.

The results of the study were quite revealing. Task-specific models significantly outperformed generative models in terms of both accuracy and efficiency. Furthermore, these models required considerably fewer computing resources, making them a more cost-effective solution for information extraction.

Fine tuning was also implemented to get better performances. It increased the performances but still didn’t beat the task-specific model.

### RAG on regulatory documents

One way to try preventing hallucination is to restrict the scope of generative models. We give them a context and they extract information from that context without innovation. That’s why many people now talk about retrieval augmented generation. It consists in performing searches in a document corpus with generative AI.

The search uses multiple processing blocks. We limit the scope by extracting the elements which are the most alike to our query by using an embedding model. Then we feed that scope to the generative model such that it extracts only the snippets which relate to the query. Finally, we ask the generative model to create a consolidated response by using the snippets it extracted itself.

One advantage is that there is no need to annotate data, a process which can be expensive and difficult. Especially in such open domains. However, one must remember that LLMs are heavy and slow at generation. Hence, a single query can take a long time to complete.

We conducted that experiment on the public corpus of the AI Act the new legislation on AI. That corpus is quite complex as it consists of multiple documents and among them, many might seem to match the query semantically while being completely irrelevant and of small importance.
