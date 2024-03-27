---
layout: post

title: MLOps DataOps
subtitle: Shipping AI projects in production
thumbnail-img: /assets/img/mlops-icon.png
cover-img: /assets/img/mlops-back.jfif

tags: [DataOps, MLOps, DevOps, Observability]

comments: true

pinned: true
---

**MLOps has become an integral part of Data Science operations. It aims to ensure that experiments are reproducible and production is managed correctly.**


# Reproducibility

It is crucial to record the results of all experiments and house these results
on a unified platform. This platform should contain our metrics and potentially
our checkpoints. For this purpose, DataLab Group employs MLFlow as a tool to
secure storage for all the metrics.

# Continuous Integration

At DataLab Group, we have conducted experiments using KubeFlow to trigger
trains from our CI. The resulting training leads to metrics stored in MLFlow.
If the performance metrics are satisfactory, the new model is deployed.

# Monitoring

A key aspect of MLOps is ensuring the consistent performance of our models. To
achieve this, DataLab Group has established its own monitoring platform, called
"MonIA". Our platform uses several metrics to track the performances of our
models in production and to alert the teams  in case of detected anomalies,
like detecting a drift in data or concepts for example.

# Data Quality

The performance and precision of Machine Learning models are significantly
impacted by the quality of the training data. It's crucial to validate the
quality with every new batch of data, during the training or prediction steps,
to ensure steady performance.

In a fully industrial environment, these validations should be initiated
automatically with each run, providing alerts if the data falls short of the
necessary quality standards.

At Datalab, we've created a data validation tool called "Diagnos". This tool,
particularly designed for tabular data, is set up at the start of our ML
pipelines. It guarantees that the data consistently fulfills quality standards
and complies with the initial criteria.

# Data Cataloging

Data Cataloging is a systematic approach to documenting data, creating an
extensive inventory of a company's data assets. It provides a structured,
searchable resource that allows users to efficiently comprehend and locate the
necessary data.

This practice helps us maintain a clear "project lineage", allowing us to trace
the data used at each project phase and how it was generated, without requiring
code comprehension or technical documentation review. This is especially useful
for non-coders. Also, this approach aids in the role transition process,
ensuring seamless continuity.

# Data Versioning

Data versioning is the practice of managing and recording changes in datasets
over time.

This method is particularly crucial for ensuring reproducibility, especially
during a project's experimental phase, when numerous data iterations need to be
explored before choosing the most efficient version for model training.

There are two primary strategies for data versioning. One strategy involves
taking a comprehensive "snapshot" of the database, while the other strategy
concentrates on tracking alterations or discrepancies between two versions.

At DataLab, we have studied and experimented several technologies to ensure a
robust versioning process applicable to all the use cases we develop for our
customers. We have also put in place guidelines and best practices do well
document the process of data versioning.
