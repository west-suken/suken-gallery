---
title: コッホの雪片をn次元化してみたかった.
date: 2019-08-28 17:37:54
tags:
cover_index: https://po0moq.bn.files.1drv.com/y4mStJhcWo8P7fK6WVNXmNuPDXHz4v23m-AqYbBh_EU6BkBSLRTQVQQejoUBnuyirtXA03KeKXPRNcgpWo0_bH1yw6LAKRrUhY4UmZuUKConHdkZnB364MdnxUTllYibnIXIUn2zT-NW1izTyEFDjPnJb2CplwM41Fo7eRDQ82CdTHoWBdXZ-21qm5O90a9g9vWcddrltMnqwuhHu6TdCeYSg?width=660&height=254&cropmode=none
cover_detail: https://po0moq.bn.files.1drv.com/y4mStJhcWo8P7fK6WVNXmNuPDXHz4v23m-AqYbBh_EU6BkBSLRTQVQQejoUBnuyirtXA03KeKXPRNcgpWo0_bH1yw6LAKRrUhY4UmZuUKConHdkZnB364MdnxUTllYibnIXIUn2zT-NW1izTyEFDjPnJb2CplwM41Fo7eRDQ82CdTHoWBdXZ-21qm5O90a9g9vWcddrltMnqwuhHu6TdCeYSg?width=1300&height=500&cropmode=none
---

