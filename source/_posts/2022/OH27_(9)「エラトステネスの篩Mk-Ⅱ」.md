---
title: エラトステネスのふるい Mk-II
date: 2022-09-19 22:12:00
tags: 2022年度
cover_index: https://dsm04pap001files.storage.live.com/y4mcKDoFg6vOpq1linjJcaFwAtuia_d2Akkli0fKlN-FdZtq3oWmnInncAqSMvO2Xe27yA8uHdfU-os_O_VAo-ndtsaGf3ytPhKhEt7I8pWxI1qzim_gX1WajAiJMOWCETb9-kgDGHdxBIlDeviCz4FLe9uJNaz5GgCzmxjPKNdWmJ4_L_J-L4hsA7Rn3PPdgTz?width=991&height=379&cropmode=none
cover_detail: https://dsm04pap001files.storage.live.com/y4mcKDoFg6vOpq1linjJcaFwAtuia_d2Akkli0fKlN-FdZtq3oWmnInncAqSMvO2Xe27yA8uHdfU-os_O_VAo-ndtsaGf3ytPhKhEt7I8pWxI1qzim_gX1WajAiJMOWCETb9-kgDGHdxBIlDeviCz4FLe9uJNaz5GgCzmxjPKNdWmJ4_L_J-L4hsA7Rn3PPdgTz?width=991&height=379&cropmode=none
---

<p style="text-align: right">OH27<sub>(9)</sub></p>
<p style="text-align: center">「エラトステネスMk-II、
OH27<sub>(9)</sub>、行きます！」</p>
エラトステネスのふるいとは、有名な素数発見方法の1つだ。1から順番に自然数を羅列していき、一定の数で次の行に移り、表を作る。2以外の2の倍数全てにチェックをつける。3以外の3の倍数全てにチェックなどをつける。そうして繰り返したあとに残った数が素数であるというものだ。

　これについて、多くの場合は１行を10ずつにして、それらしい工夫もせずにやっているものを多く見て来た。だが、これらはほとんど100までの素数を見つけるためにやっているわけで、西高の数研民ならそれぐらい暗記しているのだ。たぶん。
$$
2,3,5,7,11,13,17,19,23,29,31,37,41,43,47,53,59,61,67,71,73,79,83,89,97
$$
だよね？
~~実は筆者は今、91を素数に入れてしまった。だって7の倍数はムズイじゃん。~~<br/>これは私とあなたの秘密にしておくことにしよう。

　実はMk-IIはベトリナの企画として生み出された。ベトリナの山手線双六化計画、のちのYLSPでゲームマスターがやる無駄の1つとして、素数のふるい出し案が出たのだ。いかにベトリナでも、毎度偶数にチェックをつけるという無駄はしたくないという話になり、効率化を目指すこととなった。なお、Mk-II化には2年G組の2人のO田氏と協力してくれた。感謝している。

　まあ数研民なら、500までの素数求めてみようなどと考える人もいるだろうから、そこそこ需要はあると思っている。

　Mk-II化の方法は簡単だ。
①偶数を排除
②横幅を、2は除く小さい素数の積の個数にする

実際にやってみよう。まず一般的な形(⓪)を示す。<img src="https://dsm04pap001files.storage.live.com/y4mxll5C7djXLw8_Jyktn93HmmOayDCvyx1uXW-QodQvLwgwWpHvIzlXHdP2sHB-xde_mnBtFHcPeyUsuZZiJ3qo8tzFO4hcZRnpKIx6BGO1Gc_KJEYTZXcgcm0EqyWe4TipC56U3h2-aqWmURDTJhThauJb0BYrhPLf0c0pxRjXCV-FthnawiWsutu0X1k5bRj?width=772&height=427&cropmode=none" style="zoom:70%;" />

次に①を実行したものを示す。
<img src="https://dsm04pap001files.storage.live.com/y4mX1Bf0PdxRtjcXQpqpFglBjALwWqTnLQunNJjd1mykdTHJ9rq0x06EOTyMiA4Uj-yG9cHOnCr5cu7GBFs7YHwMmXnOgi0u57f9FYwNtMp3Q1pDcX1WJlhg09xgGxozgSmqBf950TT4avDrOPQRc-muuSM4TP4oSU5Yimr9Dvj2T3WGl4PSA2U9JWLyryck9oz?width=390&height=434&cropmode=none" style="zoom:70%;" />

そして②を実行したものを示す。今回は横幅を3×5=15個にした。
![](https://dsm04pap001files.storage.live.com/y4mRN4XcrznDDtqkK-aUuRZxXcuoU2n2ANmjNQzDlqtShLZH5wSzc_KgeaTs_kBX0FnRHlFzl-R5g8voVxNQGN2h7htKqQlz1a8AKiS3_Z1qzuxGUAuAE66Fh9TsTsiTW7Zk47_2RYu8Q9aMhlmr_icVHwhJNWjirS1to60HbBINgymWEuGiMbaVVNsNEMYF42g?width=1151&height=429&cropmode=none)

あとはふるいだすだけだ。最後に1を除き、~~取り消し線~~が引かれていない数と2が素数となる。
![](https://dsm04pap001files.storage.live.com/y4mxfTXQKSGZKomsDFk3SMsVFILH_H2ISJLBrwPYOQamn_x8Z0nkRH_gI_JoIIj5TM_GbGWmF9N3qmSAVcWZ8hn0dNjp69C8f1BS_aM6WUbmRva1NwUaP-LL5K7H9QUzH_6i-fRBrBsq_ruQnG6W-5odJz61CPT9mA3qhAYpcsEjtc1ABK-cHjBJl5Z_1okoMow?width=1149&height=433&cropmode=none)

　⓪では100個中25個が素数、①では50個中25個が素数(表にない2を含む)、②では150個中62個(表にない2を含む)が素数である。それぞれ素数の割合を求めると、⓪は25%、①は50%、②は41%だ。

　②は割合こそ低いが、縦に並んだ3の倍数と5の倍数を一瞬で消すことが出来るので、実質的に150-68=82個中62個、つまり76%が素数だ。さらに、①に比べ②は7の倍数の消しやすさが格段に良い。
　今回は横幅を3×5=15個にしたが、3×5×7=105個にすると7の倍数も縦に並ぶはずのため、さらなる効率化が可能だ。
　②の発展的な方法(Mk-III)として、3の倍数と5の倍数の縦列を消すことが考え得る。しかし、これでは倍数が一直線上に並ばない。当然だ。途中で数が抜けてるんだから。
<img src="https://dsm04pap001files.storage.live.com/y4mHf48lOKnt6CqUrY8pAdo3Z6mY-glxELtfAlbKqErj0BMaB-U5IzWs3h0-wXiTQFiY5_xA2lwMMI6zzBaEzY7cbvMOHGET1Oz-D3V5WKY7CLMvEmSuJ1LR0HJ8FVBQQ3VoEgrgie0D_47a3_HGMFoJrgxwbqrwc1FLOd-NpikJQTwctJsDAbalZxE2Nq0HAwu?width=616&height=429&cropmode=none" style="zoom:70%;" />
<br/>

## おわりに

　今回、記念祭の数研の部誌には合計3つの記事を寄稿した。エラトステネスのふるい Mk-IIだけは共作でないように見えて、先に述べた通り友達と考えたことのまとめである。西高2年目にしてようやく人脈が広がってきたということだと思いたい。

　この夏、なかなかの労力を部誌に割いて苦労したが、markdownやLaTeXのいい勉強になったのも事実だ。やっぱ数学が好きだ。そう思える夏休みであった。