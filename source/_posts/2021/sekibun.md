---
title: そうだ 積分、しよう。
date: 2021-07-24 17:04:04
tags: 2021年度
---


<div style="text-align: right">75期 でーせん </div>

## はじめに

 こんにちは。昨年部誌を書かなかったでーせんです。

 ある夜、夏休みの課題が全然進まないことに苛立ちと絶望感を覚えた私は、気分転換のためにふととある関数を積分しようと思いました(※現実逃避ではありません)。するとなんということでしょう、気づいたころには窓から清々しい朝日が差し、雀たちの快い鳴き声が聞こえてくるではありませんか。何やってるんだ、私。

 ただただ無駄なこの行為をどうにか意味のあることに昇華できないかと考えた結果、その積分計算を数研の部誌に書いてしまえばいいという結論に辿り着きました。以下、無駄に長い無駄な計算を無駄に説明していこうと思います。

## 関数 $y=x^{-x}$

  今回積分していきますのはこちらの関数 $f(x)=x^{-x}$​​​ です。グラフはこんな感じになります。

<img src="https://dm2302files.storage.live.com/y4mhM8wzb0ReuOijxy8RhYsaL_ChdSalVcy4P0_k7wAVA2fGiFLI-wcsmvK22yS2PMfQxV0nni5Ymr6_6Iq46B-kyL2nc36nBPY9YdeelWApqCkDfbLunD5Ul7rK3pYMBrrpJCTdHAf0rHm2c-trUQJW39pnLMrY9OJQVn-sQgq_d8-3ssszss_jRMqPGoSKKLL?width=1920&height=1090&cropmode=none" style="zoom:33%;" />

これを見て $0$ から $\infty$​ まで積分したくなる人は私だけではないはずです。面積、気になりますよね？？？

 しかし結論から言うと、私の頭ではどれだけ頑張っても $0$​ から $\infty$​​​ までの広義積分はうまいこと計算できませんでした。ネットを探しても全然出てこないので、初等数学では計算不可能なのかもしれません。よって、今回はこの関数の不定積分と、たまたま計算できた $0$​ から $1$​ までの定積分を計算していきます。

## 不定積分

 $x>0$​ の時を考えます。まずは、計算しやすいように $x^{-x}$​ の底を自然対数の底 $e$​​​​ で置き換え、マクローリン展開してから積分します。

$$
\begin{align}
x^{-x}&=e^{\log{x^{-x}}}=e^{-x\log{x}}\newline
&=\sum_{n=0}^{\infty}\frac{(-x\log{x})^n}{n!}\newline
&=\sum_{n=0}^{\infty}\frac{(-1)^n}{n!}(x\log{x})^n\newline
\int x^{-x}\space dx&=\int\sum_{n=0}^{\infty}\frac{(-1)^n}{n!}(x\log{x})^n\space dx\newline
&=\sum_{n=0}^{\infty}\frac{(-1)^n}{n!}\int(x\log{x})^n\space dx\tag{1}
\end{align}
$$

