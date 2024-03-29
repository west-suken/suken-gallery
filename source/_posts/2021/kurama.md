---
title: クラスマッチにおける対戦方法
date: 2021-07-24 17:04:06
tags: 2021年度
---

<div style="text-align:right">76期  椅子 </div>

##   はじめに

とある数学の問題を発展させて、クラスマッチにおいて、どのような対戦方法をとるのが効率的(平均試合数が一番少ない）なのかということを考えていきたい(少しトリビアルである）。なお、のちに出てくる「帰納的に考える」とは、もちろん数学的帰納法のことではなく、帰納的推論のことである。そのため、考察は厳密ではない。

##  考察対象

まず、対戦形式について提示する。トーナメント戦、リーグ戦、巴戦(まずはいずれも３クラスの場合）について考えたい。平均試合数は、ある試合数になる確率に、その試合数をかけ、その総和によって算出する。

##  巴戦

一つ目は、巴戦である。巴戦とは、主に大相撲において、勝ち数が相等しい三人の力士の優勝者決定のために用いられる手法である。まず3人のうち

２人が戦い、勝者が一回戦で戦わなかったもう一人と戦う。２連勝すれば、その時点で優勝者が決まる。２連勝することができなければ、一回戦の敗者

が、二回戦の勝者と戦い、、というように続いていく。とにかく、誰かが二連勝することができれば、その人が優勝者である。



さて、まず、あたりまえだが、一回戦で終わることはない。

二回戦で終わる確率・・・一回戦の勝者と同じ人が、もう一度勝てばよいので、2分の1

三回戦で終わる確率・・・余事象から、三回戦まで続いた後優勝者が決まる確率は、４分の1

四回戦で終わる確率・・・同様に考えると、8分の1

帰納的に考えて、平均試合数は
$$
\sum_{n=1}^{∞}\dfrac{n+1}{2^n}＝\dfrac{1}{2}\times2+\dfrac{1}{4}\times3+\dfrac{1}{8}\times4+・・・
$$

$$
そこで両辺を\dfrac{1}{2}倍して差をとると
$$

$$
\dfrac{1}{2}\sum_{n=1}^{∞}\dfrac{n+1}{2^n}=1+\dfrac{1}{4}\sum_{n=1}^{∞}\dfrac{1}{2^{n-1}}
$$

無限等比級数の和の公式より
$$
\begin{align}
\dfrac{1}{2}\sum_{n=1}^{∞}\dfrac{n+1}{2^n}&=1+\dfrac{1}{2}
\sum_{n=1}^{∞}\dfrac{n+1}{2^n}\newline
&=3
\end{align}
$$
ゆえに、巴戦の平均試合数は、3試合である。

##  リーグ戦

ご存じの通り、リーグ戦は、全員が総当たりで戦い、勝利数が一番多い人が勝ちである。巴戦同様3人での場合について考える。総試合数は、最小で3試合とする。つまり、だれかが、先に2連勝したとしても、その時点で優勝者が決定することはないようにするといことだ。もし3試合で終わらなければ、もう一度同様のことを行う。個人的に、リーグ戦は、一番公平性のある対戦形式であるように思う。巴戦は、1試合目と2試合目では、精神状況が大きく異なっているであろうし（つまり、1回戦の敗者と2回戦の敗者では、実力の発揮度合いが異なってしまうということだ。しかしそれにしても、スポーツのアスリートの方々の精神力と言ったら、それは並大抵のものでないだろうと思う今日この頃である。ちょうどパラリンピックや甲子園の真っ最中なのだ。）、トーナメント戦は、くじで予め決定された対戦相手と戦うことになり、相手によって成績が大きく変わることもあるだろう（くじが公平性に欠けるという感覚は些か逆説的であるが）。まあそんなことを言い訳にしては何も始まらないのだろう。閑話休題。

3試合で終わる確率・・・誰かが2回勝てばよいので、
$$
\dfrac{1}{2}\times\dfrac{1}{2}\times3=\dfrac{3}{4}
$$
6試合で終わる確率・・・3試合で終わらず、その後誰かが二回勝てばよいので、
$$
(1-\dfrac{3}{4})\times\dfrac{3}{4}=\dfrac{3}{16}
$$
9試合で終わる確率・・・同様に考えて、
$$
\dfrac{3}{64}
$$
帰納的に考えて、リーグ戦の平均試合数は、
$$
\sum_{n=1}^{∞}\dfrac{3}{4^n}・3n=\dfrac{9}{4}+\dfrac{18}{16}+\dfrac{27}{64}+・・・
$$
両辺を$\dfrac{1}{4}$倍して差をとると、
$$
\dfrac{3}{4}\sum_{n=1}^{∞}\dfrac{9n}{4^n}=\dfrac{9}{4}\sum_{n=1}^{∞}\dfrac{1}{4^{n-1}}
$$

無限等比級数の和の公式より
$$
\sum_{n=1}^{∞}\dfrac{9n}{4^n}=4
$$
ゆえに、3人で戦う場合、リーグ戦の平均試合数は、4試合である。

##  トーナメント戦

2試合である。（笑）

##  もし西高が3クラスであれば

もし西高が３クラスであれば、クラスマッチを最も効率よく終わらせる方法は、トーナメント戦である。

ここで、それぞれについて一般化していきたい。

###   巴戦

一般化も何も3者の勝負をつける場合に用いられる手法である。そして、参戦者が増加したとしても平均試合数は3試合となる。

###   リーグ戦

4人以上になると、誰かが全勝する以外にも優勝者が決定する場合がある。ここでは、全勝することによってのみ優勝者が決定する場合の平均試合数を考える。

ｎ人で優勝者を決定するとき、（nは自然数）

一回目のリーグ戦で優勝者が決定する確率・・・

$$
\dfrac{n}{2^{n-1}}
$$

2回目のリーグ戦で優勝者が決定する確率・・・

$$
(1-\dfrac{n}{2^{n-1}})\cdot\dfrac{n}{2^{n-1}}=\dfrac{2^{n-1}\cdot n-n^2}{2^{2(n-1)}}
=\dfrac{n(2^{n-1}-n)}{2^{2(n-1)}}
$$

3回目のリーグ戦で優勝者が決定する確率・・・
$$
\begin{align}
(1-\dfrac{n}{2^{n-1}}-\dfrac{2^{n-1}n-n^2}{2^{2(n-1)}})\cdot\dfrac{n}{2^{n-1}}
&=\dfrac{2^{2(n-1)}-2^{n-1}n-(2^{n-1}n-n^2)}{2^{2(n-1)}}\cdot\dfrac{n}{2^{n-1}} \newline
&=\dfrac{n^2-2^nn+2^{2(n-1)}}{2^{2(n-1)}}\cdot\dfrac{n}{2^{n-1}}  \newline
&=\dfrac{n(n-2^{n-1})^2}{2^{3(n-1)}}
\end{align}
$$

よって平均試合数は、上記の結果から帰納的に考えて、


$$
\sum_{k=1}^{∞}\dfrac{n(2^{n-1}-n)^{k-1}}{2^{k(n-1)}}{}nC_2k=n\cdot\dfrac{n(n-1)}{2}\sum_{k=1}^{∞}\dfrac{(2^{n-1}-n)^{k-1}}{2^{k(n-1)}}k・・・①
$$

ここで
$$
\dfrac{(2^{n-1}-n)^{k-1}}{2^{k(n-1)}}k＝\alpha
$$
とおく。①式の両辺を$\dfrac{2^{n-1}-n}{2^{n-1}}$倍して、差をとると、
$$
\dfrac{n}{2^{n-1}}\sum_{k=1}^{∞}\alpha=\dfrac{1}{2n-1}\sum_{k=1}^{∞}(\dfrac{2^{n-1}-n}{2^{n-1}})^{k-1}
$$
$0\leq\dfrac{2^{n-1}-n}{2^{n-1}}<1$から、無限等比級数の和の公式より,
$$
\sum_{k=1}^{∞}(\dfrac{2^{n-1}-n}{2^{n-1}})^{k-1}=\dfrac{2^{n-1}}{n}
$$
よって$\sum_{k=1}^{\infty}\alpha=\dfrac{2^{n-1}}{n^2}$

即ち、①式は、
$$
n・\dfrac{n(n-1)}{2}・\dfrac{2^{n-1}}{n^2}=2^{n-2}(n-1)
$$
ゆえに、リーグ戦(全勝したら優勝)の平均試合数は、
$2^{n-2}(n-1)$試合である。

つまり、西高でこの条件のリーグ戦でクラスマッチを行った場合、平均試合数は、448試合となる(非効率にも程がある）。仮に、「全勝で優勝」という条件をなくせば、もっと恐ろしい計算を強いられることになる（が、実用性はある）。そのときは、ぜひ文明の利器を利用されたい。

###   トーナメント戦

$(ｎー１)$試合である。（ありがたい）

##  結果報告

巴戦が最高効率かつ4人以上の場合最も不公平。トーナメント戦は、公平かつ安定した効率。リーグ戦は最も効率が悪いが、（ただ、条件をなくせば、一回目のリーグ戦で終わる確率はもちろん上がる）公平性は担保される。

クラスマッチ実行委員の方々は、これらのことを鑑みて、トーナメント形式でクラスマッチを運営しているのだと思うと、感動する次第である。

##  終わりに

ここまで読んでくれた方々には感謝を述べたい。そして、興味があれば、ぜひ条件無しのリーグ戦の平均試合を算出してみてほしい