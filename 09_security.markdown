---
layout: section
title: Security
permalink: /security/
nav_order: 9
---

The transition to a serverless model has many implications for security.
Established techniques such as secure enclaves can be used with FaaS, but doing so requires overcoming various obstacles {% cite trach2019clemmys qiang2018se goltzsche2019acctee %}.

Fine-grained isolation in FaaS offers potential security benefits, but it will be difficult for programmers to take advantage of this without supporting tools and techniques.
Information flow control {% cite sabelfeld2003language %} provides the basis for some approaches, including Valve {% cite datta2020valve %} and work by Alpernas et al. {% cite alpernas2018secure %}.
Will.iam {% cite sankaran2020workflow %} a produces more robust permission boundaries through workflow integration, and Hong et al. {% cite hong2018go %} suggest a collection of design patterns that can help develop secure serverless applications.

Researchers have found that serverless computing is susceptible to novel forms of attack.
For example, Kelly et al. {% cite bocci2021secure %} describe "denial of wallet" attacks that exploit the scalability of serverless computing to exhaust the victim's budget.
The Warmonger attack {% cite xiong2021warmonger %} is a type of denial of service attack that exploits multi-tenant infrastructure to introduce abusive activity on a victim's IPs, leading other services to block them.

Work has also focused on analyzing the security of specific applications, e.g., the OmniBallot online voting system {% cite specter2021security %}.
