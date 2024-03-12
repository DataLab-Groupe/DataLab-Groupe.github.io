---
layout: post

title: Recommender System
subtitle: Personalizing the customer journey, the rise of recommender system in the banking sector
thumbnail-img: /assets/img/moteur-de-reco-thumb.png
cover-img: /assets/img/moteur-de-reco-back.png

tags: [Recommendation]

comments: true

pinned: true
---

**In the banking sector, recommender system use algorithms to examine customer information, including profiles, habits, product ownership and transaction history, in order to offer tailor-made advice. These recommendations can include financial products, savings, credit, insurance and more. The aim is to improve the customer experience, strengthen loyalty and increase sales of banking products.**

# General context of the projects
The traditional marketing approach of banking institutions is product-based. This means that for each product (e.g. consumer credit, car insurance, etc.), a product-specific appetence score is constructed. A targeting model qualifies a customer's appetence based on historical subscription data and profile. 
Once the score has been calculated for all customers, marketing teams contact the K most appetent customers (where K is a specifically chosen number) through a precise channel (e-mail, telephone contact, etc.).

Different customer-related explanatory variables (such as financial surface, available outstandings, or monthly income) are then used to construct several product-centered scores, one model per product. This traditional approach has two major drawbacks:

* The highest-scoring customers are often scored for all products and are over-targeted in marketing campaigns. This creates significant customer irritation.
* On the other hand, less well-scored customers experience a "relationship desert", resulting in missed business opportunities for the bank.

The aim of the business lines is therefore to refocus recommendations on the customer. Identifying the customer's needs then translates into proposing the most appropriate offers (services, products, content), at the right time and via the right channel.

In this context, the DataLab Groupe has been working on a  "NBO (Next Best Offer)" project, which involves building a customer-centric recommendation engine for the Crédit Agricole’s regional banks, taking into account :

* Customer profile
* Customer action history and their sequentiality
* Commercial bias.

# Experimentations
The Group's DataLab has been conducting an R&D stream for several months to test new approaches to recommendation in order to challenge and renew existing solutions. All these approaches take into account the heterogeneous banking data supplied by the Group Crédit Agricole.
There are various types of recommendation models available on the market:

* Matrix Factorization: NeuCF
* Factorization Machine (Matrix Factorization + Linear Model): DeepFM
* Sequential: Caser, TiSASRec
* Hybrid: a set of models

These models are all based on implicit (binary) or explicit (continuous) scores, which are not available in the banking setting. Indeed, we never receive direct customer feedback on a product they hold. To the best of our knowledge, no scientific article proposes a mathematical model for constructing ratings for banking data.

It is therefore through a benchmark of different axes that we have built our scoring matrix. Building client-product appreciation matrix is a key stage in the recommendation process, as it has a major impact on the recommendation engine's performance and expressiveness. 

Finally, in order to effectively evaluate recommendation engines, specific metrics are used to capture several aspects of the recommendation:

* Relevance of the first K products recommended
* Relevance of product order
* Diversity of targeted customers by product
* Diversity of recommended products

# Results


We tested our approaches using two types of marketing metrics:

* **Customer-centered metrics** measuring the performance of the recommendation engine for a customer across all products and are well suited to evaluate the effectiveness of an individual commercial action (e.g. a customer appointment).
* **Product-centered metrics** measuring the performance of the recommendation engine for each product across all customers. They are well suited to evaluate a mass commercial action (e.g. a marketing campaign).

We obtained very encouraging performances with the different models mentioned previously. We sought to optimize the product metrics and achieved performance gains of approximately +40% on average across a wide range of products compared to traditional scoring methods. An interesting point to note is that a model that maximizes product performance will not necessarily optimize customer performance, and vice versa. Therefore, there is a balance to be identified and considerations to be made depending on the final business use of the model.

It is important that the recommendation pipeline integrate business rules. These are specific attribution rules that apply based on the product and the customer's household context. For instance, in France, we would avoid recommending a savings account “Livret A” to a customer who already has one, or home insurance for a property that is already insured, etc.
