---
title: 試験数式。
date: 2021-07-24 17:04:01
tags: 2021年度
---

$$
\begin{align}
x^{-x}&=e^{\log{x^{-x}}}=e^{-x\log{x}}\\[5pt]
&=\sum_{n=0}^{\infty}\frac{(-x\log{x})^n}{n!}\\
&=\sum_{n=0}^{\infty}\frac{(-1)^n}{n!}(x\log{x})^n\\[10pt]
\int x^{-x}\space dx&=\int\sum_{n=0}^{\infty}\frac{(-1)^n}{n!}(x\log{x})^n\space dx\\[4pt]
&=\sum_{n=0}^{\infty}\frac{(-1)^n}{n!}\int(x\log{x})^n\space dx\tag{1}
\end{align}
$$

