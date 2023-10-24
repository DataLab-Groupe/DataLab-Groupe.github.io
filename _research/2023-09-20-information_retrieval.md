---
layout: post

title: Information Retrieval
subtitle: Retrieving information from documents
thumbnail-img: /assets/img/information-retrieval-thumbnail.jpg
cover-img: /assets/img/information-retrieval-cover.png

tags: [information retrieval, question answering]

comments: true

pinned: true
---

In the banking sector, a significant challenge lies in extracting pertinent information from an extensive collection of documents. Indeed, banks amass an enormous volume of various documents, ranging from legal to other types. Expertise in these documents is crucial. However, manually combing through such document batches to find a specific clause can be time-consuming, often taking months. To address this, the DataLab Group has been committed to developing search engines, leveraging different technologies to assist entities of the Groupe Credit Agricole.

# First Generation
Initially, our focus was on traditional search engines that seek word matches in a text based on the search input. The tool included features enabling customers to search for a word sequence independently or request Boolean combinations. For instance, a query could be structured as 'Alexander not The Great,' which would return all contents related to an 'Alexander' who is not 'Alexander the Great.'

Implementing this approach required full-text search and segmentation. Full-text search could be executed by Elasticsearch, provided it was correctly configured for the language in question. Segmentation, however, proved challenging. Achieving a high-performing segmentation algorithm was difficult, leading us to adopt a custom rule set tailored to the target corpus. However, this solution struggled with generalization, a notable limitation of such approaches. Incorporating more machine learning could be a solution, but it would necessitate extensive data annotation.

# LLM-based Approach
To overcome these limitations, we developed a new generation of search engines that utilize embeddings with large generative models. This approach significantly reduces the need for extensive annotation, allowing for a more flexible approach to segmentation. We hope that the large language model (LLM) will successfully detect and extract the desired segments.

Our indexing pipeline initially retrieves PDF documents, converts them into text, and splits them into pages. These pages are then embedded and stored in a vector database. During a search, the query is augmented using the LLM, and the similarity of the segments with the query is computed. The LLM then extracts from this reduced scope and generates a response based on the segments.

# Conclusion
Considerable effort has been invested in developing search engines capable of extracting relevant information from a text corpus. We have also pioneered a new generation of search engines that harness embeddings with large generative models. Both these generations have their merits and drawbacks, but each plays a vital role in our use cases involving information retrieval.
