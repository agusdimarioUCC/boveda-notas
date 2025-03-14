tags: [#CálculoMatemático, #Funciones, #Análisis, #Ejemplo]

# Análisis Detallado de la Función $$f(x)=\frac{x^2}{x+5}$$

En esta nota se desglosan en detalle los pasos y conceptos fundamentales del análisis de funciones, utilizando como ejemplo la función racional  

$$
f(x)=\frac{x^2}{x+5}.
$$  
Esta función es representativa para estudiar no solo sus propiedades básicas, sino también la forma en que se comporta en diferentes intervalos y puntos críticos.

---

## 1. Dominio de la Función

El **dominio** de una función es el conjunto de todos los valores de $$x$$ para los que la función está definida.  
Para $$f(x)=\frac{x^2}{x+5}$$, el denominador no puede ser cero:  
$$
x+5\neq0 \quad\Longrightarrow\quad x\\neq -5.
$$  
Por lo tanto, el dominio es:  
$$
(-\infty, -5) \cup (-5, \infty).
$$

---

## 2. Ceros o Raíces

Los **ceros** de la función se encuentran igualando $$f(x)=0$$.  
Como la función es una fracción, el numerador debe ser cero (siempre que el denominador sea distinto de cero):  
$$
x^2=0 \quad\Longrightarrow\quad x=0.
$$  
Verificamos que $$x=0$$ pertenece al dominio (ya que $$0+5\neq0$$).  
**Conclusión:** La función tiene un único cero en $$x=0$$.

---

## 3. Asíntotas

### 3.1. Asíntota Vertical

Se produce cuando el denominador se anula (y el numerador no lo compensa):  
$$
x+5=0 \quad\Longrightarrow\quad x=-5.
$$  
Así, en $$x=-5$$ hay una **asíntota vertical**.

### 3.2. Asíntota Oblicua

Dado que el grado del numerador (2) es mayor que el del denominador (1), la función no posee asíntota horizontal, sino **oblicua**.  
Para hallar la asíntota oblicua se realiza la división polinómica de:
$$
\\frac{x^2}{x+5}.
$$  

**Procedimiento de división:**

1. **Primer cociente:**  
   $$x^2 \div x = x.$$  
   Multiplicamos:  
   $$x(x+5)=x^2+5x.$$  
   Restamos:  
   $$x^2 - (x^2+5x)= -5x.$$

2. **Segundo cociente:**  
   $$-5x \\div x = -5.$$  
   Multiplicamos:  
   $$-5(x+5) = -5x - 25.$$  
   Restamos y obtenemos el residuo:  
   $$-5x - (-5x-25)= 25.$$

El resultado es:
$$
f(x)= x-5+\\frac{25}{x+5}.
$$  
Cuando $$x\\to \\pm\\infty$$, la fracción tiende a 0 y la función se comporta como:  
$$
y=x-5.
$$  
**Conclusión:** La **asíntota oblicua** es:  
$$
y=x-5.
$$

---

## 4. Derivadas y Extremos

### 4.1. Primera Derivada: Identificación de Puntos Críticos

Para determinar máximos y mínimos locales, se calcula la primera derivada de  
$$
f(x)=\\frac{x^2}{x+5}.
$$

Utilizando la regla del cociente:
$$
f'(x)= \\frac{(2x)(x+5) - x^2(1)}{(x+5)^2} = \\frac{2x^2+10x-x^2}{(x+5)^2} = \\frac{x^2+10x}{(x+5)^2}.
$$  
Factorizando el numerador:
$$
f'(x)=\\frac{x(x+10)}{(x+5)^2}.
$$

Los puntos críticos se obtienen cuando el numerador es cero (sin contar los puntos donde la función no está definida):
- $$x(x+10)=0$$  
  - **Caso 1:** $$x=0$$  
  - **Caso 2:** $$x=-10$$

Verificamos que ambos puntos pertenecen al dominio (recordamos que $$x\\neq -5$$).

### 4.2. Clasificación de los Puntos Críticos

Para clasificar estos puntos, analizamos el signo de $$f'(x)$$ en los intervalos determinados por los valores críticos y el punto de discontinuidad $$x=-5$$.

- **Intervalo $$(-\\infty, -10)$$:**  
  Tomemos $$x=-11$$:  
  $$f'(-11)= \\frac{(-11)(-11+10)}{(-11+5)^2}= \\frac{(-11)(-1)}{36} = \\frac{11}{36}>0.$$

- **Intervalo $$(-10, -5)$$:**  
  Tomemos $$x=-7$$:  
  $$f'(-7)= \\frac{(-7)(-7+10)}{(-7+5)^2}= \\frac{(-7)(3)}{4}= \\frac{-21}{4}<0.$$

- **Intervalo $$(-5, 0)$$:**  
  Tomemos $$x=-1$$:  
  $$f'(-1)= \\frac{(-1)(-1+10)}{(-1+5)^2}= \\frac{(-1)(9)}{16}= \\frac{-9}{16}<0.$$

- **Intervalo $$(0, \\infty)$$:**  
  Tomemos $$x=1$$:  
  $$f'(1)= \\frac{1(1+10)}{(1+5)^2}= \\frac{11}{36}>0.$$

**Conclusiones:**
- En $$x=-10$$, $$f'(x)$$ cambia de positivo a negativo, lo que indica un **máximo local**.  
  - Valor:  
    $$f(-10)=\\frac{(-10)^2}{-10+5}= \\frac{100}{-5}= -20.$$
- En $$x=0$$, $$f'(x)$$ cambia de negativo a positivo, lo que indica un **mínimo local**.  
  - Valor:  
    $$f(0)=\\frac{0^2}{0+5}=0.$$

*Nota:* Aunque $$-20$$ es un valor bajo, se trata de un máximo local en la rama de la función correspondiente a $$x<-5$$, mientras que en otras partes la función alcanza valores mayores.

---

## 5. Concavidad e Inflexión

### 5.1. Segunda Derivada

Para analizar la **concavidad**, calculamos la segunda derivada de $$f(x)$$. Partimos de:
$$
f'(x)=\\frac{x(x+10)}{(x+5)^2}.
$$

Utilizamos la fórmula de la derivada de un cociente, donde:
- $$u(x)= x^2+10x$$  
- $$v(x)= (x+5)^2$$  
- $$u'(x)= 2x+10$$  
- $$v'(x)= 2(x+5)$$

Aplicamos la fórmula:
$$
f''(x)=\\frac{u'(x)v(x) - u(x)v'(x)}{v(x)^2}.
$$

Sustituyendo:
$$
f''(x)= \\frac{(2x+10)(x+5)^2 - (x^2+10x)\\,2(x+5)}{(x+5)^4}.
$$

Extraemos un factor común de $$x+5$$ en el numerador:
$$
f''(x)= \\frac{(x+5)[(2x+10)(x+5)-2(x^2+10x)]}{(x+5)^4} = \\frac{(2x+10)(x+5)-2(x^2+10x)}{(x+5)^3}.
$$

Realizando la expansión:
- $$ (2x+10)(x+5)= 2x^2+10x+10x+50= 2x^2+20x+50. $$
- Entonces:
  $$
  2x^2+20x+50-2x^2-20x=50.
  $$

Así, la segunda derivada es:
$$
f''(x)=\\frac{50}{(x+5)^3}.
$$

### 5.2. Análisis de la Concavidad

- **Para $$x > -5$$:**  
  $$x+5>0 \\Longrightarrow (x+5)^3>0 \\quad\\Longrightarrow\\quad f''(x)>0.$$  
  La función es **cóncava hacia arriba** en este intervalo.

- **Para $$x < -5$$:**  
  $$x+5<0 \\Longrightarrow (x+5)^3<0 \\quad\\Longrightarrow\\quad f''(x)<0.$$  
  La función es **cóncava hacia abajo** en este intervalo.

*Nota:* Aunque el cambio de concavidad ocurre en torno a $$x=-5$$, este punto es una discontinuidad (asíntota vertical) y, por tanto, no se clasifica como un punto de inflexión.

---

## 6. Intervalos de Crecimiento y Decrecimiento

Basándonos en el análisis de la primera derivada $$f'(x)=\\frac{x(x+10)}{(x+5)^2}$$, se tienen los siguientes intervalos:

- **Creciente:**  
  - Para $$x < -10$$: $$f'(x)>0$$  
  - Para $$x > 0$$: $$f'(x)>0$$

- **Decreciente:**  
  - Para $$-10 < x < -5$$: $$f'(x)<0$$  
  - Para $$-5 < x < 0$$: $$f'(x)<0$$

Recordar que la función no está definida en $$x=-5$$, por lo que se deben considerar los intervalos por separado.

---

## 7. Análisis de Signos

El **análisis de signos** ayuda a entender el comportamiento global de la función:

- **Numerador:**  
  $$x^2 \\ge 0$$ para todo $$x$$.  
  Se anula en $$x=0$$.

- **Denominador:**  
  $$x+5$$  
  - Es **positivo** si $$x > -5$$.  
  - Es **negativo** si $$x < -5$$.

**Interpretación:**
- Para $$x > -5$$, $$f(x) \\ge 0$$, siendo cero únicamente en $$x=0$$.
- Para $$x < -5$$, $$f(x) \\le 0$$, ya que un numerador no negativo dividido por un número negativo da como resultado un número negativo.

---

## 8. Resumen y Conexiones

### Resumen del Análisis de $$f(x)=\\frac{x^2}{x+5}$$
- **Dominio:** $$x\\in (-\\infty, -5)\\cup(-5,\\infty)$$.
- **Cero:** Se presenta en $$x=0$$.
- **Asíntota vertical:** En $$x=-5$$.
- **Asíntota oblicua:** La función se aproxima a $$y=x-5$$ cuando $$x\\to\\pm\\infty$$.
- **Puntos críticos:**  
  - **Máximo local:** En $$x=-10$$, con $$f(-10)=-20$$.  
  - **Mínimo local:** En $$x=0$$, con $$f(0)=0$$.
- **Concavidad:**  
  - **Cóncava hacia abajo** para $$x<-5$$.  
  - **Cóncava hacia arriba** para $$x>-5$$.
- **Crecimiento/Decrecimiento:**  
  - Creciente en $$(-\\infty,-10)$$ y $$(0,\\infty)$$.  
  - Decreciente en $$(-10,-5)$$ y $$(-5,0)$$.
- **Análisis de signos:**  
  - La función es negativa en $$x<-5$$ y positiva en $$x>-5$$, excepto en $$x=0$$ donde es cero.

### Conexiones Internas
- [[Funciones Racionales]]
- [[Derivadas y Extremos]]
- [[Concavidad e Inflexión]]
- [[Análisis de Signos]]
- [[Intervalos de Crecimiento y Decrecimiento]]

---

## 9. Reflexiones y Consejos para Aplicar

- **Profundiza en cada concepto:**  
  Comprender el dominio, ceros, y asíntotas es esencial para predecir el comportamiento de funciones complejas. No te limites a memorizar fórmulas, sino practica aplicando cada paso en diferentes ejemplos.

- **Conecta la teoría con la práctica:**  
  Relaciona este análisis con problemas reales en ingeniería y ciencias. Por ejemplo, modela fenómenos que presentan discontinuidades o cambios bruscos en comportamiento (como cambios de fase en sistemas físicos).

- **Organización y documentación:**  
  Utiliza sistemas como Obsidian para conectar conceptos. Por ejemplo, vincula tus notas de "Funciones Racionales" con "Derivadas" y "Concavidad". Esto facilita la revisión y el aprendizaje integral.

- **Mentalidad de crecimiento:**  
  Acepta los desafíos y busca siempre profundizar. Cuando un concepto te parezca complejo, divide el problema en partes más pequeñas y resuélvelo paso a paso.

- **Experimenta y cuestiona:**  
  No te quedes con la primera solución; explora variaciones y casos límite. Pregúntate qué sucede si cambias el numerador o el denominador, y utiliza software de matemáticas para visualizarlo.

---

**Tags:** #CálculoMatemático #Funciones #Análisis #Ejemplo #MatemáticasAvanzadas
