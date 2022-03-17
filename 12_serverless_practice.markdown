---
layout: section
title: Serverless in Practice
permalink: /serverless-in-practice/
nav_order: 12
---

Understanding how serverless FaaS platforms work is challenging because the leading products are either partially or entirely proprietary.
Early efforts to innovate on FaaS devoted significant effort to understanding how FaaS platforms might be implemented {% cite jonas2017occupy hendrickson2016serverless %}.
More recent work by Wang et al. {% cite wang2018peeking %} has thoroughly analyzed the major FaaS platforms, documenting their isolation mechanisms, elasticity, coldstart latencies, and container recycling policies.
Lee et al. {% cite lee2018evaluation %} provide another evaluation of FaaS providers.

Other reports and analyses of real-world experiences are valuable as well.
Shahrad et al. {% cite shahrad2020serverless %} describe the production workload of Azure Functions as well as policy optimizations that improve efficiency and quality of service.
The Wonderless Dataset {% cite eskandani2021wonderless %} contains open source serverless applications extracted from GitHub.
Eismann et al. {% cite eismann2021state %} review various serverless applications and attempt to explain why and when they are successful.
Mohanty et al. {% cite mohanty2018evaluation %} evaluate open source serverless computing frameworks.
