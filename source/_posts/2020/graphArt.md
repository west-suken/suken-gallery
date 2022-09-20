---
title: グラフでお絵描き
date: 2020-10-3 0:02:25
tags: 2020年度
---

<div style="text-align: right">74期 チョコミント</div>

## はじめに

　**関数を使って文字を書きたい！**

　筆者は暇な時とかに、自分のスマホに入れている***Desmos***という、いろんな関数のグラフを描画できるアプリで遊んでいます。今回は、**｜絶対値｜**を使ってゴシック体の文字を書いてみたいと思います。せっかくなので**「西」**という漢字を、**一つの関数だけで**書いてみましょう。目標はこんなカクカクした感じです。

<img src="https://eedeea.dm.files.1drv.com/y4moZySRU2V60TnRROsshozCNkIbRngAdIadn2r2lt5tnfGOZXd9jUsHHmgD4CQfJul8c0aCF2u63uhOdQyod0NQFtW4r7QnlvLqdYx4mOmMiN67VO9eY-wZhhJPhtNp5CdYQ1mZlQFzO21W1wcKUc_j_-d04F2kt9oZrpVTjENrre8ehfbB4RjjnFGXUQcv8i4wLk93n200RgXnJPhIzLWWA?width=1631&amp;height=1064&amp;cropmode=none" style="zoom:50%;" />

出典：https://tameshigaki.jp/



## 四角形を表す方程式

### 正方形を表す方程式

　いつものように***Desmos***で遊んでいたとき、
$$
|x+y|+|x-y|=2k \tag{1}
$$
のグラフが、対角線の交点を原点とする、**一辺$k$の正方形**を表すことに偶然気がつきました。

<img src="https://eed6yq.dm.files.1drv.com/y4mMpTPUi7k6qNrAH3PbQfxXrAPL74Fr_913BvIz0PypKGDUUBHpCLw0wWBI5FARMSQ84HLQIlCpUZ2rA7yoFS7Vmx0wisTmBWt-9Spe2q7zV-po3VP_17LRbkY3s5DNRuP84gq9RW0seIGx-FBviA9AAGZmqc8T6ndvITnNjF3GlxojDojSiCdEYugHb0yF3coWeXqB4OF9r-J2KbIod-x-w?width=2189&amp;height=1511&amp;cropmode=none" style="zoom:40%;" />

　場合分けしてみるとこんな感じです。

1. $x+y\ge 0$ かつ $x-y\ge 0$ すなわち $y\ge -x$ かつ $y\le x$ のとき直線$x=k$
2. $x+y< 0$ かつ $x-y\ge 0$ すなわち $y< -x$ かつ $y\le x$ のとき直線$y=-k$
3. $x+y\ge 0$ かつ $x-y< 0$ すなわち $y\ge -x$ かつ $y> x$ のとき直線$y=k$
4. $x+y< 0$ かつ $x-y< 0$ すなわち $y\ge -x$ かつ $y\le x$ のとき直線$x=-k$

　確かに一辺$k$の正方形になる。

### 長方形を表す方程式

　これだけだと正方形しか表わせないので、正方形を表す方程式$(1)$を改造して、任意の**長方形を表す方程式**を作ります。例えば、長方形の横と縦の辺の長さの比を$2:1$にしたければ、上の場合分けにおいて$x= \,\sim$ で表される直線が $x=2k$ や $x=-2k$となればよいので、$x$ を$\cfrac{x}{2}$で置き換えると
$$
\left|\cfrac{x}{2}+y\right|+\left|\cfrac{x}{2}-y\right|=2k
$$
<img src="https://eecv1g.dm.files.1drv.com/y4mGsUTYdEF1vg_yl_s_XxO3hlzXJ5nhn-j7qRfDnMCL_PknM3iiaEd1PPwP4r6zDEaCqcVHL1y_NHnOdvM8sNZ7_XuMlBJET3dYUz4XhJVZVpo-ykzhQ4-mY2994NtjxbjGipaydt_twUeU7PAiCgLnUHfLKszrdSQ94O54r7KiSIgr5dyK_uHzQmtyPyOkAEACwvvLJ0aPAUTOf2jJjCKSw?width=2190&amp;height=1510&amp;cropmode=none" style="zoom:40%;" />

　見事になりました！

　ということで、横と縦の辺の長さの比が$p:q$の長方形を表す方程式は
$$
\left|\cfrac{x}{p}+\cfrac{y}{q}\right|+\left|\cfrac{x}{p}-\cfrac{y}{q}\right|=2k
$$
となりますが、この方程式に$k=1$を代入してみると、横と縦の辺の**長さが**それぞれ$p$、$q$の長方形を表すことが分かります。
$$
\left|\cfrac{x}{p}+\cfrac{y}{q}\right|+\left|\cfrac{x}{p}-\cfrac{y}{q}\right|=2
$$
　こうすることで、文字を一つ減らすことができ、また、辺の長さが比でなくなったので、少し扱いやすくなりました。しかし、これではまだ長方形を原点にしか置けないので、もっと使いやすくします。

