---
layout: default
title: Home
---

<h1 id="convex-engineering-group" style="margin-top: -2rem;">Convex Engineering Group</h1>

**We use convex optimization to rethink the engineering design process.**
Engineering requires understanding tradeoffs across possible designs.
What length of night can a solar airplane fly through, and how does this depend on the weight of its sensors?
Flight altitude, wingspan, and the many other necessary considerations can be formalized as decision variables subject to algebraic constraints.
The mathematical structure of convexity lets thousands of decision variables be analyzed in seconds to find the full extent of designs possible between a project's goals and its requirements.

Our modeling framework [GPkit] uses convexity as a shared design language to help engineering teams build these understandings of fundamental system tradeoffs.
GPkit was integral to the concept and design of the [MIT Jungle Hawk Owl](http://news.mit.edu/2017/drones-stay-aloft-five-days-0607), an unmanned aircraft that can stay aloft for five days,
and is in active use at Aurora Flight Sciences (for NASA’s D8 and LEARN3 initiatives), Airbus, Hyperloop One, Shell Oil and Google \[x\]
To learn how to use it in your own work, see the [documentation](http://gpkit.readthedocs.io/en/latest/gettingstarted.html) or [model library][GPlibrary].
<br>
<iframe width="560" height="315" src="https://www.youtube.com/embed/HMu3x5WxpeM" frameborder="0" allowfullscreen></iframe>

### Open Source Research
We incorporate new insights and algorithms into our tools, develop reusable subsystem models, and combine the two to explore interesting engineering systems.
If you have any questions or would like to be involved, [send us an email](mailto:gpkit@mit.edu)!

<!-- TODO: autogenerate the below from projects page data -->
#### Software Tools
  - [GPkit] : disciplined object-oriented geometric programming
  - [GPfit] : algorithms for data-driven design optimization
  - [GPlibrary] : subsystem models for rapid prototyping 
  - [robust] : modeling framework for robust GPs and SPs

#### Design Explorations
  - [STOL] and [eVTOL] on-demand aviation
  - [solar long-endurance aircraft][solar]
  - [Jungle Hawk Owl][jho] design and prototyping
  - [comparison of gas-/solar-powered long-endurance UAVs][gassolar]
  - verified 1D core + fan flowpath [turbofan engine][turbofan] 
  - [commercial airliner models][SPaircraft] comparable to TASOPT

[GPkit]: https://gpkit.readthedocs.io/en/latest/
[GPlibrary]: https://github.com/convexengineering/gplibrary
[GPfit]: https://github.com/convexengineering/gpfit
[robust]: https://github.com/convexengineering/robust
[turbofan]: https://github.com/convexengineering/turbofan
[SPaircraft]: https://github.com/convexengineering/SPaircraft
[gassolar]: https://github.com/convexengineering/gassolar
[solar]: https://github.com/convexengineering/solar
[jho]: https://github.com/convexengineering/jho
[STOL]: https://github.com/convexengineering/STOL
[eVTOL]: https://github.com/convexengineering/eVTOL
