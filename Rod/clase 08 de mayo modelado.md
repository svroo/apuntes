# Maquina de soporte para datos no lineales
To render the data separable, we would typically transform into a higher dimensions. Consider a transform $\phi:\mathbb{R}^{d}\rightarrow\mathbb{R}^{d}$. The transformed data are:
$$z_{n}=\phi(X_{n})$$
After transforming the data, we solve the hard-margin SVM problem in the Z space:
$$minize : \frac{1}{2}w^{t}\vec{w}$$
$$subject~to:y_{n}(\vec{w}^{t}z_{n}+b)\geq 1~~~~(n=1,\dots,N)$$



## Dual formulation of the SVM
We are going to introduce the dual SVM problem wich is equivalent to the original primal problem in that solving both problems gives the smae optimal hyperplane, but the dual problem is often easier. It is this dual view of the SVM that will enable us to exploit the kernel.

### Lagrange Dual for a QP-Problem
Let us ilustrate the concept of the dual with a simplified version of the standard QP. problem using just one inequality constrain. All the consepts will easily generalize to the case with more than constraint. So, consider the QP-problem.
$$Minize_{u\in\mathbb{R}^{L}}: \frac{1}{2}u^{T}Qu+p^{T}u$$
$$Subject~to:a^{T}u\geq c$$
Here is a closelt related optimization problem.
$$minimize_{u\in\mathbb{R}^{L}}: \frac{1}{2}u^{T}Qu +p^{T}u+max_{\alpha>0}~\alpha(c-a^{T}u)$$
The advantage is that the minimization with respect to **u** is unconstrained, and the price is a slightly more complex objective that involves this "Lagranglan penalty term"
$$\mathcal{L}(u,\alpha)=\frac{1}{2}u^{T}Qu +p^{T}u+\alpha(c-a^{T}u)$$
in terms of $\mathcal{L}$ 

### Excercise
Show that the previous optimization problem is a standar QP-problem