そうしたら、$\int(x\log{x})^n\space dx$​ の部分を置換積分しながら計算していきます。まず、$x=e^s$​ とおくと、$\frac{dx}{ds}=e^s$​ より $dx=e^sds$​ だから
$$
\begin{align}
\int(x\log{x})^n\space dx&=\int(e^s\cdot s)^n e^s ds\newline
&=\int s^ne^{(n+1)s}\space ds
\end{align}
$$
今度は $t=(n+1)s$​ で置換します。両辺を $s$ で微分して $\frac{dt}{ds}=n+1$ より $ds=\frac{dt}{n+1}$​ なので
$$
\begin{align}
\int s^ne^{(n+1)s}\space ds&=\int\left(\frac{t}{n+1}\right)^ne^t\frac{dt}{n+1}\newline
&=\left(\frac{1}{n+1}\right)^{n+1}\int t^ne^t\space dt\tag{2}
\end{align}
$$
ここで、$\int t^ne^t\space dt$ を部分積分してみると、
$$
\begin{align}
\int t^ne^t\space dt&=t^ne^t-\int nt^{n-1}e^t\space dt\newline
&=t^ne^t-nt^{n-1}e^t+\int n(n-1)t^{n-2}e^t\space dt\newline
&\hspace{6pt}\vdots\newline
&=t^ne^t-nt^{n-1}e^t+n(n-1)t^{n-2}e^t-\cdots+(-1)^k\frac{n!}{(n-k)!}t^{n-k}
e^t+\cdots+(-1)^nn!e^t+C\newline
&=e^t\sum_{k=0}^n\frac{(-1)^kn!}{(n-k)!}t^{n-k}+C
\end{align}
$$
ちょっと複雑ですがインテグラルを外すことができました。あとはこの式の $t$ を $x$ にもどしていきます。$x=e^s$ 、$t=(n+1)s$ と置換したので、$t=(n+1)\log{x}$ となります。
$$
\begin{align}
e^t\sum_{k=0}^n\frac{(-1)^kn!}{(n-k)!}t^{n-k}+C&=e^{(n+1)\log{x}}\sum_{k=0}^n\frac{(-1)^kn!}{(n-k)!}\{(n+1)\log{x}\}^{n-k}+C\newline
&=x^{n+1}\sum_{k=0}^n\frac{(-1)^kn!}{(n-k)!}\{(n+1)\log{x}\}^{n-k}+C
\end{align}
$$
これを $(2)$​​​ を経由して $(1)$ に代入すれば、
$$
\begin{align}
\int x^{-x}\space dx&=\sum_{n=0}^{\infty}\frac{(-1)^n}{n!}\left(\frac{1}{n+1}\right)^{n+1}\left(x^{n+1}\sum_{k=0}^n\frac{(-1)^kn!}{(n-k)!}\{(n+1)\log{x}\}^{n-k}+C\right)\newline
&=\sum_{n=0}^{\infty}\left(\frac{(-1)^nx^{n+1}}{n+1}\sum_{k=0}^n\frac{(-1)^k}{(n-k)!}(n+1)^{-k}(\log{x})^{n-k}\right)+\sum_{n=0}^{\infty}\frac{(-1)^n}{n!}\left(\frac{1}{n+1}\right)^{n+1}C\newline
&=\sum_{n=0}^{\infty}\left(\frac{(-1)^nx^{n+1}}{n+1}\sum_{k=0}^n\frac{(-1)^k(\log{x})^{n-k}}{(n-k)!(n+1)^k}\right)+\sum_{n=0}^{\infty}\frac{(-1)^n}{(n+1)!(n+1)^n}C
\end{align}
$$
出ました！
$$
\begin{align}
\large{\int x^{-x}\space dx=\sum_{n=0}^{\infty}\left(\frac{(-1)^nx^{n+1}}{n+1}\sum_{k=0}^n\frac{(-1)^k(\log{x})^{n-k}}{(n-k)!(n+1)^k}\right)+C'}\tag{$\mathrm{*}$}\newline
\left(ただし,\space C'=\sum_{n=0}^{\infty}\frac{(-1)^n}{(n+1)!(n+1)^n}C\right)\newline
\end{align}
$$
ですが、これには $x=0$​ は含まれていません( $\log{0}$​ が定義できないから)。そのため、$x=0$​ の場合も計算しておく必要があります。

 $(*)$ の右辺の $C'$ を除く各項は、
$$
\begin{align}
\frac{(-1)^nx^{n+1}}{n+1}\cdot\frac{(-1)^k(\log{x})^{n-k}}{(n-k)!(n+1)^k}=\frac{(-1)^{n+k}}{(n-k)!(n+1)^{k+1}}x^{k+1}(x\log{x})^{n-k}\quad(0\leqq k\leqq n)
\end{align}
$$
となっています。ここで、
$$
\begin{align}
\lim_{x\to0}x^{k+1}=0\space,\space\lim_{x\to0}x\log{x}=0
\end{align}
$$
より
$$
\begin{align}
\lim_{x\to0}x^{k+1}(x\log{x})^{n-k}=0
\end{align}
$$
また、係数部分は、$(0\leqq k\leqq n)$​ の条件下では分母に $0$​ が現れません。そのため、$x$​ を $0$​ に限りなく近づけていくと、積分定数 $C'$以外の部分は $0$​​​ になります。よって、
$$
\begin{align}
\int f(0)\space dx=C’
\end{align}
$$
 だいぶ面倒でしたね。私は数学素人なのでもしかしたらもっとエレガントな導出方法があるのかもしれませんが、もうこれ以上頭を使いたくないので考えません。

## 定積分

 $0$ から $1$ までの定積分はそんなに難しくありません。$(*)$ に数値を代入して計算して終わりです。$f(0)$ の時の積分値は先ほど計算したので、
$$
\begin{align}
\int_0^1x^{-x}\space dx&={\sum_{n=0}^{\infty}\left(\frac{(-1)^n\cdot1^{n+1}}{n+1}\sum_{k=0}^n\frac{(-1)^k(\log{1})^{n-k}}{(n-k)!(n+1)^k}\right)+C'}-C'\newline
&=\sum_{n=0}^{\infty}\left(\frac{(-1)^n}{n+1}\sum_{k=0}^n\frac{(-1)^k\cdot0^{n-k}}{(n-k)!(n+1)^k}\right)
\end{align}
$$
$k=n$​ のとき $0^{n-k}=1$​ 、 $k\neq n$​ のとき $0^{n-k}=0$​​ だから
$$
\begin{align}
\sum_{k=0}^n\frac{(-1)^k\cdot0^{n-k}}{(n-k)!(n+1)^k}=\frac{(-1)^n}{(n+1)^n}
\end{align}
$$
よって
$$
\begin{align}
\int_0^1x^{-x}\space dx&=\sum_{n=0}^{\infty}\left(\frac{(-1)^n}{n+1}\cdot\frac{(-1)^n}{(n+1)^n}\right)=\sum_{n=0}^{\infty}\frac{1}{(n+1)^{n+1}}\newline
&=\sum_{n=1}^{\infty}\frac{1}{n^n}\newline
&=1+\frac{1}{2^2}+\frac{1}{3^3}+\frac{1}{4^4}+\cdots
\end{align}
$$
なんと、こんなにシンプルな式になってしまいました。美しいですね。これを見つけたときは感動しました(午前5時頃)。
この値を電卓かなんかで計算すると、
$$
\int_0^1x^{-x}\space dx\approx1.29128599706
$$
こんな感じになります。

 ちなみに、$0$​ から $\infty$​ までを積分しようとすると、$\lim_{x\to+0}\int x^{-x}\space dx$​ を計算しようとしたときに、 $x^{n+1}$​ も $\log{x}$​ も無限大に発散してしまいます。どうこねくり回してもこれらの無限大が解消できなかったので、さっきも書いた通りこの広義積分計算は断念しました。誰か解けた人がいたら教えてください。

## おわりに

 私が数研で最初に書いたこの記事ですが、結果として数研っぽい内容になったのではないかと思います(当社比)。最初に言ったようにだいぶ適当な理由で書き始めたので、これといって読者の方々に伝えたいことはなかったのですが、しいて言うならば、$\int_0^1x^{-x}\space dx$​​ はきれいに計算できるよということと、夏休みの課題は計画的に進めたほうがいいよということです。ちなみに私はこの記事を書いている3日間まったく進めておりません＼(^o^)／ こんなことになるなら初めから現実逃hｹﾞﾌﾝｹﾞﾌﾝ気分転換しなければよかったと後悔しております。

 最後まで読んでいただきありがとうございました。みなさんは気分転換は程々にしてくださいね。
