---
title: Make Numbers into 10
date: 2022-09-19 22:11:00
tags: 2022年度
cover_index: https://dsm04pap001files.storage.live.com/y4mcKDoFg6vOpq1linjJcaFwAtuia_d2Akkli0fKlN-FdZtq3oWmnInncAqSMvO2Xe27yA8uHdfU-os_O_VAo-ndtsaGf3ytPhKhEt7I8pWxI1qzim_gX1WajAiJMOWCETb9-kgDGHdxBIlDeviCz4FLe9uJNaz5GgCzmxjPKNdWmJ4_L_J-L4hsA7Rn3PPdgTz?width=991&height=379&cropmode=none
cover_detail: https://dsm04pap001files.storage.live.com/y4mcKDoFg6vOpq1linjJcaFwAtuia_d2Akkli0fKlN-FdZtq3oWmnInncAqSMvO2Xe27yA8uHdfU-os_O_VAo-ndtsaGf3ytPhKhEt7I8pWxI1qzim_gX1WajAiJMOWCETb9-kgDGHdxBIlDeviCz4FLe9uJNaz5GgCzmxjPKNdWmJ4_L_J-L4hsA7Rn3PPdgTz?width=991&height=379&cropmode=none
---

## 杉並区選挙ポスター掲示場の謎を追え！

<p style="text-align: right">OH27<sub>(9)</sub>,ド・ジッター,LikU,うーた
ん,じぇばだいあ,小夜時雨</p>

