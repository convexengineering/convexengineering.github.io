---
layout: post
title: SP commercial aircraft model functional. 
author: bozturk
---

For the last two semesters, Martin and Berk have been developing a signomial programming compatible commercial aircraft model of similar fidelity as TASOPT. They have been successful at optimizing a variety of aircraft configuration using their framework, with vast speed improvements over similar aircraft multidisciplinary design tools. (The example single-mission 737-800 optimization has over 1700 free variables, and solves in under 10 seconds, whereas TASOPT performs the same optimization in ~100 seconds). The SP aircraft model has further advantages, including the ability to easily evaluate different aircraft configurations and to reliably change objective functions. When the SP is solved, both the optimal point and the sensitivity of the optimal cost to all parameters are found. These values provide valuable design intuition and direction for future modeling enhancements. The model is available on [Github](https://github.com/hoburg/d8). Detailed documentation of the model will be made available during Summer 2017. 