　**点$(a,b)$を対角線の交点にもつ、横と縦の辺の長さが$p,q$の長方形は、**
$$
\left|\cfrac{x-a}{p}+\cfrac{y-b}{q}\right|+\left|\cfrac{x-a}{p}-\cfrac{y-b}{q}\right|=2 \tag{2}
$$
**と表される。**

## 関数の合体

　ゴシック体の**「西」**という文字を書くにあたって必要なのは、長方形の関数どうしを**合体させる**ことです。実は、簡単に関数を合体させることができる関数があります。それは **min** $(\,)$ **と max**$(\,)$ です。これを使うのは**ずるいですが、使っちゃいます**。それぞれの関数のはたらきを簡単に説明すると、

- **min$(a,b)$は$a$と$b$のうち小さい方を表す。**例えば、

$$
\min(a,b) = 0
\iff
\begin{align}
 \begin{cases}
 a = 0 \ (b \ge 0) \newline
 b = 0 \ (a \ge 0)
 \end{cases}
\end{align}
$$
 
- **max$(a,b)$は$a$と$b$のうち大きい方を表す。**例えば、

$$
\max (a,b) = 0
\iff
\begin{align}
 \begin{cases}
 a = 0 \ (b \le 0) \newline
 b = 0 \ (a \le 0)
 \end{cases}
\end{align}
$$
 

　この関数の仕組みをもっと詳しく知りたい人は、この方がすごく分かりやすくまとめられているので、こちらをご覧ください。

> **minとmaxで簡単☆本格数式お絵描き♪**
>
> https://corollary2525.hatenablog.com/entry/2019/12/11/224546

　見かけ上、$\min(a,b)$は$a$と$b$の**和集合**、$\max(a,b)$は$a$と$b$の**共通部分**みたいな感じです。

　ちなみに、今回は関数 **min** $(\)$ のみを使います。

## ついに完成へ

　どうやって、**「西」**の形にしようかいろいろ試行錯誤したところ、この長方形たちを使うことになりました。**「西」**という漢字は左右対称、つまり、 $y$軸に関して対称に書けるので$x$を$|x|$にすることで必要な式を少し減らすことが出来ます。$y$についても同様です。
$$
\begin{align}
 \begin{cases}
 \left|\cfrac{x}{7} + y \right| + \left|\cfrac{x}{7} - y \right| = 2 \newline
 \left|\cfrac{x}{7} + (|y + 8| - 4) \right| + \left|\cfrac{x}{7} - (|y + 8| - 4) \right| = 2 \newline
 \left|(|x| - 6) + \cfrac{y + 8}{5} \right| + \left|(|x| - 6) - \cfrac{y + 8}{5} \right| = 2 \newline
 \left|(|x| - 2) + \cfrac{y + 4}{5} \right| + \left|(|x| - 2) - \cfrac{y + 4}{5} \right| = 2 \newline
 \left|\cfrac{|x| - 4}{3} + ( y + 8 ) \right| + \left|\cfrac{|x| - 4}{3} - ( y + 8 ) \right| = 2 \newline
 \end{cases}
\end{align}
$$
（ちなみに上の式から、一画目、三画目の水平部分と六画目、二画目と三画目の垂直部分、四画目の垂直部分と五画目の垂直部分、四画目の水平部分と五画目の水平部分です。）

この長方形たちをminを使って合体させると...
$$
\min\left( \left|\cfrac{x}{7} + y \right| + \left|\cfrac{x}{7} - y \right|,
\left|\cfrac{x}{7} + ( |y + 8| - 4 ) \right| + \left|\cfrac{x}{7} - ( |y + 8| - 4 ) \right|,
\left|(|x| - 6) + \cfrac{y + 8}{5} \right| + \left|(|x| - 6) - \cfrac{y + 8}{5} \right|,
\left|(|x| - 2) + \cfrac{y + 4}{5} \right| + \left|(|x| - 2) - \cfrac{y + 4}{5} \right|,
\left|\cfrac{|x| - 4}{3} + ( y + 8 ) \right| + \left|\cfrac{|x| - 4}{3} - ( y + 8 ) \right|
\right) \le 2
$$
<img src="https://eebf7q.dm.files.1drv.com/y4m8Czv21zUge17M3gw4Brr3gVh0mGZ1mNLnBzR_of_H7oa3_gfMBIvarI02FCs6eNxVG8AXAHxmNUszqcBFszCzdBZGz288OpcAJeLX1dIWpR9DOcFrdboD046ZGoigeYpNAxwcuA_e5qCiNzarK1E9BZ-9dqqhhANyW1eJLtKR6sJSh0gNSDAjpEpq851EHPcpt3L6JLBvb2FzrelH449Og?width=2189&amp;height=1511&amp;cropmode=none" style="zoom:40%;" />

**できました！！！**

## おわりに

　うまくいってよかったです。数式を入力するのがすごく大変でした（そもそも式が長いのもあるけど、恥ずかしながら、筆者は初めて$\LaTeX{}$を使いました）。できれば min $(\,)$ や max$(\,)$ を使わずに表す方法が知りたいです（絶対値をいろんなところに置きまくればできる気がします（しません）（*注意：筆者の勘です*））。

　ここまで読んでくれた方はそうそういないと思います。**最後まで読んでいただきありがとうございました！！！**