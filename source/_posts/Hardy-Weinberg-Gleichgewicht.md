---
title: ハーディ・ワインベルグの法則と多項定理
date: 2019-09-22 20:29:20
tags:
---

by shundroid

## 概要
ハーディ・ワインベルグ平衡とは、集団がある条件を満たすとき、集団が進化していないことを示すものである。「進化」と聞くと抽象的で、なかなか測り表すのは難しいように思えるが、この概念を使うことで、それを単純明快な数学的モデルとして示すことができるのである。

## 用語について（参考：キャンベル生物学）

遺伝子座：ある遺伝子が染色体上で存在する場所。
対立遺伝子：ある遺伝子座に存在しうる遺伝子。
集団：同じ地域に生息する同種の集まり。
配偶子：私たちに例えると、精子や卵。(ほかの形態もありうるため、一般化した名称で示されている)
接合子：私たちで言う、精子と卵が受精した生物体。(一般化した名称)
接合：私たちで言う受精（一般化した名称）

## ハーディ・ワインベルグ平衡の条件

次の条件を満たすとき、ある集団はハーディ・ワインベルグ平衡の状態にあることがある。つまり、この条件の時に集団は進化しない。どうしてそうなるのかは、この後に証明していくこととする。

### 1. 突然変異が起きない

つまり、新たな対立遺伝子が生まれないということである。

### 2. ランダム交配する

近縁種のみで交配すると、後述するように遺伝子が均等に配分されなくなる。

### 3. 自然選択が起きない

自然選択により生存的に不利な個体が排除されていく。その時、遺伝子も間接的に選択圧を受け、遺伝子頻度に影響が出る。

### 4. 集団サイズが大きい

小さい集団サイズでは、偶然によりある対立遺伝子が欠失したり、単に遺伝子頻度が変化したりすることが起こりやすくなる。（遺伝的浮動という）

### 5. 遺伝子流動がない

外来種などにより、新たな対立遺伝子が集団に持ってこられること（＝遺伝的流動）がないことである。

  

また、「進化」を「集団内の遺伝子頻度が変化すること」と定義する。（このような進化を小進化という）
これから「ハーディ・ワインベルグ平衡⇒集団内の遺伝子が変化しない⇔進化しない」という論理の整合性を確かめていく。逆が気になるが、ここでは敢えて追求しないこととする。数学的には「自然選択が瞬間的に働きまくって結局遺伝子頻度が変わらなかった」なんてこともあり得るが、現実世界ではハーディ・ワインベルグ平衡のような状況が最も理想的である。ただ、現実に厳密なハーディ・ワインベルグ平衡となることはないこともまた事実である。

## 準備：遺伝子型頻度と遺伝子頻度

Q. ある遺伝子座における対立遺伝子$ A $、$ a $による遺伝子型$ AA,Aa,aa $（表現型でないことに注意）が存在し、それぞれの遺伝子型を示す個体数の比が$ 1:2:3 $であるとき、$ A,a $の遺伝子頻度はそれぞれどうなるか。

それぞれの遺伝子**型**の頻度は、
$$ AA=\frac{1}{6},Aa=\frac{2}{6}=\frac{1}{3},aa=\frac{3}{6}=\frac{1}{2} $$
である。
$ AA $には$ A $が$ 1 $つ、$ Aa $には$ A $が半分と$ a $が半分、$ aa $には$ a $が$ 1 $つあると考えると、
$ A=\frac{1}{6}+\frac{1}{3}\cdot\frac{1}{2}=\frac{1}{3} $
$ a=\frac{1}{3}\cdot\frac{1}{2}+\frac{1}{2}=\frac{2}{3} $

よって、$ A $の遺伝子頻度は$ \frac{1}{3} $、$ a $の遺伝子頻度は$ \frac{2}{3} $
なお、$ A+a=1 $である

## ハーディ・ワインベルグ平衡時の遺伝子頻度

