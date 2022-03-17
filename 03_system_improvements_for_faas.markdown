---
layout: section
title: System Improvements for FaaS
permalink: /faas-system-improvements/
nav_order: 3
---

A large category of serverless research involves system improvements to FaaS.
There is a tension between providing isolation, efficient multiplexing, and low-latency performance.
OpenLambda {% cite hendrickson2016serverless %} and McGrath et al. {% cite mcgrath2017serverless %} both developed early prototype FaaS systems that mirrored the inner workings of FaaS platforms and helped illustrate this research challenge.

One manifestation of the tension is in cold starts.
SOCK {% cite oakes2018sock %} uses various systems techniques to reduce these, particularly for FaaS applications that use libraries with high initialization costs.
Catalyzer {% cite du2020catalyzer %} takes on the same challenge, using checkpoints to start functions instead of executing their initialization code.
Xanadu {% cite daw2020xanadu %} provides techniques for mitigating cascading cold starts, and Mohan et al. {% cite mohan2019agile %} discuss techniques for preallocating resources such as network interfaces to reduce cold start times.

FaaS also incurs cold start latencies and other overheads from the underlying operating system and hypervisor.
Firecracker {% cite agache2020firecracker %} is a lightweight microVM technology developed by AWS that reduces the startup times and memory requirements of VM isolation.
Koller and Williams {% cite koller2017will %} have suggested using unikernels with FaaS instead of traditional operating systems in a further bid to improve efficiency.
There are also alternatives to using VMs for isolation.
Faasm {% cite shillaker2020faasm %} provides lightweight isolation based on WebAssembly {% cite haas2017bringing %}.
Alto {% cite larisch2018alto %} generalizes lightweight virtualization to other managed runtime environments.

Isolation not only creates startup costs but ongoing runtime costs as well.
Young et al. {% cite young2019true %} study the performance overheads of gVisor {% cite gvisor %}, which is used by Google's serverless products.
Anjali et al. {% cite caraza2020blending %} compare serverless isolation mechanisms, including Linux containers, gVisor, and Firecracker microVMs.

Even when no cold starts are involved, the latency of FaaS function invocation can be too high for some applications.
Contributing factors include overheads of passing data, queuing overheads, and scheduling overheads or delays.
Sonic {% cite mahgoub2021sonic %}, SAND {% cite akkus2018sand %}, SEUSS {% cite cadden2020seuss %}, and Cloudburst {% cite sreekanti2020-ec %} all address various aspects of these slowdowns.

Work on scheduling includes that by Kaffes et al. {% cite kaffes2019centralized %}, which uses a centralized scheduler with a global view to eliminate imbalances.
FnSched {% cite suresh2019fnsched %} offers another scheduler that aims to improve latency and utilization, and Caerus {% cite zhang2021caerus %} provides scheduling for serverless analytics.
Work by Mahmoudi et al. describes an algorithm for adaptive function placement.

A diverse assortment set of other work seeks to improve FaaS.
Shredder {% cite zhang2019narrowing %} embeds FaaS computations with object storage.
Faa\$T {% cite romero2021transparent %} provides a provider-managed cache for serverless applications.
Particle is a network overlay suited to the burstiness of serverless computing {% cite thomas2020particle %}.
Gupta {% cite gupta2020serverless %} et al. demonstrate straggler mitigation using error-correcting codes.
Kappa {% cite zhang2020kappa %} provides fault tolerance and extended execution times by checkpointing and restarting FaaS applications.
InfiniCache {% cite wang2020infinicache %} shows how to use erasure coding to build a cache from idle FaaS instances.
Harvest VMs {% cite zhang2021faster %} allows FaaS to run using resources momentarily left idle by traditional server VMs.
