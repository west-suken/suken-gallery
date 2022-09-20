---
title: 未解決問題が解けた！<br/>～ラマヌジャン・マシンの紹介～
date: 2022-09-19 22:09:00
tags: 2022年度
cover_index: https://dsm04pap001files.storage.live.com/y4mcKDoFg6vOpq1linjJcaFwAtuia_d2Akkli0fKlN-FdZtq3oWmnInncAqSMvO2Xe27yA8uHdfU-os_O_VAo-ndtsaGf3ytPhKhEt7I8pWxI1qzim_gX1WajAiJMOWCETb9-kgDGHdxBIlDeviCz4FLe9uJNaz5GgCzmxjPKNdWmJ4_L_J-L4hsA7Rn3PPdgTz?width=991&height=379&cropmode=none
cover_detail: https://dsm04pap001files.storage.live.com/y4mcKDoFg6vOpq1linjJcaFwAtuia_d2Akkli0fKlN-FdZtq3oWmnInncAqSMvO2Xe27yA8uHdfU-os_O_VAo-ndtsaGf3ytPhKhEt7I8pWxI1qzim_gX1WajAiJMOWCETb9-kgDGHdxBIlDeviCz4FLe9uJNaz5GgCzmxjPKNdWmJ4_L_J-L4hsA7Rn3PPdgTz?width=991&height=379&cropmode=none
---

<div style="text-align: right">76期　mathist</div>

　こんちは。mathistです。

　せっかくうちの名前が「数学**研究**同好会」なので、今回は僕なりの数学研究を書いてみようと思います。

　まず「未解決問題を解くなんて...」と思っているそこの君！　

　第五章以外は**漸化式と整式を知ってる人なら理解できる内容になっています**。それほど**難しい数学は使わない**ので安心してください。

　ちなみに第五章では「無限級数」というものやそれに関する未解決問題などを扱うので、級数に興味のある方・詳しい方は第五章もぜひ読んでいただきたいです。

　本稿では「ラマヌジャン・マシン」なる**AIが生み出した数学の予想**を紹介しますが、実は後述の理由から**学生でも解決できる可能性が非常に高い**問題です。本稿を読んでこの問題に取り組む人が少しでも増えてくれれば嬉しいなと思います。

　~~東京リベンジャ〇ズのあの名言が頭から離れませんが怒られそうなのでやめときます。~~
<br/>

## 1. 「ラマヌジャン・マシン」とは　

　そもそも「ラマヌジャン・マシン」とは何か？　

　ラマヌジャン・マシンは2020年にイスラエル工科大学の研究チームによって開発された、連分数に関する予想を生み出すAIです（すげえ）[5]。
　ただし、ラマヌジャン・マシンができるのはあくまで予想であって証明まで考えてはくれません。そのことが、まるで証明なしに様々な予想ばかりを生み出した天才数学者・ラマヌジャンのようであることからこの名前が付けられました。
<div style="text-align:center">
<img src="https://dsm04pap001files.storage.live.com/y4mo7qtOBlCN3E3M114VjDRVDPnr0q_Ff9kFqd5TsFAZrCUUqDj4ET5SrF_HB0WnG3hj2UMxZi-fDYr4Sc9iS1ifraQdqMwFS5hMlzC7zWYGqeIsT9M_2FxOGPzRSfm3WEkZrjcDo8hSMAVlL8yGBVst1B8PQpuxijlgHmkqCU9DYFWcEnr5Xzk2uQ2yG4rwkOa?width=953&height=641&cropmode=none" style="display:inline" width="350" >&emsp;&emsp;&emsp;&emsp;<img src="https://dsm04pap001files.storage.live.com/y4mlMAbh8qHXkSyOukLYIIHN6tmD56E6Xde0_jycRbpP9eIb5NoF85gKlZ3mvha_zrjKbFtA8ctujjfIchr73MBtBv4sJ9VO1GCi6DJJsDAhjuYB4l7O08Ha7ZHKstab6gToOpz_9kktrSNksRpRwYaFJITTRukITNrh1YGi57ME3AaijyXpwTPD84nwR0aX9XM?width=338&height=463&cropmode=none" style="display:inline" width="170" ></div>

<div style="text-align: center">左：ラマヌジャン・マシンを開発したイスラエル工科大学の研究チーム<br/>右：シュリニヴァ―サ・ラマヌジャン(1887-1920)</div>

　ラマヌジャン・マシンの生み出す予想（以降「RM予想」とする）は、例えばこんな感じです。
$$
\frac{16}{12-\pi^2}=9-\cfrac{27}{23-\cfrac{160}{43-{\ddots \atop \ddots -\cfrac{n(n+2)^2(2n+1)}{(3n^2+11n+9)-\ddots}}}}\tag{0}
$$美しいですね...

