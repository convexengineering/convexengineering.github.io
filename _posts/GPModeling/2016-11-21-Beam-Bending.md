---
layout: post
title: Moment of Inertia GP Formulation
author: bozturk
---

Introduction
-------------------------

In this example, we express the area moment of inertia (I) of a hollow cylindrical section as a functional of its physical dimensions to formulate the bending section design problem in a GP form.

Hollow Cylinder Bending Inertia Equations
--------------------------

The inertia of a beam describes the stiffness of the beam in bending. If we desire to create a beam bending model in GP, it is a critical quantity. Since we are also interested in structural efficiency, we want to minimize the cross-sectional area of the section, which describes the weight of the beam along with the density of the beam and its length. 

<figure>
<img src="../../public/images/MoICylinder.PNG" alt="The cross-sectional parameters of a hollow cylindrical section" style="width: 200px; align-content: center"/>
<figcaption> Figure 1. The cross-sectional parameters of a hollow cylindrical section </figcaption>
</figure>


<!-- ![The cross-sectional parameters of a hollow cylindrical section]( = 120x120) -->

<!-- \begin{figure}[h]
    \centering
    \includegraphics[width = 5cm]{MoICylinder}
    \caption{The cross-sectional parameters of a hollow cylindrical section}
    \label{fig:cylinder}
\end{figure} -->

The equations for the inertia and cross-sectional area of a hollow cylindrical section are shown in Figure 1 are: 

\begin{equation}
\tag{1}
A = \pi(r_o^2 - r_i^2) 
\end{equation}

\begin{equation}
\tag{2}
I = \frac{1}{4}\pi(r_o^4 - r_i^4)
\end{equation}

where $r_o$ is the outer radius, $r_i$ is the inner radius, $A$ is the cross-sectional area, and $I$ is the moment of inertia of the section. The form as-is is not GP compatible by the following reasoning. 

If we say that greater $I$ is good and greater $A$ is bad, then the right bounding inequalities for the expressions above are:

\begin{equation}
\tag{3}
A >= \pi(r_o^2 - r_i^2) 
\end{equation}

\begin{equation}
\tag{4}
I <= \frac{1}{4}\pi(r_o^4 - r_i^4)
\end{equation}
    
since we are trying to maximize $I$ and minimize $A$. Equation 4 is GP-compatible, since we can add $\frac{1}{4}\pi r_i^4$ to both sides of the equation and have a valid posynomial. However, no such transformation is possible for Equation 3. And if we changed the sign of the inequality in Equation 3, then $A$ would go off to $10^{-\infty}$, a non-physical solution.

GP Formulation
-------------------

We begin by rearranging Equation 3 to get the following:

\begin{equation}
\tag{5}
    \frac{A}{\pi} = r_o^2 - r_i^2
\end{equation}

We then split Equation 4 as shown in Equation 6. Note that we limit $I$ to be less than the right hand side (RHS) of the equation, for later conversion into posynomial form. This allows us to use the cross-sectional area relation from Equation 5 to describe the inertia, yielding Equation 7.

\begin{equation}
\tag{6}
    I \leq \frac{1}{4} \pi (r_o^2 - r_i^2 ) (r_o^2 + r_i^2)
\end{equation}

\begin{equation}
\tag{7}
    I \leq \frac{1}{4} A (r_o^2 + r_i^2)
\end{equation}

We use the geometric mean to make an approximation for $(r_o^2 + r_i^2)$.

\begin{equation}
\tag{8}
    2r_or_i \leq  r_o^2 + r_i^2
\end{equation}

Substituting Equation 8 into Equation 7, we can get a conservative bound on the moment of inertia that is GP-compatible. 

\begin{equation}
\tag{9}
    I \leq \frac{Ar_or_i}{2}
\end{equation}

Rearranging the area relation in Equation 3:

\begin{equation}
\tag{10}
    r_i^2 + \frac{A}{\pi} \leq r_o^2
\end{equation}

We substitute for $r_i$ from Equation 11 in Equation 12:

\begin{equation}
\tag{11}
   r_i^2 \geq \frac{4I^2}{A^2r_o^2}
\end{equation}

\begin{equation}
\tag{12}
    \frac{4I^2}{A^2r_o^2} + \frac{A}{\pi} \leq r_o^2
\end{equation}

The final formulation is as follows:

\begin{equation}
\tag{13}
   \bar{W} \geq \rho A
\end{equation}

\begin{equation}
\tag{14}
    \frac{4I^2}{A^2r_o^2} + \frac{A}{\pi} \leq r_o^2
\end{equation}


This formulation is GP-compatible, because the equations are of monomial and posynomial forms, and we have the right bounds on the two parameters we care about. Greater moment of inertia $I$ is good, but it is upper bounded by the outer radius. And area $A$ is bounded because it is directly proportional to the weight of the structure in question, which we want to minimize. Using Equations 13 and 14, we can give conservative approximations for the area moments of inertia of hollow cylindrical beams, allowing us to calculate their deflections under bending loads. 

However, it is important to note that the geometric mean has been used in Equation 8 to give a conservative bound on the moment of inertia, which means that the solution is not exact. Furthermore, it doesn't seem absolutely clear that the constraint in Equation 14 will be always tight, but results from problems that use this models show empirically that it is always tight. The engineering intuition holds!






