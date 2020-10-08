---
title: 再帰的な関数について
date: 2020-10-3 0:02:25
tags: 2020年度
---

<div style="text-align: right">73期 T@S</div>

## はじめに

　関数を再帰的に定義することは，非常に重要な意味を持つ．例えば最小の自然数かつ加法単位元かつ零元となる数$0$，$0$より大きい最小の自然数かつ乗法単位元となる数$1$と，自然数$a$に対してその次の自然数を表す後者関数$\operatorname{succ}(a)$が与えられたとき，
$$
\begin{align}
	\operatorname{succ}(a)=&a+1 \newline
	a+(-a)=&0 \newline
	-(-a)=&0 \newline
	a+b=&(a+1)+(b-1) \newline
	a-b=&a+(-b) \newline
	a+b=&b+a \newline
	(a+b)+c=&a+(b+c) \newline
	a\times b=&a+a\times(b-1) \newline
	a\times(-b)=&-(a+a\times(b-1)) \newline
	a\times\left(\frac{1}{a}\right)=&1 \newline
	a\div b=&a\times\left(\frac{1}{b}\right) \newline
	a\times b=&b\times a \newline
	(a\times b)\times c=&a\times (b\times c) \newline
	\frac{a}{b}+\frac{c}{d}=&\frac{a\times d+b\times c}{b\times d} \newline
	\frac{a}{b}\times\frac{c}{d}=&\frac{a\times c}{b\times d} \newline
\end{align}
$$
とすることで有理数とそれに対する四則演算を定義することができる（よく考えたら義務教育の最初の7年間でこれと似たようなことをやっている．侮れない．）が，見ての通り四則演算の定義に原始再帰関数を使用している．ただし，$\frac{a}{b}=a\div b$とした他，$a+0=a$，$a\times0=0$，$a\times 1=a$は条件より明らかなため省略し，2行目及び10行目の逆元の存在に関しては「存在すれば」という文言を省略した．  
　ここからさらに虚数単位を導入することで代数的数を定義し，それに対する四則演算を定義することもできるが，あまりにも趣旨からかけ離れすぎてしまうので割愛する．また，実数はまた別の方法を取る必要がある．  
　関数を再帰的に定義すると，他にもAckermann関数などの様々な関数を考えることができる．さらに，再帰的に定義された定数関数$f\colon\mathbb{N}^n\to\mathbb{C}$を考えれば，漸化式で表された数列と対応する．つまり，これは漸化式のある種の拡張である．

## Tetration

突然だが，$x>0$と，負でない定数$y$に対して，以下のような$x$の関数$f_y(x)$を考える．
$$\begin{align}
f_y(x)=\left\\{\begin{array}{cl}
	1&{(\text{when }{y=0})}\newline
	x^{f_{y-1}(x)}&{(\text{when }{y\neq0})}
\end{array}\right.
\end{align}$$
　この関数は再帰的に定義されているが，展開すると
$$\begin{align}\underbrace{x^{x^{\cdot^{\cdot^{\cdot^{x}}}}}}_{n\text{ copies of }x}\end{align}$$
となる．ここで，この関数の性質を調べるために微分をすることにした．（正確には73期前CEOに「面白そうだからちょっと微分してみてほしい．」と言われたのがきっかけであるため，この関数に関する話は微分のみで終了する．副会長は会長には逆らえないのだ．）
ちなみに，この関数は一般的に$x\uparrow\uparrow y$や${}^yx$などと表記されるものである．実は$y\in\mathbb{C}$に対する拡張が存在するのだが，今回は扱わない．

### $y=1$

　$f_1(x)=x$より，$f_y'(x)=1$

### $y=2$

　対数微分法を利用して，
$$\begin{align}
	f_2(x)=x^x\Leftrightarrow&\log f_2(x)=\log x^x\newline
			  \Leftrightarrow&\log f_2(x)=x\cdot\log x\newline
				  \Rightarrow&\frac{f_2'(x)}{f_2(x)}=f_1(x)\cdot\left({\textstyle\frac{\mathrm{d}}{\mathrm{d}{x}}\ }\log x\right)+f_1'(x)\cdot\log x\newline
			  \Leftrightarrow&\frac{f_2'(x)}{f_2(x)}=f_1(x)\cdot x^{-1}+f_1'(x)\cdot\log x\newline
			  \Leftrightarrow&f_2'(x)=f_2(x)\cdot(f_1'(x)+\log x)\newline
			  \Leftrightarrow&f_2'(x)=x^x(1+\log x)
\end{align}$$
である．

### $y=3$

　$y=2$のときと同様に，
$$\begin{align}
	f_3(x)=x^{x^x}\Leftrightarrow&\log f_3(x)=f_2(x)\log x\newline
					  \Rightarrow&f_3'(x)=f_3(x)\cdot\left(f_2'(x)\log x+f_2(x)\cdot x^{-1}\right)\newline
				  \Leftrightarrow&f_3'(x)=x^{x^x}\left(x^x(1+\log x)\log x+x^x\cdot x^{-1}\right)
\end{align}$$
となる．

### $y=n$

　$n\neq1$のとき，これまでと同様に，
$$\begin{align}
	f_n(x)=x^{f_{n-1}(x)}\Leftrightarrow&\log f_n(x)=f_{n-1}'\log x\newline
							 \Rightarrow&f_n'(x)=f_n(x)\cdot\left(f_{n-1}'(x)\cdot\log x+f_{n-1}(x)\cdot x^{-1}\right)\newline
						 \Leftrightarrow&f_n'(x)=f_{n-1}'(x)\cdot f_n(x)\cdot\log x+f_n(x)\cdot f_{n-1}(x)\cdot x^{-1}