$$
\newcommand{\FQD}[5]{ { #3 }^2-3{ #2 }{ #4 }+12{ #1 }{ #5 }}
\newcommand{\SQD}[5]{ 2{ #3 }^2-9{ #2 }{ #3 }{ #4 }+27{ #2 }^2{ #5 }+27{ #1 }{ #4 }^2-72{ #1 }{ #3 }{ #5 }}
\newcommand{\Quarticp}[5]{\frac{ 8{ #1 }{ #3 }-3{ #2 }^2}{8{ #1 }^2}}
\newcommand{\Quarticq}[5]{\frac{ { #2 }^3-4{ #1 }{ #2 }{ #3 }+8{ #1 }^2{ #4 }}{8{ #1 }^3}}
$$

by T@S

## 1 始めに

コッホの雪片というものをご存知だろうか.
それは, フラクタル図形の一種で, 下の図のようなものである.

![](https://9o0noq.bn.files.1drv.com/y4m9tEMnW3nqCEqyn1K2HVLjLESSyAoaVrvXqloTO96-u1F0lNV3ZzKR3PX8tcI_xwQ-DHH1XKCvXJlfmB5MyZ9QiR007783oEo1mYNFJ_9uOCSjWoaUlJKmeoj2p2AHj4UY70jfKVWG93N4qJ8rP_P1aHgRL9QstgVk09XxmSpMGfj_dyUWK6rtO268bcBy6vVj3O19O9_X0ruy_s1HzL7rA?width=229&height=256&cropmode=none)

この図形は, 各線分を3 等分し, 中央の線分を1 辺とする正三角形を作り, 中央の線分を消
去する, という簡単な操作を繰り返し行うことで現れるものである. 正三角形から始めたもの
をコッホの雪片, 線分から始めたものをコッホの曲線と呼ぶ. 今回はコッホの雪片を取り上げ
ようと思う.

**注意: 以下, 特別な明示のない限り, 最初の図形の各辺の長さは1 とする.**

## 2 特徴

ここで, 最初の正三角形を$F_0$, 以降$k$回の操作を行った時に得られる図形を$F_k$とする. $F_k$の周の長さ, 面積をそれぞれ$\ell_k$, $S_k$とする.
0. $\ell_0=3$, $S_0=\frac{\sqrt{3}}{4}$
1. この図形は, ステップが進むごとに周長が$\frac{4}{3}$倍される. そのため,$$\lim_{k\to\infty}\ell_k=\lim_{k\to\infty}\ 3\cdot\left(\frac{4}{3}\right)^k=\infty$$より,周の長さは$k\to\infty$で発散する.
2. $S_{k+1}-S_k=3\cdot 4^k\cdot \frac{\sqrt{3}}{4}\cdot \left(\frac{1}{3^{k+1}}\right)^2$である(証明略)ので,
$$\lim_{k\to\infty}\ S_k=\frac{\sqrt{3}}{4}+\sum_{k=1}^{\infty}\ 3\cdot 4^k\cdot \frac{\sqrt{3}}{4}\cdot \left(\frac{1}{3^{k+1}}\right)^2=\frac{\sqrt{3}}{4}\cdot\frac{8}{5}$$より, 面積は$k\to\infty$で$\frac{2\sqrt{3}}{5}$に収束する.

## 3 拡張してみる

ここまでは調べればものの数分でもっと詳しい解説が見つかって面白くないので, $n_{\small(n\geq 3)}$次元空間上にも拡張してみることにする.

## 4 3次元化してみる

とりあえず定義する. $k$, $S$は先程までとは無関係である.

<p class="ovalbox">
$Def.$<br />
正四面体の各面と底面の重心を共有し, 相似比が$3:1$の正四面体を立体の外側に作り,<br />
重複する面を削除する. この操作を$k_{(k\small\geq0)}$回行ったときの体積を$V_k$,<br />
面積を$S_k$とする. ただし, 最初の正四面体は$k=0$の場合であるものと考える.
</p>

### 4.1 体積

ステップを$1$回進めるごとに, 元の$\frac{1}{\left(3^3\right)^k}$の体積を持つ新たな正四面体が$4\cdot3^{k-1}$個増えることは明らかなので, $1$辺が$1$の正四面体の体積が$\frac{1}{6\sqrt{2}}$であることより,
$$
\begin{align\*}
\lim_{k\to\infty}\ V_k&=\frac{1}{6\sqrt{2}}+\sum_{k=1}^{\infty}\ \frac{1}{6\sqrt{2}}\cdot3^{-3k}\cdot4\cdot3^{k-1}\\\\
					  &=\frac{1}{6\sqrt{2}}+\frac{1}{6\sqrt{2}}\cdot4\cdot\sum_{k=1}^{\infty}\ \frac{3^{k-1}}{27^k}\\\\
					  &=\frac{1}{6\sqrt{2}}+\frac{1}{6\sqrt{2}}\cdot4\cdot\sum_{k=0}^{\infty}\ \frac{3^k}{27\cdot27^{k}}\\\\
					  &=\frac{1}{6\sqrt{2}}+\frac{1}{6\sqrt{2}}\cdot\frac{4}{27}\cdot\sum_{k=0}^{\infty}\ \frac{3^k}{27^{k}}\\\\
					  &=\frac{1}{6\sqrt{2}}+\frac{1}{6\sqrt{2}}\cdot\frac{4}{27}\cdot\sum_{k=0}^{\infty}\ \left(\frac{1}{9}\right)^k\\\\
					  &=\frac{1}{6\sqrt{2}}\cdot\left(1+\frac{4}{27}\cdot\frac{9}{8}\right)\\\\
					  &=\frac{7}{36\sqrt{2}}
\end{align\*}
$$
となることが~わかれ~わかる.

### 4.2 表面積

$k$回の操作で, その表面積が最初の$3^{-2k}$倍である新たな正四面体が$4\cdot3^{k-1}$個作られ, その$4$枚の面のうち$2$枚分の正三角形が削除されるので, $k\geq1$のとき,
$$S_k-S_{k-1}=S(n,0)\cdot3^{-2k}\cdot\frac{2}{4}\cdot4\cdot3^{k-1}$$
となることから,
$$\lim_{k\to\infty}\ S_k=4\cdot\frac{\sqrt{3}}{4}\cdot\left(1+\sum_{k=1}^{\infty}\ 3^{-2k}\cdot\frac{1}{2}\cdot4\cdot3^{k-1}\right)=\frac{4}{\sqrt{3}}$$
になり, 表面積も同様に収束する.

## 5 より高次元へ拡張してみる

$3$次元のときとほぼ同様の定義をする. ただし, 正単体とは$n$次元空間上に存在する, $n+1$個の頂点からなる超立体で, 辺の長さが全て等しいものである. ここでは辺の長さを$1$とする.

<p class="ovalbox">
$Def.$<br />
$n\geq2のとき, n$次元正単体と, その$n-1$次元超底面の重心を共有し,<br />
相似比が$3:1$となる新たな正単体を外側に作り, 重複する部分を削除する.<br />
この操作を$k_{(k\small\geq0)}$回行った超立体の超体積を$V(n,k)$, 超表面積を$S(n,k)$とする.<br />
ただし, 最初の正単体は$k=0$の場合であるものと考える.
</p>

### 5.1 体積

先ほどと同様に, まず体積を求める. $V(n,0)$の値は煩雑な計算が必要なので, 一旦保留する.
$k$が$1$増加するごとに, $n^{k-1}\cdot(n+1)$個, 新たな正単体が生成され, その体積は$V(n,0)の\frac{1}{\left(3^n\right)^k}$倍となることは想像に難くない. よって,
$$
\begin{align\*}
	V(n,k)&=V(n,0)+\sum_{i=1}^{k}\ V(n,0)\cdot(n+1)\cdot n^{i-1}\cdot3^{-ni}\\\\
		  &=V(n,0)+V(n,0)\cdot(n+1)\cdot\sum_{i=0}^{k-1}\ n^i\cdot3^{-n(i+1)}\\\\
		  &=V(n,0)+V(n,0)\cdot\frac{n+1}{3^n}\cdot\sum_{i=0}^{k-1}\ \left(\frac{n}{3^n}\right)^i\\\\
		  &=V(n,0)\cdot\left(1+\frac{n+1}{3^n}\cdot\cfrac{\frac{n^k}{3^{nk}}}{1-\frac{n}{3^n}}\right)\\\\
		  &=V(n,0)\cdot\left(1+\frac{n^k(n+1)}{3^{nk}\left(3^n-n\right)}\right)
\end{align\*}
$$
となる.
~一番楽そうな,~上記の式の$3$行目より, $k\to\infty$の極限を取って,
$$\lim_{k\to\infty}\ V(n,k)=V(n,0)\cdot\left(\frac{3^n+1}{3^n-n}\right)$$

#### 5.1.1 正単体の体積
この節では, 保留しておいた$V(n,0)$を求める.
さて, ここで, $n+1$個の頂点$ \mathrm{P}\_1 , \mathrm{P}\_2, \cdots, \mathrm{P}\_{n+1}$の座標を定める. 座標軸には$x_1,\ x_2,\ \cdots,\ x_n$をとる.
まず, 頂点$\mathrm{P}\_k\ (1\leq k\leq n)$の座標を, 以下の式を満たす点とする. これらの正単体の各辺の長さは$1$なので,
$$
x_i=\left\\{
\begin{array}{cl}
  \frac{1}{\sqrt{2}}&(i=k) \\\\
  0&(i\neq k)
\end{array} \right.
$$
とする. 例えば, $\mathrm{P}\_3=(0,0,\frac{1}{\sqrt{2}},0,\cdots,0)$である. この時, $\mathrm{P}_{n+1}$の$x_i$座標を$p_i$とすると,

$$
\mathrm{P}\_1\mathrm{P}_{n+1}=\sqrt{\left(p_1-\frac{1}{\sqrt{2}}\right)^2+(p_2-0)^2+\cdots+(p_n-0)^2}
$$

が成立し, 他の点$\mathrm{P}\_k$に対しても同様に考えることで, 点 $\mathrm{P}\_{n+1}$ の $x_i\ (1\leq i\leq n)$ 座標は全て等しくなることがわかる. そこで, $x_i=p$とする. したがって,

$$
\begin{align\*}
  \mathrm{P}\_k\mathrm{P}_{n+1}&=\sqrt{\left(p-\frac{1}{\sqrt{2}}\right)^2+(p-0)^2+\cdots+(p-0)^2}\\\\
        &=\sqrt{np^2-\sqrt{2}\cdot p+\frac{1}{2}}\\\\
        &=1
\end{align\*}
$$

が成立する. よって, $p$に関する$2$次方程式 $np^2-\sqrt{2}\cdot p-\frac{1}{2}=0$ を解いて, $p=\frac{1\pm\sqrt{n+1}}{\sqrt{2}\cdot n}$であることがわかる. ここでは便宜上復号は正をとることとする.
ところで, 直線 $x_1=x_2=\cdots=x_n=p$ は, 頂点 $\mathrm{P}\_k\ (0\leq k\leq n)$ を含む超平面 $\sum_{i=0}^n\ x_i=\frac{1}{\sqrt{2}}$ の, 頂点 $\mathrm{P}\_{n+1}$ を通る垂線となるので,この直線とこの超平面の交点を $\mathrm{H}$ としたとき,この正単体の高さは $\mathrm{P}\_{n+1}\mathrm{H}$ である. ここで,点 $\mathrm{H}$ の $x_i$ 座標が $\frac{1}{\sqrt{2}\cdot n}$ であることが容易にわかるので,
$$
\begin{align\*}
  \mathrm{P}\_{n+1}\mathrm{H}&=\sqrt{n}\left(\frac{1+\sqrt{n+1}}{\sqrt{2}\cdot n}-\frac{1}{\sqrt{2}\cdot n}\right)\\\\
      &=\sqrt{\frac{n+1}{2n}}
\end{align\*}
$$
となる. これを $h$ とすると, 断面の立体は $n-1$ 次元図形となるので, $V(n,0)$ を求めるには次の積分をすれば良い.
$$ \displaystyle V(n,0)=\int_0^h\ V(n-1,0)\cdot\left(\frac{x}{h}\right)^{n-1}\ dx $$
これを計算すると,
$$
\begin{align\*}
  V(n,0)&=\int_0^h\ V(n-1,0)\cdot\left(\frac{x}{h}\right)^{n-1}\ dx\\\\
      &=V(n-1,0)\cdot h^{-n+1}\left(h^n\cdot n^{-1}-0^n\cdot n^{-1}\right)\\\\
      &=V(n-1,0)\cdot h\cdot n^{-1}\\\\
      &=V(n-1,0)\cdot \sqrt{\frac{n+1}{2n}}\cdot n^{-1}
\end{align\*}
$$
となるので, $n$次元正単体の体積を求めるには, この漸化式の一般項を求めれば良い. そこで, $0以上の整数m$に対して, $V_m=V_{m-1}\cdot a_{m-1}$, $a_m=\sqrt{\frac{m+1}{2m}}\cdot m^{-1}$とおく. この時, $V_2=\frac{\sqrt{3}}{4}$から, $V_1=V_0=1$である.
$$
\begin{align\*}
	V_m&=V_{m-1}\cdot a_m\\\\
	   &=V_0\cdot a_1\cdot a_2\cdot\cdots\cdot a_{m-1}\cdot a_m\\\\
	   &=\prod_{i=1}^m\ a_i\\\\
	   &=\sqrt{\frac{m+1}{2m}}\cdot\sqrt{\frac{m}{2(m-1)}}\cdot\sqrt{\frac{m-1}{2(m-2)}}\cdot\ \cdots\ \cdot\sqrt{\frac{2}{1}}\\\\
	   &\hspace{60pt}\times m^{-1}\cdot(m-1)^{-1}\cdot(m-2)^{-1}\cdot\ \cdots\ \cdot1\\\\
	   &=\sqrt{\frac{(m+1)!}{2^m\cdot m!}}\cdot\frac{1}{m!}\\\\
	   &=\frac{\sqrt{m+1}}{\sqrt{2^m}\cdot m!}
\end{align\*}
$$

$$
\therefore\ V(n,0)=\frac{\sqrt{n+1}}{\sqrt{2^n}\cdot n!}
$$

### 5.2 表面積

$3$次元のときと同様に考えると, $k$回の操作で, 超表面積が最初の$3^{-k(n-1)}$倍である新たな$n$次元正単体が$(n+1)\cdot n^{k-1}$個作られ, $n+1$枚ある$n-1$次元面のうち$2$枚分の$n-1$次元正単体が削除されるので, $k\geq1$のとき,
$\displaystyle S(n,k)-S(n,k-1)=S(n,0)\cdot3^{-k(n-1)}\cdot\frac{n-1}{n+1}$となる. したがって,

$$
\begin{align\*}
  \lim_{k\to\infty}\ S(n,k)&=S(n,0)+\sum_{k=1}^{\infty}\ 3^{-k(n-1)}\cdot\frac{n-1}{n+1}\cdot(n+1)\cdot n^{k-1}\\\\
              &=S(n,0)\cdot\left(1+\sum_{k=1}^{\infty}\ 3^{-k(n-1)}\cdot(n-1)\cdot n^{k-1}\right)\\\\
              &=S(n,0)\cdot\left(1+\frac{n-1}{n}\cdot\sum_{k=1}^{\infty}\ \left(\frac{n}{3^{n-1}}\right)^{k+1}\right)\\\\
              &=S(n,0)\cdot\left(1+\frac{n-1}{3^{n-1}}\cdot\frac{3^{n-1}}{3^{n-1}-n}\right)\\\\
              &=S(n,0)\cdot\frac{3^{n-1}-1}{3^{n-1}-n}
\end{align*}
$$

となるので, これで体積の収束先が求まった.~体積と似た綺麗な式になったが,本当にこれで合っているのだろうか.~

### 5.3 極限(メモ)

式の意味は見ればきっとわかると思うので列挙する. 式の意味もあえて書かないでおいてみる.

$$
\begin{align\*}
  &\lim_{k\to\infty}V(n,k)=V(n,0)\\\\
  &\lim_{n\to\infty}V(n,0)=0\\\\
  &\lim_{n\to\infty}\ \frac{3^n+1}{3^n-n}=1\\\\
  &\lim_{n\to\infty}\ \left(\lim_{k\to\infty}\ V(n,k)\right)=\lim_{n\to\infty}\ V(n,0)=0
\end{align\*}
$$

## 6 あとがき

### 6.1 定義について

 このように定義を拡張したことで, 表面積が収束してしまうようになった. その差異はもち
ろん, 操作を進めたときの表面積の増え方が緩やかになってしまっているということだ. 本来
のコッホの雪片と同じような増え方をするような定義にできないか考えたこともあったが, ど
う頑張っても辺が重なってしまったので諦めた. しかし, 一応それっぽい拡張ができたので, 今回は
それを採用することにした.

### 6.2 疲れの見えるあとがき

- この題材にした経緯は全く覚えてない
- 思っていたよりもややこしかった
- ややこしすぎてフラクタル次元の話は諦めた
- 去年のろくでもない問題よりはマシな出来
- $ \LaTeX $ を使ってるから数式は他の誰よりも綺麗に表示できてる…と思う
- オンラインでしている方の部誌( 会誌…?) に $ \LaTeX $ の解説とかを載せた

## 7 謝辞

以下の方々(敬称略) にいろいろ手伝っていただきました. 本当にありがとうございます.
Shundroid, うめ, もやっしー, Ktro, さきちゃん, がいらみ

思ったより下が余ってしまったので$4$次方程式$ax^4+bx^3+cx^2+dx+e=0$の解でも書いておきます. 実質的にWikipediaのQuartic functionのページの一部をコピペしただけです. Wikipediaには導出方法や判別式なども記載されているので, 気になる方はそちらもお読みください.

$a\neq0$の$4$次方程式$ax^4+bx^3+cx^2+dx+e=0$の解は,

$$
\begin{align\*}
  p&=\Quarticp{a}{b}{c}{d}{e}\\\\
  q&=\Quarticq{a}{b}{c}{d}{e}\\\\
  \Delta_0&=\FQD{a}{b}{c}{d}{e}\\\\
  \Delta_1&=\SQD{a}{b}{c}{d}{e}\\\\
  Q&=\sqrt[3]{\frac{\Delta_1+\sqrt{\Delta_1^2-4\Delta_0^3}}{2}}\\\\
  S&=\frac{1}{2}\sqrt{-\frac{2}{3}p+\frac{1}{3a}\left(Q+\frac{\Delta_0}{Q}\right)}
\end{align\*}
$$

としたときに,
$$x=-\frac{b}{4a}\pm S\pm\frac{1}{2}\sqrt{-4S^2-2p\pm\frac{q}{S}}$$
で表すことができる. ただし, 複号は$1,\ 3$個目が異なるように選ばなければならない.
