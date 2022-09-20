---
title: $f(x)^{g(x)}$の極限について
date: 2022-09-19 22:03:00
tags: 2022年度
cover_index: https://dsm04pap001files.storage.live.com/y4mcKDoFg6vOpq1linjJcaFwAtuia_d2Akkli0fKlN-FdZtq3oWmnInncAqSMvO2Xe27yA8uHdfU-os_O_VAo-ndtsaGf3ytPhKhEt7I8pWxI1qzim_gX1WajAiJMOWCETb9-kgDGHdxBIlDeviCz4FLe9uJNaz5GgCzmxjPKNdWmJ4_L_J-L4hsA7Rn3PPdgTz?width=991&height=379&cropmode=none
cover_detail: https://dsm04pap001files.storage.live.com/y4mcKDoFg6vOpq1linjJcaFwAtuia_d2Akkli0fKlN-FdZtq3oWmnInncAqSMvO2Xe27yA8uHdfU-os_O_VAo-ndtsaGf3ytPhKhEt7I8pWxI1qzim_gX1WajAiJMOWCETb9-kgDGHdxBIlDeviCz4FLe9uJNaz5GgCzmxjPKNdWmJ4_L_J-L4hsA7Rn3PPdgTz?width=991&height=379&cropmode=none
---

<div style="text-align: right">76期　おチビ</div>

関数の和の極限や積の極限と同様に指数の極限を定義したいと思う。ただし、全ての極限において$x\to+0$は省略して$x\to0$と表す。
$$
\lim_{x\to0}f(x)=\alpha\,,\,\lim_{x\to0}g(x)=\beta
$$に対して、

(ⅰ)$α>0$の時
$$
\lim_{x\to 0} f(x)^{g(x)}= \lim_{x\to 0} e^{\log f(x)^{g(x)}}= \lim_{x\to 0} e^{g(x)\cdot\log f(x)}
$$$h(x)=\log x$は$x>0$で連続であり、$\displaystyle \lim_{x\to 0} f(x)=α$のため、ここで積の極限より
$$
\lim_{x\to 0} g(x)\cdot\log f(x)=β\cdot\log α
$$ここで更に$i(x)=e^x$は連続関数であるため
$$
\lim_{x\to 0} e^{\displaystyle g(x)\log f(x)}=e^{\displaystyle\lim_{x\to 0} {g(x)\cdot\log f(x)}}=α^β
$$

(ⅱ)$α=0,β>0$の時
$\displaystyle\lim_{x\to 0}\log f(x)$が-$\infty$に発散するため積の極限は使えないが、
ある$β\geqε>0$を考えると、xが十分に0に近く$\log f(x)$が負であるため
$$
β\cdot\log f(x)\leqqε\cdot\log f(x)
$$

であり右辺の極限を取ると-$\infty$より
$$
\lim_{x\to 0} g(x)\cdot\log f(x)=-\infty
$$以降(ⅰ)と同様にして、
$$
\lim_{x\to 0} f(x)^{g(x)}=0
$$

(ⅲ)$α=0,β=0$の時
話を広げ、$0^0$について考える。$0^0$と$\displaystyle\lim_{x\to 0} f(x)^{g(x)}$が別物であるのは一度置いておく。
$0^0$は現在一般的には定義していないと勝手に考えているのだがその理由を考えると、定義すると矛盾が生じるからだろう。
その有名な説明としてあるのは以下の２つの数式だろう
$$
\lim_{x\to 0} x^0=1,
\lim_{x\to 0} 0^x=0
$$また定義できないとする説明として次の数式が挙げられるだろう
$$
\lim_{x\to 0\,,\,y\to 0} x^y
$$これは-1〜1の値をとり一意に定まらない。
以上のように極限を用いて$0^0$を考えていこうと思う。
条件より$f(x),g(x)$は
$$
\lim_{x\to 0} f(x)=0,\lim_{x\to 0} g(x)=0,
$$であり、この時$f(x)=x$,$g(x)=x$とすると
$$
\lim_{x\to 0} f(x)^{g(x)}=1
$$$f(x)=x^\frac{1}{x}$,$g(x)=x$とすると
$$
\lim_{x\to 0} f(x)^{g(x)}=0
$$$f(x)=x$,$g(x)=\log_x a$,$a>0$とすると
$$
\lim_{x\to 0} f(x)^{g(x)}=a
$$となり値は一意に定まらないため、$\displaystyle \lim_{x\to 0} f(x)^{g(x)}$を$f(x),g(x)$に関係なく表現することは出来ない。

(補足)
任意の関数に関して
$$
\lim_{x\to 0} f(x)^{g(x)}= \lim_{x\to 0} e^{\log f(x)^{g(x)}}= \lim_{x\to 0} e^{g(x)\cdot\log f(x)}= \lim_{x\to 0} e^\cfrac{\log f(x)}{\cfrac{1}{g(x)}}
$$であり、条件を満たす限りロピタルの定理を繰り返し用いて値は求まる
一度用いると以下のようになり上記の関数や単純な関数の組み合わせは求められる。
$$
\lim_{x\to 0} f(x)^{g(x)}= \lim_{x\to 0} e^\cfrac{\cfrac{\partial}{\partial x}f(x)\cdot {g(x)}^2}{\cfrac{\partial}{\partial x}g(x)\cdot f(x)}
$$しかしロピタルの定理の条件を満たさない関数も多くあり$\cfrac{\cfrac{\partial}{\partial x}f(x)}{\cfrac{\partial}{\partial x}g(x)}$が収束しない又は$j(x)=0^x$のような近傍で0であるものや微分不可能なものは扱えない。

(ⅳ)$α=0,β<0$の時
(ⅱ)と同様に進めると
$$
\lim_{x\to 0} g(x)\cdot\log f(x)=\infty
$$
であり、

$$
\lim_{x\to 0} f(x)^{g(x)}=\infty
$$

(ⅴ)$α<0$の時
負の数の指数関数は少なくとも実数において非連続で、扱い方が分からないので定義できないとして無視する

以上より、$f(x)^{g(x)}$の極限は$\displaystyle \lim_{x\to 0} f(x)=α$,$\displaystyle\lim_{x\to 0} g(x)=β$に対して

$α>0$の時
$$
\lim_{x\to 0} f(x)^{g(x)} =α^β
$$$α=0,β>0$の時
$$
\lim_{x\to 0} f(x)^{g(x)} =0
$$$α=0,β<0$の時
$$
\lim_{x\to 0} f(x)^{g(x)} =\infty
$$$α=0,β=0$及び$α<0$の時は$f(x),g(x)$に依存し定式化出来ない



　$0^0$の関数ごとの値の判別をロピタルの定理を用いて見出そうとしたが私には何も見えなかったのと、$α<0$の時の扱いが分からなかったのが心残りであるため、どなたかご教授して頂けるとありがたいです。