　ちなみに全てのRM予想は以下のURLのサイトにて公表されています。
　http://www.ramanujanmachine.com/results/

　実はすでに証明された予想もありますが、40個を超える予想のほとんどは未だ証明されていません。それら未解決問題を解いてやろうじゃないか、というのが本稿の内容であり、実際、筆者は**5つの未解決予想を証明することに成功しました！**　

　たかが高校生になぜそんなことが可能かというと、単に**この問題に取り組む人が非常に少ないから**です。「未解決問題」と言われるとフェルマーの最終定理みたいな「数多の数学者の挑戦をはねのけた超難問」的なのを想像するかもしれませんが、星の数ほどある未解決問題の全てがそうとは限りません。そもそも挑戦する人がほとんどいないような問題もあります。**RM予想もそんな可哀そうな問題の一つなんです。**
　ただしRM予想は、**十分知名度はあるにも関わらず挑戦する人は少ない**という非常に特殊なタイプです。
　なぜそうなったのでしょう？
　本来数学上の予想にはそれが発見されるに至った経緯があり、少なくともその「経緯」に関係した研究をしている数学者ならその予想に興味をもつはずです。しかしRM予想はその「経緯」がないため挑戦するのに十分な動機を持つ数学者がいません。このことが、有名なのに解こうとする人はいないという奇妙な状況を生み出しているのです。

　ちなみに、筆者はその5つの未解決予想の証明を頑張って英語にしてラマヌジャン・マシンの研究チームに送ったのですが、未だに何も返信が来ません（笑）。　従って別に誰かのお墨付きがあるわけでもなく証明に穴がないとも限らないので、誤りがあったらLINEなどで教えていただけると嬉しいです。
<br/>

## 2. 実は漸化式の問題なんです

　さて、連分数の問題ってどうやって解くのでしょうか？　

　実は、RM予想は（例えば前述の予想(0)だったら）よく知られた方法で以下のような漸化式の問題に帰着します。（その過程は第五章で述べます。）

**問題 0. $(F_{-1},F_0)=(0,1),(1,9)$のそれぞれの場合について以下の漸化式を満たす数列**$F_n$**を求めよ。**　
$$
F_n=(3n^2+11n+9)F_{n-1}-n(n+2)^2(2n+1)F_{n-2}\tag{1}
$$
　このような漸化式を三項間漸化式と言い、高校で習う内容です！　この問題なら解けそうな感じがしますね。
　しかし、よくよく問題を見てみると突っかかる点が見えてきます。それは漸化式の係数が定数ではないということです。高校で習う三項間漸化式は
$$
a_n=2a_{n-1}-a_{n-2}
$$のように漸化式の係数が定数ですが、(1)の漸化式はそうではありません...

　さて困りました。漸化式が定数係数でないパターン（「変数係数」という）はどうやって解いたらいいのでしょう？　
　実は**変数係数の三項間漸化式を解く一般的な方法は知られていません**。

　しかし係数が整式である場合に限れば望みはあります。その鍵となるのが、整式の整数的性質の利用です。
<br/>

## 3. 整式は整数？

　整式は整数によく似た性質を持っており、問題0ではその性質を大胆に利用することが証明の鍵となります。ですがいきなりその方法を導入するとややこしくなると思うので、本章で記法などをざっとまとめておきます。

　まずは、整式どうしにおいて「互いに素」であることを以下のように定めます。
$$
\textbf{整式}p(x),q(x)\textbf{において、}p(x),q(x)\textbf{のどちらも割り切るような}1\textbf{でない整式}g(x)\textbf{が存在しないとき、}$$$$\textbf{「}p(x)\textbf{と}q(x)\textbf{は互いに素である」といい、}p(x)\perp q(x)\textbf{と表す。}$$例えば$(x-1)(2x+1)$と$(x+2)(2x-1)$は互いに素ですが、$(x-1)(2x+1)$と$(x-2)(2x+1)$は互いに素ではありません。

　さらに、整式どうしの「最大公約数」を以下のように定めます。
$$\textbf{整式}p(x),q(x)\textbf{において、最高次係数が}1\textbf{である整式}g(x)\textbf{が}p(x),q(x)\textbf{の両方を割り切り}$$$$p(x)/g(x)\perp q(x)/g(x)\textbf{であるとき、}g(x)=\gcd(p(x),q(x))\textbf{と表す。}$$例えば$\gcd((x-1)(2x+1),(x-2)(2x+1))=x+\frac{1}{2}$です。

　（脱線ですが、一般的に最小公倍数は$\text{lcm}(a,b)$と表されます。これ初見で「1<ruby>cm<rp>（</rp><rt>センチメートル</rt><rp>）</rp></ruby>」て読まないやつおるん？）

