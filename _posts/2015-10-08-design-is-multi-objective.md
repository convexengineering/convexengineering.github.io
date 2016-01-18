---
layout: post
title: Design is Multi-Objective
author: eburn
---

The hardest thing (in optimization) is figuring out what you want.
Even if we assume that all your wants are quantifiable, they’re probably not modelable: that is to say,
even if you can assign an objective number to how good a design is (e.g., yearly profit of an airplane model),
you probably can’t derive it from simpler quantities (e.g., that model’s range and speed).

If you can do both, congratulations!
What you want is so mathematical that, to you, one design is always better, worse, or interchangeable with another. But for most problems a single want (profit) is too much to model,
and so we’re left with too many wants (speed, range) as proxies.

We need to explore a design space of competing alternatives, many of which have irreducable tradeoffs
(e.g., between a fast short-hop plane and a slow long-distance one).
The good news is that numerical optimization can take our complicated model straight to these tradeoffs;
the bad is that even after that you still have to figure out which you want.

Numerical optimization is often thought of as a way to “get an answer”.
From a mathematical perspective, this is true;
it’s like going to the Oracle with your linear program and asking the priests for the minimum possible value of $x$;
after some deliberation, you get an answer you believe to be true: $3$.
But just like the Oracle, the answer lacks broader context, and misapplying it may lead your ancient empire to ruin.

It’s more useful to think of numerical optimization as an interrogation of a model;
it’s a way to understand the interconnections of variables, constraints, and objectives from a mathematical standpoint,
but inaccuracies in the model can result in absurdly unrealistic optima that are, mathematically speaking, strictly correct.

This might seem like a disadvantage:
after all, you give the computer a model you trusted, and it spat out something ridiculous.
But this is in fact a first  and vital step:
where you saw a series of trusted equations, the computer saw a hairball of emergent interconnections and told you so.

Optimization gives a way for a model to earn your trust;
as it produces good and results with the cases you throw at it,
you understand where to trust your models and where they need improvement.
Once you trust your model not just on paper, but in practice, you can use it to generate designs for comparison.

So, with your tested model and multiple objectives (e.g., airplane range and speed), you want to start examining tradeoffs, and choosing between good designs.
The variety of design possibilities is sometimes called the “design space”; but since you’ve decided to only care about certain variables (your objectives), what you want to see is each design plotted according to its merits, what I’ll call the “objective space”. [after Mueller]

And there’s really no need to look at designs that are worse in both objectives than another design:
that is, if one design is slower and shorter-range than another, there would be no reason to choose it with your current objectives.
This assumes that you always want more or less of each of your objectives
(it’s practically part of the definition of an “objective”).
If you actually do prefer the "worse" design, this is a modeling error;
either you have recognized a missing objective,
or the second design is unrealistic and you need to further constrain your model,
or it’s actually an unmodelable subjective, and should be broken down into multiple objectives.

The subset of the objective space with only designs that are not strictly worse than another design is called the “Pareto frontier”,
and as the frontier of solutions possible under your model, it’s where the consideration of tradeoffs begins.
By removing all these subpar designs, the Pareto frontier reduces the number of dimensions a designer has to consider from all variables to just those that are objectives.
Objectives, by their nature, are not just fewer in number but also directly meaningful,
so this dimensionality reduction makes the model much more human-comprehensible.

This is what computers are best at:
managing multitudes of simple interactions so as to present a human with only irreducibly complex decisions.
