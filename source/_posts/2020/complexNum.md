---
title: 複素数の複素数乗
date: 2020-10-3 0:02:25
tags: 2020年度
---

<div style="text-align: right">75期 tskk</div>

ぱっと思いついたので、複素数の複素数乗の計算についてまとめてみたいと思います。



> 公式1 複素数の複素数乗
>
> 複素数$z$、実数$p,q$について、
> $$
> \left\\{
> \begin{array}{l}
> \alpha = p {\rm Log} |z| − q \arg z \newline
> \beta = q {\rm Log}|z| + p \arg z \\
> \end{array}
> \right.
> $$
> として、
> $$
> z^{p+qi} = e^α (\cosβ + i \sinβ)
> $$
> が成り立つ。ここで、 ${\rm Log}(x)$は実数xの自然対数を、 $\arg(z)$は複素数zの偏角（多価関数）をそれぞれ表す。

（https://fermiumbay13.hatenablog.com/entry/2017/12/03/021235　参照）

### 用語説明

- 自然対数...ネイピア数$e$の対数

- 偏角...複素数平面上で複素数の点の動径があらわす一般角のこと（複素数zの偏角を$\arg z$と表し、単位はラジアン）

![pastedGraphic.png](https://upload.wikimedia.org/wikipedia/commons/thumb/7/7a/Complex_number_illustration_modarg.svg/220px-Complex_number_illustration_modarg.svg.png)

 $\varphi$が偏角で、$r$が絶対値

- 多価関数…多くの答えが出てくる関数（この場合、２πの整数倍を足したものも答え）

## 導入

複素指数関数の定義（自然指数関数$y=e^x=\exp(x)$についての定義を複素数に拡張したもの）から

$z^{p+qi} = e^{(p+qi) \log z}$ が成り立つ。

ここで、$\log z = \log(|z|e^{i arg z})$　←｛$e^{πi}=cosθ+i sinθ$（オイラーの公式）より$\arg z$が$θ$に相当、$|z|$は$z$の絶対値で、$z$の大きさになっている｝

$=(i \arg z )\log(|z|e)$　（対数の公式より）

$={\rm Log}|z| + i \arg z$

より

$e^{(p+qi) \log z} = e^{(p+qi) ({\rm Log}|z| + i \arg z)} = e^{(p{\rm Log}|z|-q \arg z)+(q{\rm Log}|z|+p \arg z)i}$
$$
\left\\{
\begin{array}{l}
α= p{\rm Log}|z|-q \arg z \newline
β= q{\rm Log}|z|+p \arg z
\end{array}
\right.
$$
と置くと$e^{α＋βi}$と表せるので

$e^{α＋βi}=e^αe^{βi}=e^α(\cosβ + i \sin β)$　←オイラーの公式

となる。

### 用語説明

- オイラーの公式…$e^{iθ} = \cosθ+ i \sinθ$となるという公式。複素数平面での角度の動きと複素数変化の関係などについて説明できる。なぜこれが成り立つのかは、自分で調べてください。

- 対数の公式…今回用いたのは$\log M + \log N = \log MN$と$\log M^p=p \log M$です。

## 例

$(1+2i)^{3+4i}$は？

$$
\left\\{
\begin{array}{l}
α=3{\rm Log}|1+2i| - 4 \arg (1+2i) \newline
β=4{\rm Log}|1+2i|+3 \arg(1+2i)
\end{array}
\right. \\
$$
$$
{\rm Log}|1+2i|={\rm Log}√5 \\
\arg(1+2i)=\tan^{-1} \frac{2}{1}+2nπ \\
$$
$$
\left\\{
\begin{array}{l}
α=\frac{3}{2}{\rm Log}5－4 \tan^{－1} \frac{2}{1}+8nπ \newline
β=2 {\rm Log}5+3 \tan^{-1} \frac{2}{1}+6nπ
\end{array}
\right. \\
$$
より
$$
(1+2i)^{3+4i}=e^{\frac{3}{2}{\rm Log}5－4 \tan^{-1}2+6nπ}\{cos(2 {\rm Log}5+3 \tan^{-1}2)+i\sin(2{\rm Log}5+3\tan^{-1}2)\}
$$
となりました。（計算ミスっている可能性あり）

## 感想

この内容は、大学で学ぶそうです。正直言って、これを何も見ずにできる気がしませんが、とりあえず指数、対数関数のしっかりとした理解から始めようと思いました。

## 参照

- Wikipedia

- RPGツクールと数学のブログ