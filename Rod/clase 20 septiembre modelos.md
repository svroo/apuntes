# Multiple Regression Analysis

As a basic example of a model with two independent variables, we eill introduce a modification of the wage equation:
$$wage=\beta_{0}+\beta_{1}\cdot educ+\beta_{2}\cdot exp+u$$

Multiple regression analysis is also useful for generalizing functional relationships bewtween variables, for example

$$wage=\beta_{0}+\beta_{1}\cdot experience+\beta_{2} \cdot experience^{2}+u$$

Mechanically, there will be no difference in using the method of OLS to estimate equations. There is however an important difference in how one interprets teh parameters. In this case, it makes no sense to measure the effect of experience on wage while holding squared expereince fixed, instead, the cange in wage with respect to the chanbe in expereince is approximated by:

$$\frac{\Delta wage}{\Delta experience}\approx \beta_{1}+2\beta_{2}~\cdot experience$$

$$\Delta wage\approx \beta_{1}\Delta~exp+2~\beta_{2}~\Delta ~exp~\cdot~exp$$
and this is equal to:

$$\frac{\Delta wage}{\Delta experience}\approx\frac{d\cdot wage}{d\cdot exp}$$


In the model with two independent variables, the key assumption about how u is related to $x_{1}$ and $x_2$ is:
$$\mathbb{E}[u\mid x_{1},x_{2}]=0$$
It means that, that any other factors affecting y, u, are not related on average to $x_{1}$ and $x_{2}$.

In the previou sexample writting $\mathbb{E}[u\mid experience, experience^{2}]$ is redundant since $\mathbb{E}[u\mid experience, experience^{2}]=\mathbb{E}[u\mid experience]=0$

## The model with k independent variables
The general multiple **regresion model** can be wirtten in the population as:


<div align='right'><h3>clase 22 de septiembre del 2023</h3></div>
