---
layout: section
title: Analytics
permalink: /analytics/
nav_order: 4
---

There have been several efforts to apply FaaS to analytics workloads.
We touch upon a few examples here and refer the reader to Werner et al. {% cite werner2020evaluation %} for an overview and comparison of serverless data processing frameworks.

PyWren {% cite jonas2017occupy %} demonstrated the benefits of simplified cloud programming with a simple FaaS-based framework geared at analytics tasks.
Subsequent work by IBM {% cite sampe2018serverless %} extends it with additional constructs, and Locus {% cite pu2019shuffling %} showed how to implement shuffling, a an important analytics primitive, in a FaaS environment.

Wukong {% cite carver2020wukong carver2019search %} focuses on optimizing analytics tasks, enhancing locality by minimizing data movement across tasks.
In a similar vein, HASTE {% cite arjavalingam2021haste %} focuses on optimizing serverless DAG execution.

In the database literature, Lambda {% cite muller2020lambada %} and Starling {% cite perron2020starling %} both and use FaaS to operate on data stored in S3.
Flint {% cite kim2018serverless %} tackles the same problem using Apache Spark {% cite zaharia2016apache %}.