　また、整式$f(x)$の係数を以下のように表します。
$$
\lbrace f(x)\rbrace^{[k]}:=f^{[k]}:=
\begin{align}
    \begin{cases}
        f(x)\text{の}(\deg(f)-k)\text{次係数}\hspace{10pt}\left(0\leq k\leq\deg(f)\right) \newline
        0\qquad\qquad\qquad\qquad\qquad\hspace{12pt}(\text{otherwise})
    \end{cases}
\end{align}
$$ただし$\deg(f)$とは$f(x)$の次数のことで、‘‘$\text{otherwise}$”は「その他」という意味です。例えば$f^{[0]}$とは$f(x)$の最高次係数を表します。（この記法だけは筆者が勝手に導入したものなので注意してください。）

　このとき、$p(x),q(x),r(x),s(x)$を整式として例えば以下が成り立ちます。

- $p(x)q(x)$が$r(x)$で割り切れ$q(x)\perp r(x)$のとき、$p(x)$は$r(x)$で割り切れる。

- $\displaystyle\frac{p(x)}{q(x)}=\frac{r(x)}{s(x)}\hspace{3pt},\hspace{3pt}p(x)\perp q(x)\hspace{3pt},\hspace{3pt}r(x)\perp s(x)\hspace{3pt},\hspace{3pt}q^{[0]}=s^{[0]}$が成り立つとき、

$$
\begin{align}
    \begin{cases}
        p(x)=r(x) \newline
        q(x)=s(x)
    \end{cases}
\end{align}
$$


## 4. いかに漸化式を解くか

　それでは、問題0を解いていきましょう。

　まずは定数係数の三項間漸化式の解法にならって以下のようにおいてみましょう。
$$
(F_n-\alpha_nF_{n-1})=\beta_n(F_{n-1}-\alpha_{n-1}F_{n-2})
$$元の漸化式と係数を比較して、
$$
\begin{align}
    \begin{cases}
        \alpha_n+\beta_n=3n^2+11n+9 \newline
        -\alpha_{n-1}\beta_n=-n(n+2)^2(2n+1)
    \end{cases}
\end{align}
$$さらに$\alpha_n$だけの式にすれば、
$$
\alpha_n=(3n^2+11n+9)-\frac{n(n+2)^2(2n+1)}{\alpha_{n-1}}\tag{2}
$$これをまともに解こうとしてもびくともしないので、**$\alpha_n$が$($整式$)/($整式$)$で表されると仮定して**考えてみましょう（$($整式$)/($整式$)$の形の関数を「有理関数」といいます）。このとき、整式$p(x),q(x)$において
$$
\alpha_n=\frac{p(n)}{q(n)}\qquad\left(p(x)\perp q(x),q^{[0]}=1\right)
$$とおけます。これを(2)に代入すると、
$$
\frac{p(n)}{q(n)}=\frac{(3n^2+11n+9)p(n-1)-n(n+2)^2(2n+1)q(n-1)}{p(n-1)}
$$となります。ここで左辺は分子と分母が互いに素になっています。よって右辺を「約分」すれば分子と分母の二つの等式に分離することができます。

　まずは右辺の分子と分母の「最大公約数」を考えます。
$$
\begin{align}
g(n)&=p^{[0]}\cdot\gcd(p(n-1),(3n^2+11n+9)p(n-1)-n(n+2)^2(2n+1)q(n-1))\newline
&=p^{[0]}\cdot\gcd(p(n-1),-n(n+2)^2(2n+1)q(n-1))\newline
&=p^{[0]}\cdot\gcd(p(n-1),-n(n+2)^2(2n+1))\qquad\left(\because p(n-1)\perp q(n-1)\right)\tag{3}
\end{align}
$$そして右辺の分子と分母を$g(n)$で割ります。ここで$P(n-1)=p(n-1)/g(n),B(n)=-n(n+2)^2(2n+1)/g(n)$とすると
$$\frac{p(n)}{q(n)}=\frac{(3n^2+11n+9)P(n-1)+B(n)q(n-1)}{P(n-1)}$$（$g(n)$に$p^{[0]}$を掛けたのはここで$q^{[0]}=P^{[0]}$が成り立つようにするためです。）よって、
$$
\begin{align}
    \begin{cases}
      p(n)=(3n^2+11n+9)P(n-1)+B(n)q(n-1)\newline
      q(n)=P(n-1)
    \end{cases}
\end{align}$$$$
\therefore g(n+1)P(n)=(3n^2+11n+9)P(n-1)+B(n)P(n-2)\tag{5}
$$あとは$g(n)$と$P(n)$の次数が分かれば、この式から係数比較で連立方程式を立てて$g(n),P(n)$が求められますね！　

