---
layout:     post
title:      "Funciones de Singularidad"
author:     Oscar Campo
date:       2016-06-17 09:59:03
tags:       funciones de singularidad
categories: ingeniería, mecánica
---

$$\newcommand{\fsin}[3]{#1\left\langle x-#2\right\rangle^{#3}} $$

# Introducción#
Para casos sencillos de cargas transversales en elementos que hacen parte de sistemas más complejos, es posible determinar el estado interno de cargas mediante el método tradicional de las "secciones", pero para configuraciones complejas de cargas transversales, el método de las secciones se vuelve engorroso. para estos casos se propone el método de las funciones de singularidad.

![Viga Compleja](https://dl.dropbox.com/s/6hfnjig90od2x6g/VigaCompleja.jpeg?dl=0)

Una función de singularidad $$ \fsin{}{a}{n} $$ se define como:

$$\fsin{}{a}{n}=\left\{ \begin{array}{rlll}(x-a)^n & si & x \gt a \wedge n\ge 0 \\ 0 & demás & casos \end{array}\right.$$

# Propiedades de las Funciones de Singularidad #
las funciones de singularidad tienen las siguientes propiedades:
$$\begin{equation}
  \frac{d}{dx}\fsin{}{a}{n}=\left\{ \begin{array}{crl}
\frac{1}{n}(x-a)^{n-1} & si & n>1 \\ 
(x-a)^{n-1} & demas & casos 
\end{array}\right.
\end{equation}$$


Se puede modelar una viga con carga transversal simple, de la siguiente manera:

$$q(x)=\fsin{Ay}{0}{-1}-\fsin{P}{a}{-1}+\fsin{By}{l}{-1}$$

Ahora, se propone la siguiente notación:

$$q(x)=\left[ \begin{array}{rrrr} Ay & -P & By \\ 0 & a & l \\ -1 & -1 & -1 \end{array} \right]_{\langle{x}\rangle}$$
$$q(x)=\left[ \begin{array}{r} \vec{c} \\ \vec{a} \\ \vec{n} \end{array} \right]_{\langle{x}\rangle}$$

Donde $$\vec{c}$$ es el vector de cargas y reacciones, $$\vec{a}$$ es el vector de puntos de aplicación de las cargas y reacciones y $$\vec{n}$$ es el vector de exponentes de singularidad.

Con esta notación, la obtención de las expresiones de V(x), M(x), etc, se puede expresar como:

$$V(x) =\left[ \begin{array}{c} \vec{c} \\ \vec{a} \\ \vec{n}+1 \end{array} \right]_{\langle{x}\rangle}=\left[ \begin{array}{cccc} &\vec{c}& \\ &\vec{a}& \\ 0 & 0 & 0 \end{array} \right]_{\langle{x}\rangle}$$