Q. ハーディ・ワインベルグ平衡時に、遺伝子頻度が変化しないことを示せ。

ある集団がハーディ・ワインベルグ平衡にあるとき、世代が代わる際遺伝子は**均等に配分**される。これは条件２のランダムな交配により保証される。
先ほどの例の対立遺伝子$ A,a $で考えてみよう。

| |$ A $|$ a $|
|--|----|-----|
|$ A $|$ AA $|$ Aa $|
|$ a $|$ Aa $|$ aa $|


上の表はこれらの対立遺伝子が配偶子として接合（受精）した際にできる接合子が持つ対立遺伝子の考えられる組合せを示している。
ここで、対立遺伝子が均等に配分されることから、次の世代での遺伝子型$ AA,Aa,aa $のそれぞれの頻度が考えられる。例えば、$ AA $の遺伝子型の頻度は、集団のすべての対立遺伝子（遺伝子プールという）から、対立遺伝子$ A $を2つを取り出す確率と考えることができる。$ AA $の遺伝子型の頻度は、$ A^2 $となる。

※ここで、1つ$ A $を取り出すと、もう１つの$ A $の頻度が変わると考えるかもしれないが、実際は条件にある通り、集団サイズが大きいため、影響されないものと考える。また、片方の配偶子は卵、もう片方は精子となる場合が多く、この場合はそれぞれの遺伝子頻度は等しく、卵から1つ、精子から1つとなるのでそれぞれの操作は実際にも影響されない。

同様に、$ Aa $の遺伝子型の頻度は$ Aa+aA=2Aa $（精子が$ A $、卵が$ a $とその逆）
$ aa $の遺伝子型の頻度は$ a^2 $である。

※$ A^2+2Aa+a^2=(A+a)^2=1 $

先ほどの例の数値を代入すると、$ A^2=\frac{1}{9},2Aa=2\cdot\frac{1}{3}\cdot\frac{2}{3}=\frac{4}{9},a^2=\frac{4}{9} $となる。
遺伝子型の比は、$ 1:4:4 $となる。
ここで、子の世代での遺伝子頻度を考える。先ほどのように求めると、$ A $は$ AA $型に1つ、$ Aa $型に半分含まれているので、$ A^2+\frac{1}{2}\cdot 2Aa=A^2+Aa $、$ a $は$ Aa $型に半分、$ aa $型に1つ含まれているので、$ Aa+a $
具体的な数値を入れてそれぞれ計算すると、$ A=\frac{1}{3},a=\frac{2}{3} $となり、親の世代と等しい。
遺伝子頻度が変わっていないため、進化していないと分かる。

## ハーディ・ワインベルグ平衡の応用

継続的にハーディ・ワインベルグ平衡が成り立っているとき、遺伝子型の頻度は遺伝子頻度から決定されることを利用する。(最初の世代での遺伝子型の頻度は任意である)

### 集団がハーディ・ワインベルグ平衡であるかを確かめる

遺伝子型頻度から遺伝子頻度を求め、そこからハーディ・ワインベルグ平衡時の遺伝子型頻度を求める。これが実際の遺伝子型頻度と一致するかどうかを確かめる。

### ハーディ・ワインベルグ平衡である集団について、遺伝子頻度や他の遺伝子型頻度を求める。

ハーディ・ワインベルグ平衡であるとき、１つの劣勢ホモ接合である遺伝子型からのみで、遺伝子頻度を求めることができる。（対立遺伝子が２つのとき）
これをさらに利用して、他の遺伝子型の頻度を求めることも可能。実際の研究にも用いられているらしい。生物学オリンピックでよく出る。今年は出なかった。がーん。

### 対立遺伝子が3つの時のハーディ・ワインベルグ平衡

Q. 対立遺伝子が3つである遺伝子座において、ハーディ・ワインベルグ平衡が成り立つ時、集団は進化しないか

親の世代での3つの対立遺伝子$ P,Q,R $の遺伝子頻度を$ p,q,r $とする($ p+q+r=1 $)