　$g(n)$の次数は簡単に求められます。整式$f_1(x),f_2(x),f_3(x)$において$f_1(x)=f_2(x)+f_3(x)$が成り立つとき
$$
\deg(f_1)\leq\max(\deg(f_2),\deg(f_3))=\left(\deg(f_2),\deg(f_3)\text{のうち大きい方}\right)
$$であることから、(5)より
$$
\deg(g)+\deg(P)\leq\max(2+\deg(P),\deg(B)+\deg(P))
$$
$$
\deg(g)\leq\max(2,4-\deg(g))
$$
ここで$2>4-\deg(g)$と仮定すると$\deg(g)\leq2$であり仮定に矛盾。よって$2\geq 4-\deg(g)$、よって上の式に当てはめて$\deg(g)\leq2$。従って$\deg(g)\geq2$かつ$\deg(g)\leq2$より$\deg(g)=2$。　

　$P(n)$の次数は、任意の整式$f(x)$と定数$c$において二項定理より
$$
\left\lbrace f(x+c)\right\rbrace^{[1]}=f^{[1]}+cf^{[0]}\deg(f)
$$が成り立つことを利用して求められます。(3)より$\deg(g)=\deg(3n^2+11n+9)=\deg(B)$から、
$$
\{g(n+1)P(n)\}^{[1]}=\{(3n^2+11n+9)P(n-1)\}^{[1]}-\{B(n)P(n-2)\}^{[1]}
$$\begin{align}
&\lbrace g(n+1)\rbrace^{[1]}\lbrace P(n)\rbrace^{[0]}+\lbrace g(n+1)\rbrace^{[0]}\lbrace P(n)\rbrace^{[1]}\newline
&=\lbrace(3n^2+11n+9)\rbrace^{[1]}\lbrace P(n-1)\rbrace^{[0]}+\lbrace(3n^2+11n+9)\rbrace^{[0]}\lbrace P(n-1)\rbrace^{[1]}\newline
&\quad\hspace{1pt}+\lbrace B(n)\rbrace^{[1]}\lbrace P(n)\rbrace^{[0]}+\lbrace B(n)\rbrace^{[0]}\lbrace P(n)\rbrace^{[1]}
\end{align}

さらに頑張って計算すれば、
$$
\deg(P)=\frac{-2g^{[0]}+B^{[1]}-g^{[1]}+11}{2g^{[0]}-3}\tag{6}
$$と分かります。

　あとは(5)の係数比較によって求められます。ただし、$g(n)$は(3)より$-n(n+2)^2(2n+1)$を割り切ることから最高次だけ係数比較すれば十分です。

　まず$g^{[0]}$を求めます。(5)より$\deg(a)=\deg(B),P^{[0]}=1$から
$$
g^{[0]}=3+B^{[0]}=3+\frac{-2}{g^{[0]}}
$$$$
g^{[0]}=1,2
$$
　ここで、$g(n)$は(3)より$-n(n+2)^2(2n+1)$を割り切るため、あり得る$g(n),B(n)$の組み合わせは以下の$8$通りに絞られます。
\begin{align}
\left(g(n),B(n)\right)=&\left(2n(n+2),-(n+2)\left(n+\frac{1}{2}\right)\right)&ensp;,&ensp;\left(2(n+2)^2,-n\left(n+\frac{1}{2}\right)\right)&ensp;,&ensp;\newline
&\left((n+2)(2n+1),-n(n+2)\right)&ensp;,&ensp;\left(n(2n+1),-(n+2)^2\right)\newline
&\left(n(n+2),-(n+2)(2n+1)\right)&ensp;,&ensp;\left((n+2)^2,-n(2n+1)\right)&ensp;,&ensp;\newline
&\left((n+2)\left(n+\frac{1}{2}\right),-2n(n+2)\right)&ensp;,&ensp;\left(n\left(n+\frac{1}{2}\right),-2(n+2)^2\right)
\end{align}これらのうち(6)において右辺が非負整数であるものは、
$$
\left(g(n),B(n),\deg(P)\right)=\left((n+2)(2n+1),-n(n+2),0\right)\,,\,\left(n(2n+1),-(n+2)^2,2\right)
$$　$\deg(P)=0$の場合、つまり$P(x)=1$のとき(5)は成り立ちます。（$\deg(P)=2$の場合は省略します。）

　よって$g(n)=(n+2)(2n+1),B(n)=-n(n+2),P(n)=1$が分かりました。よって(4),(5)より、
\begin{align}
  \begin{cases}
    p(n)=(3n^2+11n+9)P(n-1)-B(n)P(n-2)=(n+3)(2n+3)P(n)=(n+3)(2n+3) \newline
    q(n)=1
  \end{cases}
