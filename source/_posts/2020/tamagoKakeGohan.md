---
title: 卵かけご飯の総体積を求めてみた
date: 2020-10-3 0:02:25
tags: 2020年度
---

<div style="text-align: right">74期 がいらみ</div>

　ブォンジョルノ！（激寒） 数研会員兼卵かけご飯同好会会長のがいらみです。
このコーナーではみなさん疑問に思っているであろう卵かけご飯の総体積を求めたいと思います。

ということで手順を説明していくわよ

***①卵・米・醤油の体積を求める***
***②①で出た体積を全て足す***
***③終わり！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！！***

※条件
・米は0.5合(3250粒)、粒のサイズは長さ5.0mm、幅3.5mm、厚さ2.0mmとする。
・卵は長さ6.5cm、幅は関数により規定し、上から見た場合の形状は円とする。
・醤油は小さじ1杯(5mL)。ただしキッコーマンしぼりたて生しょうゆとする。

やっていきます。

**①-1-1 卵の関数を作る**

ネット漁ってたら出ました(怠惰)

![](https://jormta.sn.files.1drv.com/y4mCBZ6_N5RDOfOav4iMDyIapYBnxXfH0gOGs5wJVt2RvOnzf6z0jTmbHZSERtEzXiPzQIJU5PSpXISxymgDj9GCF9t88v6VxdZB13mWUT23czDuoHO8jMyCXczS7Vgc15j6wKY7Kwxm7_DddFcQgPvp-n6HYetWQrqzEARMHg9ff40N_jlNzdssoZlLaQJF5rFZ2_38Z_97UUftXLbEiycgA?width=1695&height=860&cropmode=none)

**①-1-2 卵の体積を求める**

上の関数を y = f(x) の形にゴリ押すと
$$
\begin{align}
&  y=\pm \sqrt{\frac{-2x^2+\frac{1}{2}x+\sqrt{4x^3+\frac{1}{4}x^2}}{2}}
\end{align}
$$
さ～～～てここまでいけば後は簡単。x軸回りに回転させて積分してから、相似比1.5:6.5=3:11より体積比27:1331、よって1331/27を掛ければ出てきます。
$$
\begin{align}
& \int_{0}^{1.5}\frac{-2x^2+\frac{1}{2}x+\sqrt{4x^3+\frac{1}{4}x^2}}{2}\pi dx \newline
=&\pi [\frac{1}{3}x^3+\frac{1}{8}x^2]\_{0}^{1.5}+\pi \int_{0}^{1.5}\sqrt{x^3+\frac{1}{16}x^2}dx
\end{align}
$$
ここでルートの中身がどうあがいても積分できなかったのでツールに頼ると
$$
\int_{0}^{1.5}\sqrt{x^3+\frac{1}{16}x^2}dx =\left[\dfrac{\left(16x+1\right)^\frac{3}{2}\left(24x-1\right)}{3840}\right]\_{0}^{1.5}=\frac{547}{480}\fallingdotseq 1.14
$$
よって
$$
\begin{align}
&\int_{0}^{1.5}\frac{-2x^2+\frac{1}{2}x+\sqrt{4x^3+\frac{1}{4}x^2}}{2}\pi dx \newline
=&\pi (-1.125+0.281+1.14) \newline
=&0.296\pi 
\end{align}
$$
これに1331/27を掛けると
$$
0.296\pi \times\frac{1331}{27}\fallingdotseq 14.6(\mathrm{cm}^3)
$$


**①-2-1 米の関数を作る**

球の方程式を良い感じに変形して作りました。（原理はよくわかって）ないです。

![](https://loox2a.sn.files.1drv.com/y4mS7QcHFDkzWavMANKPu6_PvM1Cglyf3XTQ0EUVZrK9Bgx6eBq8CWgrSpL1c22Tkqu2y3buy28FEu3CjfTAjDOFfInFztscfiJ1N9_bxne1CDWDdY30YzhOkRQlpBLE_TmWsFY9OAmVpi97fQJ9LhHK1NfFgBR6U-aEZkh_yWU-PVu8PAFiHY5r-on4Bd03uX2yL3aps5YJq4tGONzdMR9-Q?width=2316&height=1386&cropmode=none)

**①-2-2 米の体積を求める**

先ほどと同様に上の関数を z = f(x,y) の形にゴリ押すと
$$
z=\pm \sqrt{-\frac{4}{25}x^2-\frac{16}{49}y^2+1}
$$
ここからはちょっと難しくなりますが簡単です。２重積分していくわよ。

ここでめちゃくちゃめんどくさいですが積分領域Dを求めるためにxy平面で切り取った関数(楕円)について考えていきます。
$$
\begin{align}
x^2+\frac{100}{49}y^2=\frac{25}{4}
\end{align}
$$
よって
$$
\begin{align}
& y=\pm \sqrt{-\frac{49}{100}x^2+\frac{49}{10}}
\end{align}
$$
積分領域Dが求められたので以下の２重積分を計算して出た値を８倍したものが１粒の体積になります。
$$
\begin{align}
&\iint_D\sqrt{-\frac{4}{25}x^2-\frac{16}{49}y^2+1} dxdy \newline
=&\int_{0}^{2.5}\int_{0}^\sqrt{-\frac{49}{100}x^2+\frac{49}{10}}\sqrt{-\frac{4}{25}x^2-\frac{16}{49}y^2+1} dydx 
\end{align}
$$

さ～～～てよくわかんないのが出てきてひたすらめんどくさいから積分自動計算サイトを頼るわよ～～～


$$
&\int_{0}^\sqrt{-\frac{49}{100}x^2+\frac{49}{10}}\sqrt{-\frac{4}{25}x^2-\frac{16}{49}y^2+1} dy \newline
=&\dfrac{\left(28\mathrm{i}x^2-175\mathrm{i}\right)\operatorname{arsinh}\left(\frac{2\sqrt{490-49x^2}\sqrt{4x^2-25}}{28x^2-175}\right)+2\sqrt{15}\mathrm{i}\sqrt{490-49x^2}}{200}
$$

？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？(精神崩壊)

もう後に引けないので全部計算サイトにぶち込んでいきます
$$
\begin{align}
&\int_{0}^{2.5}\dfrac{\left(28\mathrm{i}x^2-175\mathrm{i}\right)\operatorname{arsinh}\left(\frac{2\sqrt{490-49x^2}\sqrt{4x^2-25}}{28x^2-175}\right)+2\sqrt{15}\mathrm{i}\sqrt{490-49x^2}}{200}dx \newline
=&\left[\dfrac{7\mathrm{i}\left(125\ln\left(\frac{\left|\sqrt{15}\sqrt{10-x^2}+3x\right|}{\sqrt{10-x^2}}\right)-125\ln\left(\frac{\left|\sqrt{15}\sqrt{10-x^2}-3x\right|}{\sqrt{10-x^2}}\right)+\left(8x^3-150x\right)\operatorname{arsinh}\left(\frac{2\sqrt{10-x^2}}{\sqrt{4x^2-25}}\right)+2{\cdot}15^\frac{3}{2}\arcsin\left(\frac{x}{\sqrt{10}}\right)+4\sqrt{15}x\sqrt{10-x^2}\right)}{1200}\right]_{0}^{2.5} \newline
=&-2.290744043242558+3.071563268594146i
\end{align}
$$
？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？？(発狂)

終わった。完全に詰みだ。絶望した私は無気力のままインターネットを放浪した。我々はどこから来てどこへ行くのか、どのような学問を究めるのか、今日のお弁当は何かなどなど様々なことを考えていると、とある先輩から「米粒の体積を求められるサイトがある」と聞き、素晴らしいものに出会った。
[https://keisan.casio.jp/exec/system/1169425933](https://keisan.casio.jp/exec/system/1169425933)←これ

ということで無事体積は求められた。今までの苦労は何だったのか。２重積分とは何だったのか。
$$
(米１粒の体積)=18.3\mathrm{mm}^3
$$
これに3250を掛けて
$$
(米０.５合の体積)=59475\mathrm{mm}^3\fallingdotseq 59.5\mathrm{cm}^3
$$
**①-3 醤油の体積を求める**
$$
5\mathrm{mL}=5\mathrm{cm}^3
$$
草


**②①で求めた体積を全て足す**
$$
14.6+59.5+5=79.1(\mathrm{cm}^3)
$$
今これを読んでいる読者は感動のあまり目に涙を浮かべているであろう。幼少期からの疑問、長きにわたる未解決、世界の真理が今、ついに、判明したのである。

我々が食す卵かけご飯の総体積はここにある。この論文は多くの数学者の卵かけご飯に対する怨霊を成仏させ、民衆は快哉を叫び、大いに世界に貢献するものとなることだろう。
今後の数学会、卵かけご飯学会の発展を祈念し、今回は筆を置かせていただく。ここまでありがとう。