配偶子は単相であり、それぞれ$ 1 $つの対立遺伝子を持つ。また、交配はランダムに行われるので、
子の世代での遺伝子型$ PP,QQ,RR,PQ,QR,RP $の頻度はそれぞれ、$ p^2,q^2,r^2,2pq,2qr,2rp $となる。…☆

子の世代での$ P,Q,R $の遺伝子頻度をそれぞれ$ p',q',r' $とする。($ p'+q'+r'=1 $)

$$
\begin{align\*}
p'&=\frac{p^2+\frac{1}{2}\cdot 2pq+\frac{1}{2}\cdot 2rp}{p^2+q^2+r^2+2pq+2qr+2rp}\\\\
&=\frac{p\left(p+q+r\right)}{\left(p+q+r\right)^2}\\\\
&=p
\end{align\*}
$$

同様に、$ q'=q,r'=r $なので、遺伝子頻度は変化しない。よって、ハーディ・ワインベルグ平衡が成り立つ時、集団は進化しない。

☆本来遺伝子型の頻度は表を書いて求めるべきであるが、ここでは多項定理を用いている。

## 遺伝子型頻度と多項定理

☆ある複相の生物の遺伝子座において、対立遺伝子$ P_1,P_2,\ldots,P_n $が存在し、それぞれ遺伝子頻度が$ p_1,p_2,\ldots,p_n(\sum_{i=1}^{n}p_i=1) $の時、遺伝子型$ P_k P_l $の頻度は

- ホモ接合のとき、$ p_k^2 $ (または、$ p_l^2 $)
- ヘテロ接合のとき、$ 2p_k p_l $

これは多項定理の展開式の各項から得られる。「なぜランダムな交配の結果が多項定理の各項から得られるのか」疑問に思うかもしれないが、これは「展開」という手順が「ランダムな交配」を見事に抽象化しているからである。
ここでは複相なので、接合体になるとき、配偶子は２つ必要である。そしてそれぞれの配偶子は「ランダム」に出会うのである。配偶子を「文字」とみてみよう。展開の際、1つ目のカッコの中の文字が、2つ目のカッコの中の文字に「ランダム」に出会っているのである。いわば、積の形で表されている式が「配偶子」としての形であり、展開後の和の形で表されている式が「接合子」としての形なのである。

$$ \left(p+q+r\right)\left(p+q+r\right)=p^2+q^2+r^2+2pq+2qr+2rp $$

確率の結果と展開の対応がここに見て取れる。

演習：対立遺伝子が$ n $個の時、ハーディ・ワインベルグ平衡が成り立つとすると、集団は進化しないことを示せ。

## 接合体が4倍体、配偶体が2倍体のときのハーディ・ワインベルグ平衡

Q. ある植物は接合体が$ 4 $倍体であり、遺伝子座には対立遺伝子$ S $と$ s $が含まれている。配偶体は$ 2 $倍体であり、配偶子を形成する際に、$ 4 $つの相同染色体のうち$ 2 $つが対合し、$ 2 $つの配偶子に分配されるという形態をとる。この植物の集団がハーディ・ワインベルグ平衡にあるとき、集団は進化しないか。

植物では$ 4 $倍体はよくある話である。ここで肝となるのは、「配偶体が$ 2 $倍体」であることである。よって、ランダムな交配が行われたとしても、遺伝子頻度が変化しないとはこの段階では言い切れない。この点に留意して考える必要がある。

親世代での対立遺伝子$ S $、$ s $の頻度を$ p,q $とする($ p+q=1 $)
また、親世代が作った配偶子$ SS,Ss,ss $の頻度を$ a,b,c $とする($ a+b+c=1 $)
この時、

$$ p=\frac{a+\frac{1}{2}\cdot b}{a+b+c}=\frac{2a+b}{2} $$
$$ q=\frac{c+\frac{1}{2}\cdot b}{a+b+c}=\frac{2c+b}{2} $$