\end{align}よって(2)を満たす$\alpha_n$として
$$
\alpha_n=(n+3)(2n+3)
$$が得られました。

　こうしてやっと$F_n$の漸化式(1)を以下のように書き換えることができました...
$$
\left\lbrace F_n-(n+3)(2n+3)F_{n-1}\right\rbrace=n(n+2)\lbrace F_{n-1}-(n+2)(2n+1)F_{n-2}\rbrace
$$よって$(F_{-1},F_0)=(0,1)$のときの$F_n$を$A_n$として、$n\geq0$において
$$
A_n-(n+3)(2n+3)A_{n-1}=\{A_0-9A_{-1}\}\prod_{i=1}^ni(i+2)=\prod_{i=1}^ni(i+2)
$$ただし任意の数列$x_n$に対して$\prod_{i=1}^0x_i=1$とする。$A_n=A_n'\prod_{i=1}^n(i+3)(2i+3)$とおけば、
$$
A_n'-A_{n-1}'=\prod_{i=1}^n\frac{i(i+2)}{(i+3)(2i+3)}=\prod_{i=1}^n\frac{i+2}{i+3}\frac{2i-1}{2i+3}\frac{i}{2i-1}=\frac{1}{n+3}\frac{9}{(2n+1)(2n+3)}\frac{n!}{(2n-1)!!}
$$（ただし$(2n-1)!!$は二重階乗と言い$2n-1$以下の奇数の総乗$\prod_{i=1}^n(2i-1)$を表す。）よって$A_0'=1$より
$$
A_n'=\sum_{k=0}^n\frac{9}{(k+3)(2k+1)(2k+3)}\frac{k!}{(2k-1)!!}
$$よって
$$
A_n=9\prod_{i=1}^n(i+3)(2i+3)\cdot\sum_{k=0}^n\frac{1}{(k+3)(2k+1)(2k+3)}\frac{k!}{(2k-1)!!}
$$　$(F_{-1},F_0)=(1,9)$のときの$F_n$を$B_n$として、$B_n$も同様に考えることで以下のように求められます。
$$
B_n=9\prod_{i=1}^n(i+3)(2i+3)
$$　こうしてやっと問題0を解くことができました...！　

　高校数学で習う漸化式がいかに恵まれた環境にあるのか分かったと思います。
<br/>

## 5. 連分数と漸化式の関係

　さて、頑張って変数係数の漸化式が解けましたが、そもそもなんでこんなことをしたのかというところを解説していませんね。本章では、先延ばしにしてきた連分数と漸化式の関係について説明し、本丸であるRM予想を証明します！
　なぜ問題0が解ければ連分数の値が求められるかというと、ずばり以下の定理が成り立つからです。
**定理 1. 数列$A_n,B_n$は以下を満たすとする。**
\begin{align}
  \begin{cases}
    A_{-1}=0,A_0=1,A_n=a_nA_{n-1}+b_nA_{n-2} \newline
    B_{-1}=1,B_0=a_0,B_n=a_nB_{n-1}+b_nB_{n-2}
  \end{cases}
\end{align}**このとき、**
$$
a_0+\cfrac{b_1}{a_1+\cfrac{b_2}{a_2+\ddots}}=\lim_{n\to\infty}\frac{B_n}{A_n}
$$

　証明を知りたい方は[1,定理1.1]をご参照ください。

　この定理から、例えば前述の連分数式について
$$
9-\cfrac{27}{23-\cfrac{160}{43-{\ddots \atop \ddots-\cfrac{n(n+2)^2(2n+1)}{(3n^2+11n+9)-\ddots}}}}=\left\lbrace\sum_{k=0}^\infty\frac{1}{(k+3)(2k+1)(2k+3)}\frac{k!}{(2k-1)!!}\right\rbrace^{-1}
$$が成り立つことが分かります。よって右辺の値が$\frac{16}{12-\pi^2}$であることが示せれば晴れて証明完了となります。

　ありがたいことに
$$
\sum_{k=0}^\infty\frac{1}{2k+n}\frac{k!}{(2k-1)!!}\qquad(n\in\mathbb{N})
$$の形の級数の値を求める方法は既に知られており[2]、次の5つのRM予想は$A_n,B_n$さえ求められれば簡単に証明できます。ただし

$$
\text{CF}[a_n,b_n]=a_0+\cfrac{b_1}{a_1+\cfrac{b_2}{a_2+\ddots}}
$$としています。

