---
layout: section
title: Autoscaling, Optimization, and Quality of Service
permalink: /autoscaling-optimization-quality-of-service/
nav_order: 5
---

Autoscaling is a defining characteristic of serverless computing, so a great deal of research touches on it in some way.
Autoscaling must balance quality of service and cost, and the work we highlight here relates directly to this tradeoff.
Even with FaaS, customers are still required to configure some resources, notably the "memory size," which serves as a proxy for instance execution resources.
Sizeless {% cite eismann2021sizeless %} and COSE {% cite akhtar2020cose %} analyze functions as they run,  attempting to find optimal resource configurations.
Winzinger and Wirtz {% cite winzinger2019model %} also provide a model for FaaS execution.
There are multiple approaches to quality of service:
Sequoia {% cite tariq2020sequoia %} targets policy goals, whereas Atoll {% cite singhvi2021atoll %} focuses on latency objectivs.

An eclectic mix of work rounds out the early autoscaling-focused efforts.
Yussupov et al. {% cite yussupov2019serverless %} study how to reengineer existing applications for scalability, introducing the notion of "serverless parachutes" that are used only under exceptional load conditions.
Spock {% cite gunasekaran2019spock %} uses both server VMs and serverless functions to meet elasticity and cost goals.
Anna {% cite wu2018eliminating %} provides autoscaling tiered storage, seeking to optimize for both cost and performance goals.
