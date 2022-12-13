Enfoque de clasiicación a través de un modelo probabilístico
Dada la probabilidad de que una instancia pertenezca a una clase es posible casificar nuevas instancias

$$p(y\mid X)$$

|Instance|Probability of class 1|Probability of class 2|
|--|-|--|
|1|0.8|0.6|
|2|0.8|0.5|
|3|0.6|0.6|

Describe la probabilidad de un evento (salida estimada),j basado en un conocimiento a priori de condiciones (características) que podrían estar relacionadas con el evento
$$P(y\mid X) = p(y) \frac{p(X\mid Y)}{p(X)}$$ 

| |cat|Documents|
|--|--|--|
|Training |-|just plain boring|
| |-|entirely predictable and lacks energy|
| |-|no suprises and very few laughs|
| |+|very powerful|
| |+|the most fun film of the summer|
| Test | ? | predictable with no fun|

Bayes y la distribución multinomial
$$Pp(y_{i}\mid d_{k}) = p(y_{i}) \prod_{i=1}^{n}p(w_{i}\mid y_{i})$$

$p(neg) = \frac{3}{5}=0.6$
$prob(pos) = \frac{2}{5}=0.4$
frecuencia:
$just  = 1$
$plain = 1$
$boring =1$
$entirely = 1$
$predictable = 1$
$and = 2$
$lacks= 1$
$energy = 1$
$no = 1$
$suprises = 1$
$very = 2$
$few = 1$
$laughs = 1$
$powerful =1$
$$