**定理 2**
$$
\frac{16}{12-\pi^2}=\text{CF}[3n^2+11n+9,-n(n+2)^2(2n+1)]
$$
**定理 3**
$$
\frac{16}{-4+\pi^2}=\text{CF}[3n^2+7n+3,-n^2(n+2)(2n-1)]
$$
**定理 4**
$$
\frac{32}{32-3\pi^2}=\text{CF}[3n^2+15n+15,-n(n+2)(n+4)(2n+1)]
$$
**定理 5**
$$
\frac{1}{1-\log(2)}=\text{CF}[3n^2+7n+4,-2n^2(n+1)^2]
$$
**定理 6**
$$
\frac{1}{-1+2\log(2)}=\text{CF}[3n+3,-2n^2]
$$　

　証明において連分数の級数表現を導出する部分は省略します。すべて前述した方法で導くことができます。

**定理2の証明.** 定理1において$a_n=3n^2+11n+9,b_n=-n(n+2)^2(2n+1)$として[2,Eq.3.58,Eq.3.59,Eq.3.96]より、
\begin{align}
&\text{CF}[3n^2+11n+9,-n(n+2)^2(2n+1)]\newline
&=\left\lbrace\sum_{k=0}^\infty\frac{1}{(k+3)(2k+1)(2k+3)}\frac{k!}{(2k-1)!!}\right\rbrace^{-1}\newline
&=\left\lbrace\sum_{k=0}^\infty\frac{k!}{(2k-1)!!}\left(\frac{1}{15}\cdot\frac{1}{k+3}+\frac{1}{5}\cdot\frac{1}{2k+1}-\frac{1}{3}\cdot\frac{1}{2k+3}\right)\right\rbrace^{-1}\newline
&=\left\lbrace\frac{1}{15}\left(6\pi-\frac{15}{16}\pi^2-\frac{35}{4}\right)+\frac{1}{5}\cdot\frac{\pi}{2}-\frac{1}{3}\left(\frac{3}{2}\pi-4\right)\right\rbrace^{-1}=\frac{16}{12-\pi^2}
\end{align}<div style="text-align: right;">☐</div>

**定理3の証明.** 定理1において$a_n=3n^2+7n+3,b_n=-n^2(n+2)(2n-1)$として[2,Eq.3.58,Eq.3.94,Eq.3.95,Eq.3.96]より、
\begin{align}
&\text{CF}[3n^2+7n+3,-n^2(n+2)(2n-1)]\newline
&=\frac{1}{2}\left\lbrace\sum_{k=0}^\infty\frac{1}{(k+1)(k+2)(k+3)(2k+1)}\frac{k!}{(2k-1)!!}\right\rbrace^{-1}\newline
&=\frac{1}{2}\left\lbrace\sum_{k=0}^\infty \frac{k!}{(2k-1)!!}\left(-\frac{1}{2}\cdot \frac{1}{k+1}+\frac{1}{3}\cdot \frac{1}{k+2}-\frac{1}{10}\cdot \frac{1}{k+3}+\frac{8}{15}\cdot \frac{1}{2k+1}\right)\right\rbrace^{-1}\newline
&=\frac{1}{2}\left\lbrace-\frac{1}{2}\left(\pi-\frac{\pi^2}{8}\right)+\frac{1}{3}\left(\frac{5}{2}\pi-\frac{3}{8}\pi^2-3\right)-\frac{1}{10}\left(6\pi-\frac{15}{16}\pi^2-\frac{35}{4}\right)+\frac{8}{15}\cdot \frac{\pi}{2}\right\rbrace^{-1}\newline
&=\frac{16}{-4+\pi^2}
\end{align}<div style="text-align: right;">☐</div>

**定理4の証明.** 定理1において$a_n=3n^2+15n+15,b_n=-n(n+2)(n+4)(2n+1)$として[2,Eq.3.58,Eq.3.59,Eq.3.96,Eq.3.97,Eq.3.98]より、
$\small\begin{align}
&\text{CF}[3n^2+15n+15,-n(n+2)(n+4)(2n+1)]\newline
&=\frac{1}{12}\left\lbrace\sum_{k=0}^\infty\frac{1}{(k+3)(k+4)(k+5)(2k+1)(2k+3)}\frac{k!}{(2k-1)!!}\right\rbrace^{-1}\newline
&=\frac{1}{12}\left\lbrace\sum_{k=0}^\infty \frac{k!}{(2k-1)!!}\left(\frac{1}{30}\cdot \frac{1}{k+3}-\frac{1}{35}\cdot \frac{1}{k+4}-\frac{1}{126}\cdot \frac{1}{k+5}+\frac{4}{315}\cdot \frac{1}{2k+1}-\frac{4}{105}\cdot\frac{1}{2k+3}\right)\right\rbrace^{-1}\newline
&=\frac{1}{12}\left\lbrace\frac{1}{30}\left(6\pi-\frac{15}{16}\pi^2-\frac{35}{4}\right)-\frac{1}{35} \left(\frac{83}{6}\pi-\frac{35}{16}\pi^2-\frac{763}{36}\right)+\frac{1}{126}\left(31\pi-\frac{315}{64}\pi^2-\frac{193}{4}\right)+\frac{4}{315}\cdot \frac{\pi}{2}-\frac{4}{105}\left(\frac{3}{2}\pi-4\right)\right\rbrace^{-1}\newline
&=\frac{32}{32-3\pi^2}
\end{align}$<div style="text-align: right;">☐</div>