\end{align}  $$
　よって，$f_n'(x)$は以下のような漸化式として表せる．

$$\begin{align}
f_n'(x)=\left\\{\begin{array}{cl}
	1&{(\text{when }{n=1})}\newline
	f_{n-1}'(x)\cdot{f_{n}(x)\cdot\log x}
	+{f_{n}(x)\cdot {f_{n}(x)\cdot f_{n-1}(x)\cdot x^{-1}}}
	&{(\text{when }{n\neq1})}
\end{array}\right.
\end{align}$$

　ここで，${f_{n}(x)\cdot\log x}=A_n$，${f_{n}(x)\cdot f_{n-1}(x)\cdot x^{-1}}=B_n$として，実際にいくつか計算してみると，
$$\begin{align}
	f_2'(x)=&A_2f_1'(x)+B_2\newline
	f_3'(x)=&A_3A_2f_1'(x)+A_3B_2+B_3\newline
	f_4'(x)=&A_4A_3A_2f_1'(x)+A_4A_3B_2+A_4B_3+B_4\newline
\end{align}$$
となる．したがって，$f_1'(x)=A_1=B_1=1$であることを用いて以下のように表せることが推測できる．
$$\begin{align}
	f_n'(x)=&A_nA_{n-1}A_{n-2}\cdots A_4A_3A_2B_1+\newline
			&A_nA_{n-1}A_{n-3}\cdots A_4A_3B_2+\newline
			&A_nA_{n-1}A_{n-4}\cdots A_4B_3+\newline
			&{\ \ \ \ \ \ }\cdots{\ \ \ \ \ \ }+\newline
			&A_nA_{n-1}B_{n-2}+\newline
			&A_nB_{n-1}+\newline
			&B_n\newline
		   =&\sum_{i=1}^{n-1}\left(B_i\cdot\prod_{j=0}^{n-i-1}A_{n-j}\right)+B_n\newline
		   =&\sum_{i=1}^{n-1}\left({f_i(x)\cdot f_{i-1}(x)\cdot x^{-1}}\cdot\prod_{j=0}^{n-i-1}{f_{n-j}}(x)\cdot\log x\right)+{f_{n}(x)\cdot f_{n-1}(x)\cdot x^{-1}}
\end{align}$$
　これは，$n=2$のとき，明らかに成立する．  
　また，$n=k$で成立することを仮定すると，
$$\begin{align}
	 &f_{n+1}'(x)\newline
	=&A_{n+1}f_n'(x)+B_n+1\newline
	=&A_{n+1}\left(\sum_{i=1}^{n-1}\left(B_i\cdot\prod_{j=0}^{n-i-1}A_{n-j}\right)+B_n\right)\newline
	=&\sum_{i=1}^{n}\left(B_i\cdot\prod_{j=0}^{n-i}A_{n+1-j}\right)+B_{n+1}
\end{align}$$
が成立することが導かれるので，$y\geq2$のとき，
$$\begin{align}f_y'(x)=\sum_{i=1}^{y-1}\left({f_i(x)\cdot f_{i-1}(x)\cdot x^{-1}}\cdot\prod_{j=0}^{y-i-1}{f_{y-j}(x)\cdot\log x}\right)+{f_{y}(x)\cdot f_{y-1}(x)\cdot x^{-1}}\end{align}$$
である．　　　∎

