---
layout: section
title: Stateful Serverless
permalink: /stateful-serverless/
nav_order: 4
---

Augmenting FaaS with state has been the subject of considerable research.
One application with specific state management requirements is analytics, which requires ephemeral storage to pass intermediate results between functions {% cite klimovic2018understanding %}.
Pocket {% cite klimovic2018pocket %} provides a solution to challenges in this area.
Though managing state for analytics can be challenging on account of the volume and transient nature of the data, its simple and well-defined usage patterns lend themselves to optimized solutions.

A more general challenge arises in managing changing application state, which is often subject to certain consistency requirements.
Serverless computing gives coordination-free techniques an opportunity to shine because they have provable advantages at scale {% cite hellerstein2020keeping %}.
Cloudburst {% cite sreekanti2020-ec %} is a stateful FaaS system that integrates with the scalable Anna {% cite wu2019anna %} key-value store.
It provides local caches in function instances and transactional causal consistency {% cite wu2020transactional %}.
FaaSTCC {% cite lykhenko2021faastcc %} is another system that provides similar guarantees.

An alternative approach is to use an underlying logging infrastructure to represent state.
Logging involves coordination, but it can provide strong consistency and better throughput scaling than distributed protocols such as two-phase commit {% cite abadi2018overview %}.
Beldi {% cite zhang2020fault %} and work by de Heus et al. {% cite de2021distributed %} both provide transaction mechanisms that integrate FaaS and underlying storage.
Boki {% cite jia2021boki %} and Retro-$\lambda$ {% cite meissner2018retro %} also make use of an underlying log to manage state.

Azure Functions {% cite azurefunctions %} includes "durable functions" in its production offering.
Durable functions use a checkpoint mechanism to allow long-running execution on top of a FaaS runtime.
In this programming model, state can be maintained reliably and for long periods of time within the functions themselves.
Burckhardt et al. {% cite burckhardt2021durable %} provide a formal model of durable functions and show that various implementations are possible.

Stateful serverless must reckon with faults.
AFT {% cite sreekanti2020fault %} provides a fault tolerance shim that can be interposed between a FaaS environment and underlying storage, providing atomicity guarantees.
Ray {% cite moritz2018ray %} is not derived from FaaS but offers similar scalability and fits under the broader definition of serverless.
The platform has served as a proving ground for various novel fault tolerance approaches {% cite wang2019lineage zhuang2021hoplite %}.
Other work on stateful serverless computing includes SFL {% cite brand2021sfl %}, a compiler for generating stateful serverless applications.
