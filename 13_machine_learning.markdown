---
layout: section
title: Machine Learning
permalink: /machine-learning/
nav_order: 13
---

FaaS can support machine learning in both training and inference applications.
Projects that focus on training include MLLess {% cite sanchez2021experience %} and LambdaML {% cite jiang2021towards %}.
Cirrus {% cite carreira2019cirrus %} and Stratum {% cite bhattacharjee2019stratum %} address end-to-end machine learning workflows, which include both training and inference.
Inference-focused projects demonstrate serving deep learning models {% cite ishakian2018serving %} and automatic model partitioning for cost optimality and SLO compliance {% cite yu2021gillis %}.

GPUs and other accelerators {% cite jouppi2017datacenter %} are commonplace in machine learning but are not presently supported by commercial FaaS offerings.
Research that addresses this shortcoming includes work on efficient GPU sharing for serverless workflows {% cite satzke2020efficient %}.
Another project, PyPlover {% cite yang2020pyplover %}, is a serverless framework that allows the deployment of GPU code directly to a FaaS environment.