### $y=n (Re)$

　……流石にこんな一般項は汚いので，もう少し簡単にしてみる．前述した式を流用する．
$$\begin{align}
	f_n'(x)=&A_nA_{n-1}A_{n-2}\cdots A_4A_3A_2B_1+\newline
			&A_nA_{n-1}A_{n-3}\cdots A_4A_3B_2+\newline
			&A_nA_{n-1}A_{n-4}\cdots A_4B_3+\newline
			&{\ \ \ \ \ \ }\cdots{\ \ \ \ \ \ }+\newline
			&A_nA_{n-1}B_{n-2}+\newline
			&A_nB_{n-1}+\newline
			&B_n\newline
		   =&\left(\prod_{i_1=0}^{n-2}f_{n-i_1}(x)\right)\cdot\left(\log x\right)^{n-1}\cdot f_1(x)\cdot f_0(x)\cdot x^{-1}+\newline
			&\left(\prod_{i_2=0}^{n-3}f_{n-i_2}(x)\right)\cdot\left(\log x\right)^{n-2}\cdot f_2(x)\cdot f_1(x)\cdot x^{-1}+\newline
			&\left(\prod_{i_3=0}^{n-4}f_{n-i_3}(x)\right)\cdot\left(\log x\right)^{n-3}\cdot f_3(x)\cdot f_2(x)\cdot x^{-1}+\newline
			&{\ \ \ \ \ \ \ \ \ \ }\vdots\newline
			&\left(\prod_{i_{n-1}=0}^{n-n}f_{n-i_{n-1}}(x)\right)\cdot\left(\log x\right)^{n-(n-1)}\cdot f_{n-1}(x)\cdot f_{n-2}(x)\cdot x^{-1}\newline
		   =&x^{-1}\cdot\left(\sum_{i=0}^{n-2}\left(\log x\right)^{n-i-1}\cdot\prod_{j=0}^if_{n-j}(x)\right)
\end{align}$$
　したがって，
$$\begin{align}f_y'(x)=\left\\{\begin{array}{cl}0&{(\text{when }{y=0})}\newline1&{(\text{when }{y=1})}\newline\displaystyle x^{-1}\cdot\sum_{i=0}^{y-2}\left(\left(\log x\right)^{y-i-1}\cdot\prod_{j=0}^if_{y-j}(x)\right)&{(\text{when }{y\geq2})}\end{array}\right.\end{align}$$
である．　　　∎

## 本題

　この記事も既に中盤だが，ここからが本題である．  
　全ての正の整数$n$と全ての実数$x$に対し，$f_n(x)$を以下のように定義する．
$$\begin{align}f_n(x)=\left\\{\begin{array}{cl}\sin x&{(\text{when }{n=1})}\newline\sin(x+f_{n-1}(x))&{(\text{when }{n>1})}\end{array}\right.\end{align}  $$
　これを展開すると，
$$\begin{align}\sin(x+\sin(x+\sin(x+\cdots)))\end{align}$$
となる．この関数$f_n\colon\mathbb{R}\to[-1,1]$（終域が$[-1,1]$であることは自明だが，値域も$[-1,1]$となると思われる．詳細は後述する．）は明らかに全ての点で$x$について微分可能である．

### 特殊な値

　とりあえず，$x$にいくつかの値を代入して計算する．  
　$x=0$のとき，
$$\begin{align}
	n>1\Rightarrow f_n(0)=&\sin(0+f_{n-1}(0))\newline
						 =&\sin(f_{n-1}(0))\newline
				   f_1(0)=&\sin0\newline
						 =&0
\end{align}$$
より，
$$\begin{align}f_n(0)=0\label{ref:fn0}\end{align}  $$
　$x=\pi$のとき，
$$\begin{align}
	n>1\Rightarrow f_n(\pi)=&\sin(\pi+f_{n-1}(\pi))\newline
						   =&\sin(f_{n-1}(\pi))\newline
				   f_1(\pi)=&\sin\pi\newline
						   =&0
\end{align}$$
より，
$$\begin{align}f_n(\pi)=0\label{ref:fnpi}\end{align}  $$
　となることがわかる．また，
$$\begin{align}
	n>1\Rightarrow f_n(x+2\pi)=&\sin(x+2\pi+f_{n-1}(x+2\pi))\newline
							  =&\sin(x+f_{n-1}(x+2\pi))\newline
				   f_1(x+2\pi)=&\sin(x+2\pi)\newline
							  =&\sin x
\end{align}$$
より，
$$\begin{align}f_n(x+2\pi)=f_n(x)\label{ref:fnx2pi}\end{align}$$
であり，
$$\begin{align}
	n>1\Rightarrow f_n(-x)=&\sin(-x+f_{n-1}(-x))\newline
				   f_1(-x)=&-f_1(x)
\end{align}$$
より，
$$\begin{align}f_n(-x)=-f_n(x)\label{ref:fnneg}\end{align}$$
である．したがって，$f_n(x)$は周期関数かつ奇関数であることがわかる．また，少なくとも$2\pi$が周期であることを考えると，ある区間$[p,p+2\pi]$における性質を考えることで，この関数全体の性質を知ることができる．  

### 微分

#### 全実数における微分

　$f_1(x)=\sin x$，$f_n(x)=\sin(x+f_{n-1}(x))$より，
$$\begin{align}
	f_n'(x)=\left\\{\begin{array}{cl}\cos x&{(\text{when }{n=1})}\newline(1+f_{n-1}'(x))\cos(x+f_{n-1}(x))&{(\text{when }{n>1})}\end{array}\right.\label{ref:dfn}
