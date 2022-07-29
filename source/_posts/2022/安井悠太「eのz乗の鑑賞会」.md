---
title: eのz乗の鑑賞会
date: 2022-07-30 8:54:00
tags: 2022年度
---



# eのz乗の鑑賞会

<div style="text-align: right">76期 椅子屋</div>

## はじめに

私は（一応）数研副会長なので、部誌を書く義務があると思い、課題や他部活の活動に追われながら、締切ギリギリでテーマをどうにか決定しました。高校の体育の授業でハンドボールをやる機会があり、私のチームの名前を私がeのx乗と名付けたことを思い出し、それならばeのz乗について書こうと思った次第です。このように動機が浅薄なので（実際問題始めるのが遅い私のせい）、内容の厳密性につきましては目をつむっていただけると幸いですね。1年生にはわからない内容を多分に含んでいますので（わかる人も西高生であればたくさんいると思います）、わからない箇所があればご自分で調べていただければ勉強になるとおもいます。今から話す内容は複素関数（複素解析）の初歩の初歩で、その美しさ（なんてまだ僕も十分に理解していませんし到底部誌で表現できません）に惹かれた人はぜひとも数研に入り、研究してみてはどうでしょうか。

## eのz乗とは

題名がわかりづらかったかもしれませんが、eのz乗とは、（別にzじゃなくてもいいんですけど一般にはz）実数の指数関数を複素関数に拡張したものです。実数の指数関数と似た性質や、異なる性質があって面白いです。
では簡単に定義から。
$$
f(z)=e^z=\sum_{n=0}^{\infty}\frac{z^n}{n!}
$$
（いや、指数関数のマクローリン展開を複素数に拡張しただけ、、、）
代数的に表すと、
$$
\begin{eqnarray*}f(z)&=&e^z\\&=&e^{x+yi}\\&=&e^x(\cos y+i\sin y)\end{eqnarray*}
$$
二つの式は同値です。ご覧のように、複素関数では変数が4つ（入力する値の実部と虚部、出力する値の実部と虚部）あるので、4次元の世界を表すことになり、グラフを視覚的に捉えることが不可能です。しかし方法はあります。

## 三次元で捉える

先ほど記した関数を実部と虚部に分けて考えます。この関数の実部をu(x,y)とおくと、
$$
u(x,y)=e^x\cos y
$$
となり、虚部をv(x,y)とおくと
$$
v(x,y)=e^x\sin y
$$
となります。この2変数関数を3次元グラフで表してみましょう。まず実部から。

