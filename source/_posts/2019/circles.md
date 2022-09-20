---
title: 大円の中に、２つずつその円に入る最大の円を入れていってみたら…
date: 2019-09-08 11:08:39
tags: 2019年度
cover_index: https://pe0goq.bn.files.1drv.com/y4mSRUL88I-aSjPQdjFLTfDZgf67oqhEkANr0cfggxiXV0xs3UThp0rg7_OD_uXalTbSR9Q8GSzZfBizAxXsOLlqwJnqBekZw4YvUZ-XIvSBoT0kpxs0Xc5ygD0kdWVYJs36XZukx2iWrM4gjfX1EuOtfeaWnzda3ipW0pfdoIe9Q3eC9ZqiZa8lc0roTr6AVaLQfMi6S0beFQyxvatE4-ZUw?width=660&height=254&cropmode=none
cover_detail: https://pe0goq.bn.files.1drv.com/y4mSRUL88I-aSjPQdjFLTfDZgf67oqhEkANr0cfggxiXV0xs3UThp0rg7_OD_uXalTbSR9Q8GSzZfBizAxXsOLlqwJnqBekZw4YvUZ-XIvSBoT0kpxs0Xc5ygD0kdWVYJs36XZukx2iWrM4gjfX1EuOtfeaWnzda3ipW0pfdoIe9Q3eC9ZqiZa8lc0roTr6AVaLQfMi6S0beFQyxvatE4-ZUw?width=1300&height=500&cropmode=none
---

by sabandhu

## はじめに

円は図形の中でもとても特殊で不思議な形である。そんな円を題材にしたら何か面白い発見があるのではないかと思い、今この記事を書いている(この記事が面白いと言っている訳ではない)。

## トピック：円の中に円を入れてみる

![](https://9p0koq.bn.files.1drv.com/y4mUMiJPoR4wKdpT1YmvpptKgsUsghdPECev5HVXGoMj5gL1MUnyFJZlYkQz1Q3gqyscaCEI-Vt_QQ7BVnNV_Fho2PI6FUUDIc3vZYJqynzC_Gb4hsZxr-YrkG-VksMFtz048EXM2DycdoGVeJufiRegPEF-noFOL1WqeTklVB4-V_zA59hbsNYAsfzzzze8HB2C6jGPix-aHvmAZ0hzsnf1g?width=1024&height=267&cropmode=none)

という具合にして2つの円を同時に入れる時、それぞれの円の半径が最大になるように円を増やしていくと、円の大きさはどういう規則性で小さくなっていくのか気になった。

(i) の円の直径を $ d_1=1 $ ,半径を $ r_1= \frac{1}{2} $ とした。
(ii) の円の直径は $ d_2=\frac{1}{2} $ ,半径は $ r_2=\frac{1}{4} $ である。
(iii) の円では三平方の定理を使って求めた。$ (\frac{1}{2}-r_3)^2+(\frac{1}{4})^2=(r_3+\frac{1}{4})^2, r_3=\frac{1}{6}, d_3=\frac{1}{3} $ となった。（余談：この時に用いた直角三角形は辺の比がなんと3:4:5になった。なぜだかわからないが…)*1

さて、ここまで円の直径（半径）は全て有理数になった。自分でやっていてびっくりした。この規則性からいくと、 (iv)の円は $ d_4=\frac{1}{4} $ だろうか。しかし、ここからが問題であった。筆者の力量では、(iv)以降の円の大きさは計算では計算できなかった。そこで、強硬手段を使ってしまった。

「実際にコンパスと定規で書いてしまえ！」

(iv) 実際に書いてみたところ円の中心は下図で示したようにふたつの円の直径の垂線の交点上に存
在する*2ように思われた。

ぴったり！３つの円に接する円がかけた。実験的に証明できたようだ。長方形を利用して(iv)の円
の大きさを求めると、直径は $ d_4=\frac{1}{6} $, 半径は $ r_4=\frac{1}{12} $となった。ここまでをまとめると、

||直径 $d$|半径 $r$|
|-|--|--|
|(i)|$\frac{1}{1}$|$\frac{1}{2}$|
|(ii)|$\frac{1}{2}$|$\frac{1}{4}$|
|(iii)|$\frac{1}{3}$|$\frac{1}{6}$|
|(iv)|$\frac{1}{6}$|$\frac{1}{12}$|

全て有理数になった。そして、直径について発見された規則性*3は、... よくわかりませんでした。もう少し(v)，(vi)の円について考えないと分からなさそうなので、続きはオンライン用のほうで書いてみたいと思います。やってみたい人はぜひ挑戦してみてください！

## 終わりに

今回、このような形で円について研究？してみて思ったよりもたのしかった。締め切り間近ということもあり、２、３時間で書き上げたこの文章にどこか変な日本語があるかもしれませんがご勘弁してください。読んでくれてありがとうございました！

## おまけ

僕は今回この記事で解決できませんでしたが、
　*1：3:4:5の直角三角形が出現する理由
　*2：(iv)で出てくる円の中心と垂線の交点が一致する理由
　*3：直径の長さの規則性
について考えてみてください。答えがわかったら是非教えてくれると嬉しいです。

## おまけのおまけ

このトピックと少し関係あるかもしれない面白いサイトを見つけたので、ここに貼り付けておき
ます。一つの円の中にどんどん円を入れていったらどうなるかが１から５０００個まで入れていっ
たときのシミュレーションのサイトです。

http://hydra.nat.uni-magdeburg.de/packing/cci/