が成り立つ。

子世代の遺伝子型の頻度を$ a,b,c $を用いて表す。
$$ SSSS=a^2,SSss=b^2+2ca,ssss=c^2,SSSs=2ab,Ssss=2bc $$
よって、子世代の$ S,s $の遺伝子頻度を$ p',q' $($ p'+q'=1 $)とすると、
$$
\begin{align\*}
p'&=\frac{a^2+\frac{1}{2}\cdot (b^2+2ca)+\frac{3}{4}\cdot 2ab+\frac{1}{4}\cdot 2bc)}{\left(a+b+c\right)^2}\\\\
&=\frac{4a^2+2b^2+4ca+6ab+2bc}{4\left(a+b+c\right)^2}\\\\
&=\frac{2\left(2a+b\right)\left(a+b+c\right)}{4}\\\\
&=\frac{2p}{2}\\\\
&=p
\end{align\*}
$$
$ q'=q $も成り立つ。よって、集団は進化しないことが示せた。

## 接合体が3倍体、配偶体が1倍体のときのハーディ・ワインベルグ平衡

Q. 仮想生物として、減数分裂時に$ 3 $本の相同染色体がそれぞれ$ 3 $つの配偶子に分配され、接合時に$ 3 $つの配偶子を必要とするものを考える。ある遺伝子座において、$ P,Q,R $の$ 3 $つの対立遺伝子が存在し、ハーディ・ワインベルグ平衡が成り立つ時、集団は進化しないか。

ここで大事なのは、接合時に$ 3 $つの配偶子が必要となる所である。今までと違い、**多項定理の積の形の次数が3になる**ことが予想される。

対立遺伝子$ P,Q,R $のそれぞれの遺伝子頻度を$ p,q,r $とする($ p+q+r=1 $)
接合体の遺伝子型は、$ PPP,QQQ,RRR,PPQ,QQR,RRP,PQQ,QRR,RPP,PQR $が考えられる。それぞれの遺伝子頻度は、
$ PPP=p^3,QQQ=q^3,RRR=r^3,PPQ=3p^2 q,QQR=3q^2 r,RRP=3r^2 p,PQQ=3pq^2,QRR=3qr^2,RPP=3rp^2,PQR=6pqr $となる。(多項定理より)
子の世代でのP,Q,Rの遺伝子頻度を$ p',q',r' $とする($ p'+q'+r'=1 $)
$$
\begin{align\*}
p'&=\frac{p^3+\frac{2}{3}\cdot 3p^2 q+\frac{1}{3}\cdot 3r^2 p+\frac{1}{3}\cdot 3pq^2+\frac{2}{3}\cdot 3rp^2+\frac{1}{3}\cdot 6pqr}{(p+q+r)^3}\\\\
&=\frac{3p^3+6p^2q+3r^2p+3pq^2+6rp^2+6pqr}{3\left(p+q+r\right)^3}\\\\
&=\frac{3p\left(p+q+r\right)^2}{3}\\\\
&=p
\end{align\*}
$$
同様に、$q'=q,r'=r$が成り立ち、集団は進化していない。

## まとめ

今まで見てきたように、「ハーディ・ワインベルグ平衡の時、集団が進化しない」ことは、対立遺伝子数、配偶子の核相、接合子の核相にとらわれず成り立つことが予想される。そこで、以下の最終問題を~丸投げして~書いて、このレポートを終わりにする。

まとめの問題：ある仮想生物は、ある遺伝子座において、ハーディ・ワインベルグ平衡が成り立っている。その遺伝子座において対立遺伝子数$ g $、配偶子の核相$ n $、接合子の核相$ N $であり、親世代の一回の交配で子世代を作り出した。対立遺伝子のうちの$ 1 $つを$ G $とし、その対立遺伝子の親世代での遺伝子頻度$ p $、子世代での遺伝子頻度$ p' $とすると、$ p=p' $が成り立つことを示せ。ただし、$ n $は$ N $の約数である。