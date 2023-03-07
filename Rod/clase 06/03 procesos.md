Generación de números aleatorios uniformemente distribuidos (mediante una secuancia congruencial periodica)

$x_{0}=semilla$
$x_{n+1}=ax_{u}+b~mod~w$

```python 3
import numpy as np
from matplotlib import pyplot as plt

def seed(ini):
    global rand
    rand = ini

def randcon(n):
    global rand
    a = 16887 # 7^5
    m = 2147483647 #2^3 -1
    num = []
    for k in range(n):
        rand = a * rand % m
        num = num + [rand]
    return np.array(num)

if __name__ =='__main__':
    plt.hist(randcon(50000),binds='auto')
    plt.show()
```

Revisar el libro de Donal knut, revisar las condiciones de divicibilidad The art of programing

$$\frac{1}{\sqrt{\pi}} \int_{-\infty}^{\infty}e^{-u^{2}}du = 1$$

Vamos a integrar la siguiente funcion dado lo que conocemos aunteriormente y lo vamos a probar en la distribucion gaussiana
$$\frac{1}{\Delta\sqrt{2\pi}}\int_{-\infty}^{\infty}e^\frac{-(x-\mu)^{2}}{2\sigma^{2}}dx$$
