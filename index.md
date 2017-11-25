---
layout: default
title: Home
---

<h1 id="convex-engineering-group" style="margin-top: -2rem;">Convex Engineering Group</h1>

**We use convex optimization to rethink the engineering design process.**
 What length of night can a solar airplane fly through, and how does this depend on the weight of its sensors? Engineering requires understanding tradeoffs across possible designs.
When wingspan, altitude, and the thousands of other design decisions are represented as variables subject to convex constraints, mathematics of convexity let the boundary of tradeoffs and possibilities be mapped in seconds.
<br>
<iframe width="560" height="315" src="https://www.youtube.com/embed/HMu3x5WxpeM" frameborder="0" allowfullscreen></iframe>
<br>
By using convexity as a shared design language, our [GPkit] modeling framework helps design teams explore and agree on engineering possibilities and fundamental tradeoffs.
GPkit was integral to the concept and design of the  [MIT Jungle Hawk Owl](http://news.mit.edu/2017/drones-stay-aloft-five-days-0607), an unmanned aircraft that can stay aloft for five days,
and is in active use at Aurora Flight Sciences, Airbus, Hyperloop One, Shell Oil and Google \[x\].
To learn how to use it in your own work, see the [documentation](http://gpkit.readthedocs.io/en/latest/gettingstarted.html) or [model library][GPlibrary].

### Our Research is Open Source
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
