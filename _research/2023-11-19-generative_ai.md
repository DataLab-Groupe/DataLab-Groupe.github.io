---
layout: post

title: Generative AI
subtitle: Using generative AI in the banking sector
thumbnail-img: /assets/img/gen-ai.jpg
cover-img: "/assets/img/fond-ca.jpg"

tags: [generative, ai, genai, LLM]

comments: true

pinned: true
---

**Here we describe some of our recent developments around generative AI**

### GenIAL : generative AI Lab platform

GenIAL, standing for Generative AI Lab, is an innovative platform developed by the DataLab Groupe. This platform is designed as a showcase for various use cases pertaining to text generative AI. GenIAL covers use cases in several areas such as text classification, information extraction, and more, thereby showcasing the diversity of applications where Gen AI can be effectively employed.

One of the key features of GenIAL is its comparative analysis of multiple approaches. Users are given the opportunity to compare and contrast open source models vs proprietary models, optimized vs vanilla models, and default vs very advanced prompts. These features provide a unique perspective on the strengths and weaknesses of each type of approach/model, fostering a deeper understanding of Generative AI capabilities. It also emphasizes an interactive approach with the AI models, aiming to make the technology more accessible and engaging. Instead of solely focusing on prompts and scripts, GenIAL presents AI concepts visually, aiding in comprehension and providing a more intuitive user experience.

This platform is currently used internally by the DataLab Groupe experts to showcase their R&D experiments.

### Benchmarking commercial vs opensource GenAI models

The DataLab Groupe conducted a comprehensive benchmarking study comparing commercial vs. open-source textual and generative AI vs traditional AI models (task-specific). The use cases for this research included sentiment analysis, information extraction, data anonymization, and many more. The DataLab Group performed the experiments using both private data using on-premise and open-source models onlya nd public datasets with commercial API of several cloud providers.

The study's findings revealed that despite the growing interest and enthusiasm over generative AI, it generally underperformed when compared to smaller but task-specific models. One should carefully consider the significant additional computational cost and poor performance according to standard machine learning metrics when contemplating such approaches. These computational requirements present a real challenge when it comes to implementing these models in real-world scenarios.

However, our study also highlighted some advantages of generative AI models. These models proved particularly useful in scenarios where there was little to no data available, thanks to their zero-shot or few-shot learning capabilities. This allows to make predictions without (or with few) prior examples, which can be highly valuable in certain situations.


## Business Use cases

### Marketing, SEO

This approach of using generative AI for SEO content generation could greatly enhance the efficiency and effectiveness of digital marketing strategies. By automating the process, marketing teams could save significant time and resources that would otherwise be spent on manual keyword research and content creation. Furthermore, the improved positioning of web pages can lead to increased visibility and traffic, potentially driving higher conversion rates and revenue.

In this context, the use case of SEO content generation involved leveraging generative AIs to optimize digital content. More specifically, it involves generating elements such as secondary keywords, a lexical field, or even a structure from a main keyword, which will support the writing of an article on a website.

### News summarization

The DataLab Groupe conducted a use case study exploring the application of generative AI in summarizing technical and scientific documents. Given the length of some documents, reaching up to approximately 80 pages, a major feat was the significant time saving that the use of AI could offer. Several methods and long prompt engineering phases were tested to determine the most efficient and accurate approach.

The study found that while the AI was able to produce syntactically correct summaries, it was not without challenges. A notable issue was the occurrence of ‘hallucination’: the model would generate information that was not present in the original text, often drawing from the paper references. This highlighted the need for caution when using such models, as they can inadvertently introduce errors or misrepresentations in the summaries.

Despite these challenges, the use of generative AI for summarizing lengthy documents demonstrates promising potential, with further improvements and refinements needed to mitigate hallucination and enhance accuracy.

### Information extraction from customers proof documents

DataLab Groupe undertook a comprehensive study on the use of generative AI in the context of information extraction from customer proof documents. This involved testing several models, both opensource and commercial.

Open source models were evaluated in an on-premise environment against task-specific models developed internally, such as DocParser. This comparison aimed to assess the performance of general-purpose models against those specifically designed for the task at hand.

Commercial models (GPT 3.5/4) were also tested, using open-source data for benchmarking. SROIE dataset, a widely used resource in the field of information extraction, was employed for this purpose.

The results of the study were quite revealing. Task-specific models significantly outperformed generative models in terms of both accuracy and efficiency. Furthermore, these models required considerably fewer computing resources, making them a more cost-effective solution for information extraction.

Fine tuning was also implemented to get better performances. It increased the performances but still didn’t beat the task-specific model.


### RAG on regulatory documents

One way to try preventing hallucination is to restrict the scope of generative models. We give them acontext and they extract information from that context without innovation. That’s why many people nowtalk about retrieval augmented generation. It consists in performing searches in a document corpus withgenerative AI.

The search uses multiple processing blocks. We limit the scope by extracting the elements which are themost alike to our query by using an embedding model. Then we feed that scope to the generative modelsuch that it extracts only the snippets which relate to the query. Finally, we ask the generative model tocreate a consolidated response by using the snippets it extracted itself.

One advantage is that there is no need to annotate data, a process which can be expensive and difficult.Especially in such open domains. However, one must remember that LLMs are heavy and slow atgeneration. Hence, a single query can take a long time to complete.
