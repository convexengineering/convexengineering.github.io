---
layout: post
title: Moment of Inertia GP Formulation
author: bozturk
---

A beam's moment of intertia determines its stiffness in bending, so it's a critical engineering quantity when one wants to limit beam bending. As a structural designer, we are also interested in structural efficiency, and want to minimize the cross-sectional area of the beam we are designing (since it is proportional to the weight, and likely the cost, of the beam). 

However, the beam cross-section optimization problem is not immediately GP-compatible. So we have created a GP approximation for the [area moment of inertia of a hollow cylindrical section](https://github.com/hoburg/gpkit-models/tree/master/gpkitmodels/moi), and hope it will facilitate the application of GPkit to general beam optimization problems. 
