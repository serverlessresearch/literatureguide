---
layout: section
title: Benchmarks and Data Sets
permalink: /benchmarks-and-data-sets/
nav_order: 11
---

Serverless computing stands to benefit from broadly accepted benchmarks.
A number of these have been proposed, though a leader has not yet emerged.
Contenders include FunctionBench {% cite kim2019functionbench %}, FaaSdom {% cite maissen2020faasdom %}, and Serverlessbench {% cite yu2020characterizing %}.
DeathStarBench {% cite gan2019open %} is targeted at microservices as well as FaaS applications.
Work by Martins et al. {% cite martins2020benchmarking %} also proposes a benchmark and uses it to compare cloud providers.
Scheuner and Leitner {% cite scheuner2020function %} provide a literature review of various FaaS performance evaluations.

The need for new benchmarks is especially evident because serverless computing emphasizes autoscaling.
The quality of this autoscaling is often referred to as "elasticity," a metaphor that suggests it might be described by a simple number or perhaps a relationship between two variables, as is the case in physics or engineering.
So far no such metric has emerged, though work by Kuhlenkamp et al. {% cite kuhlenkamp2020benchmarking %} moves in this direction.