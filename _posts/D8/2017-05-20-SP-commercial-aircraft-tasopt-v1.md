---
layout: post
title: SP commercial aircraft model completed.
author: bozturk
---

<img src="../../public/images/vsp_example.PNG" alt="vsp_example" style="width: 300px;"/>

For the last year, Martin and Berk have been developing a signomial programming compatible commercial aircraft model of similar fidelity as TASOPT. They have optimized a variety of aircraft using their framework with vast speed improvements over similar aircraft multidisciplinary design tools. (The example single-mission 737-800 optimization has over 1700 free variables, and solves in under 10 seconds, whereas TASOPT performs the same optimization in ~100 seconds). The SP aircraft model has further advantages, including the ability to more easily evaluate different aircraft configurations and to solve for different objective functions. When the SP is solved, both the optimal point and the sensitivity of the optimal cost to all parameters are found. These values provide valuable design intuition and direction for future modeling enhancements. The model is available on [Github](https://github.com/hoburg/d8). Detailed documentation of the model will be made available during Summer 2017. 