![](https://firebasestorage.googleapis.com/v0/b/type-c1c71.appspot.com/o/UqxSEMTv9IR2fYhRVxGOuZK1Obl2%2FdxFLW2EluFY2fMBr.jpg?alt=media&token=b098bbe6-b337-405e-bb73-b3caddd08e81)

（緑がy軸で赤がx軸です。って白黒印刷！？）
虚部はこんな感じです。

![](https://firebasestorage.googleapis.com/v0/b/type-c1c71.appspot.com/o/UqxSEMTv9IR2fYhRVxGOuZK1Obl2%2FJQppMY3YWOcFlTYd.jpg?alt=media&token=f2680c04-ea9b-4227-b8b6-03afc92e14d1)

当たり前ですけど、3次元で捉えても三角関数の周期性、指数関数の増加の様子が垣間見えますね。
では、今度は二次元で捉えてみましょう。

## 二次元で捉える

どうすれば二次元で捉えることができるのか？みなさんもぜひ考えてみてください（方法はたくさんあります）。

### 1.虚部固定

zの虚部の値を固定することで、zの実部だけを変化させてこの関数を捉えます。定義域を定めて、グラフを見やすくします。上のグラフが入力する値の動き方（いわゆるz平面、xとyのグラフ）で、下のグラフが出力する値の動き方（いわゆるw平面、uとvのグラフ）です。（以下のグラフも同順）どちらも媒介変数表示になります。（そのu,vの式は上記）

![](https://firebasestorage.googleapis.com/v0/b/type-c1c71.appspot.com/o/UqxSEMTv9IR2fYhRVxGOuZK1Obl2%2FZ8VAux8oQTYB41XW.jpg?alt=media&token=015b091a-f25f-4493-8817-15302c3873f9)

![](https://firebasestorage.googleapis.com/v0/b/type-c1c71.appspot.com/o/UqxSEMTv9IR2fYhRVxGOuZK1Obl2%2F17AYsAsOlpzPnZFK.jpg?alt=media&token=e680069a-a31d-4a8e-8788-bd55507abf65)

③の場合は実関数の指数関数と同じことをやっています。なぜなら、y＝0の時、uの値がe^x、vの値が0となるからです。下のグラフではuの値がu座標上で動いていますね。このuの値が実関数のyの値に相当するわけです。点の集合として捉えているので分かりづらいですが、もちろん実際の変化の速さは一様ではありません。

### 2.実部固定

今度は実部を固定します。

![](https://firebasestorage.googleapis.com/v0/b/type-c1c71.appspot.com/o/UqxSEMTv9IR2fYhRVxGOuZK1Obl2%2Fp4zSuId8rxUI6PPM.jpg?alt=media&token=e83f58e1-25ed-4c0f-ab9b-ec42aa86de3d)

![](https://firebasestorage.googleapis.com/v0/b/type-c1c71.appspot.com/o/UqxSEMTv9IR2fYhRVxGOuZK1Obl2%2FsOA2OERGDcJgT1VG.jpg?alt=media&token=b1dce007-f64d-4156-96b5-e68be354b0c7)

虚部yがf(z)の偏角の値になるので、yが変化すると、w平面に描かれるグラフは円になります。

### 3.絶対値固定

今度はzを極形式で表した時のf(z)を考えましょう。
$$
\begin{eqnarray*}f(z)&=&e^{re^{i\theta}}\\&=&e^{r({\cos{\theta}+i\sin{\theta}})}\\&=&e^{r{\cos{\theta}}}e^{ir{\sin{\theta}}}\\&=&e^{r{\cos{\theta}}}\bigr\{{{\cos(r{\sin{\theta}})}} +i{\sin({r{\sin{\theta}}})}\bigr\}\end{eqnarray*}
$$
先程と同様実部と虚部を媒介変数表示します。
$$
x(r,\theta)=r{\cos\theta}\\y(r,\theta)=r{\sin\theta}\\u(r,\theta)= e^{r{\cos{\theta}}} {{\cos(r{\sin{\theta}})}}\\v(r,\theta)= e^{r{\cos{\theta}}} {\sin({r{\sin{\theta}}})}
$$
これを利用して、zの絶対値rを固定してθを動かします。
![](https://firebasestorage.googleapis.com/v0/b/type-c1c71.appspot.com/o/UqxSEMTv9IR2fYhRVxGOuZK1Obl2%2FpjCJfgJFM9eopGl2.jpg?alt=media&token=5c61be2d-2e4c-49aa-a559-84f015e79e4f)
![](https://firebasestorage.googleapis.com/v0/b/type-c1c71.appspot.com/o/UqxSEMTv9IR2fYhRVxGOuZK1Obl2%2FrZSpiee0ADffPJJH.jpg?alt=media&token=aa9fbf05-5696-4640-83f7-a06e7a0a8134)

### 4.偏角固定

偏角を固定するとこうなります

![](https://firebasestorage.googleapis.com/v0/b/type-c1c71.appspot.com/o/UqxSEMTv9IR2fYhRVxGOuZK1Obl2%2FKZ07TmiFkbnsfgcF.jpg?alt=media&token=7e485c7c-dc59-4b7d-a715-0efd455f11c6)

![](https://firebasestorage.googleapis.com/v0/b/type-c1c71.appspot.com/o/UqxSEMTv9IR2fYhRVxGOuZK1Obl2%2FKzrtfzVXEgSTvSk0.jpg?alt=media&token=aee99044-927b-490f-a809-7ebca6b36cb3)

## 見て感じる

今まで、複素指数関数のグラフを視覚的に捉えてきましたが、これくらいであれば（極座標表示のものはちょっと複雑ですが）数式から想像することができます。しかし、実際にみてみるとその美しさを再認識することができますね。（まとめで手抜き感を払拭する）

## 終わりに（そして蛇足）

この場を借りて、一年間数研を75期会長並びに幹部の皆さん、そして76期会長、皆が気持ちよく活動できるように尽力して下さりありがとうございます。この部誌を製本してくれたみんな、知的労働だけではなく肉体労働もお疲れ様です、ありがとうございます。最後に、この部誌を読んでくれた君、本当にありがとう。記念祭の部誌は複素関数についてもっと深掘りした内容を書きたいと思います。（さて、実数の指数関数は微分しても変わりませんが、複素指数関数を微分するとどうなるでしょう？)
