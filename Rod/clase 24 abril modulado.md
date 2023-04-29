### Naive bayes
el calisficados va a trabajr bajo ciertas suposiciones:
1. Asumimos que las predicciones del modelo son condicionalmente independientes, or unreleated to any of the other feature in the model
2. all feautres contribute equality to the outcome


Excersise 
Suppose you geta sample of size 100 from your emails, where 20 of the emails in the sample are spam and 8- others are ham. You decide to count some words in the emails and after that, you got the following table

$$P(spam\mid viagra,unscribe,\vec{money}, \vec{grocies})$$
$$=p(v|s)P(u|s)P(\hat{m}|s)P(\hat{g}|s)p(s)$$
$$=\frac{4}{20}* \frac{1}{20}* \frac{10}{20} * \frac{20}{20}* \frac{20}{100}=0.012$$

$$P(ham\mid viagra,unscribe,\vec{money}, \vec{grocies})$$
$$\frac{1}{80} * \frac{23}{80} * \frac{66}{80} * \frac{71}{80} * \frac{80}{100} = 0.002$$

Normalizamos las prob
$$\frac{0.012}{0.012+0.002}=0.85\rightarrow spam$$
$$\frac{0.002}{0.012+0.002}=0.15\rightarrow ham$$

## Support vector machine
#### Hiperplano seguro
Un separador seguro con respecto a la mediad de error, si el calisficador de al dara lo hace correctamente. Un separador puede tolear una medida de error más segura.