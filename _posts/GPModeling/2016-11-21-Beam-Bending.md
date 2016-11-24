---
layout: post
title: Moment of Inertia GP Formulation
author: bozturk
---

The inertia of a beam describes the stiffness of a beam in bending; it is a critical quantity in general beam bending problems. As a structural designer, we are also interested in structural efficiency. We want to minimize the cross-sectional area of the beam we are designing, which is proportional to the weight of the beam. 

However, the beam cross-section optimization problem is not immediately GP-compatible.  

[We have created a model](https://github.com/hoburg/gpkit-models/tree/master/gpkitmodels/moi) to express the area moment of inertia (I) of a hollow cylindrical section as a function of its physical dimensions to formulate the bending section design problem in a GP-compatible form. We hope it will facilitate the application of GPkit to solve general beam optimization problems. 







