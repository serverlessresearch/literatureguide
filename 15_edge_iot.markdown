---
layout: section
title: Edge and IoT
permalink: /edge-and-iot/
nav_order: 15
---

Serverless computing has generated enthusiasm {% cite aslanpour2021serverless %} in the areas of edge computing {% cite shi2016edge %} and the Internet of Things (IoT) {% cite atzori2010internet %}.
IoT envisions embedded computing and communication in sensors, actuators, and everyday electronic items.
IoT devices are often resource-constrained, so they may benefit from offloading computation over the network.
Edge computing makes it possible to do this while maintaining low latency: It augments the cloud resources in centralized data centers with compute, storage, or other resources placed at the "edge" of the network, i.e., near devices.
Combining edge computing and IoT presents challenges since devices may move and because the resources available at a particular edge location can become oversubscribed.
These are the sorts of challenges that serverless computing is equipped for.

This is an active area of research that includes numerous works.
Hall et al. {% cite hall2019execution %} suggest an execution model for FaaS at the edge.
Gand et al. {% cite gand2020serverless %} describe a containerized management solution for deploying serverless code.
Pinto et al. {% cite pinto2018dynamic %} propose dynamically moving functions between an IoT device and the edge.
Apollo {% cite smirnov2020apollo %} provides a system for runtime function composition and flexible placement, whereas Costless {% cite elgamal2018costless %} describes an approach to optimization that includes function fusion.
LaSS {% cite wang2020lass %} focuses on meeting the needs of latency-sensitive edge applications.
Aske and Zhao describe work on supporting multi-provider serverless computing at the edge {% cite aske2018supporting %}.
In addition to processing data generated at the edge, serverless models can be applied to disseminating information sourced from centralized data centers, as Facebook does with Bladerunner {% cite barber2021bladerunner %}.
