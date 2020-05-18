{
 "cells": [
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "# Tarea Ejercicios Capítulo 6"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "#### Cuéllar Ortega Luis Enrique\n",
    "#### Arriaga Jacuinde Marco Antonio"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**1. Realizamos la mejor selección de un subconjunto, paso a paso hacía adelante y paso a paso hacía atrás en un solo conjunto de datos. Para cada enfoque, obtenemos modelos p+1, que contienen predictores 0,1,2,...,p. Explica:**"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "- *(a)¿Cuál de los tres modelos con k predictores tiene el menor RSS de entrenamiento?*"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Respuesta:** Con la selección de paso a paso hacía adelante el modelo con k predictores de entre los modelos p-k  que aumentan los predictores en Mk+1, es decir, un predictor más, es el que menor RSS de entrenamiento tiene.\n",
    "\n",
    "Con la selección de paso a paso hacía atrás el modelo con k predictores de entre los modelos que contienen k-1 predictores en Mk+1.\n",
    "\n",
    "El modelo con predictores k con el RSS de entrenamiento más bajo es el mejor dentro de todos los demás modelos comparados"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "- *(b)¿Cuál de los tres modelos con k predictors tiene el menor RSS de prueba?*"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Respuesta:** La selección de subconjuntos con RSS de prueba más pequeño tienene en cuenta más modelos que otros métodos. Pero los otros métodos podrían ajustar mejor los datos por suerte."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "- *(c) Verdadero o falso:*\n",
    "\n",
    "i. Los predictores en el modelo de k-variables identificados por avance gradual son un subconjunto de los predictores en el modelo variable (k+1) identificado por selección progresiva.\n",
    "\n",
    "**Respuestta:** Verdadero, el modelo con predictores (k+1) se obtiene al aumentar los predictores en el modelo con predictores k con predictor adicional.\n",
    "\n",
    "ii. Los predictores in el modelo de k-variables identificados por busqueda gradual hacia atrás son un subconjunto de los predictores en el modelo variable (k+1) identificado por selección progresiva hacia atrás.\n",
    "\n",
    "**Respuesta:** Verdadero, el modelo con k predictores se obtienen removiendo un predictor del modelo con (k+1) predictores.\n",
    "\n",
    "iii. Los predictores en el modelo de variable k identificados por retroceso paso a paso son un subconjunto de los predictores en el modelo variable (k+1) identificado por selección progresiva hacia adelante.\n",
    "\n",
    "**Respuesta:** Falso, no hay vinculo directo entre los modelos obtenidos de la selección hacia adelante y hacia atrás.\n",
    "\n",
    "iv. Los predictores en el modelo de variable k identificados por avance gradual son un subconjunto de los predictores en el modelo variable (k+1) identificado por selección gradual hacia atrás.\n",
    "\n",
    "**Respuesta:** Falso, no hay vinculo directo entre los modelos obtenidos de la selección hacia adelante y hacia atrás.\n",
    "\n",
    "v. Los predictores en el modelo de variable k identificados por el mejor subconjunto son un subconjunto de los predictores en el modelo variable (k+1) identificado por la mejor selección de subconjunto.\n",
    "\n",
    "**Respuesta:** Falso, el modelo con predictores (k+1) se obtiene seleccionando entre todos los modelos posibles con predcitores (k+1), por lo que no necesariamente contiene todos los predictores seleccionados para el modelo de variable k."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**2. Para las partes (a) a (c), indique cuál del i al iv es correcto. Justifica tu respuesta.**"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "<p>i). Más flexible y, por lo tanto, proporcionará una precisión de predicción mejorada cuando su aumento en el sesgo es menor que su disminución en diferencia.\n",
    "<p>ii). Más flexible y, por lo tanto, proporcionará una precisión de predicción mejorada cuando su aumento en la varianza es menor que su disminución en sesgo.\n",
    "<p>iii). Menos flexible y, por lo tanto, dará una precisión de predicción mejorada cuando su aumento en el sesgo es menor que su disminución en diferencia.\n",
    "<p>iv). Menos flexible y, por lo tanto, dará una precisión de predicción mejorada cuando su aumento en la varianza es menor que su disminución en sesgo."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "- *(a) El lasso, en relación con los mínimos cuadrados, es:*"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Respuesta:** El lasso es menos flexible y proporcionará una precisión de predicción mejorada cuando su aumento en el sesgo sea menor que su disminución en la varianza. (iii.)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "- *(b) Para la regresión de cresta en relación con los mínimos cuadrados.*"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Respuesta:** Al igual que el lasso, la regresión de cresta es menos flexible y proporcionará una precisión de predicción mejorada cuando su aumento en el sesgo sea menor que su disminución en la varianza. (iii.)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "- *(c) Para métodos no lineales relativos a mínimos cuadrados.*"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Respuesta:** Los métodos no lineales son más flexibles y proporcionarán una precisión de predicción mejorada cuando su aumento en la varianza sea menor que su disminución en el sesgo. (ii.)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**3. Suponga que estiamos los coeficientes de regresión en un modelo de regresión lineal minimizando (ecuación del libro) para un valor particular de s. Por partes (a) a (e), indica cuál de i. a través de v. es correcta. Justifica tu respuesta.**"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "- *(a) A medida qe aumentamos s desde 0, el RSS de captación:*\n",
    "\n",
    "i. Aumenta inicialmente y luego comienza a disminuir en forma de U invertida.\n",
    "\n",
    "ii. Disminuye inicialmente y uego comienza a amentar en forma de U.\n",
    "\n",
    "iii. Aumenta constantemente.\n",
    "\n",
    "iv. Disminuye constantemente.\n",
    "\n",
    "v. Permanece constante.\n",
    "\n",
    "**Respuesta:** Disminiye constantemente, a medida que aumenta s desde 0, todos los betas incrementan desde 0 hasta sus valores de minimos cuadrados estimados. El error de entrenamineto para 0 betas es el maximo y disminuye constantemente hasta ek minimo cuadrado RSS ordinario.\n",
    "\n",
    "- *(b) Repite (a) para el RSS de prueba*\n",
    "\n",
    "**Respuesta:** Disminuye inicialmente y luego comienza a aumentar en forma de U, cuando s=0, todas las betas son 0, el modelo es extremadamente simple y tienen un alto RSS de prueba. A medida que va aumentando s, betas tienen valores distintos de 0 y el modelo comienza a ajustarse bien a los datos de prueba, por lo que el RSS de prueba disminuye. Posteriormente, a medida que los beta se acercan a sus valores OLS completos, comienzan a ajustarse en exceso a los datos de entrenamiento, aumento el RSS de prueba.\n",
    "\n",
    "- *(c) Repite (a) para varianza*\n",
    "\n",
    "**Respuesta:** Aumenta constantemente, Cuando s=0, el modelo predice eficientemente, es constante y tiene una varianza muy pequeña. Conforme aumenta s, el modelo introduce mas betas y sus valores comienzan a aumentar. En este punto, los valores de las betas se convierten en predictores dependientes de los datos de entrenamiento y esto hace que incremente la varianza.\n",
    "\n",
    "- *(d) Repite (a) para sesgo (cuadrado)*\n",
    "\n",
    "**Respuesta:** Disminuye constantemente, cuando s=0, el modelo predice eficientemente una constante y por lo tanto la predicción esta lejos del valor real, el sesgo es grande. Con forme s aumenta, mas betas se vuelven distintos de cero y por lo tanto el modelo continua ajustando mejor lso datos de entrenamiento. Y así, el sesgo disminuye.\n",
    "\n",
    "- *(e) Repite (a) para el error irreducible*\n",
    "\n",
    "**Respuesta:** Permanece constante, el error irreducible es independiente del modelo."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**4. Supongamos que estimamos los coeficientes de regresión en un modelo de regresión lineal minimizando para un valor particular de λ. Para las partes (a) a (e), indique cuál del i al iv es correcto. Justifica tu respuesta.**"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "<p>i). Aumentar inicialmente, y luego eventualmente comenzar a disminuir en forma de U invertida.\n",
    "<p>ii). Disminuya inicialmente y luego comience a aumentar en forma de U.\n",
    "<p>iii). Aumentar constantemente.\n",
    "<p>iv). Disminuir constantemente.\n",
    "<p>v). Permanecer constante."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "   - *(a) A medida que aumentemos λ de 0, el RSS de entrenamiento:* "
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Respuesta:** Aumentar constantemente. A medida que aumentamos λ desde 0, estamos restringiendo los coeficientes βj cada vez más (los coeficientes se desviarán de sus estimaciones de mínimos cuadrados), por lo que el modelo se vuelve cada vez menos flexible, lo que provoca un aumento constante en el entrenamiento de RSS."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "   - *(b) Respondan (a) usando el test RSS.*"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Respuesta:** Disminuya inicialmente y luego comience a aumentar en forma de U. A medida que aumentamos λ desde 0, estamos restringiendo los coeficientes βj cada vez más (los coeficientes se desviarán de sus estimaciones de mínimos cuadrados), por lo que el modelo se vuelve cada vez menos flexible, lo que provoca al principio una disminución en la prueba RSS antes de aumentar de nuevo después de eso en forma de U típica.\n"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "   - *(c) Respondan (a) usando la varianza.*"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Respuesta:** Disminuir constantemente. A medida que aumentamos λ desde 0, estamos restringiendo los coeficientes βj más y más (los coeficientes se desviarán de sus estimaciones de mínimos cuadrados), por lo que el modelo se vuelve cada vez menos flexible, lo que provoca una disminución constante de la varianza.\n"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "   - *(d) Respondan (a) usando sesgo (al cuadrado).*"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Respuesta:** Aumentar constantemente. A medida que aumentamos λ desde 0, restringimos los coeficientes βj (los coeficientes se desviarán de sus estimaciones de mínimos cuadrados), por lo que el modelo se vuelve cada vez menos flexible, lo que provoca un aumento constante en el sesgo.\n"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "   - *(e) Respondan (a) usando el error irreducible.*"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Respuesta:** Permanecer constante. Por definición, el error irreducible es independiente del modelo y por lo tanto independiente del valor de λ."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**5. Es bien sabido que la regresión ridge tiende a dar valores de coeficientes similares a las variables correlacionadas,mientras que el lasso puede dar valores de coeficientes bastante diferentes a las variables correlacionadas. Ahora exploraremos esta propiedad en un entorno muy simple**\n",
    "\n",
    "**Suponga que n=2, p=2, x11 = x12, x21 = x22. Además, suponga que y1 + y2 = 0 y x12 + x22 = 0. Para que la estimación pora el intercepro en minimos cuadrados, regresión ridge, o modelo lasso es cero: Beta0gorrito = 0**"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "- *(a) Escriba el problema de optimización de regresión de crestas en esta configuración*\n",
    "\n",
    "**Rspuesta:** ![5a](http://localhost:8888/files/Documents/AUniversidad/UNAM/Sexto%20Semestre/Temas%20de%20compu/Tareas/Pr%C3%A1ctica%204/5a.jpeg?_xsrf=2%7Ca25add10%7Cdbbe189ee3c1030fdf2e0bddaf5bb1a2%7C1588615774)\n",
    "\n",
    "- *(b) Argumenta que en esta configuración, las estimaciones del coeficiente de ridge satisfacen B1gorrito = B2gorrito*\n",
    "\n",
    "**Rspuesta:** ![5b](http://localhost:8888/files/Documents/AUniversidad/UNAM/Sexto%20Semestre/Temas%20de%20compu/Tareas/Pr%C3%A1ctica%204/5b.jpeg?_xsrf=2%7Ca25add10%7Cdbbe189ee3c1030fdf2e0bddaf5bb1a2%7C1588615774)\n",
    "\n",
    "- *(c) Escriba el priblema de optimización de lazo en esta configuración*\n",
    "\n",
    "**Rspuesta:** ![5c](http://localhost:8888/files/Documents/AUniversidad/UNAM/Sexto%20Semestre/Temas%20de%20compu/Tareas/Pr%C3%A1ctica%204/5c.jpeg?_xsrf=2%7Ca25add10%7Cdbbe189ee3c1030fdf2e0bddaf5bb1a2%7C1588615774)\n",
    "\n",
    "- *(d) Argumenta que en este contexto, los coeficientes de lazo B1gorrito y B2gorrito no son unicos;enotras palabras, hay muchas posibles soluciones al problema de optimización en (c). Describe estas soluciones.*\n",
    "\n",
    "**Rspuesta:** ![5d](http://localhost:8888/files/Documents/AUniversidad/UNAM/Sexto%20Semestre/Temas%20de%20compu/Tareas/Pr%C3%A1ctica%204/5d.jpeg?_xsrf=2%7Ca25add10%7Cdbbe189ee3c1030fdf2e0bddaf5bb1a2%7C1588615774)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**6. Ahora exploraremos (6.12) y (6.13) más a fondo.**"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "   - *(a) Considere (6.12) con p = 1. Para alguna elección de y1 y λ > 0, trace (6.12) en función de β1. Su diagrama debe confirmar que (6.12) se resuelve con (6.14).* "
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "Para p = 1, (6.12) toma la forma (y − β) 2 + λβ2. Trazamos esta función para y = 2, λ = 2."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 1,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "image/png": "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",
      "text/plain": [
       "plot without title"
      ]
     },
     "metadata": {
      "image/png": {
       "height": 420,
       "width": 420
      },
      "text/plain": {
       "height": 420,
       "width": 420
      }
     },
     "output_type": "display_data"
    }
   ],
   "source": [
    "y = 2\n",
    "lambda = 2\n",
    "betas = seq(-10, 10, 0.1)\n",
    "func = (y - betas)^2 + lambda * betas^2\n",
    "plot(betas, func, pch = 20, xlab = \"beta\", ylab = \"Ridge optimization\")\n",
    "est.beta = y/(1 + lambda)\n",
    "est.func = (y - est.beta)^2 + lambda * est.beta^2\n",
    "points(est.beta, est.func, col = \"red\", pch = 4, lwd = 5, cex = est.beta)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "   - *(b) Considera (6.13) con p=1. Para alguna elección de y1 y lambda > 0, imprime (6.13) como un función de B1. Tu grafica debería confirmar que (6.13) se resuelve con (6.15).* "
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 2,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "image/png": "iVBORw0KGgoAAAANSUhEUgAAA0gAAANICAMAAADKOT/pAAAAM1BMVEUAAABNTU1oaGh8fHyM\njIyampqnp6eysrK9vb3Hx8fQ0NDZ2dnh4eHp6enw8PD/AAD///89ODILAAAACXBIWXMAABJ0\nAAASdAHeZh94AAAYyElEQVR4nO3d6UIaSRSA0WIRiQGG93/aEVCjibLeqq7lnB8TMjNyWeoL\nTdHRtAcelqa+AdADIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEA\nIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEA\nIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEA\nIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEA\nIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEA\nIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUGAAiElaMwdqzw+nAlGQCQhQQAhQQAhQQAh\nQQAhQQAhQQAhQQAhQQAhQQAhQQAhQQAhQQAhQQAhQQAhQQAhQQAhQQAhQYC2Qrrnb8ZDAU2F\ndN/3mID8Wgrp3u/WAtm1F5KSqFBLISmJajUVkoM7atVWSHshUacWQ1IS1RESBGgsJCVRJyFB\ngNZCst1AldoMSUlUpmhIv5+XxwyWq993jxASNSoY0m7+6eebLe4eoSQqVDCkVZr92hwvbV9m\naXXvCCFRoYIhzdLm4/Imze4eISTqUzCkL6v/fAqXQ1ISVWn1FUlIVKXse6SX7fHSQ++RlESF\nSm5/Lz7t2s13948QEtUp+znS6vg50mz5fP/nSMf/rCQq09yZDcf/LCQqU09I6bNr/t88NwPu\nMUFI61marx8b4SWJypQMabNMs/X++cFThI7/XUjUpWBIm+PqX6Wn3X67TGdfky6OUBJ1KRjS\n0+Gzo9Xpk9hdmj80QkjUpfgpQmn56Tf3jxASVSke0q/TMd0Dpwi9XZmSqEjRQ7un99MZdk+P\nnCJ0/D+ERE1K/sW+2cfKT+dfkK4ZoSRqUvRzpNV7PrOzr0dCojn1nNlw6wglUREhQYB2Q7ID\n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\nRK5CYII=",
      "text/plain": [
       "plot without title"
      ]
     },
     "metadata": {
      "image/png": {
       "height": 420,
       "width": 420
      },
      "text/plain": {
       "height": 420,
       "width": 420
      }
     },
     "output_type": "display_data"
    }
   ],
   "source": [
    "y = 2\n",
    "lambda = 2\n",
    "betas = seq(-3, 3, 0.01)\n",
    "func = (y - betas)^2 + lambda * abs(betas)\n",
    "plot(betas, func, pch = 20, xlab = \"beta\", ylab = \"Lasso\")\n",
    "est.beta = y - lambda/2\n",
    "est.func = (y - est.beta)^2 + lambda * abs(est.beta)\n",
    "points(est.beta, est.func, col = \"red\", pch = 4, lwd = 5, cex = est.beta)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**7. Ahora derivaremos la conexión bayesiana con el lazo y la regresión de cresta discutida en la Sección 6.2.2.**"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "   - *(a) Escriba la probabilidad de los datos.* "
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Rspuesta:** ![7a](http://localhost:8888/files/Documents/AUniversidad/UNAM/Sexto%20Semestre/Temas%20de%20compu/Tareas/Pr%C3%A1ctica%204/7a.jpeg?_xsrf=2%7Ca25add10%7Cdbbe189ee3c1030fdf2e0bddaf5bb1a2%7C1588615774)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "   - *(b) Escriba β en este ajuste.* "
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Rspuesta:** ![7b](http://localhost:8888/files/Documents/AUniversidad/UNAM/Sexto%20Semestre/Temas%20de%20compu/Tareas/Pr%C3%A1ctica%204/7b.jpeg?_xsrf=2%7Ca25add10%7Cdbbe189ee3c1030fdf2e0bddaf5bb1a2%7C1588615774)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "   - *(c) Argumenta que la estimación del lazo es el modo para β bajo esta distribución posterior.* "
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Rspuesta:** ![7c](http://localhost:8888/files/Documents/AUniversidad/UNAM/Sexto%20Semestre/Temas%20de%20compu/Tareas/Pr%C3%A1ctica%204/7c.jpeg?_xsrf=2%7Ca25add10%7Cdbbe189ee3c1030fdf2e0bddaf5bb1a2%7C1588615774)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "   - *(d) Ahora suponga lo siguiente para β: β1,. . . , βp son independientes y distribuido idénticamente de acuerdo con una distribución normal con media cero y varianza c. Escriba la parte posterior para β en esta configuración.* "
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Rspuesta:** ![7d](http://localhost:8888/files/Documents/AUniversidad/UNAM/Sexto%20Semestre/Temas%20de%20compu/Tareas/Pr%C3%A1ctica%204/7d.jpeg?_xsrf=2%7Ca25add10%7Cdbbe189ee3c1030fdf2e0bddaf5bb1a2%7C1588615774)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "   - *(e) Argumenta que la estimación de la regresión de la cresta es tanto el modo como la media de β bajo esta distribución posterior.*"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Rspuesta:** ![7e](http://localhost:8888/files/Documents/AUniversidad/UNAM/Sexto%20Semestre/Temas%20de%20compu/Tareas/Pr%C3%A1ctica%204/7e.jpeg?_xsrf=2%7Ca25add10%7Cdbbe189ee3c1030fdf2e0bddaf5bb1a2%7C1588615774)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**8. En este ejercicio, generaremos datos simulados y luego utilizaremos estos datos para realizar la mejor selección de subconjunto.**"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "   - *(a) Use la función rnorm () para generar un predictor X de longitud n = 100, así como un vector de ruido de longitud n = 100.*"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "*i. ¿Hay alguna relación entre el predictor y la respuesta?*"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 3,
   "metadata": {},
   "outputs": [],
   "source": [
    "set.seed(24432)\n",
    "X = rnorm(100)\n",
    "e = rnorm(100)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "   - *(b) Genere un vector de respuesta Y de longitud n = 100 de acuerdo con el modelo.*"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 4,
   "metadata": {},
   "outputs": [],
   "source": [
    "b0 = 4\n",
    "b1 = 0.5\n",
    "b2 = -3\n",
    "b3 = 1\n",
    "Y = b0 + b1 * X + b2 * X^2 + b3 * X^3 + e"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "   - *(c) Use la función regsubsets () para realizar la mejor selección de subconjunto para elegir el mejor modelo que contenga los predictores X, X2,. . ., X10. ¿Cuál es el mejor modelo obtenido según Cp, BIC y R2 ajustado? Mostrar algunas parcelas para proporcionar evidencia para su respuesta e informe los coeficientes del mejor modelo obtenido. Tenga en cuenta que deberá usar la función data.frame () para crear un único conjunto de datos que contenga tanto X como Y.*"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 5,
   "metadata": {},
   "outputs": [
    {
     "name": "stderr",
     "output_type": "stream",
     "text": [
      "Warning message:\n",
      "\"package 'leaps' was built under R version 3.6.3\"\n"
     ]
    },
    {
     "data": {
      "text/html": [
       "3"
      ],
      "text/latex": [
       "3"
      ],
      "text/markdown": [
       "3"
      ],
      "text/plain": [
       "[1] 3"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    }
   ],
   "source": [
    "library(leaps)\n",
    "data.full = data.frame(y = Y, x = X)\n",
    "mod.full = regsubsets(y ~ poly(x, 10, raw = T), data = data.full, nvmax = 10)\n",
    "mod.summary = summary(mod.full)\n",
    "\n",
    "# Se busca el mejor tamaño de modelo para Cp, BIC, adjr2\n",
    "which.min(mod.summary$cp)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 6,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "3"
      ],
      "text/latex": [
       "3"
      ],
      "text/markdown": [
       "3"
      ],
      "text/plain": [
       "[1] 3"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    }
   ],
   "source": [
    "which.min(mod.summary$bic)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 7,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "3"
      ],
      "text/latex": [
       "3"
      ],
      "text/markdown": [
       "3"
      ],
      "text/plain": [
       "[1] 3"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    }
   ],
   "source": [
    "which.max(mod.summary$adjr2)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 8,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "image/png": "iVBORw0KGgoAAAANSUhEUgAAA0gAAANICAMAAADKOT/pAAAACVBMVEUAAAD/AAD///9nGWQe\nAAAACXBIWXMAABJ0AAASdAHeZh94AAAbCUlEQVR4nO3diVbjSBJAURX//9EzDdjIm6wlUhkZ\nvvec7qIoS4ZIPYwllukLOGzq/QZABUKCAEKCAEKCAEKCAEKCAEKCAEKCAEKCAEKCAEKCAEKC\nAEKCAEKCAEKCAEKCAEKCAEKCAEKCAEKCAEKCAEKCAEKCAEKCAEKCAEKCAEKCAEKCAEKCAEKC\nAEKCAEKCAEKCAEKCAEKCAEKCAEKCAEKCAEKCAEKCAEKCAEKCAEKCAEKCAEKCAEKCAEKCAEKC\nAEKCAEKCAEKCAEKCAEKCAEKCAEKCAEKCAEKCAEKCAEKCAEKCAEKCAEKCAEKCAEKCAEKCAEKC\nAEKCAEKCAEKCAEKCAEKCAEKCAEKCAEKCAEKCAEKCAEKCAEKCAEKCAEKCAPEhTawUPnprFG79\nSOMXKXyPRfUMqd9dj0VIAxBSfkIagJDyE9IAhJSfkAYgpPyENIB2g3p7yskarSSkATQb1PTw\nwml3XY2QBtBqUNPTF0+563KShGS9luQIyRotEdIAhJSfkAaQ4zmSNVoipAHkOGtnjZYkCckq\nLUlyHckaLRDSAISUn5AG0PZkw+oLstZogZAG0DSkv/+9u2trtEBIA2gZ0vTsLp5/v5o1WiCk\nAZwe0vO7tkYLhDQAIeV3fkgvvs3dKr3WLKT/L8G0fA/WaKUsj0gWaUHD2fx8OFt31s4aLRDS\nAJJcR7JGC4Q0ACHlJ6QBNJ7N0u6t0UpCGoCQ8hPSAISUX5qQrNJrWUKyRq8JaQBCyk9IA8hy\n1s4avSakAQgpPyENQEj5CWkAQspPSANIE5JFeilPSBbpJSHlJ6QBCCk/IQ1ASPk1DGnrrwyx\nSK8IKb92IU0PL7zZo0V6RUj5NQtpevri0h4t0itCyk9IA8gTkkV6JVFIFukVIeWX6DmSRXpF\nSPklOmtnkV4RUn6JriNZpFfaDcYHuyhCGkCzwfj0O4xP7QbQajBOCMVxsmEAiUKySC9kOv1t\nkV4QUn5CGkCi50jW6AUhDSDRWTtr9EKm50gW6YVE15Gs0QuZztpZpBeElF+m60gW6QWf2uV3\nfkgvfmNf5F1Uk+lkg0V6LtWndhbpuUynv63Rc6lONlik54SUX6rT3xbpOSHlJ6QBeI6Un5AG\n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\nwt1Hu8drFPPtb65NzF682dllgS6vSneNIjVr9Pf2AccICQIICQIICQIICQIICQIICQIICQII\nCQIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQII\nCQIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQII\nCQIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQII\nCQIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQII\nCQIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQII\nCQIICQIICQIICQIICQIICQIICQIICQLEhzSxUvjo6adBSOF7LMqgKhFSNwZViZC6MahKsob0\n7/9CdpSXkCpJGtK/f/VLElIlOUP69+8DShJSJSlD+vfvE0oSUiVC6kZIlSQMaZr+Qup9zXSF\nfoMikQwhPRyZQz0i7e5OSJX0DOn1x/SBOtpPSJV0Den1P31AR0IqJWlILsgylqwhfYAPf/eL\n6RjSpx9In/7+1yKkbj79/a9FSN18+vtfi5C6+fT3vxYhdfPp738tQurm09//Wjav5tsvMRPS\nSp/+/teydTWny/9ebrh2jx9/HH38AErZuJrT3x+vthTSSh8/gFKE1M3HD6AUIXXz8QMoZf9z\nJCEd9PEDKGXXWbvF7YS00scPoJR+15E+/jj6+AGU0i0kh5EJVCKkbkygkqgfgrP5x+o4jEyg\nEo9I3ZhAJULqxgQqEVI3JlBJt6/+dhiZQCW7vrJhccN1e3QUGUEp+77WbmlLIa1kBJUIqRsj\nqERI3RhBJZ4jdWMElfQ6a+coMoJSel1HchQZQSmdQnIQmUEtQurGDCoRUjdmUImQujGDSoTU\njRlUIqRuzKASIXVjBpX0Cckx9GUItQipG0OoREjdGEIlQurGECoRUjeGUImQujGESoTUjSFU\n0iUkh9B/TKESIXVjCpXs+A7Z7/8d+g5Zh9B/TKGSHT+zYfre6MjPbHAI/ccUKtnzU4SmxS2F\ntJIpVCKkbkyhEiF1YwqV9HiO5Aj6ZgyV9Dhr5wj6ZgyV9LiO5Aj6ZgyVCKkbY6hESN0YQyX7\n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\n",
      "text/plain": [
       "plot without title"
      ]
     },
     "metadata": {
      "image/png": {
       "height": 420,
       "width": 420
      },
      "text/plain": {
       "height": 420,
       "width": 420
      }
     },
     "output_type": "display_data"
    }
   ],
   "source": [
    "reg.summary = summary(mod.full)\n",
    "par(mfrow = c(2, 2))\n",
    "plot(reg.summary$cp, xlab = \"Number of variables\", ylab = \"C_p\", type = \"l\")\n",
    "points(which.min(reg.summary$cp), reg.summary$cp[which.min(reg.summary$cp)], col = \"red\", cex = 2, pch = 20)\n",
    "plot(reg.summary$bic, xlab = \"Number of variables\", ylab = \"BIC\", type = \"l\")\n",
    "points(which.min(reg.summary$bic), reg.summary$bic[which.min(reg.summary$bic)], col = \"red\", cex = 2, pch = 20)\n",
    "plot(reg.summary$adjr2, xlab = \"Number of variables\", ylab = \"R^2 ajustado\", type = \"l\")\n",
    "points(which.max(reg.summary$adjr2), reg.summary$adjr2[which.max(reg.summary$adjr2)], col = \"red\", cex = 2, pch = 20)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "Encontramos que con los criterios Cp, BIC y R2 ajustado, se seleccionan 3, 3 y 3 modelos variables respectivamente."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 9,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<style>\n",
       ".dl-inline {width: auto; margin:0; padding: 0}\n",
       ".dl-inline>dt, .dl-inline>dd {float: none; width: auto; display: inline-block}\n",
       ".dl-inline>dt::after {content: \":\\0020\"; padding-right: .5ex}\n",
       ".dl-inline>dt:not(:first-of-type) {padding-left: .5ex}\n",
       "</style><dl class=dl-inline><dt>(Intercept)</dt><dd>3.67651890177551</dd><dt>poly(x, 10, raw = T)1</dt><dd>0.603530924793066</dd><dt>poly(x, 10, raw = T)2</dt><dd>-2.91348109370209</dd><dt>poly(x, 10, raw = T)3</dt><dd>0.939633141025814</dd></dl>\n"
      ],
      "text/latex": [
       "\\begin{description*}\n",
       "\\item[(Intercept)] 3.67651890177551\n",
       "\\item[poly(x, 10, raw = T)1] 0.603530924793066\n",
       "\\item[poly(x, 10, raw = T)2] -2.91348109370209\n",
       "\\item[poly(x, 10, raw = T)3] 0.939633141025814\n",
       "\\end{description*}\n"
      ],
      "text/markdown": [
       "(Intercept)\n",
       ":   3.67651890177551poly(x, 10, raw = T)1\n",
       ":   0.603530924793066poly(x, 10, raw = T)2\n",
       ":   -2.91348109370209poly(x, 10, raw = T)3\n",
       ":   0.939633141025814\n",
       "\n"
      ],
      "text/plain": [
       "          (Intercept) poly(x, 10, raw = T)1 poly(x, 10, raw = T)2 \n",
       "            3.6765189             0.6035309            -2.9134811 \n",
       "poly(x, 10, raw = T)3 \n",
       "            0.9396331 "
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    }
   ],
   "source": [
    "coefficients(mod.full, id = 3)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "   - *(d) Repita (c), utilizando la selección progresiva hacia adelante y también utilizando la selección progresiva hacia atrás. ¿Cómo se compara tu respuesta con la resultados en (c)?*"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 10,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "3"
      ],
      "text/latex": [
       "3"
      ],
      "text/markdown": [
       "3"
      ],
      "text/plain": [
       "[1] 3"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    }
   ],
   "source": [
    "mod.fwd = regsubsets(y ~ poly(x, 10, raw = T), data = data.full, nvmax = 10, \n",
    "    method = \"forward\")\n",
    "mod.bwd = regsubsets(y ~ poly(x, 10, raw = T), data = data.full, nvmax = 10, \n",
    "    method = \"backward\")\n",
    "fwd.summary = summary(mod.fwd)\n",
    "bwd.summary = summary(mod.bwd)\n",
    "which.min(fwd.summary$cp)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 11,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "5"
      ],
      "text/latex": [
       "5"
      ],
      "text/markdown": [
       "5"
      ],
      "text/plain": [
       "[1] 5"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    }
   ],
   "source": [
    "which.min(bwd.summary$cp)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 12,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "3"
      ],
      "text/latex": [
       "3"
      ],
      "text/markdown": [
       "3"
      ],
      "text/plain": [
       "[1] 3"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    }
   ],
   "source": [
    "which.min(fwd.summary$bic)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 13,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "5"
      ],
      "text/latex": [
       "5"
      ],
      "text/markdown": [
       "5"
      ],
      "text/plain": [
       "[1] 5"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    }
   ],
   "source": [
    "which.min(bwd.summary$bic)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 14,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "3"
      ],
      "text/latex": [
       "3"
      ],
      "text/markdown": [
       "3"
      ],
      "text/plain": [
       "[1] 3"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    }
   ],
   "source": [
    "which.max(fwd.summary$adjr2)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 15,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "5"
      ],
      "text/latex": [
       "5"
      ],
      "text/markdown": [
       "5"
      ],
      "text/plain": [
       "[1] 5"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    }
   ],
   "source": [
    "which.max(bwd.summary$adjr2)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 16,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "image/png": "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\n",
      "text/plain": [
       "plot without title"
      ]
     },
     "metadata": {
      "image/png": {
       "height": 420,
       "width": 420
      },
      "text/plain": {
       "height": 420,
       "width": 420
      }
     },
     "output_type": "display_data"
    }
   ],
   "source": [
    "# Graficar las estadísticas\n",
    "par(mfrow = c(3, 2))\n",
    "plot(fwd.summary$cp, xlab = \"Subset Size\", ylab = \"Forward Cp\", pch = 20, type = \"l\")\n",
    "points(3, fwd.summary$cp[3], pch = 4, col = \"red\", lwd = 7)\n",
    "plot(bwd.summary$cp, xlab = \"Subset Size\", ylab = \"Backward Cp\", pch = 20, type = \"l\")\n",
    "points(5, bwd.summary$cp[3], pch = 4, col = \"red\", lwd = 7)\n",
    "plot(fwd.summary$bic, xlab = \"Subset Size\", ylab = \"Forward BIC\", pch = 20, \n",
    "    type = \"l\")\n",
    "points(3, fwd.summary$bic[3], pch = 4, col = \"red\", lwd = 7)\n",
    "plot(bwd.summary$bic, xlab = \"Subset Size\", ylab = \"Backward BIC\", pch = 20, \n",
    "    type = \"l\")\n",
    "points(5, bwd.summary$bic[3], pch = 4, col = \"red\", lwd = 7)\n",
    "plot(fwd.summary$adjr2, xlab = \"Subset Size\", ylab = \"Forward Adjusted R2\", \n",
    "    pch = 20, type = \"l\")\n",
    "points(3, fwd.summary$adjr2[3], pch = 4, col = \"red\", lwd = 7)\n",
    "plot(bwd.summary$adjr2, xlab = \"Subset Size\", ylab = \"Backward Adjusted R2\", \n",
    "    pch = 20, type = \"l\")\n",
    "points(5, bwd.summary$adjr2[4], pch = 4, col = \"red\", lwd = 7)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "Vemos que las estadísticas fwd seleccionan 3 modelos variables mientras que los bwd seleccionan 5. Ahora los coeficientes:"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 17,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<style>\n",
       ".dl-inline {width: auto; margin:0; padding: 0}\n",
       ".dl-inline>dt, .dl-inline>dd {float: none; width: auto; display: inline-block}\n",
       ".dl-inline>dt::after {content: \":\\0020\"; padding-right: .5ex}\n",
       ".dl-inline>dt:not(:first-of-type) {padding-left: .5ex}\n",
       "</style><dl class=dl-inline><dt>(Intercept)</dt><dd>3.67651890177551</dd><dt>poly(x, 10, raw = T)1</dt><dd>0.603530924793066</dd><dt>poly(x, 10, raw = T)2</dt><dd>-2.91348109370209</dd><dt>poly(x, 10, raw = T)3</dt><dd>0.939633141025815</dd></dl>\n"
      ],
      "text/latex": [
       "\\begin{description*}\n",
       "\\item[(Intercept)] 3.67651890177551\n",
       "\\item[poly(x, 10, raw = T)1] 0.603530924793066\n",
       "\\item[poly(x, 10, raw = T)2] -2.91348109370209\n",
       "\\item[poly(x, 10, raw = T)3] 0.939633141025815\n",
       "\\end{description*}\n"
      ],
      "text/markdown": [
       "(Intercept)\n",
       ":   3.67651890177551poly(x, 10, raw = T)1\n",
       ":   0.603530924793066poly(x, 10, raw = T)2\n",
       ":   -2.91348109370209poly(x, 10, raw = T)3\n",
       ":   0.939633141025815\n",
       "\n"
      ],
      "text/plain": [
       "          (Intercept) poly(x, 10, raw = T)1 poly(x, 10, raw = T)2 \n",
       "            3.6765189             0.6035309            -2.9134811 \n",
       "poly(x, 10, raw = T)3 \n",
       "            0.9396331 "
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    }
   ],
   "source": [
    "coefficients(mod.fwd, id = 3)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 18,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<style>\n",
       ".dl-inline {width: auto; margin:0; padding: 0}\n",
       ".dl-inline>dt, .dl-inline>dd {float: none; width: auto; display: inline-block}\n",
       ".dl-inline>dt::after {content: \":\\0020\"; padding-right: .5ex}\n",
       ".dl-inline>dt:not(:first-of-type) {padding-left: .5ex}\n",
       "</style><dl class=dl-inline><dt>(Intercept)</dt><dd>3.72532597615409</dd><dt>poly(x, 10, raw = T)1</dt><dd>0.964004819406533</dd><dt>poly(x, 10, raw = T)2</dt><dd>-2.98627061584675</dd><dt>poly(x, 10, raw = T)5</dt><dd>0.650468139100316</dd><dt>poly(x, 10, raw = T)7</dt><dd>-0.153833572948286</dd><dt>poly(x, 10, raw = T)9</dt><dd>0.0109689187770399</dd></dl>\n"
      ],
      "text/latex": [
       "\\begin{description*}\n",
       "\\item[(Intercept)] 3.72532597615409\n",
       "\\item[poly(x, 10, raw = T)1] 0.964004819406533\n",
       "\\item[poly(x, 10, raw = T)2] -2.98627061584675\n",
       "\\item[poly(x, 10, raw = T)5] 0.650468139100316\n",
       "\\item[poly(x, 10, raw = T)7] -0.153833572948286\n",
       "\\item[poly(x, 10, raw = T)9] 0.0109689187770399\n",
       "\\end{description*}\n"
      ],
      "text/markdown": [
       "(Intercept)\n",
       ":   3.72532597615409poly(x, 10, raw = T)1\n",
       ":   0.964004819406533poly(x, 10, raw = T)2\n",
       ":   -2.98627061584675poly(x, 10, raw = T)5\n",
       ":   0.650468139100316poly(x, 10, raw = T)7\n",
       ":   -0.153833572948286poly(x, 10, raw = T)9\n",
       ":   0.0109689187770399\n",
       "\n"
      ],
      "text/plain": [
       "          (Intercept) poly(x, 10, raw = T)1 poly(x, 10, raw = T)2 \n",
       "           3.72532598            0.96400482           -2.98627062 \n",
       "poly(x, 10, raw = T)5 poly(x, 10, raw = T)7 poly(x, 10, raw = T)9 \n",
       "           0.65046814           -0.15383357            0.01096892 "
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    }
   ],
   "source": [
    "coefficients(mod.bwd, id = 5)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "En fwd se escoje x1, x2 y x3 mientras que en bwd se escoje x1, x2 y hasta x5 y x7."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "   - *(e) Ahora ajuste un modelo de lazo a los datos simulados, nuevamente usando X, X2,. . . , X10 como predictores. Utilice la validación cruzada para seleccionar el valor óptimo de λ. Cree gráficos del error de validación cruzada en función de λ. Informe los coeficientes estimados resultantes.*"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 19,
   "metadata": {},
   "outputs": [
    {
     "name": "stderr",
     "output_type": "stream",
     "text": [
      "Warning message:\n",
      "\"package 'glmnet' was built under R version 3.6.3\"\n",
      "Loading required package: Matrix\n",
      "\n",
      "Loaded glmnet 3.0-2\n",
      "\n",
      "\n"
     ]
    },
    {
     "data": {
      "text/html": [
       "0.0418952412812953"
      ],
      "text/latex": [
       "0.0418952412812953"
      ],
      "text/markdown": [
       "0.0418952412812953"
      ],
      "text/plain": [
       "[1] 0.04189524"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    }
   ],
   "source": [
    "library(glmnet)\n",
    "xmat = model.matrix(y ~ poly(x, 10, raw = T), data = data.full)[, -1]\n",
    "mod.lasso = cv.glmnet(xmat, Y, alpha = 1)\n",
    "best.lambda = mod.lasso$lambda.min\n",
    "best.lambda"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 20,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "image/png": "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\nHPwP6162yeFL2AsAAAAASUVORK5CYII=",
      "text/plain": [
       "plot without title"
      ]
     },
     "metadata": {
      "image/png": {
       "height": 420,
       "width": 420
      },
      "text/plain": {
       "height": 420,
       "width": 420
      }
     },
     "output_type": "display_data"
    }
   ],
   "source": [
    "plot(mod.lasso)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 21,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "11 x 1 sparse Matrix of class \"dgCMatrix\"\n",
       "                                1\n",
       "(Intercept)             3.6376371\n",
       "poly(x, 10, raw = T)1   0.5997765\n",
       "poly(x, 10, raw = T)2  -2.8673840\n",
       "poly(x, 10, raw = T)3   0.9224362\n",
       "poly(x, 10, raw = T)4   .        \n",
       "poly(x, 10, raw = T)5   .        \n",
       "poly(x, 10, raw = T)6   .        \n",
       "poly(x, 10, raw = T)7   .        \n",
       "poly(x, 10, raw = T)8   .        \n",
       "poly(x, 10, raw = T)9   .        \n",
       "poly(x, 10, raw = T)10  .        "
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    }
   ],
   "source": [
    "# Se ajusta el modelo usando la mejor almbda\n",
    "best.model = glmnet(xmat, Y, alpha = 1)\n",
    "predict(best.model, s = best.lambda, type = \"coefficients\")"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "Lasso al igual escoje x1, x2 y x3."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "   - *(f) Ajuste un modelo PLS en el conjunto de entrenamiento, con M elegida por validación cruzada. Informe el error de prueba obtenido, junto con el valor de M seleccionado por validación cruzada.*"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 22,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "2"
      ],
      "text/latex": [
       "2"
      ],
      "text/markdown": [
       "2"
      ],
      "text/plain": [
       "[1] 2"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    }
   ],
   "source": [
    "#Se crea una nueva beta con valor constante.\n",
    "b9 = 9\n",
    "Y = b0 + b9 * X^7 + e\n",
    "# Predicción con regsubsets\n",
    "data.full = data.frame(y = Y, x = X)\n",
    "mod.full = regsubsets(y ~ poly(x, 10, raw = T), data = data.full, nvmax = 10)\n",
    "mod.summary = summary(mod.full)\n",
    "\n",
    "# Find the model size for best cp, BIC and adjr2\n",
    "which.min(mod.summary$cp)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 23,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "1"
      ],
      "text/latex": [
       "1"
      ],
      "text/markdown": [
       "1"
      ],
      "text/plain": [
       "[1] 1"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    }
   ],
   "source": [
    "which.min(mod.summary$bic)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 24,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "2"
      ],
      "text/latex": [
       "2"
      ],
      "text/markdown": [
       "2"
      ],
      "text/plain": [
       "[1] 2"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    }
   ],
   "source": [
    "which.max(mod.summary$adjr2)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 25,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<style>\n",
       ".dl-inline {width: auto; margin:0; padding: 0}\n",
       ".dl-inline>dt, .dl-inline>dd {float: none; width: auto; display: inline-block}\n",
       ".dl-inline>dt::after {content: \":\\0020\"; padding-right: .5ex}\n",
       ".dl-inline>dt:not(:first-of-type) {padding-left: .5ex}\n",
       "</style><dl class=dl-inline><dt>(Intercept)</dt><dd>3.75248515372162</dd><dt>poly(x, 10, raw = T)7</dt><dd>8.99965768970608</dd></dl>\n"
      ],
      "text/latex": [
       "\\begin{description*}\n",
       "\\item[(Intercept)] 3.75248515372162\n",
       "\\item[poly(x, 10, raw = T)7] 8.99965768970608\n",
       "\\end{description*}\n"
      ],
      "text/markdown": [
       "(Intercept)\n",
       ":   3.75248515372162poly(x, 10, raw = T)7\n",
       ":   8.99965768970608\n",
       "\n"
      ],
      "text/plain": [
       "          (Intercept) poly(x, 10, raw = T)7 \n",
       "             3.752485              8.999658 "
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    }
   ],
   "source": [
    "coefficients(mod.full, id = 1)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 26,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<style>\n",
       ".dl-inline {width: auto; margin:0; padding: 0}\n",
       ".dl-inline>dt, .dl-inline>dd {float: none; width: auto; display: inline-block}\n",
       ".dl-inline>dt::after {content: \":\\0020\"; padding-right: .5ex}\n",
       ".dl-inline>dt:not(:first-of-type) {padding-left: .5ex}\n",
       "</style><dl class=dl-inline><dt>(Intercept)</dt><dd>3.72971045122486</dd><dt>poly(x, 10, raw = T)7</dt><dd>8.9968825500971</dd><dt>poly(x, 10, raw = T)10</dt><dd>0.000139340422208256</dd></dl>\n"
      ],
      "text/latex": [
       "\\begin{description*}\n",
       "\\item[(Intercept)] 3.72971045122486\n",
       "\\item[poly(x, 10, raw = T)7] 8.9968825500971\n",
       "\\item[poly(x, 10, raw = T)10] 0.000139340422208256\n",
       "\\end{description*}\n"
      ],
      "text/markdown": [
       "(Intercept)\n",
       ":   3.72971045122486poly(x, 10, raw = T)7\n",
       ":   8.9968825500971poly(x, 10, raw = T)10\n",
       ":   0.000139340422208256\n",
       "\n"
      ],
      "text/plain": [
       "           (Intercept)  poly(x, 10, raw = T)7 poly(x, 10, raw = T)10 \n",
       "          3.7297104512           8.9968825501           0.0001393404 "
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    }
   ],
   "source": [
    "coefficients(mod.full, id = 2)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "Se elige el modelo de 1 variable ya que es más preciso con coeficientes coincidentes y porque el otro elecciona variables adicionales."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 27,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "36.8880593314387"
      ],
      "text/latex": [
       "36.8880593314387"
      ],
      "text/markdown": [
       "36.8880593314387"
      ],
      "text/plain": [
       "[1] 36.88806"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    }
   ],
   "source": [
    "xmat = model.matrix(y ~ poly(x, 10, raw = T), data = data.full)[, -1]\n",
    "mod.lasso = cv.glmnet(xmat, Y, alpha = 1)\n",
    "best.lambda = mod.lasso$lambda.min\n",
    "best.lambda"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 28,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "11 x 1 sparse Matrix of class \"dgCMatrix\"\n",
       "                              1\n",
       "(Intercept)            6.539139\n",
       "poly(x, 10, raw = T)1  .       \n",
       "poly(x, 10, raw = T)2  .       \n",
       "poly(x, 10, raw = T)3  .       \n",
       "poly(x, 10, raw = T)4  .       \n",
       "poly(x, 10, raw = T)5  .       \n",
       "poly(x, 10, raw = T)6  .       \n",
       "poly(x, 10, raw = T)7  8.737313\n",
       "poly(x, 10, raw = T)8  .       \n",
       "poly(x, 10, raw = T)9  .       \n",
       "poly(x, 10, raw = T)10 .       "
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    }
   ],
   "source": [
    "best.model = glmnet(xmat, Y, alpha = 1)\n",
    "predict(best.model, s = best.lambda, type = \"coefficients\")"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "Lasso igual escoge el de una variable aunque el intercept varía entre uno y otro."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": []
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": []
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**9. En este ejercicio, vamos a predecir el numero de aplicaciones recibidas usando las otras variables con los datos de college**\n",
    "\n",
    "- *(a) Divida el conjunto de datos en un conjunto de entrenamiento y un ocnjunto de prueba*"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 29,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "0"
      ],
      "text/latex": [
       "0"
      ],
      "text/markdown": [
       "0"
      ],
      "text/plain": [
       "[1] 0"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    }
   ],
   "source": [
    "suppressMessages(library('ISLR'))\n",
    "suppressMessages(library('glmnet'))\n",
    "set.seed(15)\n",
    "sum(is.na(College))"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 30,
   "metadata": {},
   "outputs": [],
   "source": [
    "data(College)\n",
    "entrenamiento.size = dim(College)[1] / 2\n",
    "entrenamiento = sample(1:dim(College)[1], entrenamiento.size)\n",
    "prueba = -entrenamiento\n",
    "College.entrenamiento = College[entrenamiento, ]\n",
    "College.prueba= College[prueba, ]"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "- *(b) Ajuste un modelo lineal usando minimos cuadrados en el conjunto de entrenamiento e informe el error de prueba obtenido*"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 31,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "1404393.94893391"
      ],
      "text/latex": [
       "1404393.94893391"
      ],
      "text/markdown": [
       "1404393.94893391"
      ],
      "text/plain": [
       "[1] 1404394"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    }
   ],
   "source": [
    "fit.lm = lm(Apps ~ ., data = College.entrenamiento)\n",
    "pred.lm = predict(fit.lm, College.prueba)\n",
    "mean((pred.lm - College.prueba$Apps)^2)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "- *(c) Ajuste un modelo de regresión de ridge en el set de entrenamiento, con el lamba elegido de validación cruzada. Reporte el error de prueba obtenido*"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 32,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "0.01"
      ],
      "text/latex": [
       "0.01"
      ],
      "text/markdown": [
       "0.01"
      ],
      "text/plain": [
       "[1] 0.01"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    }
   ],
   "source": [
    "entrenamiento.mat = model.matrix(Apps~., data=College.entrenamiento)\n",
    "prueba.mat = model.matrix(Apps~., data=College.prueba)\n",
    "grid = 10 ^ seq(4, -2, length=100)\n",
    "cv.ridge = cv.glmnet(entrenamiento.mat, College.entrenamiento$Apps, alpha=0, lambda=grid, thresh=1e-12)\n",
    "bestlam.ridge = cv.ridge$lambda.min\n",
    "bestlam.ridge\n"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 33,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "1404355.90601873"
      ],
      "text/latex": [
       "1404355.90601873"
      ],
      "text/markdown": [
       "1404355.90601873"
      ],
      "text/plain": [
       "[1] 1404356"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    }
   ],
   "source": [
    "pred.ridge = predict(cv.ridge, s = bestlam.ridge, newx = prueba.mat)\n",
    "mean((pred.ridge - College.prueba$Apps)^2)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "- *(d) Ajuste en modelo de lasso enel set de entrenamiento, con la lamda elegida por validación cruzada. Reporte el error de prueba obtenido, junto con el número de estimaciones de coeficientes distintos de cero*"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 34,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "0.01"
      ],
      "text/latex": [
       "0.01"
      ],
      "text/markdown": [
       "0.01"
      ],
      "text/plain": [
       "[1] 0.01"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    }
   ],
   "source": [
    "fit.lasso = glmnet(entrenamiento.mat, College.entrenamiento$Apps, alpha = 1, lambda = grid, thresh = 1e-12)\n",
    "cv.lasso = cv.glmnet(entrenamiento.mat, College.entrenamiento$Apps, alpha = 1, lambda = grid, thresh = 1e-12)\n",
    "bestlam.lasso = cv.lasso$lambda.min\n",
    "bestlam.lasso"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 35,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "1404334.94027117"
      ],
      "text/latex": [
       "1404334.94027117"
      ],
      "text/markdown": [
       "1404334.94027117"
      ],
      "text/plain": [
       "[1] 1404335"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    }
   ],
   "source": [
    "pred.lasso = predict(fit.lasso, s = bestlam.lasso, newx = prueba.mat)\n",
    "mean((pred.lasso - College.prueba$Apps)^2)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 36,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "19 x 1 sparse Matrix of class \"dgCMatrix\"\n",
       "                        1\n",
       "(Intercept) -6.401409e+02\n",
       "(Intercept)  .           \n",
       "PrivateYes  -3.253039e+02\n",
       "Accept       1.830936e+00\n",
       "Enroll      -1.583955e+00\n",
       "Top10perc    5.689236e+01\n",
       "Top25perc   -2.331336e+01\n",
       "F.Undergrad  1.216688e-01\n",
       "P.Undergrad  4.786625e-03\n",
       "Outstate    -8.001898e-02\n",
       "Room.Board   9.720231e-02\n",
       "Books        3.068859e-01\n",
       "Personal     5.275504e-02\n",
       "PhD         -9.044248e+00\n",
       "Terminal    -1.392696e-01\n",
       "S.F.Ratio    2.030418e+01\n",
       "perc.alumni  1.718712e+00\n",
       "Expend       5.967794e-02\n",
       "Grad.Rate    9.704188e+00"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    }
   ],
   "source": [
    "predict(fit.lasso, s = bestlam.lasso, type = \"coefficients\")"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "- *(e) Ajuste un modelo de PCR en el set de entrenamiento, con la M elegida por validación cruzada. Reporte el error de prueba obtenido, junto con el valor de la M seleccionada por validación cruzada*"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 37,
   "metadata": {},
   "outputs": [
    {
     "name": "stderr",
     "output_type": "stream",
     "text": [
      "Installing package into 'C:/Users/LuisEnrique/Documents/R/win-library/3.6'\n",
      "(as 'lib' is unspecified)\n",
      "\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "package 'pls' successfully unpacked and MD5 sums checked\n",
      "\n",
      "The downloaded binary packages are in\n",
      "\tC:\\Users\\LuisEnrique\\AppData\\Local\\Temp\\RtmpEFiwhc\\downloaded_packages\n"
     ]
    }
   ],
   "source": [
    "install.packages(\"pls\")"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 38,
   "metadata": {},
   "outputs": [
    {
     "name": "stderr",
     "output_type": "stream",
     "text": [
      "Warning message:\n",
      "\"package 'pls' was built under R version 3.6.3\"\n"
     ]
    }
   ],
   "source": [
    "suppressMessages(library('pls'))"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 39,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "image/png": "iVBORw0KGgoAAAANSUhEUgAAA0gAAANICAMAAADKOT/pAAAAM1BMVEUAAABNTU1oaGh8fHyM\njIyampqnp6eysrK9vb3Hx8fQ0NDZ2dnh4eHp6enw8PD/AAD///89ODILAAAACXBIWXMAABJ0\nAAASdAHeZh94AAAcSUlEQVR4nO3diXbavBaAURnMEAKE93/aYkMSMlGGI3nae63bJmmKdSnf\nb0t2cDoAT0tdDwDGQEgQQEgQQEgQQEgQQEgQQEgQQEgQQEgQQEgQQEgQQEgQQEgQQEgQQEgQ\nQEgQQEgQQEgQQEgQQEgQQEgQQEgQQEgQQEgQQEgQQEgQQEgQQEgQQEgQQEgQQEgQQEgQQEgQ\nQEgQQEgQQEgQQEgQQEgQQEgQQEgQQEgQQEj9t0wpLbseBNcJqf9So+tBcJ1/oN57aUN66XoY\nXCWk3psfD+xSmnc9DK4SUt/tUqoOs5R2p0+bo7z18dPF7rdP96tjdqm2+ypOSH133ButDquP\n5Yamk/ZYr9r9/HRXpRP7r9KE1HfHNvaHfbNbaqUPs5+fLtq51P64V1p3OOJJElLPbU67l+Nu\nZ9N+3ux8Xo9frk5f+PppOh0B7s+VUY6Qeu5c0LGnuv38fQHv+IXFj0+bI7vFprOxTpmQ+u3j\nmK49wjucVhcOpw9mPz5dnY7ytFSekPpt/TkJOs17LspJPz9dnr+12nUz3OkSUr/NLkJ6X11o\n90yfIV1+eti/zC3bdUFIvfaaLr0e2mDaPdN50vTt09Zm4ZKi4jzhvbb8vDZofTqVdL5cqFmm\nW//4dPYxkao6G/JECanXPo7c2mWH87Hc+zzo8OPTZq18d7g4fUspQuqzl9Ma90nd7ntSe+Xd\n5ZUNl5++LzaYIpUmpD6bv5+GbZxOzTb7pZdZqpafawwXn57mR3PXNRQnpIH5to5gWaEn/DMM\njJD6yT/DwAipn/wzDIyQ+sk/w8AIqZ/8M0AAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEA\nIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEAIUEA\nIUEAIUEAIUEAIUEAIUEAIUGAAiElGJgHXuXx4XSwCYgkJAggJAggJAggJAggJAggJAggJAgg\nJAggJAggJAggJAggJAggJAggJAggJAggJAggJAggJAggJAggJAggJAgwsJDe3h553yPIbWAh\nNSkdW0qCol8GF9K7j6Dyjwb+a7AhvRMUfTD4kN4Jii6NJqR3b6ZPdKBgSKl6zb2JmL8OdysZ\nUkr1Pu8mzt6e++twt6Ihbaq0vCklITEwRUM67OuUFpt8mzgTEqWVDelw2NbNEd56e33H9Owc\nSUkUVjqkY0rL6r93OHt2tUBIFFY+pKPtup5lDcmyHYV1ElK2TUT9fbiTkCDA6K5saJkjUZiQ\nIEDRkF5XdbtgVy//c7GQkBiYgiHtZ+nTPMsm3gmJwgqGtEzVy7b9aNdcK5RjE++ERGEFQ6rS\n9uPjbapybCLq78Odulr+zntlg5IobJx7JCFRWNk50mbXfpR9jmSSRGEll7/nF6t2s6uXfwuJ\ngSl7HmnZnkeq6lXm80hCorBxXtkgJAoTEgQoH9ItF4FbtWNghAQBhAQBRhqSORJllQ3p8zxS\ntk2ceAtwyhISBBjpoZ1jO8oSEgQYa0gO7ShKSBBgpJcICYmyxhqSORJFFQ9pUzfHdvUu4yYa\nQqKo0iHNTyeRUvWjpHTpmU20hERRhUNap/m+yWSdFrk2caYkSiocUpX2p2W7zO8iJCTKKhxS\ne1hXJCTLdpRUOKTZeY+0TbNcm4h7CLhZN3OkTZXWuTYR9xBws9KrdnWRN9E/mCNRVifnkVL9\nknMTLSFR0livbBASRQkJAnQS0n+vXBASAzPakKzaUVLBkFK6+XK6iAqUREEFQ3qthMRYlTy0\n29dp3l70XeLQziSJksrOkV5Sas4gCYmxKbzYsJunei8kRqf4qt0qVRshMTbll7+3s///BKyQ\nGJguziMtioRk1Y6CRnuJkJAoSUgQoKuQ8p+QNUmiICFBgPEe2gmJgoQEAYQEAUYckmU7yhES\nBBASBBjvT8iaI1FQwZDWQmK0Sh7abavr768asIlLQqKconOkbVrm3sQlJVFM2cWGddrm3sQF\nIVHMiFftLNtRjpAggJAgwJhDMkeiGCFBACFBACFBACFBgDGHZNmOYoQEAYQEAUYdkkkSpQgJ\nAggJAggJAggJAow6JKt2lCIkCCAkCDDqkEySKEVIEEBIEEBIEEBIEGDcIVm2oxAhQQAhQYBx\nh2SORCFCggAjD8mxHWWMOyS7JAoREgQYeUgO7ShDSBBASBBg5CGZI1GGkCCAkCCAkCDA2EOy\n2kARIw/Jsh1lCAkCCAkCjD0kqw0UISQIICQIICQIICQI0J+Q0qW4Rw17JLiiPyHl2YSQKGLs\nISmJIkYfkkkSJQgJAggJAggJAggJAow+JKt2lCAkCCAkCDD6kMyRKGH8IdklUYCQIMDoQ3Js\nRwlCggDjD8mhHQUICQIICQKMPyRzJAoQEgQQEgQYf0hJSeQ3/pDskihgAiFZtiM/IUEAIUGA\nCYRkjkR+QoIAQoIAQoIAQoIAEwjJqh35TSAkJZGfkCDAFEIySSI7IUEAIUEAIUEAIUGAKYRk\n1Y7shAQBhAQBphCSORLZTSIkuyRyExIEmEJIju3ITkgQYBIhObQjt4Ihpeo19ybKPBz8UDKk\nlOp93k2UeTj4oWhImyotb0rJHImBKRrSYV+ntNjk28QfhERuZUM6HLZ1c4S33l7fMQmJgSkd\n0jGlZZUaOTbxFyWRWfmQjrbreiYkxqSTkLJtotTjwTdCggCTuLJBSOQ2jZDMkcisaEivq7pd\nsKuX/7lYSEgMTMGQ9rP0aZ5lE38REpkVDGmZqpdt+9GuuVYoxyb+IiQyKxhSlbYfH29TlWMT\nfxESmXW1/F32ygardmQ2jT2Sksis7Bxps2s/Kj5HEhKZlVz+nl+s2s2uXv4d/ro3SSKvsueR\nlu15pKpeFT6PJCQym8aVDUIiMyFBgPIh3XIRuJAYmImEZNWOvIQEAYQEAcqG9HkeKdsmfueG\nFOQlJAgwkUM7IZHXREKy/k1eQoIAUwnJoR1ZTeQSISGRl5AgQPGQNnVzbFfvMm7iN+ZIZFU6\npPnpJFKqfpSULj2ziV8JiawKh7RO832TyTotcm3id0Iiq8IhVWl/WrYr+y5CByWRV+GQ2sM6\nITE6hUOanfdI2zTLtYlyDwkfupkjbaq0zrWJcg8JH0qv2tWdvIl+noeED52cR0r1S85N/Moc\niZymcmWDkMhKSBCg7DutdnXHvoOQyKtgSB3ese8gJPIqezeKru7Yl+sx4axgSF3eHynTY8JZ\nwZA6vGNfrseEs+nskUySyKjsHKmzO/YdhERWJZe/O7xj30FIZFX2PFJnd+w7CImsJnNlg5DI\naTohWbUjIyFBgK5Cch6JUZlOSCZJZDSdQzshkZGQIICQIICQIMCEQrJsRz5CggBFfx7p5htO\nCImBKRjSuuOQzJHIp+Sh3ba6/pYnAZu4RkjkU3SOtL3+43wRm7jizbEd2ZRdbFhf/LR5pk1c\nYZdENhNatRMS+UwpJId2ZCMkCCAkCDClkMyRyEZIEEBIEEBIEEBIEGBKIVm2IxshQQAhQYBJ\nhWSSRC5CggBCggBCggDPhLRbVqlaXr313oOExMA8EdKuat/EpNqFDujLJobxsPBMSIs03x/2\n87QIHdCXTQzjYeGZkKrUHNXtUhU5nq+bGMrjMnlPhHR+a7rr71D3mFwveJMkMhESBBASBBAS\nBHgqpJvfy7vAqG4iJDKZVkhW7chkUpcICYlchAQBphWSORKZPL9q98snTxMSA/N0SFkWwbOF\n5NiOPKYVkl0SmQgJAkwsJId25CEkCCAkCDCxkMyRyGNa19oJiUyEBAGmdYmQkMhkaiFZbSCL\niYVk2Y48nglpv2w/fJ2lah03oi+bCCcksngmpKpdYdi0Sw3zwDEJicF5IqR1806rx5yqbfN+\nqy8dj+pGVhvI4omQ5ql51+/XtGp/Dd0lCYmBefrKhmV6/fwkipAYmKdDmg3qEiEhkccTIc2a\nQ7vd6WYU+9i30hcSA/NESMtmsWGRNs3H6+dv7pLteqOvW8n2yEzaEyHtq49173VK28BBWf5m\naJ46IbtIadl+5fx7mIwvdyWRQ8glQql+DRjK1U2EMUkih6ldayckshASBBASBHgipGqAPyEr\nJPJ4IqR6kCFZtSOHp67+ni1fdqGj+b6JYT00E/ZESLtFc3BXLTLEJCQG5rnFhu26Pb4Lj8kc\niYF5ftXudTVvY4oZz6+biOTtT8ghZPl7vxzOYoOQyGFyeyTHduQwuTmSkMjh6VW7LEvgOUNy\naEcGT55H2uxDR/N9E0N7bCZrclc2CIkcJnetnTkSOUzu6m8hkYOQIMD0QlISGQgJAkwwJMt2\nxBMSBBASBJhgSOZIxBMSBBASBBASBBASBJhgSFbtiDfBkJREPCFBgCmGZJJEOCFBACFBACFB\nACFBgCmGZNWOcEKCAEKCAFMMyQ0pCCckCCAkCDDFkKx/E05IEKBkSPtlc1u/1Syl+UumTdzG\noR3RCoa0q1I67M/3sJhn2cSNhES0giEtUr0//rLYNTf7S8scm7iRkIhWMKSU9udfjkd512/e\nbI7EwBQN6dDcnezik/BN3EhIRCt6aLc9HFbNL80e6eokSUgMTMGQtqlabg91dSxpM0ubHJu4\nlZIIVnL5e3Nx19lVnk3cSEgEK3tC9mUxayqqV7tsm7iJZTuCTfLKBiERTUgQoGhIr6u6nSDV\ny9dcm7iNORLBCoa0n32uNXR7iZCQiFYwpGWqXtqTSIfdpur0EiEhEa1gSNXpXGxr2+klQkIi\nWulLhH79JGwTtxISwaa5R7JsR7Cyc6TN6URs53MkIRGs5PL3/GLVbrbPsolbCYlYZc8jLdvz\nSFW96vg8kkkSwaZ5ZYOQCCYkCFA+pOsL3yGb+D8hEUtIEGCiIVm1I5aQIEDZkD7PI2XbxI0D\nyb0BJmaiIbkhBbEmemgnJGIJCQJMNCTr38QSEgSY6CVClu2IJSQIUDykTd0c29XX32pVSAxM\n6ZDmp5NIqfpRUrr0zCZuYo5EqMIhrdN832SyTotcm7iNkAhVOKQq7U/Ldt2+i5ATSQQrHFJ7\nWNeHkOySCFU4pNl5j7RNs1ybuJGQiNTNHGlTpXWuTdzIoR2RSq/a1b14E/0ym2BCOjmPlOqX\nnJu4iZCINNUrG8yRCCUkCFD2nVb7cse+g5CIVTCkHt2x7yAkYpW9G0Vf7th3EBKxCobUp/sj\nFdoGk1EwpB7dsa/UNpgMeyQIUHaO1Js79h1MkghVcvm7R3fsOwiJUGXPI/Xmjn0HIRFqslc2\nCIlIQoIA0w3Jqh2BugrJeSRGZbohKYlA0z20M0kikJAggJAgQMmQ9svmArvVLKV59+/ZICQi\nFQxpV6V02Fc9+cG+5s1WS7zJONNQMKRFqvfHXxa7Y1OL7i9abbw1jjm1vxfaJqNU9OeR9udf\njkd53f8YxfdNpougLn4vPxKGqPQP9lXp4pPwTYT4cm8ZIXGTood228Nhdfrpvv31SVI/pi6n\nnVTXo2AQCoa0TdVye6irY0mbWdrk2EQGPRoKPVZy+XtTff5g3yrPJuL1aCj0WNkTsi+L9r3t\n6tX1W8j26tXbp7HQWxO+suFGZkncQEj/JST+T0j/pyT+S0j/JyT+S0g3UBL/I6Qb9Gw49JCQ\nbtG38dA7QrpF38ZD7wjpJmZJXCek2yiJq4R0GyFxlZBupCSuEdKNXHLHNUK6VR/HRG8I6Wa9\nHBQ9IaSb9XJQ9ISQbmeWxJ+EdDsh8Sch3UFJ/EVIdxASfxHSPZTEH4R0l94OjI4J6S69HRgd\nE9J9+jsyOiWk+5gl8Ssh3eetv0OjS0K6k5L4jZDuJCR+I6R7KYlfCOluvR4cHRHS/fo9Ojoh\npPv1e3R0Qkj3M0viByHd763n46MDQnqAXRLfCekBdkl8J6RH2CXxjZAe0/8RUpSQHjSAIVKQ\nkB40gCFSkJAeZJrEJSE9SEhcEtKjlMQFIT1KSFwQ0sOUxCchPWEgw6QAIT1hIMOkACE9Yyjj\nJLv+hJQu5dlENLMk3vUnpMKbiOAqcN4J6RlK4kxIzxASZ0J6ipI4EdKTBjRUMhLSs4Y0VrIR\n0rOGNFayEdKTzJJoCOlJb4MaLbkI6Vl2SRyE9Dy7JA5CCmCXhJBiDOUqW7IRUgwpTZyQokhp\n0oQU4O3022B+jop4Qorwdk7JbmmyhBTjIqXhDZ7nCSnQxyFet8OgA0KK9CalqRJSrDcLD9Mk\npAxONUlpSoSUxVvbkpSmQ0hZOcKbCiFlZLc0HULKqj3Es1uaACEVIaWxE1IBp91S16MgJyEV\n0RzipV90PS6iCKmct7fTqvjn77/Gpa8hElKXvof1/rukBkdIffSxxzooaiCE1GcXeyo7qX4T\n0nCcD/3Mq/pISMPzc07116KgvooR0nj8GtiIcur1fyeENH4fu6uuB/KnP/amf0bz+R+K3vx/\nEtIUfFlWj3rQ2179dybyx+i/n3/7/LO+vFSENCUXixW3/YWrr/7f52rxv/9niA88DxkIaXr+\nmjv9bOWZF3gx/XixCGm6vi/1XTuE6rF+HN0Jacp6uYe5Wy9KEhJD14v76giJwetDSUJi+HpQ\nkpAYha5fMkJiHDp+zZQMab+sjr+uZinNXzJtgqnq+uiuYEi7KqXDvjqds5hn2QTT1XFJBUNa\npHp//GWxOza1SMscm2DCui2pYEgp7c+/HI/yUpVjE0xZpyUVDen4S5UuPgnfBBPX3Qun6KHd\n9nBYNb80e6SrkyQh8ZjOXjkFQ9qmark91NWxpM0sbXJsgonr7uiu5PL3pvq80niVZxNMXGcl\nlT0h+7KYNRXVq122TTBpb129eFzZwKh0VZKQGJeOSioa0uuqbidI9fI11yagk9dPwZD2s4sf\na3aJEBmVfwEVDGmZqpf2JNJht6lcIkQ2XRzdFQypOp2LbW1dIkQ+HZRU+hKhXz8J2wS0ypdk\nj8QYFS+p7BxpczoRa45EAUVfRSWXv+cXq3azfZZNwKeSL6Oy55GW7Xmkql45j0RuZY/uXNnA\nWBUtSUiMVsmSyod0yx1FhESEgiUJiXEr9FoSEiNX5sUkJMauyKupbEi33jVUSARpbvxU4jbU\nQmLc2luo5X9BObRj5E4l5X5JCYmxO93WM/NrSkhMRN6dkpCYguwzJZcIMQm5Z0pCYhre8u6U\nioe0qZv/LNTX32pVSMTLulMqHdL8dBIpVT9KSpee2QRck+fFVTikdZrvm0zWaZFrE/C3bBc6\nFA6pSvvT/w/vIkQncs2UCofUHtYJie685dkpFQ5pdt4jbdMs1ybguiyLDt3MkTZVWufaBNwk\n9kVWetWu9ib69ED48V0n55FS/ZJzE/Bf0YsOrmxgmoIXHYTEVIXulMq+06o79tE3QTulgiG5\nYx+90x7fRTxQwZDcsY/+aaZKETulgiG5PxJ99BbyfqwFQ3LHPnrr6Z2SPRI0nkyp7BzJHfvo\np6dPKpVc/nbHPnrrfH724Vde2fNI7thHb709dVW4Kxvg09ujuyUhwYVHL8ETEnzx2Gypq5Cc\nR6LP7r7eQUjwi3svHXJoB796u2vhQUjwt7dbd0tCgive3m7bLZUMab9Iab45P4g5EsNw22yp\n5A/2Vacfjz09iJAYkLf/7ZaKXrS6Pta0rtofjhUSg/L2n9lS0R+jaH/bVbOdkBic6yl18IN9\n+/lcSIxMwZCa9/0+fzQXEuNSMKTPeyLt0lxIjErJ5e/lRz2b/6yBCImBKXpCdlu/f7RbCIkx\ncWUDBBASBBASBBASBBASBBASBBASBBASBBASBBASBBASBBASBBASBBASBBASBBASBBASBBAS\nBOhpSDAwD7zK48MZxLafNuTBG3s8IT1oyIM39nhCetCQB2/s8YT0oCEP3tjjCelBQx68sccT\n0oOGPHhjjyekBw158MYeT0gPGvLgjT2ekB405MEbezwhPWjIgzf2eEJ60JAHb+zxhPSgIQ/e\n2OP1dVwwKEKCAEKCAEKCAEKCAEKCAEKCAEKCAEKCAEKCAEKCAEKCAEKCAEKCAEKCAEKCAJ2F\ntKxStdx3tfXnPPxO651bvw96gE//+9j7+ex3NZ55+2TMOtr6c7b9/Ke8wfZ90AN8+t/H3tNn\nv6PxvKZqe9hW6bWbzT9nm+quh/CY4xN++vce4NP/MfaePvsdhbRMm+OvL2nVzeafsx7msI/j\nnp9fjMN7+j/H3tNnv6OQ6rQ79PY/Lv+zTuuuh/CQtDycX4zDe/o/x97TZ7+jkM5PSu+OdG9S\np83iOFXvehh3235/3gf09H+OvafPvpDuV59mu/Oux/GAwYZ0uAipl8++kO6X0svhsF/28xDj\nuhGE1NNnX0iP2g9r9fhkBCGd9O7Z7+iprIb4L/nNEAd/HvMgn/6vo+3b2DtdtdsNaNnop779\nU97iy6rdwJ5+If1i1Z7I2KTeLb7cokrNtTUDexmenF9+g3z6P/amvXz2Xdlwv2XzAtyfTmoO\nzHCvbPgYe0+f/a52kLNermHeZl+1gx/Uf87P3g+Ihvj0n8fe02e/q5D27eXHHW38Wc3gZz1b\nfr3Ne0hDfPovx96/Z79nUzYYJiFBACFBACFBACFBACFBACFBACFBACFBACFBACFBACFBACFB\nACFBACFBACFBACFBACFBACFBACFBACFBACFBACFBACFBACFBACFBACFBACFBACFBACFBACFB\nACFBACFBACF16M47c+8XJe742LN7sw6FkDp0Z0h1SmmVaSgfZl4RD/G0dejOkFLaZRrIl43k\n38YYedo6dHdImcZRfCMj5GnL5Lj7qFO1Ory/NJtfj/9btV9bniY7x8+XHzcXX89StT59536W\n6o8HOn69vYd3an18eVml+e7LN/z34d+/631gX7Z5/uL7RjbzlOamS7cTUiYpVek0p7kMadV8\nrXmRti/1lJppT5o3f95+1H7YfvVjUWH+/vWvIbVfrvaX3/DLw68+Hv7yu94H9mWb5y+eN7I+\nbW1d7vkaOiFlcnyB7o+vx9nXkNqvnX6t2pfv9rCt0stxD9B8cT9Pm/N3vXv5/JbLo66X5nsW\nTS0X33Dl4X9+1+znNi9GW6Vt85dmhZ+0ARNSJim9Hj4O6D4+On1t9/F5c/C0aY7j6tTEs28+\nPH3XWX3+lvnhS0h18z37ppaLb7j68D++65dtXo7WYd19hJTJl5nRj48uPz9/mN6P3b5M9y++\n5fIPPj/88hhXHv6X7/qxzc+PjrOseruNezbGT0iZDDukw6qZM1UFltvHQkiZ3B3St7/59ZNM\nIf052qPNcmaOdDshZfLtpfn6+yu9mZlcTGIu/uZZ/TnPufyD+Y85Uv33wy/++K4f2/y+P0xe\nHTfzVGXy+dKcpXWzNvZrSKe1tM15We2w/nyln/2xarduVtmWP1btrj/89+/6sc3TX2qO52an\npT57pJsJKZPPl2Z7Tqb+PaRF+2fN56cTPc2s5Ot+4PME0Jc/+P080veHn397+G/f9X2bp+yb\n/dzLafJ0sXzIdULK5OL1epy4L/6axCzfLzJorjJIi93he0iHdXW+JOHrHzTraruv3/DLw9fv\nf/f37/q2zebX11kT0unKBh3dTkjjZYpTkOd6vIRUkOd6vIRUkOd6vIRUkOcaAggJAggJAggJ\nAggJAggJAggJAggJAggJAggJAggJAggJAggJAggJAggJAggJAggJAggJAggJAggJAggJAggJ\nAggJAggJAggJAggJAggJAvwDU0Gbd0FA5AkAAAAASUVORK5CYII=",
      "text/plain": [
       "Plot with title \"Apps\""
      ]
     },
     "metadata": {
      "image/png": {
       "height": 420,
       "width": 420
      },
      "text/plain": {
       "height": 420,
       "width": 420
      }
     },
     "output_type": "display_data"
    }
   ],
   "source": [
    "fit.pcr = pcr(Apps ~ ., data = College.entrenamiento, scale = TRUE, validation = \"CV\")\n",
    "validationplot(fit.pcr, val.type = \"MSEP\")"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 40,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "1942749.55086353"
      ],
      "text/latex": [
       "1942749.55086353"
      ],
      "text/markdown": [
       "1942749.55086353"
      ],
      "text/plain": [
       "[1] 1942750"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    }
   ],
   "source": [
    "pred.pcr = predict(fit.pcr, College.prueba, ncomp = 10)\n",
    "mean((pred.pcr - College.prueba$Apps)^2)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "- *(f) Ajuste un mdelo PLS en el set de entrenamiento, con el M elegido por validación cruzada. Reporte el error de prueba obtenido, junto con el valor de M seleccionado por validación cruzada*"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 41,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "image/png": "iVBORw0KGgoAAAANSUhEUgAAA0gAAANICAMAAADKOT/pAAAAM1BMVEUAAABNTU1oaGh8fHyM\njIyampqnp6eysrK9vb3Hx8fQ0NDZ2dnh4eHp6enw8PD/AAD///89ODILAAAACXBIWXMAABJ0\nAAASdAHeZh94AAAbQUlEQVR4nO3diVbiSBiA0QqERQTk/Z92CKDiMrbCn1rCveeMLQ5aGZpv\nkqpESAfgbqn0BsAUCAkCCAkCCAkCCAkCCAkCCAkCCAkCCAkCCAkCCAkCCAkCCAkCCAkCCAkC\nCAkCCAkCCAkCCAkCCAkCCAkCCAkCCAkCCAkCCAkCCAkCCAkCCAkCCAkCCAkCCAkCCAkCCAkC\nCAkCCAkCCAkCCAkCCAkCCAkCCAkCCAkCCKl+y5TSsvRG8DMh1S8NSm8EP/MXVL2nU0hPpTeD\nHwmpevPjgV1K89KbwY+EVLtdSt1hltLufHM4ylsfby52393cr47Zpd7uKzsh1e64N1odVm/L\nDUMnp2O9bvf15q5LZ/ZfuQmpdsc29of9sFs6SW9mX28uTnOp/XGvtC64xQ9JSJXbnHcvx93O\n5nR72Pk8H7/cnb/w8WY6HwHuL5WRj5Aqdyno2FN/uv26gHf8wuLLzeHIbrEptq2PTEh1ezum\nOx3hHc6rC4fzJ7MvN1fnozwt5Sekuq3fJ0Hnec9VOenrzeXlrt2uzOY+LiHVbXYV0uvqwmnP\n9B7S9c3D/mlu2a4EIVXtOV17PpyCOe2ZLpOmTzdPNguXFGXnAa/a8v3aoPX5VNLlcqFhmW79\n5ebsbSLVFdvkByWkqr0duZ2WHS7Hcq/zoMOXm8Na+e5wdfqWXIRUs6fzGvdZf9r3pNOVd9dX\nNlzffF1sMEXKTUg1m7+ehh2cT80O+6WnWeqW72sMVzfP86O56xqyE1JjPq0jWFaohL+Gxgip\nTv4aGiOkOvlraIyQ6uSvoTFCqpO/BgggJAggJAggJAggJAggJAggJAggJAggJAggJAggJAgg\nJAggJAggJAggJAggJAggJAggJAggJAggJAggJAggJAggJAggJAggJAggJAggJAggJAggJAgg\nJAggJAggJAggJAggJAiQIaQEjbnhWR4fToEhIJKQIICQIICQIICQIICQIICQIICQIICQIICQ\nIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQIEBjIb2MPzbcQEgQQEgQQEgQ\n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\nCOvDnz99l7TGlvXXKE5/7LrZTkgj+L/APv756uadm33htwr8Yt9+PhdSMf8KLfrPXMFm8r+P\na8aQhtf9vnw2F9KjyB3u2H/+n4whvb8n0i7NhcSk5Fz+Xr7Vs/lpJ3nPEFBG1hOy2/71s91C\nSEyJKxsggJAggJAggJAggJAggJAggJAggJAggJAggJAggJAggJAggJAggJAggJAggJAggJAg\ngJAggJAgQKUhQWNueJbHh9PE2HdreeNtezwh3ajljbft8YR0o5Y33rbHE9KNWt542x5PSDdq\neeNtezwh3ajljbft8YR0o5Y33rbHE9KNWt542x5PSDdqeeNtezwh3ajljbft8YR0o5Y33rbH\nE9KNWt542x6v1u2CpggJAggJAggJAggJAggJAggJAggJAggJAggJAggJAggJAggJAggJAggJ\nAggJAhQLadmlbrkvNfp9bn6l9eLWrxvd4MP/uu11Pvqltmd+ejBmhUa/z7bOv8pf2L5udIMP\n/+u2V/roF9qe59RtD9suPZcZ/j7b1JfehNscH/Dz33eDD//btlf66BcKaZk2x49PaVVm+Pus\n29zs43bPL0/G9h7+922v9NEvFFKfdodq/+fyL+u0Lr0JN0nLw+XJ2N7D/77tlT76hUK6PCjV\nHen+Sp82i+NUvfRm/Nn28+Pe0MP/vu2VPvpC+rv+PNudl96OGzQb0uEqpCoffSH9XUpPh8N+\nWechxs8mEFKlj76QbrVva/X4bAIhnVX36Bd6KLsW/yY/aXHjL9vc5MP/cWtr2/aiq3a7hpaN\nvqrtr/I3PqzaNfbwC+kbq9OJjE2qbvHlN7o0XFvT2NPw7PL0a/Lhf9ubVvnou7Lh75bDE3B/\nPqnZmHavbHjb9kof/VI7yFmVa5i/s+9OG9/U/84vXg+IWnz4L9te6aNfKqT96fLjQoPfa9j4\nWWXLr7/zGlKLD//1ttf36Fc2ZYM2CQkCCAkCCAkCCAkCCAkCCAkCCAkCCAkCCAkCCAkCCAkC\nCAkCCAkCCAkCCAkCCAkCCAkCCAkCCAkCCAkCCAkCCAkCCAkCCAkCCAkCCAkCCAkCCAkCCAkC\nCAkCCAkCCAkCCKmgP74z936R4x0fK3tv1lYIqaA/htSnlFYjbcqbmWfETTxsBf0xpJR2I23I\nh0HGH2OKPGwF/TmkkbYj+yAT5GEbyXH30adudXh9ag4fj/+sTl9bnic7x9vLtzcXX89Stz7f\ncz9L/dsPOn799B7e6eTty8suzXcf7vDPH/96r9cN+zDm5Yuvg2zmKc1Nl35PSCNJqUvnOc11\nSKvha8OT9PRUT2mY9qT58O9Pn50+PX31bVFh/vr1jyGdvtztr+/wzY9fvf3463u9btiHMS9f\nvAyyPo+2zvd4tU5IIzk+QffH5+PsY0inr50/dqen7/aw7dLTcQ8wfHE/T5vLvV49vd/l+qjr\nabjPYqjl6g4//Piv95p9HfNqa7u0Hb5plvlBa5iQRpLS8+HtgO7ts/PXdm+3h4OnzXAc16ch\nnv3w6fleF/3lLvPDh5D64T77oZarO/z447/c65sxr7fWYd3fCGkkH2ZGXz67vn35NL0eu32Y\n7l/d5fpfvH/64Wf88OO/udeXMd8/O86y+u027tGYPiGNpO2QDqthztRlWG6fCiGN5M8hffrO\njzdGCul/t/Zos5yZI/2ekEby6an5/P0zfZiZXE1irr7zon+f51z/i/mXOVL//z9+8T/3+jLm\n5/1h8uz4NQ/VSN6fmrO0HtbGvg3pvJa2uSyrHdbvz/SL/1m1Ww+rbMsvq3Y///jP9/oy5vmb\nhuO52Xmpzx7p14Q0kven5umcTP99SIvTvxtun0/0DLOSj/uB9xNAH/7F9+eRPv/4+acf/+le\nn8c8Zz/s557Ok6er5UN+JqSRXD1fjxP3xf9NYpavFxkMVxmkxe7wOaTDurtckvDxXwzraruP\nd/jmx/ev3/v9vT6NOXx8ng0hna9s0NHvCWm6THEy8lhPl5Ay8lhPl5Ay8lhPl5Ay8lhDACFB\nACFBACFBACFBACFBACFBACFBACFBACFBACFBACFBACFBACFBACFBACFBACFBACFBACFBACFB\nACFBACFBACFBACFBACFBACFBACFBgP8AT5eXNRCXRHEAAAAASUVORK5CYII=",
      "text/plain": [
       "Plot with title \"Apps\""
      ]
     },
     "metadata": {
      "image/png": {
       "height": 420,
       "width": 420
      },
      "text/plain": {
       "height": 420,
       "width": 420
      }
     },
     "output_type": "display_data"
    }
   ],
   "source": [
    "fit.pls = plsr(Apps ~ ., data = College.entrenamiento, scale = TRUE, validation = \"CV\")\n",
    "validationplot(fit.pls, val.type = \"MSEP\")"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 42,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "1406322.47608555"
      ],
      "text/latex": [
       "1406322.47608555"
      ],
      "text/markdown": [
       "1406322.47608555"
      ],
      "text/plain": [
       "[1] 1406322"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    }
   ],
   "source": [
    "pred.pls = predict(fit.pls, College.prueba, ncomp = 10)\n",
    "mean((pred.pls - College.prueba$Apps)^2)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "- *(g) Comenta sobre los resutados obtenidos ¿Con qué precisión podemos predecir el número de solicitudes universitarias recibidas? ¿Hay mucha diferencia entre os errores de prueba resultantes de estos cinco enfoques?*"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 43,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "image/png": "iVBORw0KGgoAAAANSUhEUgAAA0gAAANICAMAAADKOT/pAAAAM1BMVEUAAABNTU1oaGh8fHyM\njIyampqnp6eysrK9vb3Hx8fQ0NDZ2dnh4eHp6enw8PD/AAD///89ODILAAAACXBIWXMAABJ0\nAAASdAHeZh94AAAgAElEQVR4nO3d4ULa6BpF4QQQFYHj/V/tgQASrDrt9ktc+K71YwanNTyT\nZlcBbbtXM/t23U8DzH5DDsmsQQ7JrEEOyaxBDsmsQQ7JrEEOyaxBDsmsQQ7JrEEOyaxBDsms\nQQ7JrEEOyaxBDsmsQQ7JrEEOyaxBDsmsQQ7JrEEOyaxBDsmsQQ7JrEEOyaxBDsmsQQ7JrEEO\nyaxBDsmsQQ7JrEEOyaxBDsmsQQ7JrEEOyaxBDsmsQQ7JrEEOyaxBDsmsQQ7JrEEOyaxBDsms\nQQ7JrEEOyaxBDsmsQQ5pjrpx//FzHz58x9XThLzx3c1xN78xT9wc/f2QXvqbHx+923JS4dvd\nzXAvvzJP3Bz9/ZDe/fj4/Wb4mOSQ4jxxs/VXV+mfQxr+vV933WIS1Vf3bn+fJ262xlfpft13\n/Xp3uv24PD4Ien59+wD00fu8u8ZH73Ro93DY2dPl51x+6uXfz6vDrcXp3g63dotu/Y5wOEA/\nOoD9e5642Rpdpbv+tJiX0e3jg6C/HtL4nQ4PrE631x8PaXn53PDl9N8Ww3uNCZcDLB1SnCdu\ntkZX6WUG/eH24YPJ4ePKfnl8EPTpkI4fclajY43f6Xq4D4f0dBjI/vV1fTrA6Wc93xLeH8D+\nPU/cbF2v0tO1vT+t4fjJ1uG/7U8Pgr54suHl9r9f3+n5MIfN4V/9h0NanH7q+a3uNKtbwvkA\nm94hxXniZut6lR4es+xP/2V1+mjwsPnzJ13evLQZ//ebd1oNaxj28OFjpPGRLwe6IazO/3Hj\nkOI8cbN183jn+onV4+nWeRafDelxP3779p3e3uezIe2e18vubUj7PwjvD2D/nidutj4a0vG/\nrC9X9O71oyEddrA8/+Do2YjxO/3HkJ4Xozsb/dj1vzqk7+eJm63rVdq/eyr7+fTE2vL14yEN\nT7wtL2+fFzF6p8v77D8c0vETvsXD0/Z2SDcEh/T9PHGzdb1KV+8e8RzaPNxe6O/epz8/DPrw\nnS6He7oO6fjp20t3ebJh9Ang5YA3hMsbzw4pzhM3W9er9Pgs2cvwr+VwoZ8ftfTnn7T/831e\nzs9TX7p5p/OTbk/nj1XH1a2Hr9obT+fdR6QbwtO7p/3s3/PEzdboKn173eZleKpsuRuec1if\nf2T9wfusbr/W7s93un7Sd3yRafTmcvg5m9tZ3RJ8Hen7eeJma3SVbs5X7TCZy/MGw6Ogh+7m\n67zf3md3/nzt0s07bU9DuHxlw64bv3n+qoWuHzbzdsAbwvnnrBxSnCdutsZX6X59+ORsdX6U\nMjzUWZ4/4Bwu5oeP3md9+6UNt+90/MKH5ebtZ2+Pbz6/fVJ3eKt/2O6GA1wPeEMYDuDX2n0j\nT9wvyh38XJ75X5RD+rk8878oh/RzeeZ/UQ7p5/LM/6Ic0s/lmTdrkEMya5BDMmuQQzJrkEMy\na5BDMmuQQzJrkEMya5BDMmuQQzJrkEMya5BDMmuQQzJrkEMya5BDMmuQQzJrkEMya5BDMmuQ\nQzJrkEMya5BDMmuQQzJrkEMya5BDMmuQQzJrkEMya5BDMmuQQzJrkEMya5BDMmuQQzJrkEMy\na5BDMmuQQzJr0E8OqZs5AoJg4P7mecfn4UeH9L9Z++QiLmf4BEGI8IuR0lse7F/ve9bThriI\nCQaHNMV5cEjlDA5pivPgkMoZHNIU58EhlTM4pCnOg0MqZ3BIU5wHh1TO4JCmOA8OqZzBIU1x\nHhxSOYNDmuI8OKRyBoc0xXlwSOUMDmmK8+CQyhkc0hTnwSGVMzikKc6DQypncEhTnAeHVM7g\nkKY4Dw6pnMEhTXEeHFI5g0Oa4jw4pHIGhzTFeXBI5QwOaYrz4JDKGRzSFOfBIZUzOKQpzoND\nKmdwSFOcB4dUzuCQpjgPDqmc4TME4M+UI/xihDmkcgYEgmsIc0jlDAgE1xDmkMoZEAiuIcwh\nlTMgEFxDmEMqZ0AguIYwh1TOgEBwDWEOqZwBgeAawhxSOQMCwTWEOaRyBgSCawhzSOUMCATX\nEOaQyhkQCK4hzCGVMyAQXEOYQypnQCC4hjCHVM6AQHANYQ6pnAGB4BrCHFI5AwLBNYQ5pHIG\nBIJrCHNI5QwIBNcQ5pDKGRAIriHMIZUzIBBcQ5hDKmdAILiGMIdUzoBAcA1hDqmcAYHgGsIc\nUjkDAsE1hDmkcgYEgmsIc0jlDAgE1xDmkMoZEAiuIcwhlTMgEFxDmEMqZ0AguIYwh1TOgEBw\nDWEOqZwBgeAawhxSOQMCwTWEOaRyBgSCawhzSOUMCATXEBYfbPfQ9Y+vr0+Lrl+n9z3raQP/\n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\n+ykeIVz/hy//vy9vX4B4c2u215HOnf/3F+MH/fsZPiS9G9Kcl8MXqJ+4039s/3j86u/Ht6/+\nvrq/uuUAAAGtSURBVD7iPn75cbec7nfg6y/a+vg77dvD/NFXNixfTjefDsZpXg8c/Q8/HL+8\n+vS52/D1DMPTU9dbr0/9PF/ZcO55dT37Nydq2j4b0gyXwxeoH7nXX9XP/A5orBxS3vDJ5n71\nI19sbLAcUt75S99+4jkio+WQvtHT8MVdP60wQg7JrEEOyaxBDsmsQQ7JrEEOyaxBDsmsQQ7J\nrEEOyaxBDsmsQQ7JrEEOyaxBDsmsQQ7JrEEOyaxBDsmsQQ7JrEEOyaxBDsmsQQ7JrEEOyaxB\nDsmsQQ7JrEEOyaxBDsmsQQ7JrEEOyaxBDsmsQQ7JrEEOyaxBDsmsQQ7JrEEOyaxBDsmsQQ7J\nrEEOyaxBDsmsQQ7JrEEOyaxBDsmsQQ7JrEEOyaxBDsmsQQ7JrEEOyaxBDsmsQQ7JrEEOyaxB\nDsmsQQ7JrEEOyaxBDsmsQQ7JrEEOyaxBDsmsQQ7JrEEOyaxBDsmsQQ7JrEEOyaxBDsmsQQ7J\nrEEOyaxBDsmsQQ7JrEEOyaxBDsmsQQ7JrEEOyaxBDsmsQQ7JrEEOyaxBDsmsQQ7JrEEOyaxB\nDsmsQf8Haj+dGcIA5hMAAAAASUVORK5CYII=",
      "text/plain": [
       "Plot with title \"Test R-squared\""
      ]
     },
     "metadata": {
      "image/png": {
       "height": 420,
       "width": 420
      },
      "text/plain": {
       "height": 420,
       "width": 420
      }
     },
     "output_type": "display_data"
    }
   ],
   "source": [
    "test.avg = mean(College.prueba$Apps)\n",
    "lm.test.r2 = 1 - mean((College.prueba$Apps - pred.lm)^2) /mean((College.prueba$Apps - test.avg)^2)\n",
    "ridge.test.r2 = 1 - mean((College.prueba$Apps - pred.ridge)^2) /mean((College.prueba$Apps - test.avg)^2)\n",
    "lasso.test.r2 = 1 - mean((College.prueba$Apps - pred.lasso)^2) /mean((College.prueba$Apps - test.avg)^2)\n",
    "pcr.test.r2 = 1 - mean((College.prueba$Apps - pred.pcr)^2) /mean((College.prueba$Apps - test.avg)^2)\n",
    "pls.test.r2 = 1 - mean((College.prueba$Apps - pred.pls)^2) /mean((College.prueba$Apps - test.avg)^2)\n",
    "barplot(c(lm.test.r2, ridge.test.r2, lasso.test.r2, pcr.test.r2, pls.test.r2), col=\"red\", names.arg=c(\"OLS\", \"Ridge\", \"Lasso\", \"PCR\", \"PLS\"), main=\"Test R-squared\")"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**10. Hemos visto que a medida que aumenta el número de características utilizadas en un modelo, el error de entrenamiento necesariamente disminuirá, pero el error de prueba puede no hacerlo. Ahora exploraremos esto en un conjunto de datos simulado.**"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "   - *(a) Genere un conjunto de datos con p = 20 características, n = 1,000 observaciones, y un vector de respuesta cuantitativa asociado generado segun el modelo.*"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 44,
   "metadata": {},
   "outputs": [],
   "source": [
    "set.seed(243642)\n",
    "p = 20\n",
    "n = 1000\n",
    "x = matrix(rnorm(n * p), n, p)\n",
    "B = rnorm(p)\n",
    "B[3] = 0\n",
    "B[4] = 0\n",
    "B[9] = 0\n",
    "B[19] = 0\n",
    "B[10] = 0\n",
    "e = rnorm(p)\n",
    "y = x %*% B + e"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "   - *(b) Divida su conjunto de datos en un conjunto de entrenamiento que contenga 100 observaciones y un conjunto de prueba que contenga 900 observaciones.*"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 45,
   "metadata": {},
   "outputs": [],
   "source": [
    "train = sample(seq(1000), 100, replace = FALSE)\n",
    "y.train = y[train, ]\n",
    "y.test = y[-train, ]\n",
    "x.train = x[train, ]\n",
    "x.test = x[-train, ]"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "   - *(c) Realice la mejor selección de subconjunto en el conjunto de entrenamiento y trace el conjunto de entrenamiento MSE asociado con el mejor modelo de cada tamaño.*"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 46,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "image/png": "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\nKzIrSz+L0HQrMiuLP4vQhEsyI9VHNvR+FqEJl2RGKkN6WfV+FqEJl2RGnPxkyjWZDSFNuSaz\n4Q3ZKddkNoQ07aLMRHVIj5vjs7pN9uvGhERnakNav708KqtoSdPcp5XEj1WGtCvr/TGkXd8f\n7JtyVWah+hCh/dvRDf3vtRMSFQKHCM0mJCXxY5Uh3Z0fkZ7LXWykg5DoTuY10mP4KHAh0Zna\nvXab83EN0fNDTnaPVhI/FHkfqWx+hcb5dInxCIkfcmRDGwvTudrPI2XPZ/fZEqMSEj/jE7Jt\nLEznAru/BzDd/VlJ/EhlSPvNXD4hO/nKdM0H+yBASBBg9zcECAkCUru/V6vENJ8tAR0IhfTi\nNRKLVhHSY/loDh+jeF99oLeZmbGaR6S7jx1F306a8o48wE5I5s8hQv+sLSS+z167v5ce4n0x\nZk9Ify8tJH6gNqS5fPXl/0sLiR+oDGk2X335YW0d8X3V57WbyVdfflhbSHyfvXafrC4jvqv2\no+Zz+2Af/EhlSPP56kuo4fNIECAkCPCGLAQICQIqQirD7QdvIKQGRqAj1SGdCxISiyakr7Qw\nA90Q0ldamIFuCOlLTQxBJ4T0pSaGoBNC+lITQ9AJIX2tjSnoQlVIf5h4qgG0MQVdENIFjYxB\nBxwidEEjY9ABIV3QyBh0QEiXtDIHzRPSJa3MQfOEdEkrc9A8IV3UzCA0TkgXNTMIjRPSZe1M\nQtOEdFk7k9A0IV3WziQ0TUhXNDQKDRPSFQ2NQsOEdE1Ls9AsIV3T0iw0S0jXtDQLzRLSVU0N\nQ6OEdFVTw9AoIV3X1jQ0SUjXtTUNTRLSdW1NQ5OEdIPGxqFBQrpBY+PQICHdoLFxaJCQbtHa\nPDRHSLdobR6aI6SbNDcQjRHSTZobiMYI6SbNDURjhHSb9iaiKUK6TXsT0RQh3ajBkWiIkG7U\n4Eg0REg3anAkGiKkW7U4E80Q0q1anIlmCOlmTQ5FI4R0syaHohFCulmTQ9EIId2uzalogpBu\n1+ZUNEFI39DoWDRASN/Q6Fg0QEjf0OhYNEBI39HqXExOSN/R6lxMTkjf0epcTE5I39LsYExM\nSN/S7GBMTEjf0+5kTEpI39PuZExKSN/T7mRMSkjf1PBoTEhI39TwaExISN/V8mxMRkjf1fJs\nTEZIECAkCBASBAgJAsYPaXdXyuZx0CVgbCOGVE7/47qcbAdZAiYydkjbst0fDi/bshtiCZjI\n2CGtyv54eV/uhlhiJKU0PiCjGzuk97vgv3fF8tEPlxhFByMyurFDun8PaTXEEqMQEv8aNaTN\nw+6x/Hq9uN9e3tvQ8r20i0dNxjZqSL/vgKWs9kMsMQYh8Ykx30d6ft7tNpvTLoftxY6ERG8c\n2fBtOuJfQvo2IfEvIf2AjPibkCBASBAgJAgQEgQICQKEVKGTMRmBkGr0MieDE1KNXuZkcEKq\n0s2gDExIdfqZlEEJqU4/kzIoIVXqaFQGJKRaPc3KYIRUq6dZGYyQqnU1LAMRUrWuhmUgQqrX\n17QMQkgBnY3LAIQU0Nm4DEBICb3NS5yQIrobmDAhRXQ3MGFCyuhvYqKEFNLhyAQJKaTDkQkS\nUkqPMxMjpJguhyZESDFdDk2IkHL6nJoIIeX0OTURQgrqdGwChJTU69xUE1JSr3NTTUhR3Q5O\nJSFl9Ts5VYSU1e/kVBFSWMejU0FIECAkCBASBAgJAoQEAUIaRCnd3wS+RUgDKG+mHoMRCWkA\nQloeIeWVoqTFEVKekBZISHlCWiAhDUBHyyOkAQhpeYQ0CBktjZAgQEgQIKShzem28CUhDc7L\npSUQ0gikNH9CGsXsbhB/EdI4PCjNnJDGMsfbxG9CGo0HpTkT0oikNF9CGtVsb9jiCQkChAQB\nQpqI48PnRUiT8ImluRHSJIQ0N0KagrM6zI6QpiCk2RHSFIQ0O0KahI7mRkiTENLcCGkiMpoX\nIUGAkKa3rFs7U0JqgGd5/RNSE6TUOyE1YoE3eVaE1AoPSl0TUjuWeatnQkgN8aDULyE1RUq9\nElJjFnzTuyYkCBBSqxyM1xUhtcnh4Z0RUpuE1BkhNclHaHsjpCYJqTdCapKQeiOkNumoM0Jq\nk5A6I6RWyagrQuqB7dE8IXXBo1PrhNQJKbVNSN2wUVompH54UGqYkHoipWYJqS9SapSQemPb\nNElIECCkfjn2oSFC6pWj8ZoipF4JqSlC6tRNn1gS2miE1KkbQvKYNSIhdervkD5pRkgjElKv\nPsvk37SUNBIh9erWZ3ZCGoWQ+nV9T4OQRiOk+frnRdSnPzLqSPMlpPn65wHp81/b2AlCmrMr\nj0JCyhHScnkRFSSk5RJSkJCWS0hBQlqwvzqyX6+CkBbs3wekT38tpRsIadGuPQgJ6VZC4ms3\nvYoS2pGQ+NoNIXnMeiMkvvZ3SJ80I6Q3QuKCzzL5N60rJV3vbAYlCokLbn1md+FHbgrt6oPa\n1dQStdYsIiQuur6n4cqTv0RIgVdqQy8iJKp8+eTvz/9+/SGrqhMhTbYEGd/NpJQvf+fmn7i6\nyCA/cfkHhESlm/6ej97HAy1+5ydumlNIDOtaJYk9GkPU+s0fEBLDCoTkNdJPCWlOLt9/b/kJ\nIf2QkPjT1Rjra/U+EkxOSBAgJAgQEgQICQKEBAFCggAhQYCQIEBIECAkCBASBAgJAoQEAUKC\nACFBgJAgQEgQ0GhI0Jkf3Mvz4fSmm03Qy6CLnLOXGz2gbjZBL4Mucs5ebvSAutkEvQy6yDl7\nudED6mYT9DLoIufs5UYPqJtN0Mugi5yzlxs9oG42QS+DLnLOXm70gLrZBL0Musg5e7nRA+pm\nE/Qy6CLn7OVGD6ibTdDLoIucs5cbPaBuNkEvgy5yzl5u9IC62QS9DLrIOXu50QPqZhP0Mugi\n5+zlRkPThAQBQoIAIUGAkCBASBAgJAgQEgQICQKEBAFCggAhQYCQIEBIECAkCBASBCw8pB+f\nM31cu/cJt6uy2u4nneWS9znb3qy7u98bMbc9W72x43hu+0/83fP7hOvTtHfTTvO19znb3qzb\n02yrYz7B7dnojR3Jc9lMPcINnlfn++RTWT0ff/U08UBf+D1n05v1udzvj4+d99ntueyQduVh\n6hGu25X1+Q66LY+v//zV6ND/z9n0Zt28zXgcNbk9lx7SbuoRrivbw/kOuikvh3b/vv9/zh42\n63HU5PZcdkib8nj/+mpz6jEuez6830H//Fdr/p+zg826L+vs9mzzz2Qsm7cXxeup57imi5AO\nH0JqfrPujs/qhJRSyq/Xv5y2zT8T6Syk9jfry+r4dE5IWft2dyifdRbSm4Y36351erQUUli7\n98yz84CrrkJqeM71W+LJ7dnsbR1Tu3/iZ3/stXtpdK/doZeQXu7WL6cLye3Z6G0dyaoc399u\n+J55dr5LPpze93gsze4P+/3I2fJmffy9FyS5PZcd0va4Dfdv78u1rI8jG37P2fRmffl/b6Ij\nG1L2q9N+2mb/hn/3/iTprvHdyuc5m96s9+X/IwGD23PZIb3+tbkqd+3upX33HtL+dLTytLNc\n8nHOVjdr+RBScHsuPCTIEBIECAkChAQBQoIAIUGAkCBASBAgJAgQEgQICQKEBAFCggAhQYCQ\nIEBIECAkCBASBAgJAoQEAUKCACFBgJAgQEgQICQIEBIECAkChAQBQoIAIUGAkCBASBAgJAgQ\nUg8+/37wVr81fJH8WfRASM3zZ9EDITXPn0UPhNQ8fxY9OCVTysumrB5Ov7Fdle05pN1dWR2/\nQHxdnl7/+VTupxtzyYTUg3NIq+O32h9LWh8vbE6/uzl91f36cHgpq9dfrlb7aUddKiH14BzS\nen/YlbvD4VdZPR+eV8fffTz+5n5dHl8fml4beyi/pp51oYTUg3NIT+eLm9Olx7eLx0egfdkc\njo9Tu9O/mYCQenAO6f3ieS/D28Wzw/HJ3evLqAmnXDQh9eC2kA7bsp1uxoUTUg8uhfT/T3lE\nmpCQevBXSJvjvoXD0/8X32xeXyOtJ5pw8YTUg79Cevx/r91pB97htJPh1+sTu4eym3jUpRJS\nD/4K6e3No/vTxdNbSmX1ctivTu8jeXI3DSH14O+QDg9/HNlQ7l/ruT8f2eDJ3SSEBAFCggAh\nQYCQIEBIECAkCBASBAgJAoQEAUKCACFBgJAgQEgQICQIEBIECAkChAQBQoIAIUGAkCBASBAg\nJAgQEgQICQKEBAFCggAhQYCQIEBIECAkCBASBPwHFvUaWs3EbdwAAAAASUVORK5CYII=",
      "text/plain": [
       "plot without title"
      ]
     },
     "metadata": {
      "image/png": {
       "height": 420,
       "width": 420
      },
      "text/plain": {
       "height": 420,
       "width": 420
      }
     },
     "output_type": "display_data"
    }
   ],
   "source": [
    "regfit.full = regsubsets(y ~ ., data = data.frame(x = x.train, y = y.train), \n",
    "    nvmax = p)\n",
    "val.errors = rep(NA, p)\n",
    "x_cols = colnames(x, do.NULL = FALSE, prefix = \"x.\")\n",
    "for (i in 1:p) {\n",
    "    coefi = coef(regfit.full, id = i)\n",
    "    pred = as.matrix(x.train[, x_cols %in% names(coefi)]) %*% coefi[names(coefi) %in% \n",
    "        x_cols]\n",
    "    val.errors[i] = mean((y.train - pred)^2)\n",
    "}\n",
    "plot(val.errors, ylab = \"Entrenamiento MSE\", pch = 19, type = \"b\")"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "   - *(d) Trace el conjunto de prueba MSE asociado con el mejor modelo de cada tamaño.*"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 47,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "image/png": "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",
      "text/plain": [
       "plot without title"
      ]
     },
     "metadata": {
      "image/png": {
       "height": 420,
       "width": 420
      },
      "text/plain": {
       "height": 420,
       "width": 420
      }
     },
     "output_type": "display_data"
    }
   ],
   "source": [
    "val.errors = rep(NA, p)\n",
    "for (i in 1:p) {\n",
    "    coefi = coef(regfit.full, id = i)\n",
    "    pred = as.matrix(x.test[, x_cols %in% names(coefi)]) %*% coefi[names(coefi) %in% \n",
    "        x_cols]\n",
    "    val.errors[i] = mean((y.test - pred)^2)\n",
    "}\n",
    "plot(val.errors, ylab = \"Prueba MSE\", pch = 19, type = \"b\")"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "   - *(e) ¿Para qué tamaño de modelo el conjunto de prueba MSE toma su valor mínimo? Comenta tus resultados. Si toma su valor mínimo para un modelo que contiene solo una intercepción o un modelo que contiene todas las características, juegue con la forma en que está generando los datos en (a) hasta llegar a un escenario en el que la prueba establecer MSE se minimiza para un tamaño de modelo intermedio.*"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 48,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "14"
      ],
      "text/latex": [
       "14"
      ],
      "text/markdown": [
       "14"
      ],
      "text/plain": [
       "[1] 14"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    }
   ],
   "source": [
    "which.min(val.errors)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "El modelo de 14 variables tiene la prueba MSE más pequeña."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "   - *(f) ¿Cómo se compara el modelo en el que se minimiza el conjunto de pruebas MSE con el modelo verdadero utilizado para generar los datos? Comente sobre los valores de los coeficientes.*"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 49,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<style>\n",
       ".dl-inline {width: auto; margin:0; padding: 0}\n",
       ".dl-inline>dt, .dl-inline>dd {float: none; width: auto; display: inline-block}\n",
       ".dl-inline>dt::after {content: \":\\0020\"; padding-right: .5ex}\n",
       ".dl-inline>dt:not(:first-of-type) {padding-left: .5ex}\n",
       "</style><dl class=dl-inline><dt>(Intercept)</dt><dd>-0.217868628639689</dd><dt>x.1</dt><dd>0.424414738628298</dd><dt>x.2</dt><dd>-2.08195197395362</dd><dt>x.6</dt><dd>-0.369460139458655</dd><dt>x.7</dt><dd>-1.48055306130987</dd><dt>x.8</dt><dd>-1.62303520397763</dd><dt>x.11</dt><dd>-0.500624408232906</dd><dt>x.12</dt><dd>-1.86480929279657</dd><dt>x.13</dt><dd>-0.395333348613426</dd><dt>x.14</dt><dd>0.760305503498593</dd><dt>x.15</dt><dd>3.11851393530623</dd><dt>x.16</dt><dd>-0.337469431516375</dd><dt>x.17</dt><dd>-1.19224741638902</dd><dt>x.18</dt><dd>0.690081044683783</dd><dt>x.20</dt><dd>0.667908896157027</dd></dl>\n"
      ],
      "text/latex": [
       "\\begin{description*}\n",
       "\\item[(Intercept)] -0.217868628639689\n",
       "\\item[x.1] 0.424414738628298\n",
       "\\item[x.2] -2.08195197395362\n",
       "\\item[x.6] -0.369460139458655\n",
       "\\item[x.7] -1.48055306130987\n",
       "\\item[x.8] -1.62303520397763\n",
       "\\item[x.11] -0.500624408232906\n",
       "\\item[x.12] -1.86480929279657\n",
       "\\item[x.13] -0.395333348613426\n",
       "\\item[x.14] 0.760305503498593\n",
       "\\item[x.15] 3.11851393530623\n",
       "\\item[x.16] -0.337469431516375\n",
       "\\item[x.17] -1.19224741638902\n",
       "\\item[x.18] 0.690081044683783\n",
       "\\item[x.20] 0.667908896157027\n",
       "\\end{description*}\n"
      ],
      "text/markdown": [
       "(Intercept)\n",
       ":   -0.217868628639689x.1\n",
       ":   0.424414738628298x.2\n",
       ":   -2.08195197395362x.6\n",
       ":   -0.369460139458655x.7\n",
       ":   -1.48055306130987x.8\n",
       ":   -1.62303520397763x.11\n",
       ":   -0.500624408232906x.12\n",
       ":   -1.86480929279657x.13\n",
       ":   -0.395333348613426x.14\n",
       ":   0.760305503498593x.15\n",
       ":   3.11851393530623x.16\n",
       ":   -0.337469431516375x.17\n",
       ":   -1.19224741638902x.18\n",
       ":   0.690081044683783x.20\n",
       ":   0.667908896157027\n",
       "\n"
      ],
      "text/plain": [
       "(Intercept)         x.1         x.2         x.6         x.7         x.8 \n",
       " -0.2178686   0.4244147  -2.0819520  -0.3694601  -1.4805531  -1.6230352 \n",
       "       x.11        x.12        x.13        x.14        x.15        x.16 \n",
       " -0.5006244  -1.8648093  -0.3953333   0.7603055   3.1185139  -0.3374694 \n",
       "       x.17        x.18        x.20 \n",
       " -1.1922474   0.6900810   0.6679089 "
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    }
   ],
   "source": [
    "coef(regfit.full, id = 14)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "La mayoría de coeficientes cuadra con cero."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "   - *(g) Cree una gráfica de una función dada que muestre un rango de valores de r, donde βrj es la estimación del coeficiente j para el mejor modelo que contiene los coeficientes r. Comenta sobre lo que observas. ¿Cómo se compara esto con la trama MSE de prueba de (d)?*"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 50,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "image/png": "iVBORw0KGgoAAAANSUhEUgAAA0gAAANICAMAAADKOT/pAAAAMFBMVEUAAABNTU1oaGh8fHyM\njIyampqnp6eysrK9vb3Hx8fQ0NDZ2dnh4eHp6enw8PD////QFLu4AAAACXBIWXMAABJ0AAAS\ndAHeZh94AAAYV0lEQVR4nO3d60LaSACG4QkgKnK4/7tdA57XCjpfQoY8z4/WrrSJrK+EyWRS\nDkC1cu0dgFsgJAgQEgQICQKEBAFCggAhQYCQIEBIECAkCBASBAgJAoQEAUKCACFBgJAgQEgQ\nICQIEBIECAkChAQBQoIAIUGAkCBASBAgJAgQEgQICQKEBAFCggAhQYCQIEBIECAkCBASBAgJ\nAoQEAUKCACFBgJAgQEgQICQIEBIECAkChAQBQoIAIUGAkCBASBAgJAgQEgQICQKEBAFCggAh\nQYCQIEBIECAkCBASBAgJAoQEAUKCACFBgJAgQEgQICQIEBIECAkChAQBQoIAIUGAkCBASBAg\nJAgQEgQICQKEBAFCggAhQYCQIEBIECAkCBASBAgJAoQEAUKCACFBgJAgQEgQICQIEBIECAkC\nhAQBQoIAIUGAkCBASBAwQkgFGvOH7/J8OFfYBCQJCQKEBAFCggAhQcCIIZXuaehNwJWMGVIp\nq/2wm4ArGTWkTVfWF6UkJBozakiH/aqUu81wm4ArGTekw2G76o/wHrb/f2GqPE0M1zR2SM8p\nrbuzrQiJxowf0rPtw2ohJG7JVUIabBNwJUKCADMbIEBIECAkCBASBLQVklO1TFRLIR0rkhJT\n1FRIY20efquhkMpPn4SrEhIECAkCGgrJeySmq6mQjNoxVS2F5DwSk9VWSDBRQoIAIUGAkCBA\nSBAgJAgQEgQICQKEBAFCggAhQYCQIEBIECAkCBASBAgJAoQEAUKCACFBgJAgQEgQICQIEBIE\nCAkChAQBQoIAIUGAkCBASBAgJAgQEgQICQKEBAFCggAhQYCQIEBIECAkCBASBAgJAoQEAUKC\nACFBgJAgQEgQICQIEBIECAkChAQBQoIAIUGAkCBASBAgJAgQEgQICQKEBAFCggAhQYCQIEBI\nECAkCBASBAgJAoQEAUKCACFBwJgh7dfd86/3i1KWjwNtAq5jxJB2XSmH/fMvveUgm4ArGTGk\nu7LaP/9yt3tu6q6sh9gEXMmIIZWyf/nl+SivdENsAq5k1JCef+nKhz98+fQHf9wEXMmoh3bb\nw+G+/6V/RfrxTZKQaMyIIW1Lt94eVt1zSZtF2QyxCbiSMYe/N937sdv9MJuA6xj3hOzj3aKv\naHW/G2wTcA1mNkCAkCBASBAgJAgQEgQICQKEBAFCggAhQYCQIEBIECAkCBASBAgJAoQEAUKC\nACFBgJAgQEgQICQIEBIECAkCakN6WBwOu0VZPKV26P+bgOmrDGnTL9N9XPcxWpKQaExlSMvy\neNiWxeHxzA2PKjYBDagMqX9B2vb3OsreQEJINCYQ0qpfEF9IzFr1od12098zzKEd81Y/2HC8\ns0T5+TYtNZuABlQPf3fHu8EuztymvGYTMH1OyEKAkCCgOqTN6jhyd+bOYVWbgMmrDWl5ugd5\n6aIlCYnGVIb0UJb7PqSHchfbpYOQaE5lSF3Zn87FOiHLrAVmNggJKkNavLwi9RNXg4REYzLv\nkTZdeYjt0kFINKd21G5VTqJT7YREayLnkcoqO0NISLTGzAYIEBIEVIRUPrvyXsE1CQkCHNpB\ngJAgIBXS06p2T85uAqarNqS190hQHdJ7RxY/Yc6qL6N4PCzLbrecypLF4ZdGuEzgMor751ej\n7TTWtRvgig64RCCkTT/zexrvkUrV34Y/qwxp9XxotyuLw9MkQipffoexJG7rclwAZQprNgiJ\na6kd/r7v/3RXjsut5giJxtzWzAbvkbiSGwvJqB3XcWsrrTqPxFVYaRUCrLQKAVZahQArrUKA\nlVYhwEqrEGClVQiw0ioE3NbMBriS2ssospNVv9sENCAw/D0AIdGYwPD3AIREYypD2q+W0VVP\nvtkENKD60M66diAkiDD8DQFCggAhQYCQIEBIECAkCBASBIwf0sOilNWZuykJicbUhvSwOBx2\ni7K4YKLQ6Zzt8nT69udZ40KiMYlF9Lu+jPMlHUNal/X+Ob31z5emC4nGVIa0LI/HhU8eL7jW\n/BhSd5ouvv95sRQh0ZjA9Ujb/jjtgrl2n5bt+v/jSxlo4h4MLxDSqr8R86Uh3b2G1IX3Cq6p\n+tBuu+mbuOzQbnX/sCn9Oin79c+jDUKiMfWDDaXc95GcGdA+vB+7HT/sfryyVkg0pnr4uzu+\ntiwuWY9ru314WK2OQw7rn69QFxKNMbMBAoQEAZGVVid0xz64itqQ3LEPDu7YBxGVIbljH/QC\nMxuEBIEli92xDzLvkdyxj5mrHbVzxz44uGMfRJjZAAFCgoDA8PdR9+OFejWbgAaEQto5j8Ss\nVYS0+bTKgvNIzFnNK9LiY0fRO2AKicak3iNlCYnGGLWDACFBQG1I929vlFJ79L9NwPRVhnTv\nruZwCFzYF531/d0moAFG7SCgMqRV+Xmlxz8SEo2pDGnXLaNnYr/ZBDSg+tDOYAMICSKckIUA\nIUGAtb8hwNrfEGDtbwiw9jcEWPsbAqz9DQHW/oYAa39DgLW/IcDMBggQEgRUhHQa+jb7G4QE\nEQ7tIEBIEFAb0n7d3xipW2fXQBESjale/ORlpp3LKJi1ypCW5a5/Ldqvyyq1R183AQ1ILRBp\n1I5ZC1yP1NsLiVmrDGldjgtEPi3LOrVHXzcBDYis2WD2N3NXfR7psZ/9vQzfk0JINMYJWQgQ\nEgSYtAoBQoKAipDW99E9+W4T0IjqV6To3nzdBDSiKqSdkOCoIqS78smV9wquqSKk/UpIcJKa\n/Z0lJBojJAgwswECIksWu/Ulcxe5jMKtL5m7zG1d3PqSmQtcau6OfRAYtRMSVIbk1pfQy7xH\ncutLZq521M6tL+Hg1pcQYWYDBAgJAurXtVs6tAMrrUJA9fB3t3n+zfA3M1d9QnZ7/N0JWebt\nKvdHOvtgIdGY2CtS95t/QUjcmBHfI31edOjHDQuJxow4avfUCYlblbk/0mXnkfarsjxeSPtt\nRYOt7QXDG3dmw2MpfXLeI3FrRp4itFuW1V5I3JzakPbrfriuW+8v/dv3pdsIiVtTGdKue7nQ\n/PJVhLaL8++BhERjKkNalrv+tWi/LqvL/4E7IXFrrjKz4VebgAYEluPq7YXErFWGtC7Lp+ff\nnpZlndqjr5uABrgeCQIyMxuW0auRhERzrNkAAUKCACFBgJAgQEgQICQIEBIE1C5+cp+9C/M3\nm4AGVE9aLUO0JCQaUxnS/vFuiJaERGMC75Ge7hfploREYzKDDdt+pa3gfDsh0ZhISJtleAa4\nkGhMfUj7++eXo8Vm/1zTLy43/9UmYOpqQ3rqBxvWpwXAc1fJConGVC+iXxYPr0tx/Woh/Ys3\nAQ2oPY+02sR25R+bgAbUnkeK7cg/NwENMNcOAoQEAUKCACFBgJAgQEgQUL9A5PLiW1/+dRMw\neZYshoDKkB5K109t2HTJiyiERHOq59qd5qtuyyKzP//fBDTAjcYgIPaKFJv5/XUT0ID5vUc6\nfyto+LW5jdq93IR9sH+fmcrcaKyd80hl4H+fmZrZzIby5XfIEBIEVIRUPrvyXv3uHxYSWTML\nyXskhlF7aLc6Dn8/dXeh/flmE9l/2agdQ6gMaf12Qnad2Z//byLNeSQGYIoQBFSG1JkiBIfA\noV33dDhOEbpP7dHXTUADUlOEYuvn/38TMH2hKULhhYuFRGNmNrMBhiEkCEiF9BR9kyQkGlMb\n0rqxKUIwiOrh71fR4QYh0ZjqE7KPh2XZ7ZblKbZLByHRnMAUofvnV6Nt9lpzIdGYQEibfuET\n75GYtcqQVs+HdruyODwJiVmrDGnTB3ScJhS9IElINKZ2+Pu+/9NdyV6OJCRaY2YDBAgJAoQE\nAdVThDpThCA3RUhIzFn1CdnoXSi+2wQ0ILWKUJaQaEz1od0+tiv/2AQ0oHrxk+UutSv/2gRM\nX21IG4MNUB3SvVE7OAQu7DNqB0btIKL60M6oHQQuo1hGF2v4bhMwfdWHdgYbQEgQ4TIKCBAS\nBFSE1B/N/eXQ7qErizNnn4REY8YMabsq3cPLZIif15MUEo0Z8dBueyxoXe72h93q5xkRQqIx\nI4Z016/ZtT7dtXlfFkNsAq4kNUWoO39X89NjX+42+/9DwVL+8oYLJiEU0u6C7/3TQx5Px3Tl\nx/CERGMqQtp8eg358VDt6K5/d3Syv/t5aVYh0ZiaV6TFx47OT7nbd+V9wO/nI0Eh0ZhRL6NY\nv+bTnVkqXEg0xswGCKgN6eH5vdFuccmR3Z83AdOXuD/ScdVi95BlzipDWpbHw7YsDo/uIcus\nBQYbtv1QtuuRmLVASKuyERIzV31ot93054Qc2jFv9YMNpdz3L0ib2C4dhERzqoe/u+Nkn8Vj\naH++2QRMnxOyECAkCKgOabM6jtxlb+4iJBpTfX+k02V4pYuWJCQaUxnSQ1nu+5Aeyl1slw5C\nojnVt3XZn87FOiHLrAVmNggJKkNavLwibS+41PyPm4AGZN4jbcJ37hMSjakdtVu9rNkQnWon\nJFoTOY9UVtkZQkKiNWY2QICQIEBIECAkCBASBAgJAoQEAUKCABf2QYAL+yDAhX0Q4MI+CHBh\nHwS4sA8CXNgHAS7sgwAX9kGAmQ0QUBnSah3bk39tAhoQGP4egJBoTGD4ewBCojGVIe1Xy6fY\nvny/CWhA9aHdm9guHYREc4QEAYa/IUBIEJAa/u66xN58twloQCiknfdIzFpFSJvykcsomLOa\nV6TFx46ip5OERGNMEYIAo3YQICQIqA3pfmFmA9SGdG+KEBwC69pFFz35bhPQAKN2EFB7qbkL\n++BQHdKuc2EfuB4JIoQEAU7IfrP1gYZQuGFC+t+28zfX4PZFliy+qVtflqvvAQ2qDenmbn1Z\nvvwOl8jc1uWGbn0pJP6ieorQrd36Ukj8RWCK0G2F5D0SfxFY+/vGbn1p1I4/yLxHuq1bXzqP\nxK/Vjtq59SUcQueR3PqSuTOzAQKEBAFCggAhQYCQIEBIECAkCKhdRWgd25N/bQIaMOa6dvu7\nUpabS/6ikGhMYNLqpfbdcTLR6vSPCIlbUhnSfnX5unbrfmLr/qE7TssTEjdlxOW4utNDdt1i\nJyRuzIghvT5kv1x+F9KnO9L+fq/gmkYc/n5/P7VYekXitowY0vsCKbuyFBI3pTqkx+XF1yOt\n3+rZnDl6ExKNiaxrd+kVstvV60e7OyFxS6rXbOj6M6y3tWYD/Fr1Cdnt8fcbWkUI/iA1Reh2\n1rWDP4i9InWZ/fn/JqAB3iNBwKijdn/bBExf/Xkk69qBK2QhwRWyEDDmFbJ/2wQ0YMQrZP+4\nCWjAiFfI/nET0IARL+z74yagAUKCAMPfEGD4GwIMf0OA4W8IMPwNAUbtIEBIEGD4GwKEBAHV\nIW1W/VHdahfan+82AZMXudT8+b910ZKERGOqFz9Z7vuQ3tf1jhASjakMqSv70+wGo3bMWmCK\nkJAgMEWob8iSxcxb5j2SBSKZudpRu5UFIiF0HskCkcydmQ0QICQIEBIECAkChAQBQoIAIUGA\nkCBASBAgJAgQEgQICQKE1K7wYoLUEFKrBrgwmb8TUqvKh1+5OiE1qnz5nesSUqOENC1CapSQ\npkVIrfIeaVKE1CqjdpMipHY5jzQhQoIAIUGAkCBASBAgJAgQEgQICQKEBAFCggAhQYCQIEBI\nECAkCBASBAgJAoQ0CJcKzY2QBjCZi1f1PBohDWAiyylMpuc5EFLeVBb4mUjP8yCkvImENJHd\nmAkh5U3kO3giuzETQhrANI6phDQmIQ1gIu/yp9HzTAhpEJMYd55Iz/MgpFs2iZ7nQUgQICQI\nEBIECAkChAQBI4ZUPhtiE3AlI4b08HNIF1cG0zPmod22Ww69CdL8VLvMqO+RtmU99CaIMjni\nUuMONjyU7dCbIMl0vUsZtePfTCC/mJD4NyFdTEj8m5AuJiR+4D3SpYTED4zaXUpI/Mh5pMsI\nCQKEBAFCggAhQYCQIEBIECAkCBASBAhp1pxuTRHSVI3wPW4CUI6QpmmU73FTUnOENE1jfI+7\nSCJISJM0yve4kIKENElCao2QJmmc73HvkXKENE2jfI9nRjQMofeENE0jjUzXR2AI/URIV3L2\nW7iRH/QOD0+EdBU383PcgMULIV3FzfwcF9ILIV3D7Xz73c5XUklI13BD334389paSUjXcEsh\n3cq7vUpCuopb+jneyPDiwIR0FX6O3xohXYmf42Mb9hkXErMw9DGAkP7Aq0l7LnlXWjPbREi/\n5v1Ngy4YJz37//XHBwjp125pxG02Lgmp6gFC+q0bOgd0S84clp3/v3b2ET8/QEi/JaQJOn+4\nfeHrjZBGI6RruOgF58eQzr4D+vL7Lx8gpF/zHml05yq46IfbuTE575FGZtQurvZ7PHKUYNRu\ndM4jRQ191PWLHXEeiXbVjwNM4HBbSAxt+JHpCRxuC4lh1R+4XfSCc+3DbSExrMCB2wRecM4S\nEoPKvN5c/QXnLCExqNt4vTlPSAwqcq60AUJiWNcfmR6FkBjWTRy4nSckhnYDB27nCQkChAQB\nQoIAIUGAkCBASBAgJAgQEgQICQKEBAFCggAhQYCQIEBIECAkCBASBAgJAoQEARMNCRrzh+/y\nfDitaeYpaGVHZ7mfrXzRA2rmKWhlR2e5n6180QNq5iloZUdnuZ+tfNEDauYpaGVHZ7mfrXzR\nA2rmKWhlR2e5n6180QNq5iloZUdnuZ+tfNEDauYpaGVHZ7mfrXzRA2rmKWhlR2e5n6180QNq\n5iloZUdnuZ+tfNEDauYpaGVHZ7mfrXzRA2rmKWhlR2e5n6180QNq5iloZUdnuZ+tfNEwaUKC\nACFBgJAgQEgQICQIEBIECAkChAQBQoIAIUGAkCBASBAgJAgQEgQICQJmHtKf10wf18PrHq67\n0q33V92Xn7zu57Sf1ofF25OYez6n+sWOYzvt/+Ovtq97uDzu7eK6e/Nvr/s57ad1fdy3rs8n\n+HxO9Isdybasrr0LF9h2L9+TT6Xb9n96uvIO/cPbfk76ad2Wu33/2nmXfT7nHdJDub/2Lpz3\nUJYv36Drsnn+9XGiO/2+n5N+Wlenfex3Nfl8zj2kh2vvwnllfXj5Bl2V3WG6P+/f97OFp7Xf\n1eTzOe+QVmVz9/xu89q78bPt4fUb9PNvU/O+nw08rfuyzD6f0/x/MpbV6U3x8tr7cU4TIR0+\nhDT5p/WhP6oTUkopj88/nNaTPxJpLKTpP627rj+cE1LWfroDyi8aC+lkwk/rvju+WgopbLrf\nmS9edrBrKqQJ7+fylHjy+Zzs1zqm6f4ff/Fp1G430VG7Qysh7RbL3fGD5PM50a91JF3pz29P\n+Dvzxcu35P3xvMemTHY87O2Vc8pP6+ZtFCT5fM47pHX/HO5P5+WmrI2ZDW/7Oemndfc+mmhm\nQ8q+O47TTvYn/KvXg6TFxIeVX/Zz0k/rXXmfCRh8Pucd0vOPza4spjtK++o1pP1xtvJ19+Un\nH/dzqk9r+RBS8PmceUiQISQIEBIECAkChAQBQoIAIUGAkCBASBAgJAgQEgQICQKEBAFCggAh\nQYCQIEBIECAkCBASBAgJAoQEAUKCACFBgJAgQEgQICQIEBIECAkChAQBQoIAIUGAkCBASBAg\npFbs70pZX3rb8EnevfWmCakVq1LK/YUhLfxvHZtnvBWl7H7x2AF3hO94xlvxmziENDrP+GSs\nu7I8veg8LN7uCf78Ydd/+HIj7lMhr488/en1If1r1qp09y8P/vSpw2ZZytI7p+EIaSqW/Xd/\nt3/9qCz7/7h6/fBjSG+PPP7p7SHPf+z6D+/fQnr/1MPp7z9c78u7dUKaiMey3B/uyrr/qNse\ntl15fH4d6f/jfln6l5JjGv0v74/s//ThIaX/8KEsXl+qPnyqK9v+Ly6u+zXeMiFNxKo8HQ77\n0vUf9d1s+leSVelfofZldfgQ0vsjT396e0jpP3H8j6eQPn3KYd2whDQR7+MDLx+dgnhx+BDS\n50d+eMjpEx8/evvUupTVdjvqFzQzQpqIYUM63Pdvn7rLB9D5JSFNxD9C+vKA70L68k98Turd\nZr3wHmk4QpqI5f/eI61ePzx5C2n55T3S5tMjPr1H+vLGyOml4XhqJ+KhH2Jbfxm1O374/KlP\ngw3vjzyN4b095GNI/UHch08tTv+aV6TBCGkqvj2PdPqwezv7+s15pPeHvIe0KP0L1odPPZ7e\nLD1d64u7fUKajH5k7WVmQ/dxZkO5O/7X95DeHvk2feH0kPeQnhbHkD787ePMBh0NR0gQICQI\nEBIECAkChAQBQoIAIUGAkCBASBAgJAgQEgQICQKEBAFCggAhQYCQIEBIECAkCBASBAgJAoQE\nAUKCACFBgJAgQEgQICQIEBIECAkChAQBQoIAIUHAf7TGHLfwWpT5AAAAAElFTkSuQmCC",
      "text/plain": [
       "plot without title"
      ]
     },
     "metadata": {
      "image/png": {
       "height": 420,
       "width": 420
      },
      "text/plain": {
       "height": 420,
       "width": 420
      }
     },
     "output_type": "display_data"
    }
   ],
   "source": [
    "val.errors = rep(NA, p)\n",
    "a = rep(NA, p)\n",
    "f = rep(NA, p)\n",
    "for (i in 1:p) {\n",
    "    coefi = coef(regfit.full, id = i)\n",
    "    a[i] = length(coefi) - 1\n",
    "    f[i] = sqrt(sum((B[x_cols %in% names(coefi)] - coefi[names(coefi) %in% x_cols])^2) + \n",
    "        sum(B[!(x_cols %in% names(coefi))])^2) #función dada\n",
    "}\n",
    "plot(x = a, y = f, xlab = \"coeficientes\", ylab = \"error entre estimado y coeficientes reales\")"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 51,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "14"
      ],
      "text/latex": [
       "14"
      ],
      "text/markdown": [
       "14"
      ],
      "text/plain": [
       "[1] 14"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    }
   ],
   "source": [
    "which.min(f)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "El modelo con 9 coeficientes (10 con intersección) minimiza el error entre los coeficientes estimados y reales. El error de prueba se minimiza con el modelo de 14 variables. Un mejor ajuste de los coeficientes reales medidos aquí no quiere decir que el modelo tendrá una prueba MSE más baja."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**11. Ahora intentaremos predecir la tasa de criminalidad per capita en el set de datos de Boston.**"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "- *(a) Pruebe algunos de los métodos de regresión explorados en este capítulo, como la mejor selección de subconjuntos, lasso, ridge y PCR. Presente y discuta los resultados de los enfoques que considere.*"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 52,
   "metadata": {},
   "outputs": [],
   "source": [
    "set.seed(11)\n",
    "library(MASS)\n",
    "data(Boston)\n",
    "library(leaps)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Selección del mejor subconjunto**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 53,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "image/png": "iVBORw0KGgoAAAANSUhEUgAAA0gAAANICAMAAADKOT/pAAAAMFBMVEUAAABNTU1oaGh8fHyM\njIyampqnp6eysrK9vb3Hx8fQ0NDZ2dnh4eHp6enw8PD////QFLu4AAAACXBIWXMAABJ0AAAS\ndAHeZh94AAAfVklEQVR4nO3diXbaOhRGYZk5hOH937bYBEoIk61fx+fI+1t33aZpLXnaBQyE\ndASQLY29AkANCAkQICRAgJAAAUICBAgJECAkQICQAAFCAgQICRAgJECAkAABQgIECAkQICRA\ngJAAAUICBAgJECAkQICQAAFCAgQICRAgJECAkAABQgIECAkQICRAgJAAAUICBAgJECAkQICQ\nAAFCAgQICRAgJECAkAABQgIECAkQICRAgJAAAUICBAgJECAkQICQAAFCAgQICRAgJECAkAAB\nQgIECAkQICRAgJAAAUICBAgJECAkQICQAAFCAgQICRAgJECAkAABQgIECAkQICRAgJAAAUIC\nBAgJECAkQICQAAFCAgQICRAgJECAkAABQgIECAkQICRAgJAAAUICBAgJECAkQICQAAFCAgQI\nCRAgJECAkAABQgIECAkQICRAgJAAAUICBAgJECAkQICQAAFCAgQICRAgJECAkAABQgIEDEJK\nQDADznJ9OCNMASgREiBASIAAIQEChAQIEBIgQEiAACEBAoQECBASIEBIgAAhAQKEBAgQEiBA\nSIAAIQEChAQIEBIgYB/SZpbSYjtsikHv6AXKMwzpHMH8/A731YApugFICR5Zh7RKq8PxuF+l\nTf8pUtb0QEHWITXp0H59SLPeU6RXfwiMyjqkyz2z1/fQCAnBWIe0vITU9J6CkOCXaUiL9Wab\nvk5fHlavrzbwGAnBmIZ0/ZGUKTWH/lNw1Q5uWT6PtNttNotFd8lh9bIjnkdCNLyyARAgJECA\nkACBsUIa8DwS4BchAQLctQMECAkQCBcSjcGjUUJ6+7QqISEYPyF9+Mm2hASPRnit3QefAk1I\nCMYwpO+GkFAry7t2h0Wa77sReIyEytg+RvpK3duRckKiJHhkfLFhP0+LAyGhOuZX7dap2RIS\namN/+Xs3e//2PEJCMGM8j7QkJNQm3EuECAke+Xllw6dTEBIcIiRAINxLhAgJHoV7iRAhwaNw\nLxEiJHgU7yVClASH4r1EiJDgULyXCBESHIr3EiFCgkPxXiJESHAo3kuECAkOERIgQEiAACEB\n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\nUX7XoC9OhChTVblRftegL06EKFNVuVF+16AvToQoU1W5UX7XoC9OhChTVblRftegL06EKFNV\nuVF+16AvToQoU1W5UX7XoC9OhChTVblRftegL06EKFNVuVF+16AvToQoU1W5UX7XAKgAIQEC\nhAQIEBIgQEiAACEBAoQECBASIEBIgAAhAQKEBAgQEiBASIAAIQEChAQIEBIgECykzSw1q4PR\nZN9GO2e3TGm5t5jpsGpM9t/msufKz3edyvTU+CtWSKvuowIam911aGx2ztZso/bNearS0e4u\nH+cw7+abWUxlemo8ECqkXVoe2n+DliazLYZ8uscATbM7HhZpVX6mZTfJqvT+2zU/e+47nTbt\n9Lvv8lPZnhoPhAppcV5bmxP8a9DH5AyZpz27D6kpP1Uy2X+bNP+ZYZW2x3YD1+WnMj01HgkV\n0g+TvbW/HqPClmlnMU3r575q4WZP/zBcz+72TuQuLcpPdfkGIX3ukOYGs8zT3uaozNJx3XR3\nTIpb/9y1K3YL0dnd3/SV24+7u8FtTo2HAoa06e4wFLZOX0b/vKW06B4mW8y1aa82NJvi81iF\ndD+4yanxZD3GmniwfVPsnsJ/3d0Rq5Daiw3LwjcTZ+vu0lb5mUYKyeTUeLYeo8080KGxuPWe\ntddRrUJqHyPti14k/rFp79qdmi1+kzROSDanxrP1GG/qYeYGJ9xx2d1FsArp9peiZql9JHYo\n3+zPxjS2IZmcGk/XY8S5B9jP5hYvAcj5nPi+DC/cmjX766rdvtxVu+PNxhidGk/XY8S5+9sa\nXZWxDGnd3frtLbbsfAth8JTVz347b9q26HPNl0NkdWo8XY9RZ+/J5Gz7z+au3enR0aF94PJV\nfqpVal+Mtir/IgqzVzZcpzI+NR6sx7jT97O0u51oGc1zvpRmch7Mjaa67LlZ+fl+pjI+NR6s\nx1gTD2F4h+s8nc0823lqDF5p1+pejV1+msueO5Sf7/q4j5CA+AgJECAkQICQAAFCAgQICRAg\nJECAkAABQgIECAkQICRAgJAAAUICBAgJECAkQICQAAFCAgQICRAgJECAkAABQgIECAkQICRA\ngJAAAUICBAgJECAkQICQAAFCAgQICRAgJECAkAABQgIECMlA6j6U+PjuMwB7ftzcYZk++DTY\nu0Fvfjvep9vViJ1pIF0+R1wa0iKltP5g7me/JSQldqaB6xkvDSml/ZBVGTodXmJnGkhpdj7p\nxSENWpW85fEEO9NASru0OH9xOX9/vlqn5nRbtTo/2Dn9fnX9EPDNLDWb8988zM5LX74/2xwv\nH+PdfeuQZt2vs3Q4bk93+M5D/CzX/Z3b717nOC99naf9cPU03xbdERUjJAOnU3aZvo9/Q1q3\nMbQncFdSSu3DnjRv/7z7qvuy++71osL88v2bkE7fbG/v9qdvr8/fXv1frv0799+9DPxrns35\nL20sd0xFCMnA6ZQ932rchzQ/tOdv9/+muyaxO+6a9HW6dWi/eZi3V/u6P7/4+v9Xbu6afXUP\nwdanv53aP/nq/uRnufNEN9+9DtD+/maeJu3avzQz3TP1ICQD7Sm7af+tvw/pfCu1v/6+vWO1\nbe/HLVIbwaH98vy3fix+/sr1FuVngvb0n6Xb+S7LpfvvXudof/9rHu7WZSAkA90p3D6C+fMY\n6fj39z9fpst9t1/XBG7+yu0fLE8x7s/3//bb9fz2j8+/PPru3TynB2qL3a7ULqgeIRnozt7v\ntCwW0vfpvt2quwWaXx873f7Vh9+9m+e4bk6/NgMuqeNISCbOZ+8i7XqEdLfw79/ch3RsZu1/\n7U3TbLPd3yfz+Lt/Kj1uVzMeIw1ESAZ+7l6l2fXc/X4cUnub8vMYaft74R+L/w9xfv3BKm26\nCw7d9x4mc/3udY7zY6S7B0Y8uTQQ+83Az9m57u5CzdKmvU72MKTzFbXtz9W54+Zyvl89vmrX\nVZLO1+i+j7sHj4Zuvnudo/39zTyz86U9bpGGISQDl1O+OV++S92TOY9CWnZ/1v7+/KimfcTy\n+zbi+jzS3R/Mzt9b/Tzk+f4V0q/vXue4efTUzvN1/TsYgJAMXE757eVB/f1lh+s9sFX3SofW\n5nQ/cLk/3od03DTnVzb8uak630c7ZTL/3t7cknW//PruZY7zX7jOc35lAx0NREiAACEBAoQE\nCBASIEBIgAAhAQKEBAgQEiBASIAAIQEChAQIEBIgQEiAACEBAoQECBASIEBIgAAhAQKEBAgQ\nEiBASIAAIQEChAQIEBIgQEiAACEBAoQECBASIEBIgAAhAQKEBAj8A8ys72p6wjfZAAAAAElF\nTkSuQmCC",
      "text/plain": [
       "plot without title"
      ]
     },
     "metadata": {
      "image/png": {
       "height": 420,
       "width": 420
      },
      "text/plain": {
       "height": 420,
       "width": 420
      }
     },
     "output_type": "display_data"
    }
   ],
   "source": [
    "predict.regsubsets = function(object, newdata, id, ...) {\n",
    "    form = as.formula(object$call[[2]])\n",
    "    mat = model.matrix(form, newdata)\n",
    "    coefi = coef(object, id = id)\n",
    "    xvars = names(coefi)\n",
    "    mat[, xvars] %*% coefi\n",
    "}\n",
    "\n",
    "k = 10\n",
    "folds = sample(1:k, nrow(Boston), replace = TRUE)\n",
    "cv.errors = matrix(NA, k, 13, dimnames = list(NULL, paste(1:13)))\n",
    "for (j in 1:k) {\n",
    "    best.fit = regsubsets(crim ~ ., data = Boston[folds != j, ], nvmax = 13)\n",
    "    for (i in 1:13) {\n",
    "        pred = predict(best.fit, Boston[folds == j, ], id = i)\n",
    "        cv.errors[j, i] = mean((Boston$crim[folds == j] - pred)^2)\n",
    "    }\n",
    "}\n",
    "mean.cv.errors = apply(cv.errors, 2, mean)\n",
    "plot(mean.cv.errors, type = \"b\", xlab = \"Number of variables\", ylab = \"CV error\")"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "Vemos que la validación crizada selecciona el modelo de 12 variables. Tiene un MSE igual a 41.0345657"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**Lasso**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 54,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "image/png": "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\npEAfKC6xJ1wAAAAASUVORK5CYII=",
      "text/plain": [
       "plot without title"
      ]
     },
     "metadata": {
      "image/png": {
       "height": 420,
       "width": 420
      },
      "text/plain": {
       "height": 420,
       "width": 420
      }
     },
     "output_type": "display_data"
    }
   ],
   "source": [
    "x = model.matrix(crim ~ ., Boston)[, -1]\n",
    "y = Boston$crim\n",
    "cv.out = cv.glmnet(x, y, alpha = 1, type.measure = \"mse\")\n",
    "plot(cv.out)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "Aquí la validación cruzada selecciona una lamda igual a 0.0467489 y el MSE igual a 42.1343"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 55,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "image/png": "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\nAAAAAElFTkSuQmCC",
      "text/plain": [
       "plot without title"
      ]
     },
     "metadata": {
      "image/png": {
       "height": 420,
       "width": 420
      },
      "text/plain": {
       "height": 420,
       "width": 420
      }
     },
     "output_type": "display_data"
    }
   ],
   "source": [
    "cv.out = cv.glmnet(x, y, alpha = 0, type.measure = \"mse\")\n",
    "plot(cv.out)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "Aquí la validacion cruzada selecciona una lamda igual a 0.53749 y un MSE igual a 42.98345"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "**PCR**"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 56,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Data: \tX dimension: 506 13 \n",
      "\tY dimension: 506 1\n",
      "Fit method: svdpc\n",
      "Number of components considered: 13\n",
      "\n",
      "VALIDATION: RMSEP\n",
      "Cross-validated using 10 random segments.\n",
      "       (Intercept)  1 comps  2 comps  3 comps  4 comps  5 comps  6 comps\n",
      "CV            8.61    7.209    7.203    6.764     6.75    6.780    6.822\n",
      "adjCV         8.61    7.206    7.200    6.759     6.74    6.775    6.814\n",
      "       7 comps  8 comps  9 comps  10 comps  11 comps  12 comps  13 comps\n",
      "CV       6.817    6.698    6.728     6.729     6.720     6.687     6.622\n",
      "adjCV    6.808    6.689    6.717     6.716     6.708     6.673     6.608\n",
      "\n",
      "TRAINING: % variance explained\n",
      "      1 comps  2 comps  3 comps  4 comps  5 comps  6 comps  7 comps  8 comps\n",
      "X       47.70    60.36    69.67    76.45    82.99    88.00    91.14    93.45\n",
      "crim    30.69    30.87    39.27    39.61    39.61    39.86    40.14    42.47\n",
      "      9 comps  10 comps  11 comps  12 comps  13 comps\n",
      "X       95.40     97.04     98.46     99.52     100.0\n",
      "crim    42.55     42.78     43.04     44.13      45.4\n"
     ]
    }
   ],
   "source": [
    "pcr.fit <- pcr(crim ~ ., data = Boston, scale = TRUE, validation = \"CV\")\n",
    "summary(pcr.fit)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 57,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "image/png": "iVBORw0KGgoAAAANSUhEUgAAA0gAAANICAMAAADKOT/pAAAAM1BMVEUAAABNTU1oaGh8fHyM\njIyampqnp6eysrK9vb3Hx8fQ0NDZ2dnh4eHp6enw8PD/AAD///89ODILAAAACXBIWXMAABJ0\nAAASdAHeZh94AAAbqUlEQVR4nO3diVbqOhiA0ZShIAKH93/aS4sDDiDDnzTt3Xutq+hBUoHv\ntglV0wF4Whp6A2AKhAQBhAQBhAQBhAQBhAQBhAQBhAQBhAQBhAQBhAQBhAQBhAQBhAQBhAQB\nhAQBhAQBhAQBhAQBhAQBhAQBhAQBhAQBhAQBhAQBhAQBhAQBhAQBhAQBhAQBhAQBhAQBhAQB\nhAQBhAQBhAQBhAQBhAQBhAQBhAQBhAQBhDRaKXnw6uGxGC0h1cRjMVpCqonHAgIIaQz27Syl\n+aa/fNwR7Wap/dgjde/WszR7PRzWTZq/Drqh/19CGoFdk3pt98HxfVfVeUjz/l93bf9OSYMQ\n0gi8dZRSt086XXo5D+nk7VqLgTf2f0pI9VsfI9ke9sf9zuxw2gPtD4cve6R9d5002/bvBt3W\n/y13e/0Wp13RfrbaHfpwPiZLb+9ev7wbbDv/19zt9fsax/Gj/fmnf31Hae72+v0I6csFIVXB\n3V4/IY2Au71+8+9zpNOnhVQTd3v9fqzanT4tpJq420fg43Wk9UFIlXK3j8DrtzMbTp8VUk3c\n7WOwb48pLb68fCSkurjbIYCQIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQ\nIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQIICQ\nIICQIICQIICQIICQIMCTIa1nH38kGP7HHg3p9Mez52d/th7+x54KqU3t/nDYtWkduUkwPk+F\n1KR9d3mfZtevCuPyQBAPZfQW0vuA1we2nsHIlA5p+R5Sk2MIGEjRkBar9Sa9HC/u2+urDUJi\nZIqG9HEwmVKzzzEEDKRgSIftdr1eLPolh/ZqR0JibEqGVNUQEKmekJ5cS4QhlZwjNa+5h4CB\nlF1sWFyfGj09BAykaEibJv2xyvDkEDCQsi/I7hcpLW8481tIjEzpMxu2i+4Ib721/M2klA7p\nmFLb/LkwJyRGpnxIR9v1YiYkpmSQkLINAQMREgSo58yGwkNAJCFBACFBACFBACFBACFBgJGF\n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\nQoQEAYQEASYekkkSZQgJAggJAggJAggJAkw8JMt2lCEkCCAkCDD1kEySKEJIEEBIEEBIEEBI\nEGDqIVm2owghQQAhQYDJh2SSRAnTDymdibtZ+GL6If37d3rbvU/9+2NR/770JTCeNfmQLrkU\n2D/HgjzgfxvSRULiAUKqa3BGSkh1Dc5ICam20RklIf1klsTdhPSTv+HM3YT0C7sk7iWkXwiJ\newnpN0riTkKqcXxGR0h1bgAjI6Q6N4CREdKvrIBzHyH9SkjcR0i/s27HXYT0O7sk7iKkC+yS\nuIeQLqlhGxgNIV1SwzYwGkK6qIqNYCSEdJFZErcT0kVC4nZCukxJ3ExIlwmJmxUN6XW16H+x\n6aJ9zTVEKCVxq4Ih7WdnvyR4nmWIYJVsBiNQMKQ2NS/b/tJu06Q2xxDRatkOqlcwpCZtPy5v\nU5NjiGi1bAfVKxjSlz/6cP0vQNTyBDZJ4kb2SNc4B5wblZ0jbXb9pdHMkeySuFHJ5e/52ard\nbJ9liGh2Sdym7OtIbf86UrNYjeN1pINdEjdyZsN19WwJVasnpEr/qGtFm0LFyoe0nqW02GQd\nIlJFm0LFir+O9LbicHXRrqpnr1kSNygdUpva/eGwa9M6xxA5CIkblA6pSf269z7NcgyRgxVw\nblA6pPd1hHGcItSzS+JvpUNavoc0ilOEekLib0VDWqzWm/RyvLhvR3KKUK+uraFKRUP6eI0o\npWYcpwj16toaqlTydaTtdr1eLPolh/ZqR7U9dSvbHCpUz5kNhYe4h1kSfxHSDayA8xch3cIu\niT8I6RZC4g9CuomSuE5IN6lug6iMkG5T3xZRFSHdpr4toipCuo0VcK4S0m2ExFVCupF1O64R\n0o3skrhGSLeyS+IKId2syo2iEkK6WZUbRSWEdLs6t4oqCOl2ZklcJKTbCYmLhHQ7K+BcJKQ7\n2CVxiZDuYJfEJUK6R63bxeCEdJdqN4yBCeku1W4YAxPSXSw38Dsh3cVyA78T0n3skviVkO5j\nl8SvhHQnuyR+I6R71bxtDEZI96p52xiMkO5V87YxGCHdzSyJn4R0NyHxk5DuZgWcn4R0P7sk\nfhDS/eyS+EFID6h88xiAkB5Q+eYxACE9ovbtozghPcJyA98I6RGWG/hGSA+xS+IrIT1ESHwl\npMcoiS+E9Jj6t5CihPSgEWwiBQnpQSPYRAoS0oOsgHNOSA8SEueE9CjrdpwR0qPskjgjpIfZ\n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",
      "text/plain": [
       "Plot with title \"crim\""
      ]
     },
     "metadata": {
      "image/png": {
       "height": 420,
       "width": 420
      },
      "text/plain": {
       "height": 420,
       "width": 420
      }
     },
     "output_type": "display_data"
    }
   ],
   "source": [
    "validationplot(pcr.fit, val.type = \"MSEP\")"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "Aquí la validación cruzada selecciono la M igual a 14, el MSE de test igual a 45.6935"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "- *Proponga un modelo (o conjunto de modelos) que parezca funcionar bien en este set de datos y justifique su respuesta. Asegúrese de evaluar el error del conjunto de validación, la validación cruzada u otra alternativa razonable, en lugar de utilizar el error de entrenamiento.*"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "Como se observa en las respuestas anteriores el modelo con el menor error de validación cruzada es el elegido por el método de slección de sets."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "- *(c) ¿Su modelo elegido involucra todas las características del set de datos? ¿Por qué o por qué no?*"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "No, el modelo elegido por el mejor método de selección de subconjuntos solo tiene 13 presdictores."
   ]
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "R",
   "language": "R",
   "name": "ir"
  },
  "language_info": {
   "codemirror_mode": "r",
   "file_extension": ".r",
   "mimetype": "text/x-r-source",
   "name": "R",
   "pygments_lexer": "r",
   "version": "3.6.2"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 4
}