\end{align}$$
である．Tetrationのときと同様に一般項を求めようと試みたが，あまりにも複雑になることが予想されたので諦めた．

#### 特殊な微分係数

　$x=0$における微分係数は，
$$\begin{align}
	n>1\Rightarrow f_n'(0)=&\lim_{h\to0}\frac{f_n(0+h)-f_n(0)}{0+h}\newline
						  =&\lim_{h\to0}\frac{\sin(h+f_{n-1}(h))}{h}\newline
\end{align}$$
となるが，$x\to0$のとき$f_n(x)\to0$より，$h\to0$のとき$h+f_{n-1}(h)\to0$であるので，
$$\begin{align}
	\lim_{h\to0}\frac{\sin(h+f_{n-1}(h))}{h}=&\lim_{h\to0}\left(\frac{\sin(h+f_{n-1}(h))}{h+f_{n-1}(h)}\cdot\frac{h+f_{n-1}(h)}{h}\right)\newline
											=&\lim_{h\to0}\left(1+\frac{f_{n-1}(h)}{h}\right)\newline
											=&1+f_{n-1}'(0)
\end{align}$$
である．ここで，
$$\begin{align}
	f_1'(0)=&\lim_{h\to0}\frac{\sin(0+h)-\sin0}{0+h}\newline
		   =&\lim_{h\to0}\frac{\sin h}{h}\newline
		   =&1
\end{align}$$
であるため，
$$\begin{align}
	f_n'(0)=&n\label{ref:dfn0}
