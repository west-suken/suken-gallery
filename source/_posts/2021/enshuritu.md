---
title: 区分求積法と円周率π
date: 2021-07-24 17:04:06
tags: 2021年度
---


<div style="text-align:right">LikU</div>

”区分求積法”いう文字列がある。この文字列には「図形の面積や体積を求める方法」という意味、すなわち言葉が与えられている。

## ０．三角形

試しに三角形の面積式を区分求積法で求めてみようとしてみる。

あ～、…このソフトの図の入力を理解する労力Rが　1=R/(R+1)　..有効数字2兆桁　私は図の入力方式を理解するプロセスを停止しました。トラブルシューティングします……解決法が見つかりました。謝罪します。めんどくさいので文字記号だけで記述します。すみません。早く手を動かしたほうがいいですね。ペンを持って書きながらやるといいかも..です.



三角形を、底辺と平行にｎ等分する。分割された断片は、台形が(ｎ-1)個、三角形が1個である。そこで全ての断片を、長いほうの底辺を基にした長方形に置換する。段差のあるピラミッドを想像してほしい、平面版ピラミッドみたいなのだ。

そして全ての長方形の和を求める。しかし長方形に置換すると元の三角形との誤差が生じてしまう。そこでｎ等分のｎを限りなく、無限に大きくする。顕微鏡で見ると表面が凸凹な紙みたいなイメージ。(ｎは無限なので顕微鏡で拡大していったとしてもいつまで経っても凸凹は見れないだろう。無限倍の倍率...なら？)



というわけで、底辺a,高さhとしよう、式は

(a×h/n)+(a×((n-1)/n)h/n)+(a×((n-2)/n)h/n)+・・・+(a×((n-(n-1))/n)h/n)=ah×(n+n-1+・・+2+1)/n^2

1からnまでの総和は尻尾と頭を足して×項数÷2＝n(n+1)/2　　　なので

ah×n(n+1)/2n^2=ah(n+1)/2n=(ah/2)×(n+1)/n

さて思い出してほしい、ｎは無限に、限りなく大きいことを。(n+1)/n　の１はｎが大きくなるにつれて相対的に小さくなっていく。展開したほうがわかりやすいな、(n+1)/n=1+1/n

1/n はｎが限りなく大きくなると、限りなく０に近づく。y=1/x　のグラフを思ってほしい。

つまり　lim n➝∞(1+1/n)=1　と書ける(ぼこぼこじゃねーか)。よって



(ah/2)×(n+1)/n=(ah/2)×1=ah/2

できました！

(＊補足：長方形を１つ下にずらして一番下の長方形を抜かしたものを用意し、そいつも用いて不等号を用いて挟みうちするともっとわかりやすい)

## １．錐体

さて、なぜ錐体の体積Vは　V＝底面積＊高さ＊1/3　で求まるのだろうか。では、区分求積法で錐体の体積式を求めてみようとする。(パソンコで打つのすごく大変なのに気づきました、雑目が出ても仏の心で読んでやってください)

三角錘でも円錐でも2兆5億角錘でもなんでもいい(円は角が無限にある、つまり正無限角形ともいえると思う、なのでさっきの順序としては三角錐＜2兆5億錘＜円錐  かな、なんでもいいって？)。先程と同じように底面と平行にｎ等分し、それぞれの部分の大きい底面を基にして柱に置換する。

底面積をs,高さをhとすると

(s×h/n)+(s×((n-1)/n)^2×h/n)+(s×((n-2)/n)^2×h/n)+・・・+(s×((n-(n-1))/n)^2×h/n)

三角形のときと比べて変わったところがわかるだろうか。^2、2乗が入っている。これは、相似比がｎ倍になると面積はｎ^2　になる、そういうことだ。

sh×(n^2+(n-1)^2+・・+2^2+1)/n^3



1+2^2+3^2+・・・+n^2=n(n+1)(2n+1)/6　である。これの証明に関しては調べてくれ。頼む。(やる気的なのを)今は持ってないんだ。勘弁してくれ。

sh×n(n+1)(2n+1)/6×n^3=sh×(n+1)(2n+1)/6×n^2=(sh/3)×(n+1)(2n+1)/2n^2