**定理5の証明.** 定理1において$a_n=3n^2+7n+4,b_n=-2n^2(n+1)^2$として
\begin{align}
\text{CF}[3n^2+7n+4,-2n^2(n+1)^2)]&=2\left\lbrace\sum_{k=0}^\infty\frac{2^{-k}}{(k+1)(k+2)}\right\rbrace^{-1}\newline
&=2\left\lbrace\sum_{k=0}^\infty2^{-k}\left(\frac{1}{k+1}-\frac{1}{k+2}\right)\right\rbrace^{-1}\newline
&=2\left\lbrace2\sum_{k=1}^\infty\frac{2^{-k}}{k}-4\left(\sum_{k=1}^\infty\frac{2^{-k}}{k}-\frac{1}{2}\right)\right\rbrace^{-1}=\frac{1}{1-\log(2)}
\end{align}<div style="text-align: right;">☐</div>

**定理6の証明.** 定理1において$a_n=3n^2+7n+4,b_n=-2n^2(n+1)^2$として
\begin{align}
\text{CF}[3n+3,-2n^2]&=\frac{1}{2}\left\lbrace\sum_{k=0}^\infty\frac{2^{-k}}{(k+1)(k+2)(k+3)}\right\rbrace^{-1}\newline
&=\frac{1}{2}\left\lbrace\sum_{k=0}^\infty2^{-k}\left(\frac{1}{2}\cdot\frac{1}{k+1}-\frac{1}{k+2}+\frac{1}{2}\cdot\frac{1}{k+3}\right)\right\rbrace^{-1}\newline
&=\frac{1}{2}\left\lbrace\sum_{k=1}^\infty\frac{2^{-k}}{k}-4\left(\sum_{k=1}^\infty\frac{2^{-k}}{k}-\frac{1}{2}\right)+4\left(\sum_{k=1}^\infty\frac{2^{-k}}{k}-\frac{5}{8}\right)\right\rbrace^{-1}=\frac{1}{-1+2\log(2)}
\end{align}<div style="text-align: right;">☐</div>

　また、以下の4つの予想は、無限級数によって表せたもののその値が求められなかった**未解決問題**です。筆者はあまり級数に詳しくないので、**興味のある方はぜひ取り組んでほしい**です。
**定理 7**
$$
\text{CF}[3n^2+3n+1,-n^3(2n-3)]=-\frac{1}{4}\left\lbrace\sum_{k=0}^\infty\frac{k!}{(2k-1)!!}\frac{1}{(k+1)(k^2+3k-2)(k^2+5k+2)}\right\rbrace^{-1}
$$この値は$\displaystyle\frac{16}{4+\pi^2}$であると予想されている。

**定理 8**
$$
\small \text{CF}[3n^2+7n+3,-n^2(n+2)(2n-3)]=-\frac{1}{32}\left\lbrace\sum_{k=0}^\infty\frac{k!}{(2k-1)!!}\frac{1}{(k+1)(k+2)(k+3)(k^2+7k-4)(k^2+9k+4)}\right\rbrace^{-1}
$$この値は$\displaystyle\frac{32}{\pi^2}$であると予想されている。

