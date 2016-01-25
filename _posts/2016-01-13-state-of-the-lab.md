---
layout: post
title: State of the Lab 2016
author: whoburg
---

Welcome back from the holidays and happy 2016. I thought last night's State of the Union address a good occasion to reflect on our first 1.4 years of existence and where we're headed.

When I applied to join MIT, I wrote a research statement describing some computational challenges in aircraft design. I wrote that,
> <em>... despite the explosion in complexity, there is useful [mathematical] structure that we can (and must) find and exploit.</em>

I was describing the idea that combining arbitrary computational building blocks often leads to intractable optimization problems, and that to make progress in optimization models one needs to study the intersection of problems that matter with problems that can be solved reliably. I find this is still true.

In data science, a common refrain is that despite having lots of data, extracting actionable information remains difficult. (example of recent headline:  "Still Drowning in Big Data, and Starving for Insights"). I believe this holds for engineering design too: we're drowning in computing power and analysis tools, yet making design decisions remains as difficult and costly as ever.

How are we contributing?

As you all know intimately, our group is exploring a new opportunity: using tools from convex optimization to tackle engineering design problems. As part of this effort, we've developed a new capability:
[GPkit](http://github.com/hoburg/gpkit).
Looking back over the past 1.5 years of development, including
[1150 commits](http://github.com/hoburg/gpkit/commits/master)
on GitHub,
[289 resolved issues](http://github.com/hoburg/gpkit/issues?q=is:issue+is:closed),
6 official [releases](http://github.com/hoburg/gpkit/releases) (we're now at version 0.3.4),
and 157 unit tests running nightly on Jenkins, GPkit is sure growing up. There's still a lot of work left to do: 72
[open issues](http://github.com/hoburg/gpkit/issues) to address,
continuing to improve [documentation](http://gpkit.readthedocs.org/en/latest/), some [internal refactoring](http://github.com/hoburg/gpkit/pull/493),
and more. Ned (with help from me) will be leading that effort. But we've built a great tool, and it's time to start using it. And breaking it. And fixing it for the better. Let's continue building up our
[models library](http://github.com/aeroa/gpkit-models),
and publishing the models and methods we create.

We've made significant progress, but have more to do, on GP fitting — our tools for deriving convex optimization surrogate models from data sets. We recently submitted the final revision of a [journal paper](http://web.mit.edu/~whoburg/www/papers/gp_fitting.pdf) on GP fitting methods, and [GPfit](http://github.com/hoburg/gpfit) is our prototype software implementing those methods. GPfit would benefit from a more serious software development effort, maturing it to the level of GPkit. And there are potential connections to be made with (excuse the acronym overload) gaussian process (GP) regression methods. Mike Burton is starting a collaboration with Alex Felstein from Karen Willcox's group on exploring that possibility.

Last summer, we began an exciting new line of research on Signomial Programming (SP). This gives us a middle ground between GP and general NLP that provides fewer mathematical guarantees, but applies to many more models, and admits disciplined solution methods that do not require trust regions. SP has received far less research attention than GP, and I believe we're quickly becoming positioned to contribute at the forefront of that field, both via new solution methods/algorithms, and also by identifying new applications. I expect this to result in several new publications, starting with Philippe's recent SciTech paper describing SP models for aircraft landing gear, fuselage, and vertical fin sizing.

We're in the early stages of several exciting research projects with industrial sponsors. Our oldest is a joint project with Karen Willcox exploring unconventional aircraft configurations for Bob Liebeck's group at Boeing. Cody is leading our work on that effort. The next is another Boeing project developing mathematical models for composite fabrication — targeted at understanding the dynamics of the 787 fuselage fabrication production line in Charleston, SC. Scott Nill is leading this work. He spent last summer in Charleston absorbing all he could from the shop floor and working with Boeing experts; he's now back at MIT developing models. Finally, we've recently launched a new project with Aurora Flight Sciences and NASA, focused on developing GP and SP models for their D8 demonstrator. Philippe will be leading this work, which is a great chance to be involved in a clean-sheet design.

Beyond the details of these projects, I'd like us to push hard this term to 1) publish more journal papers, which we've gotten a slow start on, and 2) increase our web presence with occasional blog-post style updates about what we're working on and thinking about.

And now, back to work!