\end{align}$$
が導かれる．なお，先ほど求めた導関数に$x=0$を代入することでも求めることができる．
また，導関数にに$x=\pi$を代入すると，$n>1$のとき，
$$\begin{align}
	f_n'(\pi)=&(1+f_{n-1}'(\pi))\cos(\pi+f_{n-1}(\pi))\newline
			 =&(1+f_{n-1}'(\pi))\cos\pi\newline
			 =&-(1+f_{n-1}'(\pi))
\end{align}$$
であり，$n=1$のとき$f_n'(\pi)=-1$であるので，
$$\begin{align}
	f_n'(\pi&)=\left\\{\begin{array}{cl}0&{(\text{when }{n\equiv0\pmod{2}})}\newline-1&(\text{when }{n\equiv1\pmod{2}})\end{array}\right.\label{ref:dfnpi}
\end{align}$$
である．ちなみにこの式を強引に1つにまとめると，例えば$\displaystyle\frac{-1+(-1)^n}{2}$などとなるが，特にそうする意味はない．なお，他の表記としては三角関数を利用したものなどがある．

### 値域に関する考察

　前述のとおり，$f_n(x)$が$2\pi$を周期とする関数で，さらに奇関数であること，そして$f_n(0)=0$であることから，$x\in[0,\pi]$における$|f_n(x)|$の最大値を$p$としたとき，値域が$[-p,p]$であることがわかる．そのため，この章では特に記述がなければ定義域を$[0,\pi]$に限ることにする．  

#### n=1のとき

　$|f_n(x)|=|\sin x|$は明らかに$x=\frac{\pi}{2}$のときに最大値$1$をとる．したがって，$f_1(x)$の値域は$[-1,1]$である．

#### n≥2のとき

　ここから，議論の簡略化のために$f_n(x)=\sin(g_n(x))$を満たす$g_n(x)$を導入する．このとき，$g_n(x)=x+f_{n-1}(x)$である．ただし，$g_1(x)=x$とする．（このとき，$f_1(x)=\sin x=\sin g_1(x)$から$g_1(x)=x+k\pi$（$k$は整数）が導かれるが，後述する$g_n(0)=g_n(\pi)=\pi$を成立させるために$k=0$とする．）  
　ところで，$f_n(x)$のグラフを実際にコンピューターに描画させてみると，$\max f_n(x)=1$であり，さらに$\min f_n'(x)=-1$であるように思われるが，
$$\begin{align}
	f_n'(x)\geq-1\Leftrightarrow&1+f_n'(x)=g_{n+1}'(x)\geq0
\end{align}$$
となる．ここで，$x=0$および$x=\pi$のときの値から，$g_n(0)=0$，$g_n(\pi)=\pi$が導かれることを用いることで，以下の事実が導かれる．  

> 閉区間$[0,\pi]$において，任意の$n>1$に対して$f_n'(x)\geq-1$であれば，$g_n'(x)\geq0$，すなわち$g_n(x)$が広義単調増加する．このとき，$\min g_n(x)=g_n(0)=0$かつ$\max g_n(x)=g_n(\pi)=\pi$かつ$g_n'(0)=n>0$であるために$g_n(a)=\frac{\pi}{2}$を満たす実数$a$がただ一つ存在し，したがって，$f_{n+1}(x)$は開空間$(0,a)$で狭義単調増加し，$x=a$で最大値$1$をとり，開区間$(a,\pi)$で狭義単調減少する．

　したがって，$f_n'(x)\geq-1$であることが示せれば，$x\in\mathbb{R}$のとき，$f_n(x)$の値域が$[-1,1]$であることが示される．  
　ところで，明らかに$f_1'(x)\geq-1$であるので，$f_k'(x)\geq-1\Rightarrow f_{k+1}'(x)\geq-1$を示すことができれば良いこともわかるのだが，あまりにも複雑になりすぎてしまい証明を与えることが出来なかったので，$f_n(x)$の最大値及び最小値に関しては予想としておく．

### その他の考察

#### 拡張

　$f_n(x)$の拡張について考察する．  
　まず，$n\in\mathbb{Z}$に対する拡張を考える．$f_{n+1}(x)=\sin(x+f_n(x))$という式で$f_n(x)$を定義したため，$f_1(x)=\sin x=\sin (x+f_0(x))$を満たす$f_0(x)$を与えることが出来る．したがって，$f_0(x)=k\pi\ (k\in\mathbb{Z})$となるが，これに$f_n(0)=f_n(\pi)=0$という条件を課すことで，$f_n(x)$の$n=0$に対する拡張$f_0(x)=0$を得ることができる．これは奇関数かつ周期関数ではあるが，値域は$[-1,1]$とはならない．同様に，$f_{-1}(x)=-x$が与えられるが，これは前述の性質を著しく欠いているので，$n\leq-2$に拡張することは出来ない．  
　次に$n$を正の実数に拡張したいところではあるが，残念ながら実力不足により適切な関数を与えることはできなかった．周期関数であることからフーリエ級数展開をすることによって拡張することができるのではないかと考えたが，係数を求めるための積分が非常に難解であるため断念した．

#### 未解決の予想

　この研究の中で，いくつかの予想を立てたので紹介する．ただし，ここでの$n$は正の整数とする．  
　まず，$f_n(x)$は常に最大値が$1$，最小値が$-1$であると考えられる．この予想の根拠は前述した．  
　次に，$f_n(a_n)=1$を満たす$a_n$に関して，$0<a_{n+1}<a_n$と予想している．これは，実際に$n\leq8$のときの$f_n(x)$のグラフを描画したときに立てたものである．  
　最後に，$\displaystyle\lim_{n\to\infty}f_{2n+1}(x)$は$x+2k\pi=0$のとき$0$，$(x+2k\pi)\in(0,2\pi)$のとき$\cos x$になるというものである．（ただし$k$は整数とする．）これは，前述の予想を仮定したときに$\displaystyle\lim_{n\to\infty}a_n=0$から$x=0$における右側極限が$1$，左側極限が$-1$となること，$x=\pi$における微分係数が$-1$であることから予想される．$n\to\infty$のとき$f_n'(0)\to\infty$より$n\to\infty$のとき$f_n(x)$は$x=0$で微分不可能であり，さらに前述の予想を仮定すれば$\displaystyle\lim_{x\to0}\lim_{n\to\infty}f_n'(x)=0$となることから$x=2k\pi$で不連続であることもこの予想の根拠であるが，残念ながら示すにはまだ知識や能力が不十分であった．

## おわりに

　本題で扱った関数を思いついたのは，全CEOとは別の友人の，「三角関数のグラフはうねうねしていて気持ち悪い」という発言をしたときに，じゃあ三角関数を使って気持ち悪いグラフを書いてやろう，と思い立ったことである．そのときに，FM音源が$\sin(ax+\sin bx)$で表されるような波形と鳴る音声を生成していることを思い出し，最初はその具体例を1つ見せただけだったのだが，いっそのこともっと大量に入れ子にしてしまえ，という考えになり，例の関数が生まれた．ちなみに，その後$n\geq2$のときの$f_n(x)$を$\sin(x+\pi f_{n-1}(x))$や$\sin((x+f_{n-1}(x))\pi)$にするという案も浮かんだのだが，一番性質が単純そうであったため，結局最初の$\sin(x+f_{n-1}(x))$に落ち着いた．  
　また，Tetrationの微分をさせてきた友人は非常に数学が好きであるため，恐らくは$y=x^x$の微分を対数微分法を用いて微分したときにTetrationの存在を思い出し，私に微分をさせてきたのだろうと思われる．（これのせいで四半日がどこかへ吹っ飛んでいったので仕返しとして不定積分をさせようとしているのだが，なかなか着手しようとしてくれない．悲しいが賢明な判断だとは思う．~~私だって本当はこんなことをやらずに受験勉強に精を出していなければいけないはずなんだけどな．~~）  
　このように，知識があると思わぬところでそれらが繋がって，面白いことになるということを，今年の長期に渡る臨時休業期間中に学んだ．  
　ところで，これについて考えて始める少し前，[『巨大数の樹海へようこそ』](https://www.youtube.com/watch?v=9YgmJzUwTJg)という動画に出会った．投稿された方は名古屋大学の准教授で，HP上で講義資料のPDFデータを配布されていた．もともと巨大数には興味があり，急増加階層という名前を聞いたことがあったため，試しに[『2019年度 数理情報学基礎論概論2 講義ノート』](http://www.math.mi.i.nagoya-u.ac.jp/~kihara/pdf/teach/fom2019spring.pdf)というファイルを見てみたところ，当然ながらどういうことなのかはあまりわからなかった．（ただし，後にYoutubeに[今年度版の講義の動画](https://www.youtube.com/watch?v=hFivqlna0Xw)が投稿されたため少しだけは理解できるようになった．）当時かろうじて理解できたのは，$\mathbb{N}$上の関数を作るにあたって原始再帰法というものが存在するということだけだったが，関数を再帰的に定義することは非常に奥深い世界の入口であるということを感じた．考え始めたきっかけも考えた内容も全く違う2つの関数をまとめて1つの研究としたのは，その奥深い世界を体験してもらいたかったという理由もある．  
　余談だが，できる限り巨大な有限の数を作ることを目的とする巨大数の研究は，ある意味で数学の限界を試しているように感じる．（経由する数が大きすぎてペアノの公理からはその停止性を証明できないGoodstein数列などが良い例である．）有志の日本人によるインターネット上での議論は非常に発展していて，ペアノの公理などからはそのwell-defined性を示すことの出来ないものなども数多く考案されている．（[Googology Wiki](https://googology.wikia.org/ja/)やTwitter上で活発な議論が行われているようである．）大きな数というものはそれだけで魅力的であるので，巨大数の世界を理解できるようになりたいと思う．数学の本質を問う分野として，他にも逆数学などがあるが，ゆくゆくはこちらについても学んでいきたい．  
　話が脱線してしまったが，このままだと際限なく脱線していってしまいそうなのでここで終わりにしようと思う．

## 参考文献

### はじめに

[木原貴行『2019年度 数理情報学基礎論概論2 講義ノート』](http://www.math.mi.i.nagoya-u.ac.jp/~kihara/pdf/teach/fom2019spring.pdf)

### Tetration

なし．

### 本題

なし．

### おわりに

（それぞれ個別に示した．）

この文章はRimseの主催する数学に関する自由研究コンクールに応募したものを微妙に編集したものです．