**定理 9**
$$
\small\text{CF}[3n^2+11n+9,-n(n+2)^2(2n-1)=9\left\lbrace\sum_{k=0}^\infty\frac{k!}{(2k-1)!!}\frac{1}{(k+3)(2k+1)(k^2+7k+4)(k^2+9k+12)}\right\rbrace^{-1}
$$この値は$\displaystyle\frac{16}{-8+\pi^2}$であると予想されている。

**定理 10**
$$
\scriptsize\text{CF}[3n^2+9n+7,-(n+1)^3(2n-3)]=-3-\frac{1}{64}\left\lbrace\sum_{k=0}^\infty\frac{k!}{(2k-1)!!}\frac{(k+1)}{(k+2)(k+4)(k+5)(k^3+10k^2-k-2)(k^3+13k^2+22k+8)}\right\rbrace^{-1}
$$この値は$\displaystyle\frac{16+3\pi^2}{16-\pi^2}$であると予想されている。

　証明は省略します。これらもすべて前述の方法で導くことができます。
<br/>

## 6. 今後の展望

　さて無事に問題0を解きいくつかのRM予想を証明することができましたが、問題0を解くうえで最も重要なポイントは何でしょう？　

　それは、**解の限定**です。(2)において$\alpha_n$を有理関数に限定することで$\alpha_n$が導けました。これは2次方程式が、整数解を持つ場合に限れば簡単に解けることに似ていますね。しかし、2次方程式と違って(1)のような三項間漸化式の一般的な解の公式は知られていないのでした。

　また、他の予想が前述の方法で解けないことは確認済みです。

　では、残るRM予想はどうやったら解けるのでしょうか？　

　僕は**異なる解の限定**を考えることで解けるのではないか、と考えています。具体的にどんな解の限定を考えているかというと、
$$
\sum_{k=0}^n F_{n,k}\qquad\left(\frac{F_{n+1,k}}{F_{n,k}},\frac{F_{n,k+1}}{F_{n,k}}\text{が}n,k\text{についての有理関数}\right)\tag{7}
$$という形です。

　実際、連分数式
$$
\frac{6}{\zeta(3)}=\text{CF}[(2n+1)(17n^2+17n+5),-n^6]\qquad\left(\zeta(3)=\frac{1}{1^3}+\frac{1}{2^3}+\frac{1}{3^3}+\cdots\right)
$$の証明では、
$$
(n+1)^3u_{n+1}=(2n+1)(17n^2+17n+5)u_n-n^3u_{n-1}\tag{8}
$$が解
$$
u_n=\sum_{k=0}^n\frac{(n+k)!^2}{(n-k)!^2k!^4}\tag{9}
$$を持つことが用いられています。
　実は、(9)から(8)、より一般に(7)の形の数列からそれが満たす漸化式を導く方法は既に知られており「ツァイルバーガーのアルゴリズム」と呼ばれています\[3,Chapter 7][4,Chapter 6]。つまり、ツァイルバーガーのアルゴリズムの逆を考えればより多くのRM予想が証明できる可能性があるのです。

　ちなみに、この記事を書いてる最中に知ったのですが、第四章で説明した三項間漸化式の解法はより一般的なものが既に知られていたようです...かなすぃ...
　「ペトコフセクのアルゴリズム」というそうです[3,Chapter 9]。英語版Wikipedia「Petkovsek's algorithm」にも説明記事があるのでご参照ください。

　ツァイルバーガーやぺトコフセクらによる整式係数漸化式の研究は**P-再帰方程式**という分野としてまとめられています。その分野の基礎的な内容は英語版Wikipedia「P-recusive equation」にまとめられているのでぜひご覧ください。また、‘‘A=B’’というP-再帰方程式の解説書[4]は現在**無料でダウンロード可能**なので、RM予想に取り組みたい方はぜひダウンロードしてみてください。
<br/>

## 7. 最後に

　どうですか？　RM予想、解きたいと思いましたか？　
　思いましたよねぇ？　（圧）

　RM予想は有名にも関わらず解こうとする人はいない可哀そうな問題なんだ、と言いました。裏を返せば、**数学者でなくても解けるかもしれない有名未解決問題**という、まさに我々 学生数学徒にとっての**理想郷**がここにあるのです！　

　ガチで、ここまで読んでくれたあなたは相当の猛者なのでぜひ取り組んでほしいです。
　~~ちなみに筆者はこれ以上数学をしてるとまじで進級が危ないのでこれからは自粛しようと思ってます（）~~

　残る未解決問題も、本稿の読者がいつか解いてくれることを願って。
<br/>

## 8. 謝辞（的なもの）

　証明の成否を確認するにあたって多和田先生には快くご協力いただきました。ありがとうございました。また、数研の副会長と会計には本当に様々な場面で助けてもらいました。二人なしでは数研は成り立たないので本当に感謝しています。そして顧問の田中先生はじめ部誌の制作に協力していただいた全ての方々、本当にありがとうございました。
<br/>

## 参考文献

[1] 片山 喜美. ネイピア数$e$の連分数展開について. 2021

[2] T. Sherman. $\textit{Summation of Glaisher and Ap\'{e}ry-like series}$. 2000.

[3] Wolfram Koepf. $\textit{Hypergeometric Summation : An Algorithmic Approach to Summation and Special Function Identities}$. Universitext. 2014.

[4] Marko Petkovsek, Herbert S Wilf, Doron Zeilberger. $A=B$. 1996.以下のURLから閲覧・ダウンロード可能.
	  https://www2.math.upenn.edu/~wilf/AeqB.pdf

[5] 鈴木 治郎. 連分数公式を予測するラマヌジャン・マシンの紹介. 2021.
　  https://iiiar.org/iiars/doc/iiars_workshop9_4_5.pdf