さぁやってまいりました、に ん じ ん し り し り  ！ここをねほら、こうやる(やったから)と、

((n+1)/n)×((2n+1)/2n)

(n+1)/n　　　ここは、１だよね！(迫 真)

(2n+1)/2n　　ここも、１だよね！！(ねぇ！！)



ほらみて、

に　ん　じ　ん　｛(sh/3)×1×1=　sh/3=V｝　し　り　し　り

おえ(嬉しい)



## ２．Divided quadrature～区分求積法～：円(3.14才)の場合

錐体の1/3が数列を経由して導かれた。

私はまた、同じように円の面積を求めてみようとした。(ここでLikU(16)、画像挿入がボタン１つでできることに気づき驚愕、涙が止まらない)

![円　区分求積](https://dm2302files.storage.live.com/y4m0MLHzVHn-5Ya2H60uR2c_6sWReGifBErgyIxTcM4tyH7rzsKOiDT_vsv1GrV9z0gGhz6W1f9cUu0N8Y6_CAUgSpdnCIUUKoHU01d1A_wILY6jj6T1cVNU-8OvhbroOngAfc0fvTF47IZoWt3rz7bBkM_eVOrnQZW0Jmfex4MlyvxrKefhp_ceJ4UD5u9ULgg?width=1437&height=1139&cropmode=none)

円の面積を求めるにあたってまず円を半分に分割し、できた半球をさらにｎ等分して長方形を生やす。

任意のｒは三平方の定理により求まる。

r₁=r,　r₂=√(r^2-(r/n)^2),　rₙ=√(r^2-((n-1)×r/n)^2)　　　　r列の図  ↓

![IMG_20210912_190141](https://dm2302files.storage.live.com/y4m5OEZbJ6rZuLTgKj-hdWASNTrQTyXaX11rZOgDFmftQeVcgcenVDJtREN9MVZeqndtIND8ENb3rnDmdZgEBRauIehvMq_ztjedtOB5ojzzKueKcSOaCQPBAJGWikq4-6OAMGSU-45LwToS9xPHz_dP8UhkOlNwDX5ANQ_Ct76-6YDQQJp5l4ounZD3NmG8S9r?width=3078&height=462&cropmode=none)

(それぞれのｒにr/nをかけたものの総和)×４、係数をまとめると、(ｒの総和)×(r/n)×４、それが円の面積となるはずである。ｒの総和をＳᵣとする。

![](https://dm2302files.storage.live.com/y4m2dNaxfK7fmWhAX3lDy4sMWCsdMK-ljMewmFiRCw1bwZGnwqWcsdlKyOF25Yksl4gZh6wuVCsrlQ773kmW8In4uRWk-ZozC7x_-DbCBSCaw0ska2jonmr4Cue3xGUnM805N1nIsm2Ddda7C4SN07M0cFVDtCYaS3YF87rsWOWVYpfNkt0_uckrxflUkYp8bbQ?width=1661&height=344&cropmode=none)

Ｓᵣを数式で表すためにΣ(シグマ)を用いた。Σは数列の総和の記号である。

![IMG_20210912_190746](https://dm2302files.storage.live.com/y4mmQhJhiUJFoVL0TG4Cy6sMfA-izk-hbBETAZvG70v44XppcGwwUSUPldsmCwdu_-kezk2TIYVM22ORRsJnQs6MaWhOljl_FQn4FPKf0jVkKEgqKpWBm8SsixnZjTnFljr-szePOoUWPHqmkmhUiBzdTEWDB7tfl9QLdjjnM4Rr_WsKBcDLOXlIufLqSNVVJJr?width=2216&height=332&cropmode=none)

![IMG_20210912_190218](https://dm2302files.storage.live.com/y4mJY8o6S9HU98XOuZosgY-t__wn7q2Xrhpwq6APRNcn3cCroIBxvojErTXdpa5-5z9HxmvMI01AZVn2O_9BUZ6MCwAmToZ0EqTawFqxBm76HEd8IYkXqgCLUNoLGhJsPpQMg_FjH9TTLDopnsV7GJbKLtPla1crO0xc2p8OA6zj1R3PPUli9UEjRInpF7jprgS?width=2665&height=403&cropmode=none)

式のＳᵣに中身を代入すると、

![IMG_20210912_190814](https://dm2302files.storage.live.com/y4md1jovA8fVsd0McvLTrIaQcHtMJHGlsevuK10DUAwhST9LGyr0buSKk0KeGM5q_8M3hfbgTGqxPv6QxYGhr7zLetruOWETUr4Z-3dO1zdFi9u6-SOU4VV8k4VB6obZzPLIb6LYZmE8FYNpBQ4dOzIO1QOZ1guVhYF3ndiHi1Vv9vjBoZFcbRpAEMGszWoco2M?width=1941&height=402&cropmode=none)

円の面積式が得られた..。



初めてこの数列・数式に出くわしたとき、√によってこれ以上の計算ができず行き詰まり、困惑した(球の体積は求めることができたのだが円ではできなかったからだ)。



そこで逆に、世の中で知られている円面積の式、　S₌πr^2　　のSに、得られた式を代入して



![IMG_20210912_202118](https://dm2302files.storage.live.com/y4mm90NQYOAWWKi-yJGcmW4Z6hRcv8MCwVCAJjtU10PclA1umq0sd9oO3aox8g4AIFurH684G7bblCJEzBWn5i9lozquBtNxT9UxFHgQTd1ZI3g1ghRDYuSwpGNZWorCotHITyUVDTRm7Q51jlcW9_UIA6CiDjP1DCXa4deVctGFGjDZfpZyBAwFFgs9U8KSqEI?width=2137&height=595&cropmode=none)

r^2で割ると

![](https://dm2302files.storage.live.com/y4m_P9iN4lmVM5IosHioFkPWp7iZ3kVrk94t-byu0Vj4C-LcTqIENSloDRX82mKBMwMwd7DU-4z-BpUY8cc9lRiyBTvne9Ln8-oNI4ePpUEff2oe2ttvoyLb5gm8CQXFOBOsU6rnp8WdgeYL0QwC75w5wU_495to02JhE2jb991I5s2gmkxofA2mjGHjw6GmB0J?width=1380&height=452&cropmode=none)

さいごにｎは無限だということをお忘れなく

![last](https://dm2302files.storage.live.com/y4m0AEwJSg2n-4Q65HM3tlnOvBm9uP-f9QuzU5fZ3OZnGnBiHQ90hAOsSP1LstNNCKNzkpJ_KxIGF8iHMmyw7fhisUsG9oYQe621yv5asrLLTDZBZKi5izbAvaX-WqbyBb0-6yGqBbl9daWyUnghOxScSp4beK_fp1kHqmzETJUgl11ICBGkxOMkLefm8_Xiqxn?width=1362&height=517&cropmode=none)

できた。



πが無理数であることや、円の面積がなぜπr^2なのかといったことは示せていないが、

πを数列で表すことができた。

自分が初めて見つけたわけではないかもしれない、いや初めてではないだろう、しかし自分はこの式を発見した。とても興奮することであった。



以上、区分求積法に関して少し語らせてもらった。区分求積法は他にも、曲線に囲まれた領域の面積を出したりすることができるらしい。

数学にとりこまれるきっかけとなった主題である。



区分求積法を知った本　「モノグラフ　数学史　　矢野健太郎　著」

P.S.

今のところ自分が一番納得する円の面積式の解釈

https://www.youtube.com/watch?v=nu1Mamdbt0U&list=PLa2RYiNh0IwWowsuvIhfIMJvHIJvyR6E4&index=2

![IMG_20210912_212229](https://dm2302files.storage.live.com/y4mnpgdaAHE2CVQVDjWhPTwTQONaEC6zCidHB4cyaby4HE3wdowu6pDv26JV6C9Fnd0VYJcP1aQcCaTuJsCmRl8oEmSHGllzBZ6QOkfbrf3j_j64Jw5dmVMlqVr_8D0xgJVdsYfI4NZs1cREZqV_IzkXIggxpgXg2HIyHV_OlnRQ2S0V_-bTDmnd24XZ93GVYcP?width=1309&height=1117&cropmode=none)

r × 2πr=2πr^2