2022/6/1　数研会員T氏が投稿した一言から始まった。
「この順番になる数列ありますか？」
![](https://dsm04pap001files.storage.live.com/y4mJGV0xOb1-1U5bjVKCl2M1AKge3lAaw3_w280TEaixls_ZikUcCqaZv72OweYT11E0Rhu7NXJO_rvp-q7HUy-HheNw9zLixJmqNcpM8z2alfyrOl7oeI9cCkJuOfhPFcbKZMFip5VdChrSaZm1ynDp9PXN1O1tjEgW26CAXoRihD5Tk5PQW8IazbL7a7gKJ_i?width=1075&height=400&cropmode=none)

OH27<sub>(9)</sub>は、四則演算で10にするゲーム(テンパズル、メイクテンというらしい)を思いつき、会員にアンケートをとった。その結果を報告する場としてこの記事を書く。なお、多くの回答が四則演算を逸脱している。
早速見て行こうと思うのだが、**控えめに言ってえぐすぎ**なので驚かないように。

### 勝手に関数作ってみた

便宜上、ここだけで通じる関数をつくる。

$〔a,b,c,\cdots 〕= n$　　$(a,b,c$は整数$)$

$a,b,c,\cdots$を、四則演算に限らずどうにかして$n$にするという関数。需要はほぼない...
<div style="page-break-before:always"></div>

### アンケート結果

あまりにも式が多い(たくさん回答してくれたおかげです)ので、1つの関数につき1つの回答だけを紹介する。

#### 基本レベル

①$〔15,1,6,13〕= (1-6)(13-15) = 10$　by 小夜時雨
　　マイナス同士をかけるという発想が面白うございますね

②$〔1,14,13,4〕= 4-(14-13)-1 = 10_{(2)}$　by LikU
　　に、二進数だとおぉ！

③$〔14,8,4,3〕= 14+8+4×3 = 29 = P(10)$$(=10$番目の素数$)$　by LikU
　　なんで素数が思いつくん！？

④$〔8,10,3,11〕= 8+10+3-11 = 10$　by じぇばだいあ,小夜時雨
　　シンプルな美しさってやつ

⑤$〔6,13,5,2〕= 13+5-6-2 = 10$　by ド・ジッター,LikU,うーたん,じぇばだいあ,小夜時雨
　　みんな同じだったw

⑥$〔13,4,2,7〕= 4×(2+7) ≡ 10(\text{mod}\,13)$　by LikU
　　世界が広すぎるんだって

⑦$〔4,3,7,9〕= (4-3)^7+9 = 10$　by うーたん
　　1の累乗って有用性高いよね

⑧$〔3,11,9,12〕= \displaystyle\frac{(9×12+3)}{11} ≒ 10$　by LikU
　　≒は敵わんって

⑨$〔4,2,5,14〕= \displaystyle\frac{14}{2}+5-\sqrt{4} = 10$　by ド・ジッター
　　ルートは上手すぎるぜ

⑩$〔2,11,14,6〕= 6+(14-11)!-2 = 10$　by ド・ジッター
　　感嘆の声が漏れてしまった

⑪$〔11,7,6,13〕= 11-\displaystyle\frac{13}{(7+6)} = 10$　by じぇばだいあ
　　与えられた数のいくつかで和を作れると強いみたい

⑫$〔7,1,13,10〕= {}_{7-Ta(1)}C_{13-10} = 10$　by ド・ジッター
　　もうよく分かんないけど、$Ta$はタクシー数を表すらしい

⑬$〔5,14,15,12〕= 14-\displaystyle\frac{5×12}{15} = 10$　by じぇばだいあ
　　60をつくるのいいね

⑭$〔14,6,12,8〕= 14-\displaystyle\frac{6×8}{12} = 10$　by 小夜時雨
　　48つくるのもいいね

⑮$〔6,13,8,3〕= 13-\displaystyle\frac{6}{\sqrt[3]{8}} = 10$　by 小夜時雨
　　3乗根も上手すぎるぜ

⑯$〔13,10,3,9〕= |-9|+\log_{13} (10+3) = 10$　by LikU
　　その絶対値へのこだわり好き



#### 応用レベル

⑰$〔15,1,14,6,13,4,5,2,7〕= 6+4+(15-14-1)×2×5×7×13 = 10$　by じぇばだいあ
　　0よ、待ってたぞ。

⑱$〔1,14,8,13,4,3,2,7,9〕= (7×8×13)/(1×9×14)$　$(4$捨$(2+3)$入$)=
10$　by LikU
　　マジでよく思いついたな

⑲$〔14,8,10,4,3,11,7,9,12〕=
\displaystyle\frac{14+8-10}{4}-\displaystyle\frac{11+7}{9}+12-3 = 10$　byうーたん
　　なんとも言えないこの興味深さ

⑳$〔4,2,11,5,14,6,15,12,8〕=
φ\left(\displaystyle\frac{((p(10)+μ((13+6)×7)+1_\mathbb{Q}(11))×\log_3 9}{8}\right) =
10$　by ド・ジッター
　　$φ(n)$：オイラーの$φ$関数、$p(n)$：分割関数、$μ(n)$：メビウス関数、$1_\mathbb{Q}(n)$：ディリクレの関数らしい。感服。

㉑$〔2,11,7,14,6,13,12,8,3〕= 2+11+7-14-6-13+12+8+3 = 10$　by 小夜時雨
　　分かる言葉で書いてくれて本当にありがとう。泣きそう

㉒$〔11,7,1,6,13,10,8,3,9〕=
3×6×12×\displaystyle\frac{8}{\frac{11-7}{2-(14-13)}} = IO_{(25)}$　byLikU
　　次元違くて草

<div style="page-break-before:always"></div>
### まだまだ募集中∩全編公開中

![](https://dsm04pap001files.storage.live.com/y4mAjR2InbTYr-2D5_qPjquvnkfCkEGeNyXBCWpZLDZCSCDQ4C0akrKGz0JtJ9fEUCNVBlfQw9IGPnJG89AoJfMOKW9MD2nHLRF_QGNNU31nA9iAtStgk7ATIQ2PnTrmF6HJtsykjLbtT5qhNSRSgpQ83mPkk0s-67P0hG0bzDYODvnIl3BNsNPSMqKOfr346Ky?width=727&height=352&cropmode=none)

この記事を読んで、俺も考えたぞ！という人は、ぜひとも左のQRコードから回答してほしい。
どうせなら全ての回答を見てみたいという人は、右のQRコードから見てくれたまえ。
自分の回答も表示されているはず。



### おわりに

OH27<sub>(9)</sub>より
こんなの見たら、俺に数権ないじゃん...
こうなったら来年の新歓もテンパズルで書いてやる！